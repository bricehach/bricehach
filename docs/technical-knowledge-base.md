# Base de connaissances IT — Projet 00

## Portfolio professionnel LinkedIn + GitHub

Cette base de connaissances complète mon portfolio professionnel.

Son objectif n'est pas uniquement de montrer des technologies ou des projets terminés. Elle vise à **capitaliser, structurer et partager des connaissances IT pratiques, vérifiables et réutilisables**, issues de l'expérience, de la formation, des laboratoires, du dépannage et de l'analyse technique.

> **Chaque contenu publié doit apprendre quelque chose, résoudre un problème, fournir une méthode ou permettre de reproduire une expérience.**

---

## Comment utiliser cette base

Les contenus sont organisés selon quatre formats principaux :

| Type | Objectif |
|---|---|
| **GUIDE** | Permettre de réaliser une tâche de manière reproductible |
| **REFERENCE** | Retrouver rapidement commandes, paramètres, ports, Event ID ou informations utiles |
| **LAB** | Montrer une mise en pratique réelle, avec tests et validation |
| **EXPLAINED** | Comprendre pourquoi une technologie fonctionne, ses limites et ses risques |

La méthode commune reste :

```text
Comprendre
    ↓
Configurer / reproduire
    ↓
Tester
    ↓
Observer
    ↓
Diagnostiquer
    ↓
Corriger
    ↓
Vérifier
    ↓
Documenter
```

---

## Statut des contenus

- **Publié** : contenu déjà visible dans un repository public.
- **Matière disponible** : sujet déjà travaillé et pouvant être transformé en ressource GitHub.
- **À construire** : domaine ou repository prévu, mais pas encore suffisamment documenté pour être publié.

---

# 01 — Windows & Infrastructure

**Repository cible : `windows-infrastructure-lab` — à construire**

### Matière disponible

- Installation propre de Windows 10 / 11
- Installation de Windows 11 avec compte local
- Configuration d'un poste Windows avec davantage de transparence sur la collecte et l'utilisation des données
- Télémétrie, services et fonctions optionnelles
- Hardening Windows
- Microsoft Defender et politiques de sécurité
- GPO
- Winget : mise à jour et maintenance des applications
- Diagnostic des pilotes
- Réparation du démarrage Windows
- `bootrec` et outils associés
- BSOD / Bug Check : compréhension, diagnostic et pistes de réparation
- Journaux Windows : Event ID liés à la stabilité et aux redémarrages
- Troubleshooting matériel / BIOS / pilotes
- Procédures de vérification avant et après modification

### Orientation documentaire

```text
Fonction Windows
      ↓
À quoi sert-elle ?
      ↓
Quelles données / ressources utilise-t-elle ?
      ↓
Impact sécurité / confidentialité / stabilité
      ↓
Modification éventuelle
      ↓
Vérification
      ↓
Retour arrière
```

---

# 02 — Networking, Cisco & Security

