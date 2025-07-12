# Trenddit Flow Example Notebooks

This directory contains example notebooks demonstrating the capabilities of the trenddit-flow package.

## Getting Started

1. **Install dependencies**:
   ```bash
   source .venv/bin/activate
   poetry install
   ```

2. **Set up API keys**:
   - Copy `.env.example` to `.env.local`
   - Add your actual API keys to `.env.local`

3. **Launch JupyterLab**:
   ```bash
   source .venv/bin/activate
   jupyter lab
   ```

## Available Notebooks

### Agent Framework Comparison (`agent_framework_comparison.ipynb`)

This notebook demonstrates and compares various agent frameworks and LLM APIs for the same basic use case. It measures performance metrics including:

- Time to first token
- Overall completion time  
- Total tokens used
- Success rate

**Frameworks Compared:**
1. **Direct OpenAI API** - Direct API calls to OpenAI
2. **Direct Anthropic API** - Direct API calls to Anthropic  
3. **LangChain** - Using LangChain framework with OpenAI
4. **Strands Agents** - Using Strands Agents framework

**Use Case:** Customer Research Agent that researches a company and provides key insights for B2B sales preparation.

**Required API Keys:**
- `OPENAI_API_KEY` - For OpenAI GPT models
- `ANTHROPIC_API_KEY` - For Anthropic Claude models
- `XAI_API_KEY` - For xAI Grok models (optional)
- `GOOGLE_API_KEY` or `GEMINI_API_KEY` - For Google Gemini models (optional)

The notebook handles missing API keys gracefully and only tests frameworks with available keys.

## Environment Setup

Create a `.env.local` file with your API keys:

```bash
# Copy the example file
cp .env.example .env.local

# Edit with your actual API keys
# The notebook checks both .env.local and .env files (.env.local takes precedence)
```

## Output

The notebooks generate:
- Performance comparison tables
- Visualization charts
- Detailed analysis and recommendations
- CSV export of results
- Sample responses from each framework