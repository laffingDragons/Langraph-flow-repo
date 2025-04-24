
# Langgraph


LangGraph, created by LangChain, is an open source AI agent framework designed to build, deploy and manage complex generative AI agent workflows. It provides a set of tools and libraries that enable users to create, run and optimize large language models (LLMs) in a scalable and efficient manner.


<img style="text-align:center" width="284" alt="image" src="https://github.com/user-attachments/assets/fc62cc3e-1de1-442b-a3a0-e02714221412" />


## Requirements

- Python 3.9+
- langchain_community
- arxiv
- wikipedia

## List of tools used

- arxiv (For research paper queries)
- wikipedia
- groq llm

## Setup

1. Clone this repository:
    ```bash
    git clone https://github.com/laffingDragons/Langraph-flow-repo.git
    ```

2. Install required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Code Explanation

### Arxiv Query Example
This section demonstrates how to query Arxiv for papers using the `ArxivQueryRun` class.

```python
from langchain_community.tools import ArxivQueryRun
from langchain_community.utilities import ArxivAPIWrapper

# Setting up Arxiv query
api_wrapper_arxiv = ArxivAPIWrapper(top_k_results=2, doc_content_chars_max=500)
arxiv = ArxivQueryRun(api_wrapper=api_wrapper_arxiv, description="Query arxiv papers")

# Output
print(arxiv.name)
print(arxiv.description)
```

### Wikipedia Query Example
This section demonstrates how to query Wikipedia for articles using the `WikipediaQueryRun` class.

```python
from langchain_community.tools import WikipediaQueryRun
from langchain_community.utilities import WikipediaAPIWrapper

# Setting up Wikipedia query
api_wrapper_wikipedia = WikipediaAPIWrapper(top_k_results=1, doc_content_chars_max=500)
wikipedia = WikipediaQueryRun(api_wrapper=api_wrapper_wikipedia, description="Query for information retrieval of wikipedia")

# Output
print(wikipedia.name)
print(wikipedia.description)
```

## How to Contribute

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a new pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
