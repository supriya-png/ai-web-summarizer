# AI Web Content Summarizer

## Description

This project scrapes product pages from e-commerce websites, summarizes the content using OpenAI GPT-4, and performs sentiment analysis using HuggingFace Transformers. The API is built with FastAPI and packaged with Docker.

## Tech Stack

- Python 3.10+
- BeautifulSoup4
- OpenAI GPT-4 API
- HuggingFace Transformers
- FastAPI
- Docker
- Pytest
- GitHub Actions



## Setup

Clone the repo:

```bash
git clone <https://github.com/supriya-png/ai-web-summarizer>
cd ai-web-summarizer
```

Create virtual environment:

```bash
python -m venv venv
venv\Scripts\activate  # Windows
# or
source venv/bin/activate  # Linux/Mac
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Set environment variables:

Create a `.env` file:

```
OPENAI_API_KEY=your_openai_api_key
```

Run the API:

```bash
uvicorn src.api:app --reload
```

Access API docs locally.

## Testing

Run tests with:

```bash
pytest tests/
```

## Docker

Build Docker image:

```bash
docker build -t ai-web-summarizer .
```

Run Docker container:

```bash
docker run -d -p 8000:8000 --env-file .env ai-web-summarizer
```

## Sample API Request

POST `/summarize`

```json
{
  "url": "https://www.example.com/product-page"
}
```

Response:

```json
{
  "summary": "AI-generated product summary...",
  "sentiment": [{"label": "POSITIVE", "score": 0.98}]
}
```

## Author

Supriya S P
