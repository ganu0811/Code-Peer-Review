# Code-Peer-Review

n automated code review system built using LangGraph and LangChain that generates, reviews, and improves Python code using AI agents. This project demonstrates the power of agentic AI workflows for code quality assurance and documentation generation.

## 🌟 Features

- **Automated Code Generation**: Generate Python code based on natural language descriptions
- **Intelligent Code Review**: AI-powered code analysis with feedback and suggestions
- **Error Detection**: Automatic detection of missing error handling and best practices
- **Documentation Generation**: Automated docstring and comment generation
- **Visual Workflow**: Interactive graph visualization of the review process
- **Iterative Improvement**: Conditional logic for code refinement loops

## 🛠️ Tech Stack

- **LangGraph**: For building the agentic workflow graph
- **LangChain**: For LLM integration and prompt management
- **Groq**: High-performance LLM inference with Qwen-QwQ-32B model
- **Python**: Core programming language
- **Jupyter Notebook**: Interactive development environment

## 📋 Prerequisites

Before running this project, ensure you have:

- Python 3.8+
- Jupyter Notebook or JupyterLab
- Groq API key (sign up at [Groq Console](https://console.groq.com/))

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone <your-repository-url>
   cd code-peer-review

2. **Install required packages**
pip install langchain-groq langgraph python-dotenv typing-extensions ipython

3. **Set up environment variables**
 Create a .env file in the project root: GROQ_API_KEY=your_groq_api_key_here

## 🏗️ Architecture
The system uses a state-based graph architecture with the following components:

State Schema
class State(TypedDict):
    topic: str        # Input topic for code generation
    base_code: str    # Generated code
    review: str       # Review feedback
    docstring: str    # Generated documentation

Workflow Nodes

1. generate_code: Creates Python code based on the input topic
2. review_code: Analyzes the generated code for improvements
3. reviews: Validates code quality (error handling, best practices)
4. generate_docstring: Creates comprehensive documentation
