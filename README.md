# DrawArchi

> **Outil de modelisation d'architectures d'entreprise TOGAF**
> Concevez et visualisez vos architectures d'entreprise TOGAF via l'interface Komos Architect, un outil de diagramme interactif base sur les standards ArchiMate.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![TOGAF](https://img.shields.io/badge/TOGAF-Architecture-blue)](https://www.opengroup.org/togaf)
[![ArchiMate](https://img.shields.io/badge/ArchiMate-3.2-orange)](https://www.opengroup.org/archimate-forum)

---

## Table des matieres

- [Presentation](#presentation)
- [Fonctionnalites](#fonctionnalites)
- [Architecture TOGAF supportee](#architecture-togaf-supportee)
- [Composants](#composants)
- [Installation](#installation)
- [Utilisation](#utilisation)
- [Roadmap](#roadmap)
- [Licence](#licence)

---

## Presentation

**DrawArchi** est un outil de modelisation visuelle d'architectures d'entreprise selon le framework **TOGAF (The Open Group Architecture Framework)**. Il integre **Komos Architect**, un moteur de diagramme specialise pour la notation **ArchiMate 3.2**, permettant de creer des vues architecturales professionnelles couvrant les 4 domaines TOGAF.

Concu pour les architectes d'entreprise, les consultants en transformation numerique et les DSI souhaitant documenter et communiquer leur SI selon les standards industriels.

---

## Fonctionnalites

- **Canvas interactif** : Creation de diagrammes ArchiMate drag-and-drop
- **Notation ArchiMate 3.2** : Tous les types d'elements et relations standards
- **Vues TOGAF** : Architecture Metier, Applicative, Technique, Donnees
- **Export** : Schemas exportables (PNG, SVG, JSON)
- **Navigation** : Zoom, pan, selection multiple, minimap
- **Collaboration** : Partage de diagrammes par lien
- **Templates** : Vues pre-configurees pour les livrables TOGAF courants

---

## Architecture TOGAF supportee

### Les 4 domaines d'architecture

| Domaine | Elements ArchiMate | Description |
|---|---|---|
| **Architecture Metier** | BusinessActor, BusinessRole, BusinessProcess, BusinessFunction | Processus, acteurs, roles, capacites |
| **Architecture Applicative** | ApplicationComponent, ApplicationService, ApplicationInterface | Applications, services, interfaces |
| **Architecture Technique** | Node, SystemSoftware, Technology Service | Infrastructure, serveurs, reseaux |
| **Architecture des Donnees** | DataObject, Artifact | Entites, flux, referentiels |

### Relations ArchiMate

- **Association** : Lien generique entre elements
- **Aggregation / Composition** : Hierarchie structurelle
- **Realization** : Element qui realise un autre
- **Assignment** : Role assigne a un element
- **Serving** : Service fourni a un element
- **Triggering / Flow** : Sequences et flux de donnees

---

## Composants

```
DrawArchi/
|-- komos-architect/     # Moteur de diagramme ArchiMate (submodule)
|                        # Interface de modelisation TOGAF interactive
|-- README.md
```

### Komos Architect

[Komos Architect](https://github.com/komos-architect) est le composant principal de DrawArchi. C'est un outil de modelisation d'architectures d'entreprise base sur les standards ArchiMate et TOGAF, offrant :

- Un canvas interactif pour la creation de diagrammes
- Une palette complete d'elements ArchiMate
- Des templates de vues TOGAF pre-configurees
- Un export vers differents formats

---

## Installation

### Cloner avec les submodules

```bash
git clone --recurse-submodules https://github.com/dagornc/DrawArchi.git
cd DrawArchi
```

Ou si deja clone :

```bash
git submodule update --init --recursive
```

### Lancer Komos Architect

```bash
cd komos-architect
npm install
npm run dev
```

L'application est disponible sur `http://localhost:5173`.

---

## Utilisation

### Creer un diagramme TOGAF

1. Ouvrir l'application sur `http://localhost:5173`
2. Selectionner un template de vue TOGAF (Metier, Applicatif, Technique, Donnees)
3. Glisser-deposer les elements ArchiMate depuis la palette
4. Connecter les elements avec les relations appropriees
5. Exporter le diagramme au format souhaite

### Exemple de vue applicative

```
ApplicationComponent [CRM]
  |-- Realization --> ApplicationService [Gestion Clients]
  |-- Association --> ApplicationComponent [ERP]
  |-- Serving --> BusinessProcess [Vente]
```

---

## Contexte du projet

DrawArchi est l'un des deux outils de modelisation TOGAF du portfolio :

| Outil | Description | Stack |
|---|---|---|
| **DrawArchi** | Modelisation ArchiMate via Komos Architect | TypeScript |
| **DrawTogaf** | Plateforme full-stack React + FastAPI avec export PPTX | TypeScript + Python |

DrawTogaf est la version plus complete avec backend API, GraphQL, PostgreSQL et export PowerPoint.

---

## Roadmap

- [x] Integration Komos Architect
- [x] Support ArchiMate 3.2
- [x] Vues TOGAF (Metier, Applicatif, Technique, Donnees)
- [ ] Export PowerPoint des livrables
- [ ] Import depuis DrawArchi / ArchiStudio
- [ ] Versioning des diagrammes
- [ ] Collaboration temps reel
- [ ] Integration avec DrawTogaf (backend API)

---

## Ressources TOGAF

- [TOGAF Standard](https://www.opengroup.org/togaf) - The Open Group Architecture Framework
- [ArchiMate 3.2](https://www.opengroup.org/archimate-forum) - Notation d'architecture d'entreprise
- [Komos Architect](https://github.com/komos-architect) - Moteur de diagramme

---

## Licence

Ce projet est sous licence **MIT**.

---

> Construit par [dagornc](https://github.com/dagornc) - Architecte logiciel et IA en Bretagne.
