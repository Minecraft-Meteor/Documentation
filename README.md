# Bienvenue sur la documentation Meteor
  Meteor est un projet d'unification monétaire Minecraftienne sous une cryptomonnaie unique nommée **Meteor** (oui, le logo ressemble à un cookie, mais c'est un astéroïde).

## Principe de la monnaie

Il s'agit d'une cryptomonnaie *Proof-of-Stake* et non Proof-of-Work, soft-forkée de NXT, ce qui signifie qu'elle ne consomme pas beaucoup de ressources puisqu'au lieu de donner le bloc à résoudre à tous les mineurs (appelés forgeurs dans le cas d'une monnaie PoS), il en sélectionne un au hasard (pondéré avec la solde de Meteor qu'il possède) pour le résoudre, ce bloc peut être ensuite validé par tous les forgeurs (ce qui est bien plus rapide que de le résoudre).

### Et Minecraft alors ?

Le Meteor est prévu pour être utilisable sur tous les serveurs Minecraft et, à terme, avoir une valeur réelle ce qui permettrait de les échanger contre de l'argent réel. Nous prévoyons de plafonner ce prix à 10 centimes d'Euro.
Afin de permettre une telle chose, plusieurs serveurs doivent accepter cette monnaie virtuelle, en considérant qu'elle vaut éffectivement 10 cts d'Euro, cela lui permettra progressivement d'obtenir de la valeur.

### J'ai entendu parler de SpaceLauncher, kesaco ?

Le SpaceLauncher sera un launcher contenant un mod qui permettra au joueur de forger de façon transparente pour lui et d'en donner les bénéfices au serveur qu'il visite, si celui-ci adhère au réseau Meteor, sinon, le bénéfice sera envoyé sur un compte appartenant au réseau puis sera redistribué aux serveurs, il permetra également de multiplier les gains de Meteor du joueur selon un coeficient calculé selon sa participation au réseau. Le coeficient est un nombre compris entre 1 et 2, il est calculé de la façon suivante : 
``` (Nombre de blocs calculés par le joueurs durant le dernier mois / (Nombre de blocs calculés par le réseau entier durant le dernier mois / 2)) + 1```
Cette formule pourras être améliorée au fûr et à mesure.

**Le mod et le launcher SpaceLauncher ne sont pas encore développés. Ils arriveront dans un futur proche. Suivez le développement sur la page Github du projet.**
**Les noms ne sont par ailleurs pas définitifs et peuvent être amenés à changer au cours du développement**

## Je veux utiliser Meteor sur mon serveur, comment faire ?

Afin de pouvoir utiliser le Meteor sur votre serveur, l'utilisant comme seule monnaie utilisable en jeu et sur votre boutique web, vous devrez mettre en place au minimum deux systèmes :

 - Un moyen de convertir les euros en Meteor (autrement dit, permettre d'acheter des Meteors, en sens unique pour l'instant)
 - Un système multipliant les gains de Meteor aux joueurs sous SpaceLauncher (voir ci-dessous) par le coeficient de ce joueur
 
À ces fins devra également et surtout être mis en place une connection avec notre système de lien pseudo/compte Meteor, ce qui interdit les serveurs cracks pour le moment, exception faite de ceux ayant leurs propre serveur d'authentification. Nous contacter dans ces cas particulier.

Votre serveur devra également utiliser son compte Meteor pour forger afin de promouvoir la décentralisation du réseau, il devra donc héberger un Node Meteor, ce Node sera ajouté à la Known-Node List ce qui signifie qu'il sera un acteur important du réseau.

Une fois le serveur rendu compatible avec Meteor, vous pourrez nous contacter et nous vous donnerons quelques Meteors à distribuer au joueurs selon vos désirs (dans la limite du raisonnable), en général nous donnons un million de Meteors renouvellable si besoin est.

#### Cas spécial : Mon serveur utilise deux monnaies
Eventuellement pourra être conservé votre monnaie actuelle si vous utilisez une monnaie déjà présente. 
Beaucoup de serveurs ont actuellement deux monnaies, l'une est généralement appelée "Points Boutique" et l'autre peut avoir differents nom et n'est utilisable qu'en jeu (nous l'appelerons ici "MineDollar" ou M$). 
Dans le cadre de ces serveurs, le Meteor remplacera le Point Boutique, il devra cependant être mis en place un système permettant la convertion à un taux fixe des M$ en Meteor (et inversement) afin de respecter les EULAs de Mojang et le fait que les Meteors se gagnent en jouant.
Dans ce cas, le système doublant les gains de Meteor aux joueurs sous SpaceLauncher pourra se présenter sous deux formes : une multiplication des gains de M$ ou bien une division du taux d'échange M$ -> Meteor par le coeficient soustrait de 1 point. `Taux d'échange réduit = Taux classique / (Coeficient - 1)` 

