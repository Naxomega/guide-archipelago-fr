# Guide Archipelago en Français
Bonjour, ceci est un guide pour configurer Archipelago.

Avant toute chose, si vous parlez Anglais (ou avec un traducteur), je vous recommande de jeter un oeil à la documentation officielle (ainsi qu'a celle de votre jeu si celui-ci n'est pas officiellement pris en charge), elle va dans les détails et parcours divers cas de figures alors que dans ce guide, je vais être assez géneraliste de manière à ce que l'installation d'Archipelago soit plus simple.
# Qu'est qu'Archipelago ?
Archipelago est un mod de randomizer (concept adapté dans plein de mods de jeu, qui consite à rendre plein de choses aléatoires (objets reçus, capacités, téleportation etc...)) mais les objets sont dispersés dans d'autres jeux. Archipelago (abregé en "AP" à partir de maintenant) se joue à plusieurs (enfin, vous pouvez y jouer tout seul, mais bonne chance pour changer de jeu à chaque fois).

Prenons un exemple : Joueur 1 joue à Metroid Prime, Joueur 2 joue à Super Mario Sunshine.

Dans ce cas de figure tout les objets des 2 jeux sont mélangés à l'intérieur même de ces jeux, mais aussi entre eux. Donc par exemple vous pourrez récupérer la Cata-Buse sur Prime et le rayon de plasma sur Sunshine.

Evidemment la Cata-Buse n'est pas un objet de Prime, donc il sera "envoyé" à votre partenaire pour que lui puisse l'utiliser, et inversement.

 # Configurer Archipelago
 AP peut paraître un peu complexe à configurer, mais on va voir ca simplement ensemble.

 ## Qu'est que l'on va faire dans ce guide ?
 - Nous allons mettre en place le logiciel Archipelago (le logiciel est en Anglais)
 - Générer et héberger un multimonde (une partie avec plusieurs jeux, ou "monde" est un jeu)
- Et enfin connecter tout ceci une fois la partie hébergée
## Installation
Pour commencer, installez Archipelago depuis ce [lien](https://github.com/ArchipelagoMW/Archipelago/releases/latest)

Si vous ne savez pas quel fichier choisir, .apk est pour Android, .AppImage et .tar.gz sont pour Linux, et .exe pour Windows

(Je vais utiliser Windows dans ce guide, les instructions pour Linux doivent être similaire (mis à part les chemins de fichiers) mais je ne peut garantir la fiabilité de ce guide sur Android)

Une fois votre logiciel installé, il faut le lancer (oui, logique :/ ). Il sera trouvable sous le nom "Archipelago Launcher"

Ce programme est composé de pleins de sous-programmes qui accomplissent des rôles différents (héberger une partie, générer une ROM, lier votre jeu au serveur AP...)

Je vais pas m'attarder sur l'auto hébergement (car l'hébergement sur archipelago.gg est gratuit est simple d'utilisation)

## Géneration d'une partie
### Installer des jeux (facultatif, mais lisez-le quand même)
Pour faire simple, y'a des jeux pris en charge officiellement ([ici](https://archipelago.gg/games)), mais si vous aussi vous ne trouvez pas votre bonheur, soit faites une recherche Google avec le nom de votre jeu et Archipelago (ex. "Metroid Prime Archipelago"), ou allez voir du côté de [ce wiki](https://archipelago.miraheze.org/wiki/Category:Implementations) qui liste les jeux pris en charge non officiellement (oui y'en a beaucoup plus :) )

Il vous faut un .apworld, en gros ce fichier sert à "apprendre" à Archipelago que votre jeu existe (il installe le client, un génerateur de fichier YAML (d'exemple, il faudra quand même le remplir, j'en parle un peu plus loin), et un patcheur de ROM si besoin)
### C'est quoi un YAML ??
Un fichier YAML (YAML Ain't a Markup Language, ou YAML n'est pas un langage de formatage) est utilisé pour configurer chaque monde (règles, collectibles, deathlink...)

