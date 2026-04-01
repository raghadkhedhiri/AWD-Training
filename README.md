
# 🚀 Architecture Microservices : Du Monolithe vers l'Écosystème Distribué
📅 **Année universitaire : 2025–2026** 
Ce dépôt contient l'ensemble des ressources pédagogiques et techniques pour le module de développement d'architectures microservices. L'objectif est de transformer une application monolithique de recrutement en un système distribué résilient et scalable.

---

## 🎯 Objectifs d'Apprentissage (AA)

À l'issue de cette formation, l'apprenant sera capable de :

* **AA1 :** Distinguer les architectures microservices des monolithes en identifiant leurs avantages et contraintes opérationnelles.
* **AA2 :** Concevoir et développer des services autonomes en respectant les principes de découplage et de responsabilité unique.
* **AA3 :** Mettre en œuvre la découverte de services pour automatiser la mise en relation dynamique des composants du système.
* **AA4 :** Configurer une API Gateway pour centraliser le routage des flux et appliquer des filtres transverses.
* **AA5 :** Gérer la configuration externalisée pour modifier le comportement des services sans redémarrage manuel.
* **AA6 :** Sécuriser l'architecture via des mécanismes d'authentification et d'autorisation centralisés.
* **AA7 :** Conteneuriser les applications avec Docker pour assurer un déploiement fluide et reproductible.
* **AA8 :** Réaliser un projet complet intégrant la communication inter-services et la validation des flux de bout en bout.

---

## 🏗️ Étude de Cas : Plateforme de Recrutement (Job Board)

Le projet s'appuie sur un système réel de gestion d'offres d'emploi.

### 1. Du Monolithe (Conceptuel) ...
Initialement, toutes les entités (Candidats, Jobs, Candidatures, Meetings) partagent le même espace et la même base de données.
* **Schéma :** ![class-diagram](https://github.com/badi3a/AWD-Training/blob/main/documentation/diag/class-diagram.png)

### 2. ... Vers les Domaines Microservices (DDD)
Pour valider l'**AA2**, nous avons découpé l'application en domaines métier autonomes (**Bounded Contexts**) :
* **Candidate Domain** (Microservice 1)
* **Job Domain** (Microservice 2)
* **Application Domain** (Microservice 3)
* **Notification Domain** (Microservice 4)
* **Meeting Domain** (Microservice 5)

* **Schéma de découpage :** [`domain-class-diagram`](https://github.com/badi3a/AWD-Training/blob/main/documentation/diag/domain-class-diagram.png)

---

## 🛠️ Architecture Technique Globale

L'architecture finale (Validation **AA8**) intègre l'ensemble des composants d'infrastructure nécessaires à un environnement de production :

* **API Gateway :** Point d'entrée unique (Spring Cloud Gateway).
* **Service Discovery :** Annuaire dynamique (Netflix Eureka).
* **Config Server :** Gestion centralisée des propriétés (Git/Native).
* **Message Broker :** Communication asynchrone (RabbitMQ).
* **Identity Provider :** Sécurisation des accès (Keycloak).

* **Schéma Global :** `[microservices-global-architecture`](https://github.com/badi3a/AWD-Training/blob/main/documentation/diag/microservices-global-architecture.png)

---

## 📦 Stack Technologique

| Composant | Technologie |
| :--- | :--- |
| **Langages** | Java (Spring Boot), Python (FastAPI), Node.js |
| **Bases de données** | H2, MySQL, MongoDB |
| **Infrastructure** | Docker, Docker Compose |
| **Communication** | REST (Synchrone) & RabbitMQ (Asynchrone) |
| **Front End** | Angular |

---

## 🏫 Cadre pédagogique

### Enseignante : [Badia Bouhdid](https://www.linkedin.com/in/badiabouhdid)

Ce workshop a été développé dans le cadre du module **Applications Web Distribuées**,  
à l’**École d’Ingénieurs ESPRIT**.
