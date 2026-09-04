<h1 align="center"> 🏦 MDBank AI </h1>

<img width="1100" height="580" alt="MDBank AI" src="https://github.com/user-attachments/assets/69fd6095-1584-4a85-b758-90ba297becc3" />

---

## 💻 Technologies Used in the Project

<img loading="lazy" src="https://img.shields.io/badge/Python-darkblue"/>      <img loading="lazy" src="https://img.shields.io/badge/FastAPI-purple"/>      <img loading="lazy" src="https://img.shields.io/badge/FastMCP-pink"/>      <img loading="lazy" src="https://img.shields.io/badge/React-darkgreen"/>      <img loading="lazy" src="https://img.shields.io/badge/Streamlit-red"/>      <img loading="lazy" src="https://img.shields.io/badge/Docker_Compose-blue"/>      <img loading="lazy" src="https://img.shields.io/badge/JavaScript-yellow"/>     <img loading="lazy" src="https://img.shields.io/badge/A2A-green"/>

---

## 📌 About

**MDBank AI** was developed during the **Alura - Protocols and Architecture for Building Agents: MCP, A2A, AG-UI, and Backend for Agents (BFA)** course.

The goal of this project was to build a multi-agent architecture applied to a banking scenario, exploring modern protocols for communication between agents, tools, the front end, and the backend.

The application simulates an intelligent banking assistant capable of understanding the user's intent, routing the request to the appropriate agent, and performing actions related to MDBank services, such as opening a bank account and checking or requesting a credit card.

---

## 🧠 Project Goals

This project focused on practicing the development of real-world AI agent architectures, going beyond a simple chatbot.

The main goals were:

* Design a distributed multi-agent architecture
* Use protocols such as **MCP**, **A2A**, and **AG-UI**
* Implement a **Backend for Agents (BFA)** layer
* Separate business rules from the agent layer
* Create specialized agents for different banking intents
* Integrate the front end, backend, agents, and external tools
* Run multiple isolated services with Docker Compose

---

## 🏗️ System Architecture

The MDBank AI architecture consists of different layers responsible for communication, routing, business rules, and agent execution.

<p align="center">
<img width="500" height="700" alt="MDBank Agent Architecture" src="https://github.com/user-attachments/assets/7a7d34ab-11f3-438d-b2f9-5b1853a41da8" />
</p>

---

## 🤖 System Agents

The project uses specialized agents to handle different types of user requests.

### 🏦 Account Opening Agent

Responsible for managing the bank account opening process.

This agent can:

* Request the necessary user information
* Validate the information received
* Create or retrieve an existing account
* Return personalized messages to the user

### 💳 Credit Card Agent

Responsible for handling credit card-related requests.

This agent can:

* Retrieve credit card information
* Request a credit card
* Display the card number, type, and limit
* Format responses with highlighted information

### 🧭 Supervisor

Responsible for identifying the user's intent and routing the request to the appropriate agent.

Examples of intents:

* “I want to open an account”
* “I want a credit card”
* “When displaying my card number...”

---

## 🔌 Protocols Explored

### MCP - Model Context Protocol

**MCP** was used to expose resources and tools that can be accessed by the agents.

Examples of resources and tools used in the project:

* `consultar_conta`
* `consultar_cartao`
* `criar_ou_buscar_conta`
* `solicitar_cartao`
* `gerar_prompt_abertura`
* `abrir_conta_prompt`
* `solicitar_cartao_prompt`
* `obter_conta`
* `obter_cartao`

---

### A2A - Agent to Agent

The **A2A** protocol was used to represent communication between specialized agents.

In this project, it allows the router to forward requests to agents such as:

* Account opening agent
* Credit card agent
* Customer support agent

---

### AG-UI

**AG-UI** was explored to create an interactive interface connected to the agents.

The interface allows users to:

* Send messages to the assistant
* View response history
* Track the shared state
* Display structured responses from the agents
* Render information such as cards, tables, and visual highlights

---

### BFA - Backend for Agents

The **Backend for Agents (BFA)** layer was used to organize business logic and decouple the agents from the application's internal rules.

This layer is responsible for:

* Centralizing business rules
* Organizing complex workflows
* Exposing reusable services
* Enabling integration between agents, tools, and data

---

## ✨ Features

* Chat with an intelligent banking assistant
* Automatic intent routing
* Bank account opening
* Credit card requests
* Credit card information lookup
* Structured response display
* Response history
* Shared conversation state
* Integration between specialized agents
* Communication between services via APIs
* Execution with Docker Compose

---

## 🖼️ Project Demo

### Account Opening Chat

<p align="center">
<img width="700" alt="MDBank Account Opening" src="https://github.com/user-attachments/assets/9ff7eba6-71a7-4fbd-bb28-f88a059fa3ae" />
</p>

---

### Credit Card Lookup and Display

<p align="center">
<img width="700" alt="MDBank Credit Card" src="https://github.com/user-attachments/assets/ee06b663-ee38-47cd-a035-dc0fdab09699" />
</p>

---

### Response History and Shared State

<p align="center">
<img width="700" alt="MDBank Response History" src="https://github.com/user-attachments/assets/9ddfd458-88dd-4ae5-a328-e40b3ccf0d46" />
</p>

---

## 📂 Project Structure

```text
MDBank_agent/
├── MDBank/
│   └── Supervisor / main router
│
├── agents/
│   ├── abrir_conta/
│   └── cartao_credito/
│
├── bfa/
│   └── Backend for Agents layer
│
├── frontend/
│   └── Streamlit interface
│
├── frontend2/
│   └── React / AG-UI interface
│
├── recursos/
│   └── Resources and tools used by the agents
│
├── docker-compose.yml
└── README.md
```

---

## ▶️ How to Run the Project

### 1. Clone this repository

```bash
git clone https://github.com/StellaLeoni2008/MDBank_agent.git
```

### 2. Navigate to the project folder

```bash
cd MDBank_agent
```

### 3. Run the services with Docker Compose

```bash
docker compose up --build
```

### 4. Access the application

After the containers are running, open the interface in your browser:

```text
http://localhost:9090
```

---

## 🧠 Concepts Practiced

During the development of this project, advanced concepts related to AI agent architecture were explored, including:

* Multi-agent systems
* Intent routing
* Communication between agents
* MCP, A2A, and AG-UI protocols
* Backend for Agents
* Separation between agents and business rules
* Agent and tool catalogs
* Distributed communication with JSON-RPC
* MCP services with FastMCP
* Interactive interfaces with React and Streamlit
* Shared state between users and agents
* Docker Compose for service orchestration
* Modularization of systems using multiple containers

---

<br>

## 👩🏻‍💻 Author

| [<img loading="lazy" src="https://avatars.githubusercontent.com/u/237313711?v=4" width=115><br><sub>Stella Leoni</sub>](https://github.com/StellaLeoni2008) |
| :---------------------------------------------------------------------------------------------------------------------------------------------------------: |

---

<p align="right">
06/11/2026
</p>
