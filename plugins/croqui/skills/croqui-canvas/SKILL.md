---
name: croqui-canvas
description: Desenhar ou alterar telas, componentes e design systems no Croqui pelo MCP (create_design, replace_design, get_board_html). Use quando pedirem uma tela, landing, dashboard, app ou ajuste visual "no Croqui".
---

# Desenhar no Croqui

O Croqui é um canvas onde cada quadro é HTML/CSS de verdade. Você lê e escreve pelas ferramentas do servidor `croqui`.

## Antes de desenhar
1. `list_files` para achar o arquivo (ou `create_file` se a pessoa pediu um novo) e `list_pages` para ver as páginas e quadros.
2. `list_guidelines` + `get_guidelines` do arquivo e `list_decisions`: siga o que estiver lá.
3. `list_skills`: se alguma skill da pessoa combinar com o pedido, leia com `get_skill` e siga.
4. Design novo: `get_guide({ topic: "direcao-de-arte" })`. Recriar igual um print: `get_guide({ topic: "clonar-design" })` (fidelidade total).

## Como construir
- Estrutura com flex e grid, no fluxo do documento. Posição absoluta só para o que flutua (selos, botões flutuantes, enfeites).
- Estilos inline, CSS com hífen (`font-size`, não `fontSize`), tamanhos em px.
- O que se repete (botões, cards, linhas de lista, abas) fica igual em todos os lugares.
- Um quadro por tela: `create_design` com o HTML completo; para refazer, `get_board_html` e depois `replace_design`.
- Quadros marcados como prontos para desenvolvimento não mudam sem pedido explícito.
- Ao salvar com `save_board`, mande a `baseVersion` lida; em conflito, releia e concilie.

## Ao terminar
Diga o que criou ou mudou, em que arquivo e página, e o que ficou como espaço reservado (fotos, textos a personalizar).
