---
name: croqui-site
description: Criar um site completo no DevWeb do Croqui, ou trazer um site do DevWeb para o projeto atual. Use quando pedirem "cria um site/landing no Croqui", "puxa o site do Croqui pra cá" ou quiserem que os agentes do próprio Croqui façam um trabalho grande.
---

# Sites no Croqui (DevWeb)

## Criar um site com os agentes do Croqui
1. `croqui_app_status`: precisa de um app do Croqui aberto (é lá que rodam os agentes, com os planos de IA da pessoa). Se não houver, peça para abrir.
2. `ask_croqui_agent({ task: "site", text, kind })` com o pedido completo (público, seções, tom, cores, idioma). `kind`: `site`, `landing` ou `sales`.
3. Acompanhe com `get_croqui_agent_request({ requestId })` a cada 20–30 s até `done` ou `error`. Leva alguns minutos.
4. No fim, conte à pessoa o nome do site; ele já fica aberto no DevWeb para editar e publicar.

Para muitas telas num arquivo de design, use `ask_croqui_agent({ task: "design", fileId, text })`.

## Trazer um site do DevWeb para este projeto
1. `list_devweb_projects` e escolha o projeto.
2. `get_devweb_project` mostra o manifesto, as rotas e as imagens (com URL).
3. `get_devweb_files` em lotes e grave os arquivos no projeto atual, mantendo os caminhos. Baixe as imagens pelas URLs.
