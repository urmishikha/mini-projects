# mini-projects
Overview

The Research Agent System is an AI-powered tool designed to automate structured research planning, information gathering, drafting, reviewing, and finalizing research reports. It utilizes LangChain, OpenAI models, and Tavily search to streamline the research workflow efficiently.

Features

Automated Research Planning: Generates a structured research strategy.

Web-Based Information Gathering: Fetches the latest data using Tavily search.

AI-Powered Drafting: Compiles a structured report based on collected information.

Automated Review & Critique: Provides AI-based feedback on research drafts.

Decision Logic for Iterative Improvement: Determines whether to revise, accept, or reject a draft.

Memory Management: Stores past research interactions for reference.

Installation

Prerequisites

Ensure you have the following installed:

Python 3.8+

pip (Python package manager)

API keys for OpenAI and Tavily search

Setup Instructions

Clone the repository:

git clone https://github.com/your-repo/research-agent.git
cd research-agent

Install dependencies:

pip install -r requirements.txt

Set up environment variables:

export OPENAI_API_KEY='your_openai_api_key'
export TAVILY_API_KEY='your_tavily_api_key'

Usage

Running the Research Agent

To start the research process, execute the main script:

python main.py

Input Parameters

task: The research topic to be explored.

max_revisions: Maximum number of iterations allowed for refinement.

Example Execution

from research_agent import ResearchAgent

agent = ResearchAgent(api_key='your_tavily_api_key')
response = agent.research_node({
    "task": "AI trends in 2024",
    "max_revisions": 3,
    "revision_number": 0
})
print(response)

System Architecture

1. AgentState (Manages research process state)

Stores the research plan, collected content, draft, critique, editor comments, and revision details.

2. AgentNodes (Executes research operations)

plan_node(): Generates research strategy using OpenAI.

research_node(): Conducts web searches via Tavily API.

draft_node(): Drafts structured research responses.

review_node(): Provides AI-driven critique.

3. Decision Logic

Determines whether the draft should:

Be reviewed

Go for revision

Be accepted or rejected

4. Memory Management

Stores research interactions in memory for tracking revisions and improvements.

