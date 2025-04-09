# 📚 Local RAG

![local-rag-demo](demo.gif)

[![OpenSSF Best Practices](https://www.bestpractices.dev/projects/8588/badge)](https://www.bestpractices.dev/projects/8588)
![GitHub Commit Activity](https://img.shields.io/github/commit-activity/t/jonfairbanks/local-rag)
![GitHub Last Commit](https://img.shields.io/github/last-commit/jonfairbanks/local-rag)
![GitHub License](https://img.shields.io/github/license/jonfairbanks/local-rag)

Offline, Open-Source RAG

Ingest files for retrieval augmented generation (RAG) with open-source Large Language Models (LLMs), all without 3rd parties or sensitive data leaving your network.

Features:

- Offline Embeddings & LLMs Support (No OpenAI!)
- Support for Multiple Sources
    - Local Files
    - GitHub Repos
    - Websites
- Streaming Responses
- Conversational Memory
- Chat Export

Learn More:

- [Setup & Deploy the App](docs/setup.md)
- [Using Local RAG](docs/usage.md)
- [RAG Pipeline](docs/pipeline.md)
- [Planned Features](docs/todo.md)
- [Troubleshooting](docs/troubleshooting.md)
- [Known Bugs & Issues](docs/todo.md#known-issues--bugs)
- [Resources](docs/resources.md)
- [Contributing](docs/contributing.md)




Notes from Dale
---------------
At the end of installation, this app loaded on the browser with the import error, no module named coloroma (which in the Pipfile is mentioned as win32 depedency). Remove that, run
- pipenv install --python=3.13
- docker buildx build --platform linux/arm64 -t local-rag --load .
- docker run -d -p 8501:8501 local-rag run main.py --server.port=8501 --server.address=0.0.0.0
- cannot access ollama running on the host machine
