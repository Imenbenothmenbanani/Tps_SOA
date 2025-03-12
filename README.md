# 📌 API GraphQL de Gestion des Tâches

## 📖 Description

Cette API, développée avec Node.js, Express et Apollo Server, permet de gérer un système de tâches de manière efficace et flexible.

## 🚀 Installation

### 📂 1. Cloner le dépôt et installer les dépendances

```sh
mkdir tp-graphql
cd tp-graphql
npm init -y
npm install express @apollo/server body-parser @graphql-tools/schema graphql
```

## 🎯 Lancer le serveur

```sh
node index.js
```

Accéder à l'interface graphique d'Apollo Studio :

```
http://localhost:5000/graphql
```

## 📡 Exemples de requêtes GraphQL

### 🔍 Récupérer toutes les tâches

```graphql
query {
  tasks {
    id
    title
    description
    completed
  }
}
```

### ✏️ Ajouter une nouvelle tâche

```graphql
mutation {
  addTask(
    title: "Nouvelle tâche"
    description: "Description de la tâche"
    completed: false
  ) {
    id
    title
  }
}
```

### ✅ Marquer une tâche comme terminée

```graphql
mutation {
  completeTask(id: "1") {
    id
    title
    completed
  }
}
```

### 🔄 Modifier la description d'une tâche

```graphql
mutation {
  changeDescription(id: "1", description: "Nouvelle description") {
    id
    title
    description
  }
}
```

### ❌ Supprimer une tâche

```graphql
mutation {
  deleteTask(id: "1")
}
```
