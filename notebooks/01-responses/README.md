# Responses API Examples

This directory contains examples demonstrating how to use the Llama Stack Responses API for various AI applications including simple inference, Retrieval-Augmented Generation (RAG), and Model Context Protocol (MCP) tool calling.

## Overview

The Responses API provides a unified interface for AI interactions that can handle:

- Simple model inference
- Retrieval-Augmented Generation with document search
- Tool calling through Model Context Protocol (MCP) servers
- Complex multi-step workflows

## Files in this Directory

- [responses-api.ipynb](./responses-api.ipynb) - Main Python notebook with comprehensive examples
- [nps_mcp_server.py](./nps_mcp_server.py) - US National Park Service MCP server implementation
- [requirements.txt](./requirements.txt) - Python dependencies for running the examples
- [run.yaml](./run.yaml) - Llama Stack configuration file
- [README.md](./README.md) - This file.
- [README_NPS.md](./README_NPS.md) - Additional README file with more information about the National Park Service MCP server.

## Instructions

To see all the prerequisites for running the notebook and how to meet them, see the instructions at the start of the notebook. Set up a Python 3.12 environment, e.g., using Anaconda, `venv`, or similar tool. Then do the following steps in one terminal window:

```shell
# Install the dependencies:
pip install -r requirements.txt
# Run the Llama Stack server
llama stack run run.yaml --image-type venv --port 8321
```

In a second window, run the National Park Service MCP server:

```shell
python nps_mcp_server.py --transport sse --port 3005 --log-level DEBUG
```

Open the notebook [`reponses-api.ipynb`](reponses-api.ipynb) using [Jupyter](https://jupyter.org/), which is not installed as part of the `requirements.txt`. You can install Jupyter Lab as follows:

```shell
pip install jupyterlab
```

Then run the lab environment and open the notebook in the left-hand side browser:

```shell
jupyter lab
```

## What You'll Learn

The notebook demonstrates three main approaches to using the Responses API:

### 1. Llama Stack Client

- Direct integration with Llama Stack
- Complete control over API interactions
- Best for users new to the ecosystem

### 2. OpenAI Client

- Using OpenAI's client library with Llama Stack
- Good for existing projects already using the OpenAI client
- Requires URL suffix: `/v1/openai/v1`

### 3. LangChain Integration

- Higher-level abstractions for complex workflows
- Framework-based approach
- Simplified code with `use_responses_api=True`

## Troubleshooting

### Common Issues

1. **Port already in use**: If port 8321 or 3005 is busy, use different ports:
   ```bash
   llama stack run run.yaml --image-type venv --port 8322
   python nps_mcp_server.py --transport sse --port 3006
   ```

2. **API key not working**: Verify your API keys are correctly set:
   ```bash
   echo $OPENAI_API_KEY  # Should show your key
   ```

3. **Connection Error**: You might need to change the port used for Llama Stack. Notice the URL printed in the terminal window where you are running Llama Stack. Make sure `LLAMA_STACK_URL` uses the same port number in the notebook.

4. **Python version issues**: Ensure you are using Python 3.12+:
   ```bash
   python --version
   ```

5. **Dependency conflicts**: Use a fresh virtual environment if you encounter package conflicts.

## Support

This notebook and README were developed with assistance from Google Gemini and Cursor using Claude Sonnet 4. For issues with:

- **The notebook itself**: Review the notebook cells for detailed explanations that may help. Post an [issue](https://github.com/The-AI-Alliance/llama-stack-examples/issues) or open a [discussion](https://github.com/The-AI-Alliance/llama-stack-examples/discussions) if you need more help.
- **Llama Stack**: Check the [official documentation](https://llama-stack.readthedocs.io/).
- **MCP Protocol**: See [Model Context Protocol docs](https://modelcontextprotocol.io/).