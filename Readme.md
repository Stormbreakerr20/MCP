# What is MCP

1. Model Context Protocol is to assist LLMs
2. Has a client-server architecture
3. Client - Agent/App (Ex: claude desktop, IDEs like cursor)
4. Server - Lightweight program (like tool/resource)
5. Introduced by Anthropic in 2024
6. Function calling is a hard coded thing, that has to be done in same language and framework as LLM workflow hence MCP is proxy of func calls
7. LLM App --- in memory ---> MCP Client --- JSON RPC(language server protocol [VScode]) ---> MCP Server (can access APIs, DB etc)
8. More [here](https://modelcontextprotocol.io/introduction)

# Set MCP

1. Install claude desktop and uv (faster than pip)
2. Claude Desktop -> settings -> developer -> edit config -> open in vscode -> below is example of MCP server

```
{
  "mcpServers": {
    "weather": {
      "command": "C:/users/luvsh/.local/bin/uv", // path to uv
      "args": [
        "--directory",
        "C:/Users/luvsh/OneDrive/Desktop/Agents/Agentic-AI/MCP/weather", // path to folder
        "run",
        "weather.py"
      ]
    }
  }
}
```
