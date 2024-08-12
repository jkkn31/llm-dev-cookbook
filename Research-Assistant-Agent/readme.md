# LLM-Based Research Agent

## Overview

This project is an implementation of an LLM-based research agent that automates the process of researching a given topic, finding relevant information, and generating a concise summary. The agent is designed to streamline the research process using state-of-the-art language models (Gemini or Ollama) and an advanced search API (SERPER from LangChain). The goal is to create a tool that can efficiently handle complex research tasks with minimal manual intervention.

## Features

### 1. Topic Breakdown Tool
The Topic Breakdown Tool is designed to take a broad research topic and decompose it into smaller, more manageable subtopics. This is achieved using an LLM (Gemini or Ollama), which intelligently generates focused subqueries based on the main topic, enabling more targeted and efficient research.

### 2. Query Expansion Tool
The Query Expansion Tool enhances the initial subqueries by generating related keywords, synonyms, and phrases. This expansion ensures that the search results are comprehensive, capturing a wider range of relevant information.

### 3. Search Tool
The Search Tool leverages the SERPER tool from LangChain to gather relevant information based on the expanded subqueries. This tool is critical for retrieving accurate and up-to-date data. The search results are cached to optimize performance and reduce unnecessary API calls, especially considering the limitations of the free tier.

### 4. Critique Tool
The Critique Tool reviews the generated summary, providing feedback on its quality and suggesting potential improvements. It may also propose additional topics that could enhance the research, ensuring a thorough exploration of the subject matter.

### 5. Summarizer Tool (Optional)
The Summarizer Tool condenses the gathered information into a concise paragraph, ensuring that the final output is easy to digest and directly relevant to the research topic.

## Workflow

The research agent follows a structured workflow that integrates all the tools mentioned above:

1. **Input Topic**: The agent receives a research topic from the user.
2. **Topic Breakdown**: The Topic Breakdown Tool generates subtopics or subqueries.
3. **Query Expansion**: The Query Expansion Tool expands the subqueries with related keywords and phrases.
4. **Search**: The Search Tool gathers relevant information using the expanded queries and subqueries.
5. **Summary Generation**: The agent generates a summary incorporating the search results (optional).
6. **Critique**: The Critique Tool reviews the summary, offers suggestions for improvement, and possibly identifies additional topics for research (optional).
7. **Final Output**: The agent presents the final, refined summary to the user.

## Setup

1. Create a `.env` file in the root directory of the project. Add your API keys for the Gemini (or Ollama) LLM and the SERPER search API as follows:
   ```
   GEMINI_API_KEY=your_gemini_api_key
   SERPER_API_KEY=your_serper_api_key
   ```
2. Open the Notebook
   ```bash
   Research_Assistant_Agent.ipynb
   ```

## Usage

Once the setup is complete, the agent can be used to research any topic. Simply provide a topic, and the agent will autonomously handle the research process, from breaking down the topic to generating a final summary.

## Conclusion

This research agent leverages advanced LLMs and search tools to provide an efficient, automated solution for conducting research. By simply providing the necessary API keys in the `.env` file, you can easily run the agent and obtain high-quality research summaries with minimal effort.