**Repository : [networking-cisco-security-lab](https://github.com/bricehach/networking-cisco-security-lab) — publié / actif**

### Déjà structuré

- Fondamentaux réseau
- Subnetting
- Switching
- VLAN et trunking
- Routage / Layer 3
- Packet Tracer
- Troubleshooting
- Sécurité réseau
- Analyse de trafic

### Matière à intégrer progressivement

- CIDR et exercices de subnetting
- Cisco 2960
- Cisco 3560 Layer 3
- VLAN / trunks
- Inter-VLAN routing
- Labs Packet Tracer avec 4 PC
- Adaptation d'une topologie en cas de matériel manquant
- Méthodologie de tests par saut
- Validation par ping
- Dépannage des interfaces
- Connexion console et problèmes de ports COM / PuTTY
- pfSense
- Wireshark et lecture des flux

---

# 03 — Linux Security

**Repository : [linux-security-lab](https://github.com/bricehach/linux-security-lab) — publié / actif**

### Déjà structuré

- Fondamentaux Linux
- Utilisateurs et permissions
- Processus et services
- Réseau
- Logs et monitoring
- Gestion des paquets
- Hardening
- Automatisation Bash
- Kali / Parrot
- Outils de sécurité

### Matière à intégrer progressivement

- Mise à jour et changement de version Parrot Security
- Mise à jour Kali Linux
- Administration Linux utile à la cybersécurité
- Maintenance de machines virtuelles
- Clonage de VM de laboratoire
- Nmap — utilisation défensive et compréhension avancée
- Netcat — usages, diagnostic et concept de relais
- Lynis — audit et hardening
- chkrootkit — détection et limites
- Procédures de diagnostic avant utilisation d'un outil de sécurité

---

# 04 — Cybersecurity / SOC

**Repository : [cybersecurity-soc-lab](https://github.com/bricehach/cybersecurity-soc-lab) — publié / actif**

### Déjà structuré

- Fondamentaux SOC
- Logging et télémétrie
- Sysmon
- Sigma
- Wazuh
- Microsoft Defender
- Cas de détection
- Corrélation et triage
- Workflow incident
- Labs

### Matière à intégrer progressivement

- Event ID Windows utiles au SOC
- Sysmon et télémétrie avancée
- Sigma et logique de détection
- Wazuh
- Exercices d'analyse de logs
- Corrélation d'événements
- Détection d'activités SSH anormales
- Comptes de service
- Security Onion / Kibana
- Différence événement / alerte / incident
- Construction d'un raisonnement de triage

---

# 05 — Windows DFIR

**Repository : [windows-dfir-lab](https://github.com/bricehach/windows-dfir-lab) — publié / actif**

### Déjà structuré

- Fondamentaux DFIR
- Windows Event Logs
- Event ID
- Sysmon
- Hayabusa
- Chainsaw
- DeepBlueCLI
- Velociraptor
- Artefacts Windows
- Timelines
- Méthodologie d'investigation
- Labs

### Matière à intégrer progressivement

- Analyse EVTX
- Méthodologie d'investigation Windows
- Utilisation de Hayabusa
- Utilisation de Chainsaw
- Utilisation de DeepBlueCLI
- Velociraptor
- Corrélation des événements
- Construction d'une timeline
- Hypothèses, validation et limites de l'analyse

---

# 06 — PowerShell & Automation

**Repository cible : `powershell-automation` — à construire**

### Matière disponible

- Administration Windows avec PowerShell
- Winget et automatisation des mises à jour
- Inventaire et vérification système
- Diagnostic des pilotes
- Lecture et filtrage des journaux Windows
- Maintenance et vérifications récurrentes
- Scripts orientés administration et cybersécurité
- Bash et Python comme outils complémentaires

### Principe

L'automatisation n'est pas une fin en soi : elle doit rendre une tâche **plus fiable, reproductible, contrôlable et documentée**.

---

# 07 — IA, ChatGPT & IT

**Repository : [ai-for-it-cybersecurity](https://github.com/bricehach/ai-for-it-cybersecurity) — publié / actif**

### Déjà structuré

- Prompting
- Vérification
- Confidentialité
- RAG
- Cas d'usage IT
- Cas d'usage cybersécurité
- Gouvernance
- Publications

### Matière à intégrer progressivement

- Bien configurer ChatGPT
- Commandes et fonctions utiles
- Méthodes de prompting
- Vérification des réponses
- Confidentialité et données
- Utilisation professionnelle de l'IA
- IA appliquée à l'administration IT
- IA appliquée à la cybersécurité
- RAG et sources documentaires
- Limites des modèles et validation humaine
- Guides pédagogiques et fiches de référence

### Principe

> **L'IA assiste. L'humain comprend, vérifie et décide.**

---

# 08 — Développement & sécurité applicative

**Repository : [ELearningPlatform](https://github.com/bricehach/ELearningPlatform) — publié / actif**

### Contenus actuels

- C# / ASP.NET Core .NET 8
- API REST
- SQL Server
- Repository pattern
- JWT
- Cookies sécurisés
- BCrypt
- Swagger / OpenAPI
- Rate limiting
- Architecture applicative
- Installation
- Revue de sécurité

### Objectif dans le portfolio

Le développement est utilisé comme **outil de compréhension des applications** afin de mieux analyser ensuite leur exposition, leurs mécanismes d'authentification, leurs traces et leurs besoins de sécurisation.

---

# 09 — Troubleshooting

Le dépannage est transversal à l'ensemble de la base.

Chaque cas utile doit idéalement être documenté selon la structure :

```text
Symptôme
    ↓
Contexte
    ↓
Hypothèses
    ↓
Tests
    ↓
Cause
    ↓
Correction
    ↓
Vérification
    ↓
Ce que j'en retiens
```

Exemples de matière disponible :

- Windows qui redémarre de manière inattendue
- Event ID système
- BIOS et compatibilité Windows
- Pilotes
- Démarrage Windows
- BSOD
- Connectivité réseau
- VLAN / trunks
- Packet Tracer
- Ports COM / PuTTY
- Mise à jour Linux
- Machines virtuelles

---

# 10 — Reference Sheets

Cette section regroupera progressivement les informations qui doivent pouvoir être retrouvées très rapidement.

Exemples :

- Commandes Windows
- Commandes PowerShell
- Commandes Linux
- Commandes Git / GitHub
- Commandes et fonctions ChatGPT utiles
- Ports réseau
- CIDR / subnetting
- Event ID Windows
- Filtres de logs
- Outils SOC / DFIR
- Check-lists de diagnostic

L'objectif n'est pas de reproduire des documentations officielles, mais de construire des **fiches de référence contextualisées**, avec usage, limites, sécurité et exemples.

---

# Gouvernance de la base de connaissances

Avant publication, un contenu doit être vérifié selon plusieurs critères :

1. **Utilité** — apporte-t-il quelque chose de concret ?
2. **Exactitude** — les commandes, procédures et affirmations sont-elles vérifiées ?
3. **Reproductibilité** — une autre personne peut-elle suivre la méthode ?
4. **Sécurité** — aucune donnée sensible, secret ou information client / privée n'est publiée.
5. **Contexte** — les versions, prérequis et limites sont indiqués.
6. **Réversibilité** — lorsqu'une modification système est proposée, le retour arrière est documenté lorsque cela est possible.
7. **Source** — les informations évolutives doivent pouvoir être reliées à une documentation fiable.

---

# Vue d'ensemble

```text
Expérience + Formation + Labs + Dépannage
                  ↓
              Projet 00
                  ↓
        Base de connaissances IT
                  ↓
   ┌──────────────┼──────────────┐
   ↓              ↓              ↓
Guides         Références       Labs
   ↓              ↓              ↓
Comprendre     Retrouver      Démontrer
   └──────────────┼──────────────┘
                  ↓
              GitHub
                  ↓
              LinkedIn
```

GitHub constitue la **preuve technique et documentaire**.

LinkedIn présente le **parcours, le positionnement et les travaux les plus significatifs**.

Les deux sont conçus comme les deux niveaux d'un même portfolio professionnel.
