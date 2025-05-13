# 🇫🇷 ELK Stack sur Docker

Ce projet déploie une stack ELK (Elasticsearch, Logstash, Kibana) complète à l’aide de Docker Compose.  
Elle permet de collecter, parser, stocker et visualiser des logs.

---

## Technologies utilisées

- **Docker & Docker Compose**
- **Elasticsearch** : moteur de recherche & stockage de logs
- **Logstash** : pipeline de traitement de logs
- **Kibana** : interface de visualisation
- **Grok** : pour parser les logs Apache

---

## Architecture du projet

```text
log (sample.log) --> Logstash --> Elasticsearch --> Kibana
```

---

## Lancer le projet

```bash
git clone git@github.com:cedouiri/elk-docker-project.git
cd elk-docker-project
docker compose up --build
```

Accéder à Kibana : [http://localhost:5601](http://localhost:5601)

---

## Structure du projet

```bash
elk-docker-project/
├── docker-compose.yml         # Orchestration Docker
├── logstash/logstash.conf     # Pipeline de Logstash
├── sample-logs/sample.log     # Fichier de log d'exemple
├── elasticsearch/             # Config ES (optionnel)
├── kibana/                    # Config Kibana (optionnel)
└── README.md                  # Documentation
```

---

## Exemple de log utilisé

```log
127.0.0.1 - - [10/May/2025:13:55:36 +0000] "GET /index.html HTTP/1.1" 200 1024
```

---

## TODO

- Ajouter Filebeat pour collecte plus réaliste
- Créer un dashboard Kibana par défaut
- Ajouter une application qui génère des logs

---

## Auteur

- Nom : Chamsseddine Douiri
- Projet personnel pour renforcer le portfolio DevOps

---

# 🇬🇧 ELK Stack on Docker

This project deploys a full ELK stack (Elasticsearch, Logstash, Kibana) using Docker Compose.  
It allows you to collect, parse, store, and visualize logs.

---

## Technologies Used

- **Docker & Docker Compose**
- **Elasticsearch**: log storage and search engine
- **Logstash**: log pipeline and transformation
- **Kibana**: UI for visualization
- **Grok**: to parse Apache-style logs

---

## Project Architecture

```text
log (sample.log) --> Logstash --> Elasticsearch --> Kibana
```

---

## Run the project

```bash
git clone git@github.com:cedouiri/elk-docker-project.git
cd elk-docker-project
docker compose up --build
```

Access Kibana at: [http://localhost:5601](http://localhost:5601)

---

## Project Structure

```bash
elk-docker-project/
├── docker-compose.yml         # Docker orchestration
├── logstash/logstash.conf     # Logstash pipeline
├── sample-logs/sample.log     # Example log file
├── elasticsearch/             # ES config (optional)
├── kibana/                    # Kibana config (optional)
└── README.md                  # Documentation
```

---

## Sample log used

```log
127.0.0.1 - - [10/May/2025:13:55:36 +0000] "GET /index.html HTTP/1.1" 200 1024
```

---

## TODO

- Add Filebeat for realistic log ingestion
- Create a default Kibana dashboard
- Add an app that generates logs

---

## Author

- Name: Chamsseddine Douiri
- Personal project to strengthen my DevOps portfolio