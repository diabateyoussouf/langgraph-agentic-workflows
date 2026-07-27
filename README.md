# 🤖 Agentic RAG Architectures & LangGraph Workflows

[![Python](https://img.shields.io/badge/Python-3.11%2B-blue.svg)](https://www.python.org/)
[![LangGraph](https://img.shields.io/badge/Orchestration-LangGraph-orange.svg)](https://github.com/langchain-ai/langgraph)
[![LLM](https://img.shields.io/badge/LLM-Mistral_AI-purple.svg)](https://mistral.ai/)
[![Pydantic](https://img.shields.io/badge/Validation-Pydantic_v2-red.svg)](https://docs.pydantic.dev/)

Bienvenue dans ce dépôt d'architectures d'**Agents IA** et de systèmes **Agentic RAG (Retrieval-Augmented Generation)** prêts pour la production. 

Ce repository regroupe des implémentations de flux agentiques complexes s'appuyant sur **LangGraph**, **Pydantic v2** et **Mistral AI**, avec un accent particulier sur la gestion d'état typée, l'évaluation automatique (*Self-RAG* / *Audit Node*), la sécurité des prompts (*Guardrails*) et le contrôle des boucles d'exécution.

---

## 🛠️ Tech Stack & Frameworks

| Catégorie | Technologie | Rôle / Usage dans le Repository |
| :--- | :--- | :--- |
| **Orchestration Agentique** | `LangGraph` | Construction de graphes d'états cycliques, boucles de réévaluation et routage conditionnel |
| **LLM & Inference** | `Mistral AI` | Modèles de raisonnement (`mistral-small-latest`), génération structurée et routage d'intention |
| **Vector DB / RAG** | `ChromaDB` | Stockage vectoriel, requêtes sémantiques et recherche contextuelle |
| **Validation & Structured Output** | `Pydantic v2` | Saisie, validation et parsing des sorties LLM (Noms, Scores, Classifications, Audits) |
| **Document Loaders** | `LangChain PyPDF` | Extraction directe et injection automatique de textes à partir de fichiers PDF |
| **Gestion d'État** | `TypedDict` | Modélisation d'état sérialisable, compteurs de sécurité et historique d'exécution |

---

## 📁 Structure du Repository

```text
langgraph-agentic-workflows/
│
├── Projet01_Contrat_Securite/        # Projet 1 : RAG Juridique & Guardrails
│   ├── main.py                       # Definition du StateGraph et exécution
│   ├── state.py                      # Définition des schémas UserState & Pydantic
│   └── README.md                     # Documentation technique du système RAG contractuel
│
├── Projet02_Agent_Recruteur/         # Projet 2 : Agent Recruteur IA & Audit RH (Colab / Jupyter)
│   └── Projet02_Agent_Recruteur.ipynb # Notebook autonome : Parsing PDF, extraction nominative & Audit Anti-Biais
│
├── Projet03_Agent_Belvedere_Hotel/   # Projet 3 : Agent Concierge Hôtelier Multi-Tours (Colab / Jupyter)
│   └── Projet03_Agent_Belvedere_Hotel.ipynb # Notebook : RAG Agentique, Routage d'intention & Mémoire
│
├── .env.example                     # Modèle de configuration des variables d'environnement
├── requirements.txt                 # Dépendances Python du projet
└── README.md                        # Documentation générale du repository
