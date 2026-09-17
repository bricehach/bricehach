# Windows & Infrastructure — Roadmap de publication

## Projet 00 — Portfolio professionnel LinkedIn + GitHub

Ce document organise la matière déjà travaillée autour de Windows et de l'infrastructure afin de la transformer progressivement en ressources GitHub utiles, vérifiables et réutilisables.

> **Objectif : ne pas publier une collection de commandes, mais des ressources permettant de comprendre, agir, vérifier et revenir en arrière.**

---

## Règle documentaire commune

Chaque ressource publiée doit, autant que possible, suivre cette structure :

```text
Contexte
   ↓
Objectif
   ↓
Prérequis
   ↓
Comprendre le mécanisme
   ↓
Procédure
   ↓
Vérification
   ↓
Risques / limites
   ↓
Retour arrière
   ↓
Troubleshooting
   ↓
Ce qu'il faut retenir
```

Les contenus seront classés selon quatre formats :

- **GUIDE** : réaliser une tâche de manière reproductible ;
- **REFERENCE** : retrouver rapidement commandes, paramètres et informations ;
- **LAB** : reproduire une expérience ou un diagnostic ;
- **EXPLAINED** : comprendre un mécanisme, ses effets, ses risques et ses limites.

---

# 1 — Installation et préparation de Windows

## 1.1 Installation propre de Windows 11 Pro

**Statut : matière disponible**  
**Format cible : GUIDE + EXPLAINED**

Points à documenter :

- prérequis matériels ;
- UEFI / Secure Boot / TPM ;
- création du support d'installation ;
- installation sur SSD / NVMe ;
- choix des partitions ;
- compte local et compte Microsoft ;
- installation des pilotes ;
- Windows Update ;
- vérifications après installation ;
- points spécifiques aux machines non officiellement prévues pour Windows 11 ;
- restauration et plan de retour arrière.

## 1.2 Compte administrateur local

**Statut : matière disponible**  
**Format cible : GUIDE + EXPLAINED**

Objectif : expliquer les différentes méthodes légitimes de création et de gestion d'un compte local, leurs limites et les différences avec un compte Microsoft.

## 1.3 Post-installation reproductible

**Statut : à structurer**  
**Format cible : CHECKLIST / GUIDE**

- pilotes ;
- mises à jour ;
- applications ;
- navigateur ;
- sauvegarde ;
- Defender ;
- confidentialité ;
- journaux ;
- point de restauration ;
- image système si nécessaire.

---

# 2 — Confidentialité, télémétrie et transparence des données

## 2.1 Comprendre la collecte de données Windows

**Statut : matière disponible, à vérifier avant publication**  
**Format cible : EXPLAINED**

Le document devra distinguer clairement :

- télémétrie ;
- diagnostics ;
- publicité / identifiant publicitaire ;
- historique d'activité ;
- personnalisation ;
- données de localisation ;
- recherche Windows ;
- services cloud ;
- synchronisation ;
- données facultatives et obligatoires selon édition et configuration.

Aucune option ne sera présentée comme « inutile » sans expliquer son rôle et l'impact de sa désactivation.

## 2.2 Windows 11 — Configuration orientée confidentialité

**Statut : matière disponible**  
**Format cible : GUIDE**

Pour chaque réglage :

```text
Fonction
↓
À quoi sert-elle ?
↓
Quelles données sont concernées ?
↓
Impact de la désactivation
↓
Procédure
↓
Vérification
↓
Retour arrière
```

## 2.3 Services et fonctions optionnelles

**Statut : matière disponible, à consolider**  
**Format cible : REFERENCE + EXPLAINED**

Objectif : éviter le « debloat aveugle ». Toute recommandation devra préciser :

- nom du service / composant ;
- fonction ;
- dépendances ;
- impact ;
- conditions dans lesquelles une modification est pertinente ;
- méthode de restauration.

---

# 3 — Maintenance et gestion des applications

