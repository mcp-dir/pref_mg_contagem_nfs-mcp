---
name: pref_mg_contagem_nfs-mcp
description: Skill da REST API do Prefeitura MG Contagem: NFS-e (Nota Fiscal Eletrônica de Serviços) na MCP.AI: 1 endpoint em /api/pref_mg_contagem_nfs. Prefeitura MG Contagem: NFS-e (Nota Fiscal Eletrônica de Serviços), consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Prefeitura MG Contagem: NFS-e (Nota Fiscal Eletrônica de Serviços) — REST API skill

Você tem acesso à **Prefeitura MG Contagem: NFS-e (Nota Fiscal Eletrônica de Serviços)** REST API na MCP.AI.

> Prefeitura MG Contagem: NFS-e (Nota Fiscal Eletrônica de Serviços), consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/pref_mg_contagem_nfs
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/pref_mg_contagem_nfs/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"numero_nota":"...","codigo_verificacao":"...","cpf_cnpj_prestador":"...","declaracao":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/pref_mg_contagem_nfs/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `pref_mg_contagem_nfs_consultar`

Prefeitura MG Contagem: NFS-e (Nota Fiscal Eletrônica de Serviços), consulta em fonte oficial. _(POST /api/pref_mg_contagem_nfs/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `numero_nota` | string | Sim | Parâmetro de consulta "numero_nota". |
| `codigo_verificacao` | string | Sim | Parâmetro de consulta "codigo_verificacao". |
| `cpf_cnpj_prestador` | string | Sim | Parâmetro de consulta "cpf_cnpj_prestador". |
| `declaracao` | string | Sim | Parâmetro de consulta "declaracao". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_pref_mg_contagem_nfs` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
