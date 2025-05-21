# MCP Research Assistant

A powerful research assistant built using the Model Context Protocol (MCP) that helps users search, analyze, and organize academic papers from arXiv.

## Features

- **Paper Search**: Search for academic papers on any topic using arXiv's API
- **Paper Organization**: Automatically organize papers by topic in a structured format
- **Paper Information Extraction**: Extract and store detailed information about papers including:
  - Title
  - Authors
  - Publication date
  - Summary
  - PDF URL
- **Interactive Chat Interface**: Chat with an AI assistant to help with your research queries
- **Topic-based Organization**: Papers are automatically organized into topic-based folders
- **Comprehensive Research Analysis**: Get summaries and analysis of research trends in your area of interest

## Prerequisites

- Python 3.x (used `3.12.8`)
- Node.js and npm (used `v22.13.0`)
- Anthropic API key

## Installation

1. Clone the repository:
```bash
git clone https://github.com/ezequiroga/mcp-bases
cd mcp-bases
```

2. Install Python dependencies:
```bash
pip install -r requirements.txt
```

3. Copy the environment file and add your API key:
```bash
cp .env-example .env
# Edit .env and add your Anthropic API key
```

4. Update npm
```bash
npm install -g npm@latest
```

## Project Structure

- `research_server.py`: Main server implementation for paper search and management
- `mcp_chatbot.py`: Interactive chatbot implementation
- `server_config.json`: Configuration for MCP servers
- `papers/`: Directory where paper information is stored (created automatically)

## Usage

1. Start the research assistant:
```bash
python mcp_chatbot.py
```

2. Interact with the chatbot using natural language queries. For example:
   - "Search for papers about quantum computing"
   - "What are the latest papers on machine learning?"
   - "Summarize the research on artificial intelligence"

3. Finish the chatbot by typing `quit`.

## Available Tools

The system provides several tools through the MCP interface:

- `search_papers`: Search for papers on a specific topic
- `extract_info`: Get detailed information about a specific paper
- `get_available_folders`: List all available topic folders
- `get_topic_papers`: Get detailed information about papers in a specific topic

## Configuration

The `server_config.json` file configures three MCP servers:
- `filesystem`: For file system operations
- `research`: The main research server
- `fetch`: For fetching operations
