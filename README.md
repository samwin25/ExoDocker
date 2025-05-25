Voici un **README complet et détaillé** pour ton projet **myevent-app**, conçu pour permettre à toute personne externe de forker, cloner, exécuter et tester l'application localement sans erreur.

---

# 🎉 myevent-app

**myevent-app** est une application web full-stack permettant de créer, visualiser et gérer des événements. Elle est construite avec React pour le frontend, Node.js/Express pour le backend, PostgreSQL pour la base de données, et Docker Compose pour l'orchestration.

---

## 🌐 Sous-domaines en production

* **Frontend** : [https://samson-eventapp-frontend.ldsdevops.xyz](https://samson-eventapp-frontend.ldsdevops.xyz)
* **Backend** : [https://samson-eventapp-backend.ldsdevops.xyz](https://samson-eventapp-backend.ldsdevops.xyz)

---

## 📁 Arborescence du projet

```bash
myevent-app/
├── TP_EVENT_API/               # Backend Express
│   ├── Dockerfile
│   └── ...
├── TP_EVENT_WEB_APP/           # Frontend React
│   ├── Dockerfile
│   └── ...
├── nginx/
│   └── conf.d/
│       └── default.conf        # Configuration Nginx
├── .env                        # Variables d'environnement
├── docker-compose.yml
└── README.md
```



---

## 🚀 Fonctionnalités

* Création et gestion d'événements
* Interface utilisateur réactive avec React
* API RESTful sécurisée avec Express
* Base de données PostgreSQL
* Orchestration avec Docker Compose
* Reverse proxy avec Nginx
* Déploiement continu via GitHub Actions([FreeCodeCamp][1], [Medium][2])

---

## 🛠️ Prérequis

* [Docker](https://docs.docker.com/get-docker/)
* [Docker Compose](https://docs.docker.com/compose/install/)
* [Git](https://git-scm.com/)

---

## 📦 Installation et exécution locale

1. **Cloner le dépôt**

   ```bash
   git clone https://github.com/<votre-nom-utilisateur>/myevent-app.git
   cd myevent-app
   ```



2. **Configurer les variables d'environnement**

   Créer un fichier `.env` à la racine du projet avec le contenu suivant :

   ```env
   DB_HOST=postgres
   DB_PORT=5432
   DB_USER=eventuser
   DB_PASSWORD=eventpass
   DB_NAME=eventdb
   BACKEND_PORT=9002
   REACT_APP_API_URL=http://backend:9002
   ```



3. **Construire et démarrer les conteneurs**

   ```bash
   docker-compose up --build
   ```



4. **Accéder à l'application**

   * Frontend : [http://localhost:8082](http://localhost:8082)
   * Backend API : [http://localhost:9002](http://localhost:9002)
   * Base de données PostgreSQL : accessible sur le port `5433`([GitHub][3])

---

## 🧪 Tests

* Accédez à l'interface frontend via [http://localhost:8082](http://localhost:8082).
* Créez un nouvel événement et assurez-vous qu'il apparaît dans la liste.
* Vérifiez que les données sont correctement stockées en interrogeant l'API backend ou en accédant à la base de données PostgreSQL.

---

## 🐳 Déploiement avec GitHub Actions

Le projet est configuré pour un déploiement continu via GitHub Actions. À chaque push sur les branches `myevent-app-samson` ou `develop` :

1. Les images Docker du frontend et du backend sont construites et poussées vers GitHub Container Registry.
2. Le serveur distant est mis à jour via SSH, les conteneurs sont redémarrés avec les nouvelles images.

**Remarque** : Assurez-vous que les secrets suivants sont configurés dans les paramètres du dépôt GitHub :

* `TOKEN` : Jeton d'accès personnel pour GitHub Container Registry.
* `SSH_PRIVATE_KEY` : Clé privée SSH pour accéder au serveur distant.
* `SSH_USER` : Nom d'utilisateur SSH.
* `SSH_HOST` : Adresse IP ou nom de domaine du serveur distant.
* `REACT_APP_API_URL` : URL de l'API backend pour le frontend (par exemple, `https://samson-eventapp-backend.ldsdevops.xyz`).

---

## 📝 Notes importantes

* Le fichier `.gitignore` est configuré pour exclure les fichiers sensibles et les dépendances :

```gitignore
  node_modules/
  .env
  .env.local
  .env.development.local
  .env.test.local
  .env.production.local
```



* Assurez-vous que la variable `REACT_APP_API_URL` est correctement définie dans le fichier `.env` pour que le frontend puisse communiquer avec le backend.

---

## 🤝 Contribuer

Les contributions sont les bienvenues ! Pour contribuer :

1. Forkez le projet.
2. Créez une branche pour votre fonctionnalité : `git checkout -b ma-fonctionnalité`.
3. Commitez vos modifications : `git commit -m 'Ajout de ma fonctionnalité'`.
4. Poussez vers la branche : `git push origin ma-fonctionnalité`.
5. Ouvrez une Pull Request.


---

N'hésitez pas à me faire savoir si vous avez besoin d'autres informations ou d'assistance supplémentaire !

[1]: https://www.freecodecamp.org/news/how-to-write-a-good-readme-file/?utm_source=chatgpt.com "How to Write a Good README File for Your GitHub Project"
[2]: https://medium.com/%40matthew.rosendin/dockerizing-a-full-stack-application-89a7d69e11e9?utm_source=chatgpt.com "Dockerizing a Full-stack Application | by Matthew Rosendin - Medium"
[3]: https://github.com/tiangolo/full-stack-flask-couchbase/blob/master/%7B%7Bcookiecutter.project_slug%7D%7D/README.md?utm_source=chatgpt.com "full-stack-flask-couchbase/{{cookiecutter.project_slug ... - GitHub"
