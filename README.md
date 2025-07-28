# 📈 Stock Predictor Chatbot

An AI-powered financial assistant that performs real-time stock analysis using a modular multi-agent system. Built with FastAPI, React.js, and OpenAI, the chatbot enables users to query sentiment, fundamentals, technicals, and more through natural language.

## 🚀 Features

- 🔍 Natural Language Query Support – Ask questions like “Should I invest in AAPL?” or “Show me RSI for TSLA.”
- 🤖 Multi-Agent Architecture – Specialized agents for sentiment, technicals, fundamentals, price, news, and screening.
- 📊 Real-Time Financial Data – Powered by Alpha Vantage API with Redis caching for performance.
- 🧠 LLM-Powered Routing – Dispatcher uses OpenAI tool-calling to dynamically assign tasks to relevant agents.
- 🌐 Interactive Frontend – Built with React and TailwindCSS for real-time visualizations and portfolio views.
- 🐳 Dockerized Deployment – Scalable and reproducible setup using Docker and docker-compose.

## 🧱 Architecture Overview

Frontend (React.js + TailwindCSS)  
↓  
FastAPI Backend  
├── Dispatcher Agent (OpenAI Tool Calling)  
├── SentimentAgent  
├── TechnicalAgent  
├── FundamentalAgent  
├── NewsAgent  
├── PortfolioAgent  
├── ScreenerAgent  
└── PriceAgent  
↓  
External APIs (Alpha Vantage, News, etc.)

## ⚙️ Setup Instructions

### 🔧 Prerequisites

- Docker & Docker Compose  
- Python 3.10+  
- Node.js 18+  
- Alpha Vantage API Key  
- OpenAI API Key  

### 🐳 Backend (FastAPI)

cd backend  
cp .env.example .env  # Add your keys here  
docker-compose up --build  

### 💻 Frontend (React.js)

cd frontend  
npm install  
npm run dev  

## 📚 Example Queries

- "What is the current sentiment around NVDA?"  
- "Give me the RSI and MACD for TSLA."  
- "Screen stocks with P/E < 15 and ROE > 10%"  
- "Summarize my portfolio with risk and gain info."  

## 📦 Technologies Used

- FastAPI, Redis, Docker  
- OpenAI, Alpha Vantage  
- React.js, TailwindCSS  
- Tool Calling, JSON Agent Outputs  

## 📄 License

This project is licensed under the MIT License.

## 💡 Future Improvements

- Add support for crypto market analysis  
- Expand agent registry to handle macroeconomic signals  
- Integrate Pine Script-based technical strategies
