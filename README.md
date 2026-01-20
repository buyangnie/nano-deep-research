# DeepResearch Agent

A lightweight ReAct agent for deep information-seeking tasks, powered by OpenRouter API and Tavily search.

## 🚀 Quick Start

### 1. Setup Environment

```bash
# Python 3.10+ recommended
pip install -r requirements.txt
pip install python-dotenv tiktoken
```

### 2. Configuration

Create `.env` file with your API keys:

```bash
# OpenRouter API (LLM)
OPENAI_API_KEY="your-openrouter-key"
OPENAI_BASE_URL="https://openrouter.ai/api/v1"
OPENAI_MODEL="as-you-wish"  # or other models

# Tavily API (Search + Web Extract)
TAVILY_API_KEY="your-tavily-key"
```

### 3. Run Test

```bash
cd inference
python3 test_query.py
```

## 📂 Project Structure

```
DeepResearch/
├── .env                 # API configuration
├── requirements.txt     # Dependencies
└── inference/
    ├── react_agent.py   # Main ReAct agent
    ├── prompt.py        # System prompts
    ├── tool_search.py   # Tavily search tool
    ├── tool_visit.py    # Tavily extract tool
    └── test_query.py    # Test script
```

## 🔧 Supported Tools

| Tool | API | Description |
|------|-----|-------------|
| `search` | Tavily `/search` | Web search with multiple queries |
| `visit` | Tavily `/extract` | Extract content from URLs |

## 🤖 Supported Models (via OpenRouter)

- `deepseek/deepseek-v3.2`
- `qwen/qwen3-32b`
- `alibaba/tongyi-deepresearch-30b-a3b`
- Any OpenAI-compatible model

## 📝 Example Usage

Edit `test_query.py` to change the test question:

```python
test_query = "Your research question here"
```

Output logs are saved to `output/` directory.

## License

See [LICENSE](LICENSE) for details.
