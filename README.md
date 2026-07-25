# 🤖 Agentic RAG Architectures & LangGraph Workflows

[![Python](https://img.shields.io/badge/Python-3.11%2B-blue.svg)](https://www.python.org/)
[![LangGraph](https://img.shields.io/badge/Orchestration-LangGraph-orange.svg)](https://github.com/langchain-ai/langgraph)
[![LLM](https://img.shields.io/badge/LLM-Mistral_AI-purple.svg)](https://mistral.ai/)
[![Pydantic](https://img.shields.io/badge/Validation-Pydantic_v2-red.svg)](https://docs.pydantic.dev/)

Bienvenue dans ce dépôt d'architectures d'**Agents IA** et de systèmes **Agentic RAG (Retrieval-Augmented Generation)** prêts pour la production. 

Ce repository regroupe des implémentations de flux agentiques complexes s'appuyant sur **LangGraph**, **Pydantic v2** et **Mistral AI**, avec un accent particulier sur la gestion d'état typée, l'évaluation automatique (*Self-RAG*) et la sécurité des prompts (*Guardrails*).

---

## 🛠️ Tech Stack

| Catégorie | Technologie | Rôle / Usage |
| :--- | :--- | :--- |
| **Orchestration** | `LangGraph` | Construction de graphes d'états dynamiques, boucles d'évaluation et routeurs conditionnels |
| **LLM & Embeddings** | `Mistral AI` | Modèles de raisonnement (`mistral-small-latest`), génération et routage structuré |
| **Vector DB** | `ChromaDB` | Stockage vectoriel et recherche sémantique des clauses contractuelles |
| **Validation & Schémas** | `Pydantic v2` | Saisie et validation des sorties structurées (Grades, Classifications) |
| **Gestion d'État** | `TypedDict` / `NotRequired` | Modélisation d'état sérialisable et sécurisée au fil du graphe |

---

## 📁 Structure du Projet

```text
langgraph-agentic-workflows/
│
├── Projet01_Contrat_Securite/      # Projet  : RAG Juridique & Guardrails
│   ├── main.py                     # Script principal et définition du StateGraph
│   ├── state.py                    # Définition des schémas UserState & Pydantic
│   └── README.md                   # Documentation technique spécifique
│
├── 02-intent-routing-basics/       # Modèle basique d'aiguillage d'intention
├── 03-self-rag-evaluation/         # Boucles de contrôle qualité et anti-hallucination
│
├── .env.example                    # Modèle de configuration des variables d'environnement
├── requirements.txt                # Liste des dépendances Python
└── README.md                       # Documentation générale du repository
