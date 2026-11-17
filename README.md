# CPF – Catalogue des Formations Professionnelles (AMU)

Application Spring Boot de gestion des formations CPF (Compte Personnel de Formation) de l'université Aix-Marseille.

## Contexte 
Aix-Marseille Université propose plus de 350 formations CPF. Jusqu'ici, elles étaient décrites dans des fichiers Excel remplis par chaque composante (UFR, faculté), puis le fichier XML était produit à la main. Ce processus était peu fiable, difficile à maintenir et inadapté au volume de données.
Cette application remplace les fichiers Excel et la production manuelle du XML

## Prérequis

- Java 21
- Avoir un compte utilisateur AMU pour l'authentification CAS

## Lancer
Le profil `test` est actif par défaut. La base de données est en mémoire (H2), recréée à chaque démarrage.

```bash
mvn spring-boot:run
```

L'application est accessible sur [http://localhost:8080](http://localhost:8080).  
La connexion redirige vers le CAS AMU (`ident.univ-amu.fr`).


## Build JAR

```bash
mvn clean package -DskipTests
java -jar target/cpf-0.0.1-SNAPSHOT.jar
```
