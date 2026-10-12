# Agent Tool Discovery · Détection et réparation des outils

[简体中文](README.md) · [繁體中文](README.zh-Hant.md) · [English](README.en.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Español](README.es.md)

**Catégorie :** outils et interopérabilité des agents · **Version :** 1.0.2

## Le problème résolu

« Je l’ai déjà installé, mais un autre agent ne le trouve pas. » Les dossiers de Skills, les configurations MCP et les sessions d’authentification diffèrent entre clients. Un outil CLI peut fonctionner dans le terminal mais manquer dans le PATH d’une application de bureau.

Ce Skill inventorie les agents locaux et leurs outils, réutilise une source commune de compétences et choisit la découverte native, les liens symboliques par Skill ou des copies suivies selon les capacités réelles. Il adapte les définitions MCP par client, vérifie les chemins CLI, crée un index local et distingue présence des fichiers, découverte et appel réussi.

## Télécharger et installer

Téléchargez le [ZIP autonome](https://github.com/xisheng687/open-skills/releases/download/agent-tool-discovery-v1.0.2/agent-tool-discovery.zip), ou extrayez le dossier complet `skills/agent-tool-discovery/`. Conservez tous les fichiers et références : ni un SKILL.md isolé ni le ZIP de tout le dépôt ne constitue le paquet complet de cette compétence.

Les clients compatibles peuvent utiliser `~/.agents/skills/agent-tool-discovery/` ; Claude Code utilise `~/.claude/skills/agent-tool-discovery/`. Vérifiez le produit et sa version. Comparez une compétence existante du même nom avant toute écriture.

Joignez le ZIP ou indiquez le dossier extrait, puis demandez :

> Installe uniquement cette compétence dans le dossier utilisateur confirmé de ce client. Conserve tout le paquet et les versions en conflit. Vérifie sa détection dans une nouvelle session. N’exécute pas encore l’audit ni la réparation.

## Utiliser

> Utilise agent-tool-discovery pour auditer les agents et outils de cet ordinateur. Rapporte les résultats sans rien modifier. Réponds en français.

> Utilise agent-tool-discovery pour inspecter et réparer la découverte des outils entre mes agents locaux. Préserve les configurations. Demande mon intervention pour une connexion ou un conflit non résolu. Réponds en français.

Codex permet l’invocation `$agent-tool-discovery`. Sans installation, copiez le [prompt anglais complet](references/client-prompt.en.md) ou [chinois](references/client-prompt.zh-CN.md). Ces prompts autorisent des réparations réversibles limitées par défaut ; indiquez explicitement « audit uniquement, aucune modification » pour une inspection sans écriture.

## Autorisation, confidentialité et limites

Préserve les configurations, les états désactivés et les périmètres de projet. N’installe pas de dépendances, ne mets pas les outils à jour, ne supprime pas les originaux et ne copie pas de jetons OAuth ni de secrets intégrés vers d’autres clients. En mode audit seul, aucun index, règle, sauvegarde ou tâche n’est créé. Télécharger ou installer n’autorise pas la réparation.

Les inventaires, sauvegardes et rapports restent dans un emplacement local privé, hors des dépôts suivis et du partage public. C’est une compétence guidée par des instructions, sans service permanent ni script d’envoi ; elle exige un accès local. Le catalogue n’est pas une certification de compatibilité. Les validations impossibles restent signalées comme non vérifiées. Les produits tiers ont leurs propres politiques de données.

## Vérifications périodiques facultatives

Après le travail, vous pouvez choisir des contrôles périodiques. Votre accord, la fréquence, le planificateur et l’accès à l’environnement local doivent être confirmés. Par défaut, les contrôles sont en lecture seule et silencieux si rien ne change. Les réparations automatiques nécessitent une autorisation distincte ; les connexions et conflits ne sont pas traités automatiquement.

[Licence MIT](LICENSE).
