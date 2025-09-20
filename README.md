# Math Routing Agent

## 🌟 Project Overview

The Math Routing Agent is a sophisticated educational AI system designed to revolutionize how students and educators approach mathematical problem-solving. By employing an Agentic-RAG (Retrieval-Augmented Generation) architecture, the system intelligently determines the best source of information—whether from a curated knowledge base or real-time web search—to provide comprehensive, step-by-step mathematical solutions.

Unlike traditional math solvers that rely on static databases or simple computational engines, our system combines the reliability of curated mathematical knowledge with the freshness of web-based information, ensuring users receive both accurate foundational solutions and cutting-edge mathematical insights.

## 🎯 Key Features

🤖 **Intelligent Routing System**

  * **Smart Decision Engine**: Automatically routes questions between the knowledge base and web search based on confidence scores.
  * **Hybrid Approach**: Combines multiple sources when needed for comprehensive solutions.
  * **Adaptive Learning**: Routes improve over time based on user feedback and success rates.

📚 **Advanced Knowledge Management**

  * **Vector Database**: Qdrant-powered semantic search through mathematical concepts and solutions.
  * **Curated Content**: Pre-loaded with verified mathematical problems and step-by-step solutions.
  * **Dynamic Expansion**: The knowledge base grows through validated user interactions and feedback.

🔍 **Real-Time Information Retrieval**

  * **Web Search Integration**: Access to the latest mathematical research, methods, and applications.
  * **Source Validation**: Prioritizes educational and authoritative mathematical sources.
  * **Content Filtering**: Ensures retrieved information is relevant and educational.

🧠 **AI-Powered Solution Generation**

  * **Google Gemini Integration**: Leverages advanced language models for mathematical reasoning.
  * **Step-by-Step Breakdown**: Decomposes complex problems into understandable steps.
  * **Multiple Difficulty Levels**: Adapts explanations to beginner, intermediate, and advanced levels.

🛡️ **Quality Assurance**

  * **Input Guardrails**: Validates questions for mathematical content and appropriateness.
  * **Output Validation**: Ensures solutions are mathematically sound and educationally valuable.
  * **Safety Measures**: Prevents misuse and maintains an educational focus.

🔄 **Continuous Improvement**

  * **Human-in-the-Loop**: User feedback directly improves system performance.
  * **Analytics Dashboard**: Tracks usage patterns and solution effectiveness.
  * **Self-Learning**: The system becomes more accurate with each interaction.

-----

## 🚀 Getting Started

Follow these instructions to get the project up and running on your local machine.

### Prerequisites

  * **Docker Desktop**: Required for the recommended Docker-based setup.
  * **Python 3.10+**: Required for running the backend separately.
  * **Node.js v14+**: Required for running the frontend separately.
  * **API Keys**: You will need API keys from **Gemini** and **Tavily**.

### Installation

You can run this project in two ways:

#### 1\. Using Docker (Recommended)

This is the easiest way to get started, as it sets up the backend, frontend, and Qdrant database automatically.

**1. Clone the repository:**

```bash
git clone https://github.com/saibalaji-2003/project1.git
cd project1
```

**2. Create the environment file:**

Navigate to the `backend` directory and create a `.env` file by copying the example:

```bash
cd backend
cp .env.example .env
```

**3. Add your API keys:**

Open the `.env` file and add your API keys:

```
GEMINI_API_KEY="your-gemini-api-key-here"
TAVILY_API_KEY="your-tavily-api-key-here"
```

**Important:** Ensure that the `ALLOWED_MATH_TOPICS` variable in your `.env` is a valid JSON array of strings:

```
ALLOWED_MATH_TOPICS='["calculus", "algebra", "trigonometry"]'
```

**4. Start the services:**

Return to the root directory and use Docker Compose to start all the services:

```bash
cd ..
docker-compose up -d
```

**5. Access the application:**

  * **Frontend**: `http://localhost:3000`
  * **Backend API Docs**: `http://localhost:8000/docs`

#### 2\. Running Backend and Frontend Separately

If you prefer not to use Docker, follow these steps to run each service individually.

##### **Backend Setup**

**1. Navigate to the backend directory:**

```bash
cd backend
```

**2. Create and activate a virtual environment:**

```bash
python -m venv venv
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
```

**3. Install dependencies:**

```bash
pip install -r requirements.txt
```

**4. Run the backend server:**

```bash
uvicorn app.main:app --host 0.0.0.0 --port 8000 --reload
```

##### **Frontend Setup**

**1. Navigate to the frontend directory:**

```bash
cd frontend
```

**2. Install dependencies:**

```bash
npm install
```

**3. Start the frontend server:**

```bash
npm start
```

This will automatically open the application in your browser at `http://localhost:3000`.
