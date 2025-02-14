# Fetch MCP Server
[![smithery badge](https://smithery.ai/badge/@ExactDoug/mcp-fetch)](https://smithery.ai/server/@ExactDoug/mcp-fetch)

A Model Context Protocol server that provides web content fetching capabilities. This server enables LLMs to retrieve and process content from web pages, converting HTML to markdown for easier consumption.

The fetch tool will truncate the response, but by using the `start_index` argument, you can specify where to start the content extraction. This lets models read a webpage in chunks, until they find the information they need.

### Available Tools

- `fetch` - Fetches a URL from the internet and extracts its contents as markdown.
    - `url` (string, required): URL to fetch
    - `max_length` (integer, optional): Maximum number of characters to return (default: 5000)
    - `start_index` (integer, optional): Start content from this character index (default: 0)
    - `raw` (boolean, optional): Get raw content without markdown conversion (default: false)

### Prompts

- **fetch**
    - Fetch a URL and extract its contents as markdown
    - Arguments:
        - `url` (string, required): URL to fetch

## Installation

### Installing via Smithery

To install Fetch Server for Claude Desktop automatically via [Smithery](https://smithery.ai/server/@ExactDoug/mcp-fetch):

```bash
npx -y @smithery/cli install @ExactDoug/mcp-fetch --client claude
```

Optionally: Install node.js, this will cause the fetch server to use a different HTML simplifier that is more robust.

### Using uv (recommended)

When using [`uv`](https://docs.astral.sh/uv/) no specific installation is needed. We will
use [`uvx`](https://docs.astral.sh/uv/guides/tools/) to directly run `mcp-server-fetch`.

### Using PIP

Alternatively you can install `mcp-server-fetch` via pip:

```
pip install mcp-server-fetch
```
