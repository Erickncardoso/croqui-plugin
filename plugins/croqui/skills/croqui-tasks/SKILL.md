---
name: croqui-tasks
description: Ler, criar, atualizar e fechar tarefas e usar a lousa do Croqui. Use quando pedirem para ver o que está pendente, registrar tarefas, ou montar um brainstorm, fluxo ou retrospectiva na lousa do Croqui.
---

# Tarefas e lousa no Croqui

## Tarefas
- `list_task_projects` e `list_tasks` para ver o que existe antes de criar.
- `create_task` aceita linguagem natural no título ("revisar hero amanhã 14h p1"). Ligue a um design com `linkedFileId` + `nodeId` quando fizer sentido.
- `update_task` para mudar prazo, prioridade ou descrição; `complete_task` ao terminar. Tarefas ligadas a issues do GitHub refletem lá.

## Lousa
- `create_whiteboard` ou `get_whiteboard` de uma existente.
- `add_whiteboard_items` em poucas chamadas: notas, formas, seções, tabelas e setas. Organize por seções (ex.: "Ideias", "Votadas", "Próximos passos").
- `update_whiteboard_items` / `delete_whiteboard_items` para ajustar.
