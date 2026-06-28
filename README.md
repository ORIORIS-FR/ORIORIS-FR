<div align="center">
  <img src="banniere_orioris.jpg" alt="ORIORIS Cyber Security" width="100%" />

  <h1>ORIORIS | Architecte Système & Cybersécurité</h1>
  
  <p><b>Industrialiser l'Éphémère. Protéger la Connaissance.</b></p>

  <p>
    <a href="https://github.com/ORIORIS"><img src="https://img.shields.io/badge/Certification-AIS_En_Cours-blue?style=for-the-badge&logo=shield&logoColor=white" alt="AIS"/></a>
    <a href="https://github.com/ORIORIS"><img src="https://img.shields.io/badge/Focus-Zero_Trust_%26_Agentic_AI-red?style=for-the-badge&logo=target&logoColor=white" alt="Focus"/></a>
    <a href="https://github.com/ORIORIS"><img src="https://img.shields.io/badge/Mindset-B2B_To_Cyber-success?style=for-the-badge&logo=rocket&logoColor=white" alt="Mindset"/></a>
  </p>

<h1> 🛠️ Stack Technique</h1>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/n8n-FF5722?style=for-the-badge&logo=n8n&logoColor=white" alt="n8n"/>
  <img src="https://img.shields.io/badge/Cybersecurity-000000?style=for-the-badge&logo=hackthebox&logoColor=white" alt="Cybersecurity"/>
  <img src="https://img.shields.io/badge/Obsidian-483699?style=for-the-badge&logo=obsidian&logoColor=white" alt="Obsidian"/>
  <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL"/>
</p>
</div>

---

## 🚀 Mission : Transformer le Bruit en Intelligence Tactique

Avec 20 ans d'expérience technique et commerciale B2B, je ne code pas pour faire de la théorie. **Je conçois des écosystèmes résilients.** Ma transition vers la Cybersécurité (AIS) s'appuie sur une conviction stricte : la sécurité commence par l'isolation, et la performance par l'automatisation autonome.

### 🧠 Mon OS Personnel : L'Architecture "Bunker IA"

Je développe et maintiens un environnement local "Zero Trust" où des agents IA autonomes effectuent la veille technologique et la résolution de problèmes sans exposer de données à l'extérieur.

```mermaid
graph TD
    %% --- Environnement Cloud / Externe ---
    subgraph Cloud [Cloud & Synchronisation]
        G1[GitHub Privé<br/>Dépôt: Bunker_IA]
        G2[GitHub Privé<br/>Dépôt: Cerveau]
    end

    %% --- Système de Fichiers Local (Windows/WSL) ---
    subgraph Host [Serveur Hôte : Dossiers Locaux]
        V1[(📁 /Bunker_IA<br/>Le Sas / Inbox AI)]
        V2[(📁 /Cerveau<br/>Le Sanctuaire PKM)]
    end

   %% --- Tunnels & Accès Externes ---
    subgraph Access [Couche d'Accès Sécurisé]
        CF(☁️ cloudflared<br/>Tunnel API)
        TS(🔒 tailscale<br/>VPN Host)
    end

    subgraph Host [Serveur Hôte Windows / WSL]
        %% --- Volumes Locaux ---
        subgraph Volumes [Dossiers Locaux Bind Mounts]
            V1[(Obsidian<br/>Bunker_IA)]
            V2[(n8n_reception)]
            V3[(Configs<br/>YAML)]
        end

        %% --- Réseau Interne Docker ---
        subgraph DockerNet [Réseau Isolé : bunker_net]
            
            %% Cœur Applicatif
            N8N[⚙️ n8n_bunker<br/>Port 5678]
            LITELLM[🧠 litellm_bunker<br/>Port 4000]
            SEARCH[🌐 searxng_bunker<br/>Port 8080]
            AGENT[🤖 agent_veille_bunker<br/>Conteneur Python]
            
            %% Front & Monitor
            WEBUI[🖥️ open_webui<br/>Port 3001]
            DOZZLE[👁️ dozzle_bunker<br/>Port 8082]
            
            %% Persistance
            subgraph Databases [Couche de Données]
                PG[(🐘 postgres_bunker)]
                RED[⚡ redis_bunker]
                QDR[(🎯 qdrant_bunker)]
            end
        end
    end

    %% --- Routage & Dépendances ---
    CF -.->|Expose Sécurisé| N8N
    CF -.->|Expose Sécurisé| LITELLM
    
    N8N -->|DB_HOST| PG
    N8N -->|REDIS_HOST| RED
    
    LITELLM -->|DATABASE_URL| PG
    SEARCH -->|SEARXNG_REDIS_URL| RED
    
    AGENT -->|depends_on| N8N
    AGENT -->|depends_on| PG
    AGENT -->|LITELLM_URL| LITELLM
    
    DOZZLE -.->|Lecture seule| DockerSock(Socket Docker)
    
    %% --- Montages Volumes ---
    V1 -.->|/obsidian_vault| AGENT
    V2 -.->|/app/reception| AGENT
    V2 -.->|/BUNKER_IA/n8n_reception| N8N
    V3 -.->|litellm_config| LITELLM
    V3 -.->|searxng_config| SEARCH

    %% --- Styles ---
    classDef net fill:#34495e,stroke:#fff,stroke-width:2px,color:#fff
    classDef app fill:#2980b9,stroke:#ecf0f1,stroke-width:2px,color:#fff
    classDef db fill:#c0392b,stroke:#ecf0f1,stroke-width:2px,color:#fff
    classDef vol fill:#8e44ad,stroke:#ecf0f1,stroke-width:2px,color:#fff
    classDef agent fill:#27ae60,stroke:#ecf0f1,stroke-width:2px,color:#fff

    class CF,TS net
    class N8N,LITELLM,SEARCH,WEBUI,DOZZLE app
    class PG,RED,QDR db
    class V1,V2,V3 vol
    class AGENT agent
```

