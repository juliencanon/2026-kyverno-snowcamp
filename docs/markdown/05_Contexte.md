
<!-- .slide: class="flex-row center" data-background="./assets/snowcamp/bkgnd-7.png"-->
## Contexte Kubernetes
![h-500](./assets/snowcamp/k8s-logo-trans.png)
![h-500](./assets/snowcamp/illus-cluster-2.png)

##==##
<!-- .slide: class="flex-row center" data-background="./assets/snowcamp/bkgnd-7.png"-->
![h-700](./assets/snowcamp/arrivee-client.png)

##==##
<!-- .slide: class="flex-row center" data-background="./assets/snowcamp/bkgnd-7.png"-->
![h-700](./assets/snowcamp/team-mature.png)
Notes:
Equipes matures (staff, sre, cicd,...)

##==##
<!-- .slide: class="flex-row center" data-background="./assets/snowcamp/bkgnd-7.png"-->
## L'entropie du système augmente...
![h-600](./assets/snowcamp/arrivee_client.png)
Notes: 
- arrivée d'un junior dans l'entreprise
- il reste plein de secrets obsoletes
- ce à quoi on n'en pas pensé en amont

##==##
<!-- .slide: data-background="./assets/snowcamp/bkgnd-7.png"-->
## Sources de problèmes
- La définition des requests/limits manquent, scheduling pas optimal
<!-- .element: class="text-blue" -->
- Il est difficile de savoir le propriétaire de certaines resources
<!-- .element: class="text-blue" -->
- Les resources utilisent des apiVersions vieillissantes
<!-- .element: class="text-blue" -->
- Les containers ne sont pas sécurisés (possibilité d'évasion)
<!-- .element: class="text-blue" -->
- Les images proviennent de diverses registries, parfois obscures
<!-- .element: class="text-blue" -->
- Il reste des resources oubliées lors de décommissionnement
<!-- .element: class="text-blue" -->
- Le nommage laisse à désirer
<!-- .element: class="text-blue" -->
- Tout autre grain de sable dont on n'a pas encore pris conscience...
<!-- .element: class="list-fragment text-blue" -->

##==##
<!-- .slide: class="flex-row center" data-background="./assets/snowcamp/bkgnd-7.png"-->
## Comment Kyverno nous aide-t-il ?
![h-500](./assets/snowcamp/kyverno2.png)
![h-500](./assets/snowcamp/Question_mark_alternate.svg)
