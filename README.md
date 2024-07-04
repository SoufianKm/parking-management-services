# Projet de Gestion de Parkings Privés - Backend

Bienvenue dans le dépôt GitHub de la partie backend de notre application de gestion de parkings privés. Ce document fournit des informations détaillées sur l'installation, la configuration et l'utilisation de l'application backend.

> **Note** : La partie frontend de ce projet est disponible dans un autre dépôt. Vous pouvez la trouver à l'adresse suivante : [parking-management](https://github.com/OussamaFASSIR/parking-management.git).

## Table des Matières

1. [Description](#description)
2. [Technologies Utilisées](#technologies-utilisées)
3. [Prérequis](#prérequis)
4. [Installation](#installation)
5. [Configuration](#configuration)
6. [Exécution](#exécution)
7. [Tests](#tests)
8. [Déploiement](#déploiement)
9. [Contribution](#contribution)
10. [Licence](#licence)

## Description

Cette application backend fait partie d'un projet de gestion de parkings privés. Elle fournit les services backend nécessaires pour gérer les utilisateurs, les parkings, les réservations, et les abonnements. Elle expose une API RESTful utilisée par la partie frontend de l'application.

## Technologies Utilisées

- **Java EE** : Plateforme de développement.
- **Maven** : Gestionnaire de projet et des dépendances.
- **Spring Boot** : Framework pour le développement d'applications Java.
- **Spring Security** : Sécurité de l'application.
- **Spring MVC** : Architecture Modèle-Vue-Contrôleur.
- **Hibernate JPA** : Gestion de la persistance des données.
- **MySQL** : Base de données relationnelle.
- **Apache** : Serveur web.

## Prérequis

Avant d'installer et d'exécuter cette application, assurez-vous d'avoir les éléments suivants installés sur votre machine :

- JDK 11 ou supérieur
- Maven 3.6 ou supérieur
- MySQL 5.7 ou supérieur
- Git

## Installation

Clonez ce dépôt sur votre machine locale en utilisant la commande suivante :

```bash
git clone https://github.com/SoufianKm/parking-management-services.git
cd parking-management-services
```

## Configuration

1. Créez une base de données MySQL pour l'application :

```sql
CREATE DATABASE nom_database;
```

2. Modifiez le fichier `src/main/resources/application.properties` pour configurer la connexion à votre base de données MySQL :

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/nom_database
spring.datasource.username=yourUsername
spring.datasource.password=yourPassword
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
...
```

3. (Optionnel) Configurez les autres paramètres nécessaires tels que la sécurité et les ports dans le fichier `application.properties`.

## Exécution

Pour exécuter l'application, utilisez la commande Maven suivante :

```bash
mvn spring-boot:run
```

L'application sera accessible à l'adresse `http://localhost:8080`.

## Tests

Pour exécuter les tests unitaires, utilisez la commande Maven suivante :

```bash
mvn test
```

## Déploiement

Pour déployer cette application, vous pouvez construire un fichier JAR exécutable avec la commande suivante :

```bash
mvn clean package
```

Le fichier JAR sera généré dans le répertoire `target`. Vous pouvez alors exécuter l'application en utilisant la commande suivante :

```bash
java -jar target/parking-management-services.jar
```

## Contribution

Les contributions sont les bienvenues ! Si vous souhaitez contribuer à ce projet, veuillez suivre les étapes suivantes :

1. Fork ce dépôt
2. Créez une branche pour votre fonctionnalité (`git checkout -b feature/nouvelle-fonctionnalité`)
3. Commitez vos modifications (`git commit -m 'Ajouter une nouvelle fonctionnalité'`)
4. Poussez votre branche (`git push origin feature/nouvelle-fonctionnalité`)
5. Ouvrez une Pull Request

## Licence

Ce projet est sous licence MIT. Voir le fichier `LICENSE` pour plus de détails.