## 3.1 Winget

**Statut : matière disponible**  
**Format cible : GUIDE + REFERENCE**

Contenu prévu :

- `winget search` ;
- `winget list` ;
- `winget upgrade` ;
- `winget upgrade --all` ;
- installation ;
- désinstallation ;
- sources ;
- export / import ;
- exécution depuis PowerShell / Terminal ;
- erreurs fréquentes ;
- utilisation dans une routine de maintenance.

## 3.2 Mise à jour logicielle contrôlée

**Statut : matière disponible**  
**Format cible : GUIDE**

Objectif : proposer une procédure cohérente combinant Windows Update, pilotes, applications et vérification après mise à jour.

---

# 4 — Pilotes et matériel

## 4.1 Cartographie des commandes de diagnostic des pilotes

**Statut : matière disponible**  
**Format cible : REFERENCE**

À couvrir :

- `driverquery` ;
- PowerShell / CIM ;
- PnPUtil ;
- Gestionnaire de périphériques ;
- vérification des versions ;
- pilotes signés ;
- erreurs et périphériques problématiques.

## 4.2 BIOS / firmware / compatibilité Windows

**Statut : matière disponible**  
**Format cible : EXPLAINED + TROUBLESHOOTING**

Objectif : expliquer quand un BIOS ou firmware peut contribuer à l'instabilité, comment vérifier les versions et quelles précautions prendre avant une mise à jour.

---

# 5 — Réparation du démarrage Windows

## 5.1 Bootrec et environnement de récupération

**Statut : matière importante disponible**  
**Format cible : GUIDE + REFERENCE**

Contenu prévu :

- WinRE ;
- Startup Repair ;
- `bootrec /scanos` ;
- `bootrec /fixmbr` ;
- `bootrec /fixboot` ;
- `bootrec /rebuildbcd` ;
- BCD ;
- `bcdboot` ;
- `diskpart` ;
- UEFI / EFI System Partition ;
- différences BIOS/MBR et UEFI/GPT ;
- sauvegarde avant intervention ;
- arbre décisionnel.

## 5.2 Arbre de décision de réparation

**Statut : matière disponible**  
**Format cible : GUIDE / DECISION TREE**

```text
Windows démarre ?
├── Oui → analyser stabilité / journaux
└── Non
    ├── WinRE accessible ?
    ├── disque détecté ?
    ├── partition EFI présente ?
    ├── BCD valide ?
    └── réparation adaptée
```

---

# 6 — BSOD / Bug Check

## 6.1 Comprendre un BSOD

**Statut : matière importante disponible**  
**Format cible : EXPLAINED**

- bug check ;
- stop code ;
- dump mémoire ;
- différence symptôme / cause ;
- pilote, RAM, stockage, firmware, matériel ;
- événements associés ;
- collecte avant modification.

## 6.2 Outils d'analyse

**Statut : matière disponible**  
**Format cible : GUIDE + REFERENCE**

- WinDbg ;
- fichiers `.dmp` ;
- Event Viewer ;
- Reliability Monitor ;
- outils Microsoft utiles ;
- commandes de vérification système.

## 6.3 Cartographie des Bug Checks

**Statut : à construire progressivement**  
**Format cible : REFERENCE**

Pour chaque code :

```text
Code
↓
Signification générale
↓
Causes fréquentes
↓
Données à collecter
↓
Tests
↓
Pistes de correction
```

---

# 7 — Journaux Windows et stabilité

## 7.1 Event ID liés aux arrêts et redémarrages

**Statut : matière disponible**  
**Format cible : GUIDE + REFERENCE**

Premiers cas déjà travaillés :

- Event ID 6008 ;
- Event ID 1101 ;
- corrélation avec redémarrages inattendus ;
- hypothèses pilotes / BIOS / alimentation / système ;
- importance de la chronologie.

## 7.2 Méthode d'analyse d'un incident Windows

