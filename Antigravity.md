# Antigravity Workflows (n8n)

Este documento foi criado para centralizar a arquitetura, regras e documentação técnica dos fluxos de trabalho (workflows) desenvolvidos no n8n para a sua plataforma. 

O objetivo principal é garantir automações robustas, escaláveis e com o mais alto padrão de qualidade para o projeto Antigravity.

---

## 🛠 Ferramentas Ativas (n8n MCP & Skills)

Com base nas documentações analisadas, nossa inteligência de criação de fluxos funcionará de forma muito mais poderosa agora. Temos acesso a:

**Funcionalidades do n8n-mcp:**
- Criação e atualização de fluxos diretamente via integração (`n8n_create_workflow`, `n8n_update_full_workflow`).
- Busca e validação avançada de nós do n8n (`search_nodes`, `validate_node`, `validate_workflow`).
- Importação de templates da comunidade (`search_templates`, `get_template`, `n8n_deploy_template`).
- Testes diretos e histórico de execução (`n8n_test_workflow`, `n8n_executions`).

**Diretrizes e Regras aplicadas (n8n-skills):**
- **Syntax & Expressions:** Utilização correta de `$json`, `$node` e `$env`.
- **Validação & Teste:** Resolução preditiva de erros baseada em *profiles* estritos (runtime, AI-friendly).
- **Programação em Nodes:** Foco absoluto em *JavaScript* (nó Code) utilizando `$input.all()` e `$helpers.httpRequest()`, reservando Python apenas para casos restritos.
- **Padrões de Arquitetura:** 5 padrões arquitetônicos consolidados (Webhook, API HTTP, Banco de Dados, AI e Agendado).

---

## 🚀 Como Vamos Trabalhar
1. **Definição da Ideia:** Você me passa o objetivo do fluxo (Ex: "Disparar WhatsApp logo que o cliente for aprovado no Painel Admin Lunnar/Antigravity").
2. **Setup e Criação:** Eu estruturo a ideia, uso as ferramentas MCP para validar, buscar os melhores links ou criar o JSON do fluxo do Zero.
3. **Revisão e Deploy:** Posso injetar a automação diretamente no seu n8n usando `n8n_create_workflow` ou te entregar o JSON validado e blindado contra erros.

***
**Status Atual:** Integrações e regras de ouro (n8n-skills) injetadas no meu contexto interno. Tudo pronto para construirmos o primeiro fluxo!
