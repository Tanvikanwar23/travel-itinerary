# TourGenie: AI-Powered Trip Architect

Welcome to **TourGenie**! This project is an intelligent, autonomous trip-planning application that leverages large language models and multi-agent orchestration to build highly personalized, budget-friendly day-to-day travel itineraries. The system searches the internet in real-time to find the best flights, hotels, and attractions, delivering a complete markdown-formatted guide directly to a sleek web interface.

##  Key Features
- **Real-Time Web Intelligence:** Fetches the latest data on places, flights, and accommodations.
- **Multi-Agent Orchestration:** Utilizes autonomous AI agents that mimic a real-world travel agency (research, logistics, and planning).
- **Streaming Responses:** Provides a real-time progress panel as the AI actively builds the itinerary using Server-Sent Events (SSE).
- **Modern User Interface:** Built with React, featuring a responsive, dual-column Deep Navy glassmorphic layout.

##  Technology Stack
- **Backend Infrastructure:** Python, FastAPI
- **AI & Orchestration:** CrewAI framework, Google Gemini (LLM)
- **Data & Search APIs:** Serper (Web Search), SerpAPI (Flights & Hotels)
- **Frontend App:** React, Vite, Custom CSS (Glassmorphism design)

##  How the AI Works

Behind the scenes, the application delegates tasks to a specialized crew of AI agents:
1. **The Destination Analyst:** Focuses purely on scoping out the best local spots, top-rated restaurants, and cultural activities based on the user's selected interests.
2. **The Budget & Logistics Coordinator:** Operates alongside the analyst to find viable flight routes and hotel options, ensuring everything aligns with the user's specified budget limits.
3. **The Master Planner:** Collects all the raw data and insights from the other two agents to synthesize a beautifully formatted, logical, and engaging day-by-day itinerary.

##  Getting Started

Follow these instructions to get the project up and running on your local machine.

### Prerequisites
Make sure you have Node.js and Python installed. You will also need API keys for:
- [Google AI Studio](https://aistudio.google.com/) (Gemini API)
- [Serper.dev](https://serper.dev/) (Google Search API)
- [SerpApi](https://serpapi.com/) (Flights/Hotels API)

### 1. Environment Configuration
Create a `.env` file in the root directory of the project and populate it with your API keys:
```env
GEMINI_API_KEY=your_gemini_api_key_here
SERPER_API_KEY=your_serper_api_key_here
SERPAPI_API_KEY=your_serpapi_api_key_here
```

### 2. Backend Installation & Execution
Open your terminal in the root folder to set up the Python backend:
```bash
# Initialize a virtual environment
python -m venv venv

# Activate the virtual environment (Windows)
venv\Scripts\activate
# For Mac/Linux use: source venv/bin/activate

# Install the required packages
pip install -r requirements.txt

# Start the FastAPI server
python api.py
```
*The backend API will now be listening on http://localhost:8000.*

### 3. Frontend Installation & Execution
Open a second terminal window and navigate into the `frontend` folder:
```bash
cd frontend

# Install Node dependencies
npm install

# Launch the Vite development server
npm run dev
```
*The React UI will be accessible at http://localhost:5173.*

## Repository Structure
- `/backend`: Contains the AI agent logic (`agents.py`, `tasks.py`, `crew.py`, `tools.py`).
- `/frontend`: Contains the React application and custom styling.
- `api.py`: The FastAPI application entry point.
- `requirements.txt`: Python package dependencies.
