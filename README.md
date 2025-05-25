---
 README  
---

### 📝 `README.md` (sans DNS & CI/CD multi-environnement)

````markdown
# 🎉 EventApp - Projet Fullstack DevOps

**Développé par :** Samson Edorh  
**Technologies :** React (Frontend) · Express + PostgreSQL (Backend) · Docker · GitHub Actions  
**URL de démo (IP publique)** :  
- Frontend : http://157.180.38.74:8082  
- Backend : http://157.180.38.74:9002/events  

## 📚 Description

EventApp est une application web de gestion d'événements développée dans le cadre d’un devoir DevOps avancé. Elle permet :
- La création, visualisation et mise à jour des événements.
- Une API REST sécurisée en Node.js avec Sequelize/PostgreSQL.
- Un frontend moderne développé avec React.
- Un déploiement conteneurisé avec Docker & orchestré par `docker-compose`.
- Une pipeline de déploiement automatisée via GitHub Actions.
- Déploiement sur un VPS Linux Debian.

---

## 🧱 Architecture

```plaintext
📦 TP_EVENT_API
📦 TP_EVENT_WEB_APP
🔧 NGINX (à venir)
🔧 GitHub Actions
🐳 Docker & docker-compose
🌍 Serveur VPS public (IP : 157.180.38.74)
````

---

## ⚙️ Technologies utilisées

* **Frontend** : React + Tailwind CSS + Zustand
* **Backend** : Node.js, Express, Sequelize, PostgreSQL
* **CI/CD** : GitHub Actions
* **Déploiement** : Docker, GHCR, VPS Linux

---

## 🚀 Lancer l’application localement

```bash
# Cloner les deux dépôts
git clone https://github.com/tonpseudo/TP_EVENT_API
git clone https://github.com/tonpseudo/TP_EVENT_WEB_APP

# Lancer les services
cd myevent-app
docker compose up --build
```

* Frontend : [http://localhost:8082](http://localhost:8082)
* Backend : [http://localhost:9002/api/events](http://localhost:9002/api/events)

---

## 🌍 Démo en ligne

Accessible via l'IP publique du serveur :

| Composant | URL en ligne                                                                 | Port |
| --------- | ---------------------------------------------------------------------------- | ---- |
| Frontend  | [http://157.180.38.74:8082](http://157.180.38.74:8082)                       | 8082 |
| Backend   | [http://157.180.38.74:9002/api/events](http://157.180.38.74:9002/events) | 9002 |

---

## 🔁 Déploiement GitHub Actions (CI/CD)

* À chaque push sur le dépôt, l'image Docker est générée et poussée sur GHCR.
* Déploiement automatique sur le serveur via SSH.

---

## 📸 Démonstration

> Tu peux intégrer ici :

* Des captures d’écran de l’interface
* Une vidéo Loom ou MP4 si possible

---

## 📂 Structure des répertoires

```bash
myevent-app/
├── backend/           # Express + Sequelize
├── frontend/          # React app
├── docker-compose.yml
├── docker-compose.dev.yml
├── .github/workflows/ # GitHub Actions
└── README.md
```

---

## 📌 Auteur

**Samson Edorh-Tossa**
[GitHub](https://github.com/samwin25)

``
