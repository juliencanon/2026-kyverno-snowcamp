
<!-- .slide: class="flex-row center" data-background="./assets/snowcamp/bkgnd-7.png"-->
## Niveau 300 : Une demande du CISO vient de tomber...
![h-600](./assets/snowcamp/100-chateau-600.png)

Il faut sécuriser les containers dans le cluster !

##==##
<!-- .slide: class="flex-row center blue" data-background="./assets/snowcamp/bkgnd-7.png"-->
## Commencer par la base, de façon fiable et maîtrisée

### Documentation Kubernetes -> Pod Security Standards

- interdiction de tourner sous l'indentité root
<!-- .element: class="text-blue" -->
- filesystem / en lecture seule
<!-- .element: class="text-blue" -->
- isolation des "namespaces" de la machine hôte (PID, IPC, Network, HostAlias,...)
<!-- .element: class="text-blue" -->
- desactivation de toutes les capabilities (CAP_NET_RAW, CAP_SYS_ADMIN, ...)
<!-- .element: class="text-blue" -->
- interdiction des escalations de privilege
<!-- .element: class="text-blue" -->
<BR>
<BR>
<BR>
https://kubernetes.io/docs/concepts/security/pod-security-standards


##==##
<!-- .slide: class="flex-row center" data-background="./assets/snowcamp/bkgnd-7.png"-->
## Pod Security Standards
![h-800](./assets/snowcamp/pss-700.png)


##==##
<!-- .slide: class="flex-row center" data-background="./assets/snowcamp/bkgnd-7.png"-->
## Le repo helm kyverno offre un chart kyverno-policies

Choix du profil : 
<!-- .element: class="text-blue" -->
![h-200](./assets/snowcamp/policies-baseline.jpg)

Mode : Audit ou Enforce
<!-- .element: class="text-blue" -->
![h-200](./assets/snowcamp/policies-enforce.jpg)

##==##
<!-- .slide: class="flex-row center" data-background="./assets/snowcamp/bkgnd-7.png"-->
## Utilisons le helm chart kyverno-policies
![h-600](./assets/snowcamp/demo-time-girl.png)

