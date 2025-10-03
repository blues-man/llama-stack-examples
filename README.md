# Llama Stack Example Apps

This repo contains a growing suite of example applications for <a href="https://github.com/meta-llama/llama-stack">Llama Stack</a> that demonstrate various stack features and common application patterns.

See the corresponding README for each example for more information. Here we summarize the examples.

## Application Examples

These applications are in the [`apps`](apps/) directory.

* [`01-chatbot`](apps/01-chatbot): A getting-start chatbot app, which shows how to build and deploy Llama Stack applications. It includes two different UI options and inference with an [ollama](https://ollama.com)-hosted [Llama 3](https://www.llama.com/models/llama-3/) model.
* [`02-deep-research`](apps/02-deep-research): A _deep research_ app (under development), which illustrates an emerging, common application pattern for AI. The user asks for detailed information about a topic, for example the market performance and financials for a publicly-traded company, agents find relevant data from diverse sources, and finally an LLM digests the information retrieved and prepares a report. This example will demonstrate Llama Stack support for agent-based application development, including the use of protocols like [MCP](https://modelcontextprotocol.io/introduction).

## Notebook Examples

These examples use Jupyter notebooks to illustrate their concepts. They are located in the [`notebooks`](notebooks/) directory.

* [`01-responses`](notebooks/01-responses): This notebook demonstrates how to use the Llama Stack _Responses_ API for simple inference, Retrieval-Augmented Generation (RAG), and Model Context Protocol (MCP) tool calling.

> [!NOTE]
> **Please join us!** We welcome new examples. You can submit them or submit improvements to the current examples using [PRs](https://github.com/The-AI-Alliance/llama-stack-usecase1/pulls), make suggestions or report bugs as [issues](https://github.com/The-AI-Alliance/llama-stack-usecase1/issues), or use the [discussions forum](https://github.com/The-AI-Alliance/llama-stack-usecase1/discussions) for general questions and suggestions. For more information about joining this project or other AI Alliance projects, go [here](https://the-ai-alliance.github.io/contributing/). The main AI Alliance website is [here](https://aialliance.org).
>
> If you are interested in running Llama Stack on Kubernetes or OpenShift, see [these examples from opendatahub.io](https://github.com/opendatahub-io/llama-stack-demos).
