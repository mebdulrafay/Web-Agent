<div align="center">

<!-- HERO BANNER -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=200&section=header&text=ROEX%20AI%20Assistant&fontSize=52&fontColor=ffffff&fontAlignY=38&desc=Intelligent%20Portfolio%20Agent%20•%20Powered%20by%20n8n%20%2B%20Google%20Gemini&descAlignY=58&descSize=16" width="100%"/>

<br/>

<!-- BADGES ROW 1 -->
[![n8n](https://img.shields.io/badge/Built%20with-n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)](https://n8n.io)
[![Gemini](https://img.shields.io/badge/LLM-Google%20Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://ai.google.dev)
[![Status](https://img.shields.io/badge/Status-Active-22c55e?style=for-the-badge&logo=statuspage&logoColor=white)]()
[![License](https://img.shields.io/badge/License-MIT-f59e0b?style=for-the-badge)](LICENSE)

<!-- BADGES ROW 2 -->
[![GitHub](https://img.shields.io/badge/GitHub-mebdulrafay-181717?style=flat-square&logo=github)](https://github.com/mebdulrafay)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Hafiz%20Abdul%20Rafay-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/hafiz-abdul-rafay-4577a5395/)
[![Email](https://img.shields.io/badge/Email-mebdulrafay@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:mebdulrafay@gmail.com)
[![HP LIFE](https://img.shields.io/badge/Certified-HP%20LIFE%20AI-0096D6?style=flat-square&logo=hp&logoColor=white)]()

<br/>

> **ROEX** is the official AI-powered personal assistant for **Hafiz Abdul Rafay** — a smart, always-on agent that represents his skills, projects, and services to clients, recruiters, and developers around the world.

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Architecture](#-architecture)
- [Tech Stack](#-tech-stack)
- [Workflow Nodes](#-workflow-nodes)
- [Agent Capabilities](#-agent-capabilities)
- [Screenshots & Images](#-screenshots--images)
- [Getting Started](#-getting-started)
- [Configuration](#-configuration)
- [About the Author](#-about-the-author)

---

## 🌐 Overview

**ROEX** is a production-ready, chat-based AI agent built on [n8n](https://n8n.io), powered by Google Gemini, and equipped with memory, code execution, Wikipedia search, and live GitHub integration. It acts as a 24/7 intelligent representative for Hafiz Abdul Rafay's portfolio.

```
User sends a message  ──►  n8n Chat Trigger  ──►  AI Agent (ROEX)  ──►  Response
                                                        │
                              ┌─────────────────────────┼───────────────────────┐
                              ▼                         ▼                       ▼
                       Google Gemini            Simple Memory             Tool Layer
                       (LLM Core)              (Context Window)     [Code | Wikipedia | GitHub]
```

### ✨ What ROEX Can Do

- 💬 Answer questions about Abdul Rafay's **skills, projects & services**
- 🧮 Execute **JavaScript** to solve logic/math problems on-the-fly
- 📚 Query **Wikipedia** for knowledge augmentation
- 🐛 **Create GitHub Issues** directly from a conversation
- 🧠 Maintain **conversation context** across multiple turns

---

## 🏗 Architecture

```
┌─────────────────────────────────────────────────────────────────────┐
│                        ROEX WORKFLOW ARCHITECTURE                    │
├─────────────────────────────────────────────────────────────────────┤
│                                                                       │
│   ┌──────────────────┐        ┌───────────────────────────────────┐  │
│   │  Chat Trigger     │──────►│           AI Agent (ROEX)          │  │
│   │  (Webhook/Public) │  main │   System Prompt: Portfolio Rep     │  │
│   └──────────────────┘        └───────────┬───────────────────────┘  │
│                                           │                           │
│                    ┌──────────────────────┼──────────────────────┐   │
│                    │                      │                       │   │
│            ai_languageModel          ai_memory              ai_tool  │
│                    │                      │                       │   │
│          ┌─────────▼──────┐   ┌──────────▼──────┐              ┌─┴─┐ │
│          │ Google Gemini  │   │  Simple Memory   │    ┌─────────┤ 3 │ │
│          │  Chat Model    │   │  Buffer Window   │    │         └───┘ │
│          └────────────────┘   └─────────────────┘    │               │
│                                                       │               │
│                                            ┌──────────▼────────────┐ │
│                                            │     TOOL LAYER        │ │
│                                            ├───────────────────────┤ │
│                                            │ 🔧 Code Tool (JS)     │ │
│                                            │ 📖 Wikipedia Search   │ │
│                                            │ 🐙 GitHub Issues      │ │
│                                            └───────────────────────┘ │
└─────────────────────────────────────────────────────────────────────┘
```

---

## 🛠 Tech Stack

### 🤖 AI & Automation

| Technology | Role | Version |
|:---:|:---|:---:|
| ![n8n](https://img.shields.io/badge/n8n-Workflow_Engine-EA4B71?style=flat-square&logo=n8n) | Workflow orchestration & automation | Latest |
| ![Gemini](https://img.shields.io/badge/Google_Gemini-LLM_Core-4285F4?style=flat-square&logo=google) | Language model powering the agent | PaLM API |
| ![LangChain](https://img.shields.io/badge/LangChain-Agent_Framework-1C3C3C?style=flat-square) | AI agent & memory abstraction | n8n Integration |

### 🔧 Tools & Integrations

| Tool | Purpose | Type |
|:---:|:---|:---:|
| ![JavaScript](https://img.shields.io/badge/JS_Code_Tool-Logic_%26_Math-F7DF1E?style=flat-square&logo=javascript&logoColor=black) | Dynamic code execution | `ai_tool` |
| ![Wikipedia](https://img.shields.io/badge/Wikipedia-Knowledge_Base-gray?style=flat-square&logo=wikipedia&logoColor=white) | External knowledge retrieval | `ai_tool` |
| ![GitHub](https://img.shields.io/badge/GitHub_Issues-Issue_Creation-181717?style=flat-square&logo=github) | Authenticated via OAuth2 to create issues | `ai_tool` |

### 🌐 Abdul Rafay's Core Tech (Portfolio)

| Category | Technologies |
|:---|:---|
| **Frontend** | ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3) ![JavaScript](https://img.shields.io/badge/JavaScript_ES6+-F7DF1E?style=flat-square&logo=javascript&logoColor=black) |
| **Python** | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![PyQt5](https://img.shields.io/badge/PyQt5-41CD52?style=flat-square&logo=qt) ![CustomTkinter](https://img.shields.io/badge/CustomTkinter-blue?style=flat-square) |
| **Hardware / IoT** | ![Arduino](https://img.shields.io/badge/Arduino-00979D?style=flat-square&logo=arduino&logoColor=white) Servo • Ultrasonic Sensors • Serial Comm |
| **Design** | Glassmorphism • Branding • Social Media Creatives |
| **AI/Automation** | ![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n) Google Gemini • LangChain Agents |

---

## 🔩 Workflow Nodes

| # | Node Name | Type | Description |
|:---:|:---|:---|:---|
| 1 | **When chat message received** | `chatTrigger` | Public webhook that receives user messages and initiates the workflow |
| 2 | **AI Agent (ROEX)** | `agent` | Core LangChain agent with a detailed system prompt defining ROEX's identity |
| 3 | **Google Gemini Chat Model** | `lmChatGoogleGemini` | Connected via PaLM API — serves as the language brain of the agent |
| 4 | **Simple Memory** | `memoryBufferWindow` | Sliding window of conversation history for contextual responses |
| 5 | **Code Tool** | `toolCode` | Executes JavaScript for real-time logic, math, and data-processing tasks |
| 6 | **Wikipedia** | `toolWikipedia` | Fetches encyclopedia data to answer knowledge-based queries |
| 7 | **Create an issue in GitHub** | `githubTool` | Authenticated via OAuth2 to create issues in specified GitHub repos |

---

## ⚡ Agent Capabilities

<table>
<tr>
<td width="50%">

### 🎯 What ROEX Knows
- ✅ Abdul Rafay's full technical skill set
- ✅ All key portfolio projects
- ✅ Freelancing services offered
- ✅ PAEC Science Expo 2nd Place achievement
- ✅ Contact details & social links
- ✅ HP LIFE AI Certification

</td>
<td width="50%">

### 🚫 Integrity Boundaries
- ❌ Won't fabricate skills not in portfolio
- ❌ Won't claim uncertified expertise
- ❌ Routes unknown queries to direct contact
- ✅ Always directs to `mebdulrafay@gmail.com`

</td>
</tr>
</table>

---


## 🚀 Getting Started

### Prerequisites

- [n8n](https://n8n.io) instance (self-hosted or cloud)
- Google Gemini (PaLM) API key
- GitHub account with OAuth2 app configured

### Installation

**1. Clone this repository**
```bash
git clone https://github.com/mebdulrafay/roex-ai-assistant.git
cd roex-ai-assistant
```

**2. Import the workflow into n8n**
```
n8n Dashboard → Workflows → Import from File → Select My_workflow.json
```

**3. Configure credentials**
```
Settings → Credentials → Add New:
  • Google Gemini (PaLM) API  →  Paste your API key
  • GitHub OAuth2             →  Authorize your GitHub account
```

**4. Activate the workflow**
```
Toggle the workflow to "Active" in the n8n dashboard
```

**5. Test the chat**
```
Open the Chat Trigger URL in your browser and start chatting with ROEX!
```

---

## ⚙️ Configuration

### System Prompt Customization

The agent's personality and knowledge are defined in the **AI Agent** node's `systemMessage`. To update:

1. Open the workflow in n8n
2. Click on the **AI Agent** node
3. Edit the `System Message` field under **Options**

### Memory Window

The **Simple Memory** node uses a buffer window — adjust the window size in the node settings to control how many past messages ROEX remembers per session.

### Tool Permissions

| Tool | Enable/Disable | Notes |
|:---|:---:|:---|
| Code Tool | ✅ | Always on for math/logic tasks |
| Wikipedia | ✅ | Knowledge augmentation |
| GitHub Issues | ⚙️ | Requires valid OAuth2 credentials |

---

## 👨‍💻 About the Author

<div align="center">

| Field | Detail |
|:---:|:---|
| **Name** | Hafiz Abdul Rafay |
| **Role** | Student • AI-Assisted Web Developer • Freelancer |
| **Location** | 📍 Mianwali, Pakistan |
| **Achievement** | 🏆 2nd Place — Science Expo 2025, PAEC Education Center (Level VI–VIII) |
| **Certification** | 🎓 HP LIFE Certified — AI's Business Impact & Ethics |

</div>

### 🤝 Connect with Abdul Rafay

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-mebdulrafay-181717?style=for-the-badge&logo=github)](https://github.com/mebdulrafay)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/hafiz-abdul-rafay-4577a5395/)
[![Email](https://img.shields.io/badge/Email-Say%20Hello!-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mebdulrafay@gmail.com)

</div>

---

### 📌 Full Project Portfolio

| Project | Stack | Description |
|:---|:---|:---|
| 🎯 **Radar System** | Arduino • Ultrasonic Sensor | Object detection with AI voice alerts & real-time distance feedback |
| 🌦 **Weather Forecast App** | HTML/CSS/JS • OpenWeather API | Responsive live weather app with dynamic UI |
| 🔢 **Binary Converter** | Python • PyQt5 | Desktop app for efficient text-to-binary conversion |
| 🔔 **PC-Controlled Buzzer** | Arduino • Serial Comm | Hardware alert system controlled via PC |
| 🌐 **Personal Portfolio** | HTML/CSS/JS • Glassmorphism | Premium interactive site showcasing all digital & hardware projects |
| 🤖 **ROEX AI Assistant** | n8n • Gemini • LangChain | *This project* — AI-powered portfolio representative |

---

### 💼 Freelancing Services

| Service | Description |
|:---|:---|
| 🌐 Modern Web Development | Responsive & premium UI/UX with glassmorphism aesthetics |
| 🤖 AI-Assisted Development | Faster turnaround using AI-powered n8n workflows |
| ⚡ Arduino & IoT Prototyping | Sensor integration, serial comms, and hardware projects |
| 🎨 Graphic Design & Branding | Social media creatives, logos, and visual identity |

> 📬 Interested in working together? Reach out at **mebdulrafay@gmail.com**

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302b63,100:0f0c29&height=100&section=footer" width="100%"/>

**Made with 💜 by [Hafiz Abdul Rafay](https://github.com/mebdulrafay) — Mianwali, Pakistan**

*"Specializing in elegant solutions that combine beautiful design with powerful functionality."*

⭐ **Star this repo if ROEX impressed you!**

</div>
