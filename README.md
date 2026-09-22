# Guide Archipelago en Français
Bonjour, ceci est un guide pour configurer Archipelago.
## Qu'est qu'Archipelago ?
Archipelago est un mod de randomizer (concept adapté dans plein de mods de jeu, qui consite à rendre plein de choses aléatoires (objets reçus, capacités, téleportation etc...)) mais les objets sont dispersés dans d'autres jeux. Archipelago (abregé en "AP" à partir de maintenant) se joue à plusieurs (enfin, vous pouvez y jouer tout seul, mais bonne chance pour changer de jeu à chaque fois).

Prenons un exemple : Joueur 1 joue à Metroid Prime, Joueur 2 joue à Super Mario Sunshine.

Dans ce cas de figure tout les objets des 2 jeux sont mélangés à l'intérieur même de ces jeux, mais aussi entre eux. Donc par exemple vous pourrez récupérer la Cata-Buse sur Prime et le rayon de plasma sur Sunshine.

Evidemment la Cata-Buse n'est pas un objet de Prime, donc il sera "envoyé" à votre partenaire pour que lui puisse l'utiliser, et inversement.

 ## Configurer Archipelago
 AP peut paraître un peu complexe à configurer, mais on va voir ca simplement ensemble.

 ### Qu'est que l'on va faire dans ce guide ?
 - Nous allons mettre en place le logiciel Archipelago (le logiciel est en Anglais)
 - Générer et héberger un multimonde (une partie avec plusieurs jeux, ou "monde" est un jeu)
- Et enfin connecter tout ceci une fois la partie hébergée
### Installation
Pour commencer, installez Archipelago depuis ce [lien](https://github.com/ArchipelagoMW/Archipelago/releases/latest)

Si vous ne savez pas quel fichier choisir, .apk est pour Android, .AppImage et .tar.gz sont pour Linux, et .exe pour Windows

(Je vais utiliser Windows dans ce guide, les instructions pour Linux doivent être similaire (mis à part les chemins de fichiers) mais je ne peut garantir la fiabilité de ce guide sur Android)

Une fois votre logiciel installé, il faut le lancer (oui, logique :/ ). Il sera trouvable sous le nom "Archipelago Launcher"

Ce programme est composé de pleins de sous-programmes qui accomplissent des rôles différents (héberger une partie, générer une ROM, lier votre jeu au serveur AP...)

Je vais pas m'attarder sur l'auto hébergement (car l'hébergement sur archipelago.gg est gratuit est simple d'utilisation)

### Géneration d'une partie
#### Installer des jeux (facultatif)
Pour faire simple, y'a des jeux pris en charge officiellement ([ici](https://archipelago.gg/games)), mais si vous aussi vous ne trouvez pas votre bonheur, soit faites une recherche Google avec le nom de votre jeu et Archipelago (ex. "Metroid Prime Archipelago"), ou allez voir du côté de [ce wiki](https://archipelago.miraheze.org/wiki/Category:Implementations) qui liste les jeux pris en charge non officiellement (oui y'en a beaucoup plus :) )
<!-- Non terminée -->
#### C'est quoi un YAML ??
Un fichier YAML (YAML Ain't a Markup Language, ou YAML n'est pas un langage de formatage) est utilisé pour configurer chaque monde (règles, collectibles, deathlink...)

Pour les technophiles, le YAML est grosso-modo un JSON mais formatté de manière à être lu plus facilement par un humain (pour peu que l'on existe encore, merci OpenAI :/ )

#### Création d'un YAML
La plupart des packs AP fournissent un YAML d'exemple, afin de remplir les paramètres vous mêmes (pour les jeux officiellement supportés, c'est par [ici](https://archipelago.gg/games), sinon ca doit sûrement se trouver quelque part dans la repo)
<!-- Non terminée -->

> [!IMPORTANT]
> Si vous voyez ceci, c'est que je n'ais pas encore terminé d'écrire ce guide.
