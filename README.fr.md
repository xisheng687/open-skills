# Open Skills · Bibliothèque de compétences pour agents IA

[简体中文](README.md) · [繁體中文](README.zh-Hant.md) · [English](README.en.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Español](README.es.md)

Une collection publique de compétences pratiques pour agents IA. Le chinois simplifié est la langue principale ; des guides existent aussi en chinois traditionnel, anglais, français, allemand et espagnol. Installez uniquement les compétences dont vous avez besoin.

## Catalogue

| Catégorie | Compétence | Utilité | Téléchargement |
| --- | --- | --- | --- |
| Outils et interopérabilité des agents | [Agent Tool Discovery](skills/agent-tool-discovery/README.fr.md) | Retrouver et réparer l’accès aux Skills, serveurs MCP et outils CLI qui fonctionnent dans un agent local mais restent introuvables dans un autre, sans remplacer la configuration existante. | [ZIP](https://github.com/xisheng687/open-skills/releases/download/agent-tool-discovery-v1.0.2/agent-tool-discovery.zip) |

**1 compétence publiée.** Le paquet comprend les instructions, les références, des prompts complets en chinois et en anglais et des guides en six langues. Il ne contient pas les outils privés ni les données de l’ordinateur du mainteneur.

## Télécharger et utiliser

1. Téléchargez le ZIP de la compétence, ou extrayez le dossier complet `skills/<nom>/` du dépôt.
2. Conservez tous les fichiers, références et licences. Le ZIP du dépôt entier n’est pas un paquet d’importation pour une seule compétence.
3. Suivez le [guide français](skills/agent-tool-discovery/README.fr.md), ou copiez le [prompt anglais](skills/agent-tool-discovery/references/client-prompt.en.md) ou [chinois](skills/agent-tool-discovery/references/client-prompt.zh-CN.md). Vous pouvez demander une réponse en français.

Les chemins et mécanismes d’installation varient selon le client et sa version. Un agent distant peut ne pas accéder aux fichiers locaux. Télécharger ou installer ne vaut pas autorisation d’exécuter la procédure.

## Ajouter des compétences

Chaque compétence conserve un dossier stable `skills/<nom>/`, avec catégorie et mots-clés dans ses métadonnées. Ajoutez une documentation principale en chinois, une version anglaise et les traductions utiles, puis une ligne au catalogue. Consultez les [règles de contribution](CONTRIBUTING.md), en chinois et en anglais.

## Confidentialité et validation

Ce dépôt ne doit contenir que des instructions génériques et des sources publiques : aucun secret, inventaire réel de machine, chemin personnel, service privé, sauvegarde ou donnée client. La validation statique et le contrôle du paquet ne prouvent pas un fonctionnement dans tous les agents.

[Licence MIT](LICENSE), également incluse dans chaque paquet autonome.
