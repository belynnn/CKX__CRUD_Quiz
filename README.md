# 🧠 Quizz App

Application MERN permettant la **création, gestion et participation à des quiz en temps réel**.

## 🎯 Objectif

Permettre à un·e administrateur·ice de créer des quiz dynamiques avec différents formats de question (QCM, réponse libre, choix multiples) et de lancer des sessions de jeu où les utilisateur·ices (inscrit·es ou anonymes) peuvent jouer ensemble en direct.  
Une session dure jusqu'à la complétion du quiz, avec un **système de score** et un **classement final**.

---

## 🧩 Diagrammes (Modèle de données simplifié)

### 🧑 User

| Champ       | Type     |
|-------------|----------|
| userId      | ObjectId |
| pseudo      | String   |
| mail        | String   |
| password    | String   |
| privacy     | Boolean  |
| createdAt   | Date     |

---

### ❓ Quiz

| Champ       | Type     |
|-------------|----------|
| quizId      | ObjectId |
| title       | String   |
| theme       | String   |
| type        | String   |
| questions   | [Object] |
| createdAt   | Date     |

---

### 🕹️ Party (Participation)

| Champ       | Type     |
|-------------|----------|
| userId      | ObjectId |
| quizId      | ObjectId |
| score       | Number   |
| createdAt   | Date     |

---

## 🖥️ Pages

### 👯 Partagées
- Cookies RGPD / Consentement

### 🧑 Utilisateur·ice
- Register (pseudo, mail, password)
- Login / Logout
- Liste des quiz
- Participation à une session

### 👩‍💼 Admin
- Liste des quiz
  - ➕ Créer un quiz (titre, thème, type, questions, réponses)
  - 🖊️ Modifier un quiz
  - ❌ Supprimer / désactiver un quiz
  - ▶️ Lancer une session
  - 🗑️ Supprimer une session

---

## 🛠️ Fonctionnalités

### 🧑 Utilisateur·ice
- ✅ S’inscrire et se connecter
- 👥 Rejoindre une session de quiz en direct
- 📝 Répondre aux questions (choix multiples, libre, etc.)
- 📊 Voir ses résultats à la fin du quiz

### 👩‍💼 Admin
- 🧪 Créer / Modifier / Supprimer des quiz
- 📋 Ajouter / modifier / supprimer des questions et réponses
- ▶️ Lancer ou supprimer des sessions de jeu
- 💤 Désactiver un quiz sans le supprimer (soft delete)

---

## #️⃣ Technologies utilisées

### 🧱 Méthodologie
- Kanban via Trello

### ⚙️ Infrastructure
- Raspberry Pi 4
- Linux Debian

### 🗄️ Base de données
- MongoDB

### 🔙 Backend
- Node.js
- Express.js

### 🎨 Frontend
- HTML / CSS / JavaScript
- React (JSX)