**Statut : à structurer**  
**Format cible : LAB / TROUBLESHOOTING**

```text
Symptôme
↓
Horodatage
↓
Logs système
↓
Logs applicatifs
↓
Reliability Monitor
↓
Pilotes / firmware
↓
Hypothèses
↓
Tests
↓
Correction
↓
Validation
```

---

# 8 — Hardening Windows

## 8.1 Microsoft Defender

**Statut : matière disponible**  
**Format cible : GUIDE + EXPLAINED**

- paramètres de protection ;
- contrôles ;
- scans ;
- exclusions ;
- risques d'exclusions trop larges ;
- validation de l'état de protection.

## 8.2 GPO et paramètres de sécurité

**Statut : matière disponible / à consolider**  
**Format cible : GUIDE + LAB**

## 8.3 Hardening reproductible

**Statut : à construire progressivement**  
**Format cible : GUIDE / BASELINE**

Principe : toujours documenter ce qui est modifié, pourquoi, comment le vérifier et comment restaurer le réglage précédent.

---

# 9 — Troubleshooting Windows

## 9.1 Méthode générale

**Statut : matière disponible**  
**Format cible : GUIDE**

```text
Observer le symptôme
↓
Définir le périmètre
↓
Collecter avant de modifier
↓
Établir des hypothèses
↓
Tester une variable à la fois
↓
Mesurer le résultat
↓
Documenter
↓
Conserver un retour arrière
```

## 9.2 Cas pratiques disponibles

- démarrage ;
- BSOD ;
- pilotes ;
- BIOS ;
- événements 6008 / 1101 ;
- applications Windows ;
- problèmes liés à la suppression de composants ;
- associations de fichiers ;
- maintenance et mises à jour.

---

# Ordre de publication recommandé

| Priorité | Ressource | Format | État |
|---:|---|---|---|
| 1 | Installation propre Windows 11 Pro | GUIDE | Matière disponible |
| 2 | Confidentialité et télémétrie Windows 11 | EXPLAINED + GUIDE | À vérifier / structurer |
| 3 | Winget — guide et référence | GUIDE + REFERENCE | Matière disponible |
| 4 | Réparer le démarrage Windows | GUIDE | Matière disponible |
| 5 | BSOD — méthode de diagnostic | EXPLAINED + GUIDE | Matière disponible |
| 6 | Pilotes Windows — diagnostic | REFERENCE | Matière disponible |
| 7 | Event ID et stabilité Windows | GUIDE + LAB | Matière disponible |
| 8 | Microsoft Defender / hardening | GUIDE | À consolider |
| 9 | Troubleshooting Windows | GUIDE | Matière disponible |
| 10 | Baseline Windows reproductible | GUIDE / BASELINE | À construire |

---

# Structure cible du futur repository

```text
windows-infrastructure-lab/
├── README.md
├── CHANGELOG.md
├── docs/
│   ├── roadmap.md
│   ├── troubleshooting.md
│   └── lessons-learned.md
├── installation/
├── privacy-telemetry/
├── maintenance-winget/
├── drivers-hardware/
├── boot-recovery/
├── bsod-debugging/
├── event-logs/
├── defender-hardening/
├── gpo-security/
├── labs/
└── reference/
```

---

# Critères de publication

Une ressource passe de **matière disponible** à **publiée** uniquement si :

- les commandes ont été relues ;
- les versions de Windows concernées sont indiquées ;
- les effets secondaires possibles sont documentés ;
- les données sensibles ont été retirées ;
- une méthode de vérification est fournie ;
- un retour arrière est documenté lorsque cela est pertinent ;
- le contenu ne présente pas une préférence personnelle comme une règle générale ;
- les informations susceptibles d'évoluer ont été vérifiées avant publication.

---

## Fil conducteur

**Installer proprement → comprendre la configuration → réduire les risques → maintenir → diagnostiquer → réparer → durcir → documenter.**
