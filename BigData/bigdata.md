# 🗂️ Big Data - Fiche récapitulative

## 📌 1. Outils techniques & définitions
Liste des principaux outils abordés durant la formation, avec une courte définition.

### 📂 Stockage & Bases de Données

| Outil                | Définition |
|----------------------|-----------|
| **HDFS**            | Système de fichiers distribué permettant le stockage de gros volumes de données sur plusieurs serveurs. |
| **Hive**            | Outil permettant d’exécuter des requêtes SQL sur Hadoop. |
| **Apache Drill**     | Moteur d’interrogation SQL rapide et flexible, alternative moderne à Hive. |
| **NoSQL** (MongoDB, Cassandra, Elasticsearch) | Bases de données non relationnelles conçues pour stocker des données volumineuses et non structurées. |
| **NewSQL** (Google Spanner, CockroachDB) | Bases relationnelles modernes alliant scalabilité et compatibilité SQL. |

### ⚡ Traitement des données

| Outil                | Définition |
|----------------------|-----------|
| **MapReduce**       | Modèle de traitement parallèle utilisé par Hadoop pour exécuter des calculs distribués. |
| **Apache Spark**    | Moteur de traitement distribué en mémoire, plus rapide que MapReduce. |
| **RDD**            | Structure de données distribuée propre à Spark, permettant le traitement parallèle. |
| **DataFrame**       | Structure tabulaire optimisée dans Spark, plus facile à utiliser que les RDD. |
| **Dataset**         | Version améliorée des DataFrames, avec typage fort et meilleure gestion des erreurs. |

### 📡 Ingestion & Streaming de données

| Outil                | Définition |
|----------------------|-----------|
| **Apache Kafka**    | Plateforme de messagerie distribuée permettant la gestion de flux de données en temps réel. |
| **Kafka Connect**   | Outil permettant d’intégrer Kafka avec des bases de données ou autres systèmes externes. |
| **Kafka Streams**   | API de traitement de flux permettant de transformer les données en temps réel. |
| **Apache Flink**    | Outil de traitement de flux en temps réel, concurrent de Kafka Streams. |
| **Airbyte**         | Outil open-source facilitant l’ingestion et la synchronisation de données entre plusieurs systèmes. |

### 🤖 Machine Learning & Analytique

| Outil                | Définition |
|----------------------|-----------|
| **MLlib (Spark ML)** | Bibliothèque de machine learning distribuée dans Apache Spark. |
| **GraphX**          | Librairie Spark pour l’analyse de graphes et des réseaux de relations. |
| **Tableau / Power BI / Looker** | Outils de visualisation et d’analyse des données. |

---

## 📌 2. Glossaire des termes Big Data

### 📂 Concepts fondamentaux

| Terme                | Définition |
|----------------------|-----------|
| **Big Data**        | Ensemble des technologies permettant de stocker, traiter et analyser de grands volumes de données. |
| **Data Lake**       | Système de stockage permettant de conserver de grandes quantités de données brutes. |
| **Data Warehouse**  | Entrepôt de données conçu pour l’analyse et la prise de décision (ex : BigQuery, Snowflake). |
| **Modern Data Stack** | Ensemble d’outils et architectures modernes permettant d’exploiter le Big Data de manière scalable. |

### 📡 Ingestion & Streaming

| Terme                | Définition |
|----------------------|-----------|
| **Data Ingestion**   | Processus d'acquisition et d'importation de données depuis plusieurs sources vers un système de stockage. |
| **Batch Processing** | Traitement des données à intervalles réguliers (ex : analyse quotidienne des ventes). |
| **Streaming Processing** | Traitement des données en temps réel dès leur arrivée (ex : analyse en direct des transactions bancaires). |
| **ETL**             | Extraction -> Transformation -> Chargement (données transformées avant stockage). |
| **ELT**             | Extraction -> Chargement -> Transformation (transformation après ingestion). |
| **Producer (Kafka)** | Application qui envoie des messages à Kafka. |
| **Consumer (Kafka)** | Application qui lit des messages depuis un topic Kafka. |
| **Topic (Kafka)**    | Catégorie logique où sont stockés les messages dans Kafka. |
| **Partition (Kafka)** | Sous-division des topics permettant la parallélisation du traitement. |
| **Offset (Kafka)**   | Numéro unique attribué à chaque message dans une partition Kafka. |

### ⚡ Traitement & Stockage

| Terme                | Définition |
|----------------------|-----------|
| **MapReduce**       | Modèle de programmation permettant de traiter des données en parallèle sur un cluster Hadoop. |
| **Apache Spark**    | Moteur de traitement en mémoire, plus rapide et plus efficace que MapReduce. |
| **RDD**            | Structure de données distribuée dans Spark, utilisée pour le traitement parallèle. |
| **DataFrame**       | Version plus optimisée des RDD, proche d’un tableau SQL. |
| **Dataset**         | DataFrame amélioré avec typage fort et gestion des erreurs. |
| **Scalabilité verticale** | Augmentation de la puissance d’une seule machine (ajout de RAM, CPU…). |
| **Scalabilité horizontale** | Ajout de plusieurs machines pour répartir la charge et améliorer les performances. |

### 🔒 Sécurité & Réglementation

| Terme                | Définition |
|----------------------|-----------|
| **RGPD (GDPR)**     | Réglementation européenne sur la protection des données personnelles. |
| **Anonymisation**   | Processus de modification des données pour empêcher l’identification des individus. |
| **Tokenisation**    | Remplacement des données sensibles par des jetons uniques et sécurisés. |

### 🛠️ Formats & Outils Complémentaires

| Terme                | Définition |
|----------------------|-----------|
| **JSON**            | Format de stockage léger et structuré, utilisé pour les échanges de données. |
| **Parquet**         | Format de stockage optimisé pour l’analyse Big Data (utilisé avec Spark, Hive, etc.). |
| **Avro**            | Format binaire conçu pour stocker et transmettre des données de manière efficace. |
| **Schema Registry**  | Service utilisé pour gérer et valider les schémas Avro en production. |

---

## 📌 3. Récapitulatif - Approches d’Ingestion et Traitement

| Approche             | Mode                      | Avantages                            | Inconvénients |
|----------------------|--------------------------|--------------------------------------|---------------|
| **Batch Processing** | Traitement par lots      | Moins coûteux, adapté aux gros volumes | Pas adapté au temps réel |
| **Streaming Processing** | Temps réel         | Faible latence, idéal pour les applications en direct | Plus complexe à implémenter |
| **ETL**             | Extraction -> Transformation -> Chargement | Données transformées avant stockage | Moins flexible pour l'analyse brute |
| **ELT**             | Extraction -> Chargement -> Transformation | Exploite la puissance des entrepôts de données modernes | Plus gourmand en ressources |

---

## 📌 4. Conclusion

Cette fiche regroupe **les outils techniques**, **les concepts clés**, et **les terminologies** utilisés dans l’écosystème **Big Data**. Kafka, Spark, Hive, et bien d’autres outils permettent de **collecter, traiter et analyser** les données en fonction des besoins métier.

💡 **Ressources complémentaires :**  
📚 **[Documentation Apache Spark](https://spark.apache.org/docs/latest/)**  
📚 **[Documentation Apache Kafka](https://kafka.apache.org/documentation/)**  
📚 **[Guide ETL vs ELT](https://www.databricks.com/blog/elt-vs-etl-whats-the-difference-and-why-does-it-matter/)**  
