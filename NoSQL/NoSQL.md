# 📌 Fiche NoSQL

## 🔹 Introduction à NoSQL
**NoSQL** (Not Only SQL) est une catégorie de bases de données conçues pour répondre à des besoins différents des bases relationnelles (SQL), notamment en matière de **scalabilité**, de **flexibilité** et de **performance**.

**Principaux avantages :**
- Gestion efficace des **Big Data** (Volume, Variété, Vélocité)
- Modèle **sans schéma rigide** (flexibilité accrue)
- **Scalabilité horizontale** (ajout de serveurs pour gérer plus de données)
- Adapté aux **données non structurées ou semi-structurées**
- **Haute disponibilité et tolérance aux pannes**

---

## 🔹 Différents Types de Bases NoSQL

### 📌 1. Clé-Valeur
- Stocke des paires **clé-valeur**, simple et rapide.
- Exemples : Redis, Riak, DynamoDB
- **Commande Redis** :
  ```sh
  SET nom "Paul"
  GET nom  # Renvoie Paul
  ````

### 📌 2. Document
- Stocke des **documents JSON/BSON**.
- Exemples : MongoDB, CouchDB
- **Commande MongoDB** :
  ```json
  db.utilisateurs.insertOne({"nom": "Paul", "age": 25})
  db.utilisateurs.find({"nom": "Paul"})
  ```

### 📌 3. Colonne-Famille
- Stocke les données **en colonnes** plutôt qu’en lignes.
- Exemples : Cassandra, HBase
- **Commande Cassandra (CQL)** :
  ```sql
  CREATE TABLE users (id UUID PRIMARY KEY, name text, age int);
  INSERT INTO users (id, name, age) VALUES (uuid(), 'Paul', 25);
  ```

### 📌 4. Graphe
- Stocke des données sous forme de **graphes (nœuds, arêtes)**.
- Exemples : Neo4j, OrientDB
- **Commande Cypher (Neo4j)** :
  ```cypher
  CREATE (p:Person {name: 'Paul'})
  MATCH (p:Person) RETURN p;
  ```

---

## 🔹 Commandes NoSQL
### 📌 Opérations CRUD de base
| Type | Commande |
|------|---------|
| **Insertion** | `db.collection.insertOne({...})` |
| **Lecture** | `db.collection.find({...})` |
| **Mise à jour** | `db.collection.updateOne({...}, {$set: {...}})` |
| **Suppression** | `db.collection.deleteOne({...})` |

### 📌 Requêtes MongoDB (Query NoSQL)
- **Filtrage** : `db.utilisateurs.find({age: {$gte: 25}})`
- **Tri** : `db.utilisateurs.find().sort({age: -1})`
- **Agrégation** :
  ```json
  db.orders.aggregate([
    { $match: { status: "livré" } },
    { $group: { _id: "$client", total: { $sum: "$montant" } } }
  ])
  ```

---

## 🔹 Types de Données NoSQL
### 📌 JSON (Document)
```json
{
  "nom": "Paul",
  "age": 25,
  "adresse": {"ville": "Paris", "code_postal": "75001"}
}
```

### 📌 Clé-Valeur (Redis)
```sh
SET user:1001 "{nom: 'Paul', age: 25}"
GET user:1001
```

### 📌 HSTORE (PostgreSQL)
```sql
CREATE TABLE users (id SERIAL PRIMARY KEY, infos HSTORE);
INSERT INTO users (infos) VALUES ('"nom"=>"Paul", "age"=>"25"');
SELECT infos -> 'nom' FROM users;
```

### 📌 Graphe (Neo4j)
```cypher
CREATE (p:Person {name: 'Paul'})-[:CONNAIT]->(q:Person {name: 'Quentin'})
MATCH (p:Person)-[:CONNAIT]->(q) RETURN p, q;
```

---

## 🔹 NoSQL vs SQL
| Critère | SQL (Relationnel) | NoSQL |
|---------|------------------|--------|
| **Modèle** | Tables & Relations | Document, Clé-Valeur, Graphe, Colonne |
| **Schéma** | Rigide | Flexible |
| **Requêtes** | SQL (normé) | API spécifiques |
| **Scalabilité** | Verticale (serveur unique) | Horizontale (cluster) |
| **ACID** | Fort | Variable (BASE / CAP) |

---

## 🔹 Concepts Avancés
### 📌 Théorème CAP
- **C** : Cohérence (les données sont les mêmes partout)
- **A** : Disponibilité (toujours accessible)
- **P** : Tolérance aux partitions (continue à fonctionner même en cas de panne réseau)

→ **NoSQL ne peut garantir que 2 des 3 propriétés en même temps**.

### 📌 Transactions : ACID vs BASE
| ACID (SQL) | BASE (NoSQL) |
|------------|-------------|
| **Atomicité** : Tout ou rien | **Basically Available** : Disponible |
| **Cohérence** : Toujours valide | **Soft state** : Données peuvent changer |
| **Isolation** : Transactions isolées | **Eventual consistency** : Cohérence à terme |
| **Durabilité** : Les données sont persistantes | - |

---

## 🔹 Exemples de Cas d’Usage
| Cas d’usage | Type de NoSQL recommandé |
|------------|-------------------------|
| Réseau social (relations complexes) | Graphe (Neo4j) |
| Cache mémoire rapide | Clé-Valeur (Redis) |
| Analyse de données | Colonne-Famille (Cassandra) |
| Stockage flexible de documents | Document (MongoDB) |
| Système de session utilisateur | Clé-Valeur (Redis) |

---

## 📌 Conclusion
NoSQL offre une grande flexibilité et performance pour traiter les **Big Data** et s’adapte à de nombreux cas d’usages modernes. Il ne remplace pas complètement SQL mais complète son écosystème dans un contexte de **persistance polyglotte**.

---

## 📚 Ressources complémentaires
- **MongoDB** : [https://www.mongodb.com/docs/](https://www.mongodb.com/docs/)
- **Redis** : [https://redis.io/documentation](https://redis.io/documentation)
- **Neo4j** : [https://neo4j.com/developer/](https://neo4j.com/developer/)
- **Cassandra** : [https://cassandra.apache.org/doc/latest/](https://cassandra.apache.org/doc/latest/)

