# Instalação detalhada

Prefeitura MG Contagem: NFS-e (Nota Fiscal Eletrônica de Serviços) é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_pref_mg_contagem_nfs`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_pref_mg_contagem_nfs` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_pref_mg_contagem_nfs` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_pref_mg_contagem_nfs` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.pref_mg_contagem_nfs` (ou `servers.pref_mg_contagem_nfs` no VS Code) do config do cliente e reinicie.
