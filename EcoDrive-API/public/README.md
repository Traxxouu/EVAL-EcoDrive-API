# EcoDrive – API de suivi de conduite écologique 🚘

## Sommaire
* [À propos](#à-propos)
* [Fonctionnalités](#fonctionnalités)
* [Modèles de données](#modèles-de-données)
* [Technologies utilisées](#technologies-utilisées)
* [Prérequis](#prérequis)
* [Installation](#installation)
* [Utilisation de l'API](#utilisation-de-lapi)
* [Documentation Swagger](#documentation-swagger)
* [Roadmap](#roadmap)
* [Contact](#contact)

## À propos
**EcoDrive** est une API qui permet aux utilisateurs d'enregistrer leurs trajets en voiture et de recevoir des informations sur leurs conduites. Elle vise à promouvoir une conduite eco responsable, a réduire la consommation de carburant et à limiter les émissions de CO2.

<div>
  <img src="pollution.png" width=500px>
</div>

## Fonctionnalités

| Fonction | Méthode | Endpoint |
|----------|---------|----------|
| Créer un utilisateur | `POST` | `/users` |
| Obtenir la liste des utilisateurs | `GET` | `/users` |
| Récupérer un utilisateur par ID | `GET` | `/users/{id}` |
| Démarrer un trajet | `POST` | `/trips` |
| Obtenir les infos d'un trajet | `GET` | `/trips/{id}` |
| Obtenir les statistiques d'un utilisateur | `GET` | `/users/{id}/stats` |

## Modèles de données

### 🧍 Utilisateur (`User`)
```json
{
  "id": 1,
  "username": "Mael",
  "email": "mael.barbe@efrei.net"
}
```

### 🛣️ Trajet (`Trip`)
```json
{
  "id": 1,
  "userId": 1,
  "distance_km": 12.5,
  "score": 87 / 100,
  "date": "18-04-2025"
}
```

### 📊 Statistiques (`Stats`)
```json
{
  "total_trips": 5,
  "total_distance": 78.2,
  "average_score": 82
}
```

## Technologies utilisées
* **Backend** : Node.js
* **Documentation API** : Swagger
* **Base de données** : MySQL
* **Outils** : VS Code

## Prérequis
* Node.js
* Git
* Vs code

## Installation

1. Cloner le dépôt
```bash
git clone https://github.com/Traxxouu/EVAL-EcoDrive-API.git
cd EcoDrive-API
```

2. Installer les dépendances (si Node.js)
```bash
npm install
```

3. Lancer le projet
```bash
npm run dev
```

## Utilisation de l'API

Tu peux tester l'API avec Swagger :

Exemple de requête :
```http
POST /users
Content-Type: application/json

{
  "username": "Traxxouu",
  "email": "mael.barbe@efrei.net"
}
```

## Documentation API sur Swagger

Tu peux accéder à la documentation complète via Swagger :

👉 `http://localhost:3000/api-docs` *(ou selon ton port local)*
Tu peux aussi ouvrir le fichier `swagger.json` dans Swagger Editor et visualiser la page 

## Roadmap
* Authentification basique
* Création et récupération de trajets
* Ajout d'un score automatique via algorithme
* Ajout du support géographique via GPS
* Exportation CSV / JSON

## Version du Readme 
version : v1 (18-04-2025)



Créé par : **Maël Barbe**
🔗 GitHub : @Traxxouu
📧 Email : mael.barbe@efrei.net

