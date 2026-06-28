# Text2SQL-AI

> An AI-powered multi-agent Text-to-SQL system that converts natural language questions into executable SQL queries using LangGraph and Large Language Models.

![Python](https://img.shields.io/badge/Python-3.10+-blue)
![LangGraph](https://img.shields.io/badge/LangGraph-Multi--Agent-green)
![LangChain](https://img.shields.io/badge/LangChain-Framework-orange)
![LLM](https://img.shields.io/badge/LLM-Claude%20%7C%20Groq-purple)
![SQL](https://img.shields.io/badge/Database-SQL-blue)

---

## Overview

QueryPilot AI is a multi-agent AI system that enables users to query relational databases using natural language.

Instead of directly prompting a language model to generate SQL, the system follows a structured multi-agent workflow where specialized agents collaborate to understand the user's intent, identify relevant database schema, generate optimized SQL queries, execute them, and return accurate results.

The project is built using **LangGraph**, enabling stateful orchestration and modular agent interactions for reliable Text-to-SQL generation.

---

## Key Features

- Multi-Agent workflow using LangGraph
- Natural Language to SQL conversion
- Intelligent database schema selection
- SQL query generation using LLMs
- Query execution on relational databases
- Modular agent architecture
- Stateful workflow management
- Claude / Groq LLM integration
- Olist e-commerce dataset support

---

## System Workflow

```

User Question
│
▼
Router Agent
│
▼
Schema Selection
│
▼
SQL Generation Agent
│
▼
SQL Validation
│
▼
Database Execution
│
▼
Final Response

```

---

## Tech Stack

| Category | Technologies |
|-----------|--------------|
| Language | Python |
| AI Framework | LangGraph, LangChain |
| LLM | Claude 3.5 Sonnet, Groq |
| Database | SQL |
| Data Processing | Pandas |
| Development | Jupyter Notebook |

---

## Project Structure

```

QueryPilot-AI
│
├── agents/
│   ├── router_agent.py
│   ├── customer_agent.py
│   └── ...
│
├── helper/
│
├── notebook/
│
├── dataset/
│
├── knowledge_base/
│
├── prompts/
│
└── README.md

````

---

## Multi-Agent Architecture

The application follows a modular agent-based design where each component is responsible for a single task.

### Router Agent
Determines the user's intent and routes requests through the appropriate workflow.

### Schema Selection
Identifies relevant tables and columns required to answer the user's query.

### SQL Generation Agent
Generates optimized SQL queries using an LLM while considering the selected schema.

### Execution Layer
Runs generated SQL against the connected database.

### Response Generation
Formats database results into concise natural language responses.

---

## Installation

Clone the repository

```bash
git clone https://github.com/your-username/QueryPilot-AI.git
````

Navigate to the project

```bash
cd QueryPilot-AI
```

Install dependencies

```bash
pip install -r requirements.txt
```

Configure your LLM API keys and execute the notebook or application.

---

## Example Query

**Input**

```
Which product category generated the highest revenue last year?
```

**Generated SQL**

```sql
SELECT product_category_name,
SUM(payment_value) AS revenue
FROM orders
...
```

**Output**

```
The Health & Beauty category generated the highest total revenue during the selected period.
```

---

## Future Improvements

* FastAPI backend integration
* Interactive web dashboard
* Support for multiple SQL databases
* Query history and analytics
* User authentication

---

## License

This project is intended for educational and research purposes.