Pour les technophiles, le YAML est grosso-modo un JSON mais formatté de manière à être lu plus facilement par un humain (pour peu que l'on existe encore, merci OpenAI :/ )

### Création d'un YAML
La plupart des packs AP fournissent un YAML d'exemple, afin de remplir les paramètres vous mêmes (pour les jeux officiellement supportés, c'est par [ici](https://archipelago.gg/games), sinon ca doit sûrement se trouver quelque part dans la repo, si aucun n'est présent, dans le client AP se trouve une option "Generate Template Options", et il vous ouvrira un dossier avec des templates pour tout les jeux installés, y compris les non-officiels)


Une fois votre YAML rempli (par vos soins, via une IA ou via le générateur pour les jeux officiellement supportés), vous devrez vous procurer les YAMLs de vos partenaires (si vous jouez à plusieurs, sinon pas besoin). Si c'est un autre de vos partenaires qui s'occupe de l'hébergement, envoyez lui votre fichier et c'est tout bon pour vous :)

### Création d'une partie multijoueur

> [!NOTE]
> A partir de maintenant, ce guide ne s'adresse plus qu'au host de la partie. Si vous êtes simple joueur (y'a rien de mal à l'être hein), vous avez fini votre boulot.

Pour rester simple, je vais parler uniquement de la géneration locale (c'est aussi possible de le faire via le site web, mais c'est incompactible avec les jeux non-officiels. Et étant donné le nombre ahurissant de jeux officiels, vous comprendrez que ca vaut plus le coup de parler de la géneration locale)

> [!IMPORTANT]
> Si un de vos partenaires joue à un jeu non-officiel, il faut que vous l'installez sur votre PC (demandez-lui les fichiers, au cas où 2 mods existe pour le même jeu)

Il faut maintenant placer les fichiers YAML dans le dossier Archipelago/Players (Pour Windows c'est `C:/ProgramData/Archipelago/Players`, côté Linux c'est `/opt/archipelago/players` ou `/usr/local/lib/archipelago/players`). Il faut que les fichiers soient nommés en fonction de leur joueur (si je veut jouer à Metroid Prime, il faut que mon fichier de configuration de Metroid Prime s'appelle `Naxomega.yaml`)

Ensuite il faut génerer la partie (option "Generate" dans le launcher) Si tout s'est bien passé, il doit y avoir un fichier .zip dans le dossier output

Si vous jouez à un jeu console, dans votre .zip se trouve un (ou plusieurs) fichiers .ap(abréviation du nom du jeu) (pour Metroid Prime c'est .apmp1 (mp1 pour Metroid Prime 1)). Il faut donc aller dans "Open Patch File" dans votre client Archipelago, et lui donner votre ROM (je ne donnerais aucune aide sur comment en trouver)

### Hébergement sur archipelago.gg
Une fois que vous avez votre .zip, il est temps d'héberger votre partie. On va utiliser le site officiel d'archipelago car c'est gratuit et très simple d'utiliation (et merci à eux d'avoir mis leur serveurs à notre disposition)

Rendez-vous [ici](https://archipelago.gg/uploads) pour commencer. Cliquez sur "Upload File" et donnez lui votre .zip

Et normalement tout est bon. Vous avez surement envie de mettre un mot de passe (pour éviter qu'on vous embête). Si c'est le cas, dans la console du serveur, entrez `/option server_password true` et `/option password [votre mot de passe]`.

# Crédits
- Les devs d'Archipelago (pour le guide original et l'accès aux serveurs)
- UltiNaruto (pour son guide d'installation de Metroid Prime, sur lequel je me suis aussi appuyé)
- Julgane (pour m'avoir fait connaître Archipelago par le biais d'une de ses vidéos)
- Naxoméga (moi) (pour l'écriture de ce guide)
