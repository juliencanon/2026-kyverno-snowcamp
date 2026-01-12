
<!-- .slide: class="flex-row center" data-background="./assets/snowcamp/bkgnd-7.png"-->
## Cleaning : 2 façons de suppression automatique
![h-600](./assets/snowcamp/clean-policy.png)


##==##
<!-- .slide: class="with-code-dark max-height" data-background="./assets/snowcamp/bkgnd-7.png"-->
## Cleanup Policy sur expression cron
<!-- .element: class="text-black" -->
```yaml [2,4,11-13,19]
apiVersion: kyverno.io/v2
kind: ClusterCleanupPolicy
metadata:
  name: cleandeploy
spec:
  match:
    any:
      - resources:
          kinds:
            - Deployment
          selector:
            matchLabels:
              canremove: "true"
  conditions:
    any:
      - key: "{{ target.spec.replicas }}"
        operator: LessThan
        value: 2
  schedule: "*/5 * * * *"
  # use Foreground deletion propagation policy
  deletionPropagationPolicy: Foreground
```


##==##
<!-- .slide: class="with-code-dark max-height" data-background="./assets/snowcamp/bkgnd-7.png"-->
## Cleanup Policy sur présence de ttl (label)
<!-- .element: class="text-black" -->
```yaml [2,5-6]
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-server
  labels:
    cleanup.kyverno.io/ttl: 2m
spec:
  replicas: 2
  selector:
    matchLabels:
      app: nginx-server
  template:
    metadata:
      labels:
        app: nginx-server
    spec:
      containers:
      - name: nginx-server
        image: nginx:1.27.5
```

