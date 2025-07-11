## Project Overview

The trenddit-flow package is a low code workflow automation SDK which uses AI agents and lean principles. It is built on top of popular AI agent frameworks like Strands Agents, LangChain, LangGraph, and native agent capabilities offered by leading foundation model APIs like OpenAI, Anthropic, xAI, and Gemini. It also offers easy integration with MCP and A2A standards for tool use by agents.

### Specialized Workflows

The trenddit-flow package specializes in **customer engagement lifecycle workflows** for B2B AI-backed technology businesses offering services to enterprises. Key workflow capabilities include:

1. **Lead Generation** - AI agents search online sources and use LLMs to identify potential customers
2. **Customer Research** - Deep analysis of customer needs, challenges, and technology/product adoption patterns
3. **Solution Matching** - Intelligent matching of customer requirements with available technology offerings
4. **Meeting Preparation** - Automated preparation of customer-specific presentations and talking points
5. **Project Management Automation** - Streamlined customer project tracking and milestone management
6. **Sales Playbook Generation** - Dynamic creation of sales strategies and playbooks tailored to specific customer segments
7. **Competitive Analysis** - Automated research and analysis of competitive landscape for customer accounts
8. **Proposal Generation** - AI-assisted creation of technical proposals and service offerings
9. **Customer Success Workflows** - Post-sale engagement and success tracking automation

## Development Contexts

- Use context7 for documentation of frameworks, libraries, packages

## Project Requirements

### Python Environment
- ALWAYS activate and use the Python virtual environment `.venv` when working on this project
- Before running any Python code: `source .venv/bin/activate`
- All dependencies are managed by Poetry in `pyproject.toml`
- To add dependencies: `poetry add <package-name>`
- To add dev dependencies: `poetry add --group dev <package-name>`
- To install all dependencies: `poetry install`
- Package source code is in `src/trenddit_flow/`

### Development Methodology
- Follow Test-Driven Development (TDD) approach:
  1. Write tests first before implementing functionality
  2. Write minimal code to make tests pass
  3. Refactor while keeping tests green
  4. Ensure comprehensive test coverage

### Technology Stack

#### Core Dependencies
- **Strands Agents SDK** (v0.2.1) - Primary agent framework for building AI agents
  - `strands-agents` - Core SDK for agent creation and execution
  - `strands-agents-tools` - Pre-built tools for common tasks
  - `strands-agents-builder` - Agent that helps build custom agents and tools

- **LangChain Ecosystem** (v0.3.26) - Alternative agent framework and LLM utilities
  - `langchain` - Core framework for LLM applications
  - `langgraph` - Framework for building stateful, multi-actor applications

- **Tool Use Standards**
  - `mcp` (v1.11.0) - Model Context Protocol SDK for secure LLM-tool integration
  - `a2a-sdk` (v0.2.11) - Agent-to-Agent Protocol for inter-agent communication

#### Foundation Model Integration
- Design for compatibility with leading AI model APIs:
  - OpenAI (GPT-4, GPT-3.5, etc.)
  - Anthropic (Claude 3.5, Claude 3, etc.)
  - xAI (Grok models)
  - Google (Gemini Pro, Gemini Flash)
  - AWS Bedrock models
  - Azure OpenAI models

#### Development Tools
- **Poetry** - Dependency management and packaging
- **JupyterLab** - Interactive development and example notebooks
- **PyTest** - Testing framework (to be added)

### Architecture Patterns
- Apply SOLID principles:
  - **S**ingle Responsibility: Each class/function should have one reason to change
  - **O**pen/Closed: Open for extension, closed for modification
  - **L**iskov Substitution: Derived classes must be substitutable for base classes
  - **I**nterface Segregation: Many specific interfaces are better than one general interface
  - **D**ependency Inversion: Depend on abstractions, not concretions

- Follow DRY (Don't Repeat Yourself):
  - Extract common functionality into reusable functions/classes
  - Use configuration and parameters instead of duplicating code
  - Create abstractions for repeated patterns

- **Agent-First Design**:
  - Build workflows as collections of interacting agents
  - Use MCP for secure tool access and resource management
  - Use A2A for agent-to-agent communication and collaboration
  - Design for modularity and composability

- **Low-Code Philosophy**:
  - Provide high-level abstractions for common workflow patterns
  - Use configuration over code where possible
  - Enable visual workflow composition through notebooks
  - Support both declarative and imperative programming styles