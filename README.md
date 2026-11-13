# AI Travel Planning Assistant

A Streamlit app where AI agents plan a trip from your preferences: they recommend cities, research the destination, build a day-by-day itinerary and break down the budget.

It runs on **Llama 3.1 8B (via Groq)** and comes in two versions:

| Version | Entry point | Logic | Notes |
|---|---|---|---|
| CrewAI | `main.py` | `travel.py` | 4 CrewAI agents (City Selector, Local Expert, Travel Planner, Budget Manager) |
| LangChain | `main_langchain.py` | `travel_langchain.py` | Prompt chains; extra inputs (companions, stay, transport, food, visa) |

## How it works
1. **City selection**: suggests 3 cities based on travel type, interests and season
2. **City research**: attractions, food, culture and transport tips
3. **Itinerary**: a day-by-day plan for the trip length you choose
4. **Budget**: costs broken down for your budget range

## Setup
```bash
pip install streamlit crewai langchain-core langchain-groq langchain-ollama python-dotenv
```
Create a `.env` file:
```
GROQ_API_KEY=your_key_here
```

## Run
```bash
streamlit run main.py            # CrewAI version
streamlit run main_langchain.py  # LangChain version
```
