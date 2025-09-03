# Phishing Analysis TCC

[![Docker](https://img.shields.io/badge/Docker-Compose-blue)](https://www.docker.com/)

This project is developed for **collection, preparation, and classification of phishing emails** using automated workflows with **n8n** and various classification models (LLMs).

---

## Table of Contents

- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Workflow Setup](#workflow-setup)
- [LLM Configuration](#llm-configuration)
- [Notes](#notes)

---

## Getting Started

### 1. Install Dependencies

Make sure you have **Docker** and **Docker Compose** installed:

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

### 2. Configure Volumes and Ports

The project uses Docker volumes to persist data and access CSV files:

- `n8n_data`: Stores persistent n8n workflow data.  
- `data`: Access folder for input CSV files.  

Place your emails for classification in the `/inputs` folder. The dataset contains **5 spreadsheets**.

### 3. Start the Docker Container

Run the following command:

```bash
docker compose up -d

### 4. Import Workflows

After importing the workflows, make sure that the classification spreadsheets in the **Read Data node** are correctly set.

### 5. Configure LLMs

Before running the workflows, open the model nodes and set your credentials.  
- **Claude** and **Gemma**: You need to create a **Groq** account to use these models.  
- **GPT** and **Llama**: You need to create an account and subscribe to a plan to run these models.