---

```mermaid
graph TD
    %% --- Inputs ---
    subgraph Acquisition [Vecteurs d'Entrée]
        A[Veille Cyber/CVE]
        B[Forums Techniques]
    end

    %% --- Le Bunker ---
    subgraph Bunker [Bunker IA : Infrastructure Locale - Docker]
        C(Sas n8n)
        D{Escouade CrewAI<br>LangGraph}
        E[(Qdrant<br>Vector DB)]
        
        C -->|Nettoyage| D
        D <-->|RAG| E
    end

    %% --- Outputs ---
    subgraph PKM [Digital Garden]
        F[Obsidian Vault]
    end

    Acquisition -->|Triggers| C
    D -->|Documentation Structurée| F

    %% Styles (Dark Mode GitHub)
    style Acquisition fill:#1e1e1e,stroke:#333,color:#fff
    style Bunker fill:#0d1117,stroke:#ff5722,stroke-width:2px,color:#fff
    style PKM fill:#1e1e1e,stroke:#7b61ff,stroke-width:2px,color:#fff
    style D fill:#238636,stroke:#fff,color:#fff
```

---

## 💡 Expertise
*   **Infrastructure as Code & Conteneurisation :** Architecture multi-services (PostgreSQL, Qdrant, LiteLLM) sous Docker.
*   **Ingénierie Agentique :** Développement d'agents Python avec `CrewAI` pour l'analyse et la structuration de données complexes.
*   **Passerelles IA :** Implémentation de protocoles `MCP` pour la communication inter-agents.

---

Technique-Commercial avec 20 ans d'expérience, en transition vers la **Cybersécurité**.
Je conçois et maintiens des architectures locales agentiques pour optimiser la connaissance et l'automatisation.

## 🚀 Projets & Focus
*   **Bunker IA (Privé) :** Infrastructure locale conteneurisée (Docker) orchestrant des workflows IA (RAG/Vector DB) et des agents autonomes.
*   **Veille Agentique :** Développement d'agents Python pour l'analyse de flux et la structuration de données (RAG/Qdrant).
*   **Transition AIS :** Préparation à la certification Administrateur d'Infrastructures Sécurisées.

## 📈 Objectif
Fusionner mon expertise B2B avec les nouvelles capacités de l'IA et de la Cybersécurité pour construire des systèmes résilients et sécurisés.

---
*En recherche active d'opportunités en cybersécurité / AIS pour la rentrée 2026.*
