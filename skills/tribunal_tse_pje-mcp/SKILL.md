---
name: tribunal_tse_pje-mcp
description: Skill da REST API do Tribunal TSE: Processo Judicial Eletrônico (PJe) na MCP.AI: 1 endpoint em /api/tribunal_tse_pje. Tribunal TSE: Processo Judicial Eletrônico (PJe), consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Tribunal TSE: Processo Judicial Eletrônico (PJe) — REST API skill

Você tem acesso à **Tribunal TSE: Processo Judicial Eletrônico (PJe)** REST API na MCP.AI.

> Tribunal TSE: Processo Judicial Eletrônico (PJe), consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/tribunal_tse_pje
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
curl -X POST https://api.mcp.ai/api/tribunal_tse_pje/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/tribunal_tse_pje/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `tribunal_tse_pje_consultar`

Tribunal TSE: Processo Judicial Eletrônico (PJe), consulta em fonte oficial. _(POST /api/tribunal_tse_pje/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `numero_processo` | string | Não | Parâmetro de consulta "numero_processo". |
| `cpf` | string | Não | Parâmetro de consulta "cpf". |
| `cnpj` | string | Não | Parâmetro de consulta "cnpj". |
| `classe_judicial` | string | Não | Parâmetro de consulta "classe_judicial". |
| `objeto` | string | Não | Parâmetro de consulta "objeto". |
| `orgao` | string | Não | Parâmetro de consulta "orgao". |
| `uf` | string | Não | Parâmetro de consulta "uf". |
| `municipio` | string | Não | Parâmetro de consulta "municipio". |
| `ano_eleicao` | string | Não | Parâmetro de consulta "ano_eleicao". |
| `data_inicial_autuacao` | string | Não | Parâmetro de consulta "data_inicial_autuacao". |
| `data_final_autuacao` | string | Não | Parâmetro de consulta "data_final_autuacao". |
| `nome_parte` | string | Não | Parâmetro de consulta "nome_parte". |
| `nome_advogado` | string | Não | Parâmetro de consulta "nome_advogado". |
| `oab` | string | Não | Parâmetro de consulta "oab". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_tribunal_tse_pje` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
