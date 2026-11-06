# Croqui para o Claude Code

Plugin oficial do [Croqui](https://croqui.erickcardoso.com.br): conecta o Claude Code ao seu canvas de design, à lousa, às tarefas e aos sites do DevWeb, pela nuvem, com login da sua conta do Croqui no navegador.

## Instalar

```bash
claude plugin marketplace add Erickncardoso/croqui-plugin
claude plugin install croqui@croqui
```

Depois abra o Claude Code, rode `/mcp`, escolha **plugin:croqui:croqui** e clique em **Authenticate**. Entre com a sua conta do Croqui e volte ao terminal.

## O que vem junto

- **Servidor MCP na nuvem** (`https://croqui-api.erickcardoso.com.br/mcp`): arquivos, telas, lousa, tarefas, diretrizes, skills da sua conta, sites do DevWeb e pedidos aos agentes do Croqui.
- **Skills**
  - `croqui-canvas`: desenhar e alterar telas seguindo as diretrizes do arquivo.
  - `croqui-site`: criar um site inteiro no DevWeb com os agentes do Croqui, ou trazer um site do DevWeb para o projeto atual.
  - `croqui-tasks`: tarefas e lousa.

## Nome do agente no canvas

Para a equipe saber quem é quem quando vários agentes trabalham juntos:

```bash
CROQUI_AGENT_ROLE=Designer claude
```

## Só o servidor, sem as skills

```bash
claude mcp add --transport http -s user croqui https://croqui-api.erickcardoso.com.br/mcp
```

Guia completo de conexão (Claude, Codex, Cursor, VS Code, ChatGPT, Grok, OpenCode e outros): https://croqui.erickcardoso.com.br/docs/
