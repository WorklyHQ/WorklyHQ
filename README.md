#  Workly Project - Desktop Mate

**Organisation multi-repos du projet Workly Desktop-Mate**

---

##  Vue d'ensemble

Workly est une application hybride **Unity + Python** qui affiche un avatar VRM interactif sur le bureau Windows, avec l'objectif à terme de créer un assistant virtuel conversationnel alimenté par IA.

** Inspiration :** [Desktop Mate sur Steam](https://store.steampowered.com/app/3301060/Desktop_Mate/)

---

##  Organisation des repos

Ce projet est organisé en **3 repos GitHub séparés** :

###  [workly-desktop](https://github.com/WorklyHQ/workly-desktop)

**Application principale** - Avatar VRM interactif sur bureau Windows

-  **Python** (PySide6) - Interface graphique et logique
-  **Unity 2022.3 LTS** - Rendu 3D de l'avatar VRM
-  **IA** - Moteur conversationnel avec LLM local
-  **IPC** - Communication TCP entre Python et Unity

**Convention de commits :** **Strict** (Conventional Commits)
`ash
feat: add new feature
fix: resolve bug
docs: update documentation
`

 **Contenu :**
- Code source Python (src/)
- Scripts Unity C# (unity/Assets/Scripts/)
- Tests unitaires (	ests/)
- Modèles VRM et LLM (ssets/, models/)

---

###  [workly-website](https://github.com/WorklyHQ/workly-website)

**Site web vitrine** du projet Workly

-  HTML/CSS/JavaScript  
-  Design responsive
-  Pages : Accueil, About, Privacy, Terms
-  **Live** : https://workly.xyon.site.elsites.fr

**Convention de commits :** **Libre**
`ash
[ADD] Page contact
Mise à jour du CSS
`

 **Contenu :**
- Pages HTML (pages/)
- Assets web (ssets/)

---

###  [workly-docs](https://github.com/WorklyHQ/workly-docs)

**Documentation complète** du projet

-  Guides techniques par session
-  Historique des chats de développement  
-  Notes et architecture
-  Tutoriels et troubleshooting

**Convention de commits :** **Semi-Strict**
`ash
docs: add session 13 guide
Notes brainstorming
`

 **Contenu :**
- Documentation par session (sessions/)
- Transitions (chat_transitions/)
- Guides (1st/, START_HERE.md)

---

##  Démarrage rapide

### Cloner les 3 repos

`powershell
mkdir c:\\Dev\\workly_project
cd c:\\Dev\\workly_project

git clone https://github.com/WorklyHQ/workly-desktop.git
git clone https://github.com/WorklyHQ/workly-website.git  
git clone https://github.com/WorklyHQ/workly-docs.git
`

### Lancer l'application

`powershell
cd workly-desktop
python -m venv venv
.\\venv\\Scripts\\Activate.ps1
pip install -r requirements.txt
python main.py
`

---

##  Documentation

** Pour commencer :**
- [workly-docs/START_HERE.md](https://github.com/WorklyHQ/workly-docs/blob/main/START_HERE.md)
- [workly-desktop/README.md](https://github.com/WorklyHQ/workly-desktop/blob/main/README.md)

** Guides techniques :**
- [Configuration Git](https://github.com/WorklyHQ/workly-docs/tree/main/sessions/session_0_git_configuration)
- [Installation Unity](https://github.com/WorklyHQ/workly-docs/tree/main/sessions/session_2_unity_installation)
- [Python-Unity IPC](https://github.com/WorklyHQ/workly-docs/tree/main/sessions/session_4_python_unity_connection)
- [Expressions faciales](https://github.com/WorklyHQ/workly-docs/tree/main/sessions/session_6_expressions)
- [Moteur IA](https://github.com/WorklyHQ/workly-docs/tree/main/sessions/session_10_ai_chat)
- [Optimisations](https://github.com/WorklyHQ/workly-docs/tree/main/sessions/session_11_performance)

---

##  Stack technique

**Python :** PySide6, Socket TCP, llama-cpp-python, pytest  
**Unity :** 2022.3 LTS, UniVRM, C# Scripts  
**Architecture :** IPC TCP, JSON messages, Thread-safe queues

---

##  Conventions de commits

| Repo | Convention | Guide |
|------|-----------|-------|
| workly-desktop | Strict | [GIT_COMMIT_CONVENTIONS.md](https://github.com/WorklyHQ/workly-desktop/blob/main/GIT_COMMIT_CONVENTIONS.md) |
| workly-website | Libre | [GIT_COMMIT_CONVENTIONS.md](https://github.com/WorklyHQ/workly-website/blob/main/GIT_COMMIT_CONVENTIONS.md) |
| workly-docs | Semi-Strict | [GIT_COMMIT_CONVENTIONS.md](https://github.com/WorklyHQ/workly-docs/blob/main/GIT_COMMIT_CONVENTIONS.md) |

 **Guide complet :** [GIT_MULTI_REPOS_CONFIG.md](https://github.com/WorklyHQ/workly-docs/blob/main/sessions/session_0_git_configuration/GIT_MULTI_REPOS_CONFIG.md)

---

##  Roadmap

###  Phase 1 : MVP (TERMINÉ)
- Avatar VRM sur bureau
- Communication Python-Unity
- Expressions faciales
- Animations et transitions
- Clignement auto + mouvements tête

###  Phase 2 : Intelligence (TERMINÉ)  
- Moteur LLM conversationnel
- Analyse d'émotions
- Sync expressions-émotions
- Bot Discord
- Optimisations performance

###  Phase 3 : Audio (EN COURS)
- Détection audio micro
- Text-to-Speech
- Lip-sync visèmes
- Réactions émotionnelles

###  Phase 4 : Assistant avancé
- Mouvement libre bureau
- Interactions environnement
- Personnalité évolutive
- Mémoire conversationnelle

---

##  Contribution

1. Choisir le repo approprié
2. Cloner et créer une branche
3. Respecter les conventions de commits
4. Ajouter tests et documentation
5. Créer une Pull Request

**Guidelines :**
-  Documentation obligatoire
-  Tests unitaires (Python)
-  PEP 8 (Python) / Conventions C# (Unity)
-  Code en anglais, doc en français

---

##  Ressources

- [Unity Hub](https://unity.com/download)
- [UniVRM](https://github.com/vrm-c/UniVRM)
- [PySide6](https://doc.qt.io/qtforpython/)
- [llama-cpp-python](https://github.com/abetlen/llama-cpp-python)
- [VRM Specification](https://vrm.dev/en/)

---

##  Sessions documentées

1. Configuration Git & Unity
2. Setup projet
3. Installation Unity
4. Installation UniVRM
5. Connexion Python-Unity
6. Chargement VRM
7. Expressions faciales
8. Animations
9. Clignement auto
10. Mouvements tête
11. Moteur IA
12. Optimisations
13. Site web

 **Toutes les sessions :** [workly-docs/sessions/](https://github.com/WorklyHQ/workly-docs/tree/main/sessions)

---

##  Pourquoi 3 repos ?

 Séparation des préoccupations  
 Déploiements indépendants  
 Conventions adaptées  
 Gestion des droits facilitée  
 Historique clair  
 Maintenance simplifiée

`
workly_project/
 workly-desktop/     Code (Python + Unity)
 workly-website/     Site (HTML/CSS/JS)  
 workly-docs/        Docs (Markdown)
`

---

##  Contact

-  **GitHub** : [WorklyHQ](https://github.com/WorklyHQ)
-  **Site** : https://workly.xyon.site.elsites.fr
-  **Email** : [À définir]

---

** Bienvenue ! Crée ton Desktop-Mate personnalisé ! **

*Dernière mise à jour : 10 novembre 2025*  
*Made with  by [WorklyHQ](https://github.com/WorklyHQ)*
