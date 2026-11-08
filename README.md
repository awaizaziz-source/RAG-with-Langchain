# LangChain Updated

A practical, notebook-based introduction to building applications with
[LangChain](https://www.langchain.com/) and modern large language models (LLMs).
This project demonstrates the core LangChain workflow, model integration, and
tool calling through focused examples that can be run and explored
interactively.

## What You Will Learn

- The fundamentals of LangChain and its modern APIs
- How to initialize and invoke chat models from different providers
- How to connect LangChain with OpenAI, Google Gemini, and Groq models
- How to define tools and allow a model to use them
- How to inspect model responses and tool-calling behavior in a notebook

## Project Structure

```text
.
├── updated langchain/
│   ├── 1-updatedlangchainintroo.ipynb  # LangChain introduction and basics
│   ├── 2-modelintegration.ipynb        # Chat model integration examples
│   └── 3-tools.ipynb                   # Tool definition and tool calling
├── pyproject.toml                      # Project metadata and dependencies
├── uv.lock                             # Reproducible dependency lock file
└── .gitignore
```

## Requirements

- Python 3.14 or newer
- API access to at least one supported model provider
- Jupyter Notebook or JupyterLab

The project uses `uv` for dependency management. Install it by following the
[official uv installation guide](https://docs.astral.sh/uv/getting-started/installation/).

## Installation

1. Clone the repository and move into the project directory:

   ```bash
   git clone <repository-url>
   cd "Langchain Updated"
   ```

2. Create the project environment and install the locked dependencies:

   ```bash
   uv sync
   ```

3. Configure your API keys in a `.env` file at the project root. Add only the
   keys for the providers you intend to use:

   ```env
   OPENAI_API_KEY=your_openai_api_key
   GOOGLE_API_KEY=your_google_api_key
   GROQ_API_KEY=your_groq_api_key
   ```

   Never commit `.env` or expose API keys in notebooks or source code.

## Running the Notebooks

Start Jupyter from the project root:

```bash
uv run jupyter notebook
```

Then open the notebooks in the following order:

1. **LangChain Introduction** — Start with the basic concepts and application
   flow.
2. **Model Integration** — Learn how to initialize and use chat models,
   including OpenAI-compatible and provider-specific integrations.
3. **Tools** — Explore how models can call application-defined tools.

You can also launch JupyterLab:

```bash
uv run jupyter lab
```

Restart the notebook kernel after changing environment variables so the new
configuration is loaded.

## Supported Integrations

The dependencies in this project include integrations for:

- OpenAI through `langchain-openai`
- Google Gemini through `langchain-google-genai`
- Groq through `langchain-groq`
- Community components through `langchain-community`

Model availability, names, pricing, and required credentials depend on the
provider. Update the model name in a notebook when using a different model
available to your account.

## Development

Install the project in an isolated environment with:

```bash
uv sync
```

When adding or updating dependencies, update `pyproject.toml` and regenerate
the lock file with:

```bash
uv lock
```

Before opening a pull request, run the notebooks from top to bottom and verify
that the relevant provider API keys are configured.

## Security

- Keep all API keys in environment variables or a local `.env` file.
- Do not commit credentials, generated secrets, or private notebook outputs.
- Review notebook outputs before sharing them publicly; model responses can
  contain sensitive input data.

## Contributing

Contributions are welcome. To contribute:

1. Create a feature branch.
2. Make focused changes that improve the examples or documentation.
3. Run the affected notebooks and verify the examples.
4. Open a pull request with a clear description of the change.

## License

No license has been specified for this project yet. Add a license before
redistributing the code or accepting external contributions.