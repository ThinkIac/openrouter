# openrouter

App de configuração do provider OpenRouter — insere/gerencia o slot em agent.config.json → llm.pools[] (chave de API + modelo), liga/desliga e testa a conexão ao vivo. OpenRouter é uma API OpenAI-compatible que dá acesso a centenas de modelos (Anthropic, OpenAI, Google, Meta, DeepSeek…) com uma única chave.

Repositório: https://github.com/ThinkIac/openrouter.

## Uso no ThinkIac

Este pacote foi extraído de `packages/openrouter`. Preserve a identidade `openrouter` do manifest ao instalá-lo em um workspace Lógos. Views, rotas, ferramentas e hooks são descobertos pelo runtime e dependem dos provedores correspondentes. Esta extração publica o código atual; não converte JavaScript para LógosType nem implementa instalação por perfil.

Entrada declarada: `index.js`.

## Dependências e validação

Dependências declaradas: `logos`.

O pacote não declara scripts npm de build/teste. Os testes existentes acompanham o fonte; a composição completa requer o host ThinkIac.

## Segurança e dados locais

Credenciais devem ser configuradas no ambiente de destino. Não acompanham esta extração bancos, sessões, uploads, perfis pessoais, arquivos `.env`, caches ou backups. As exclusões foram registradas em relatório externo à publicação. Configure segredos pelo host, sem incluí-los em commits.


## Registros encontrados no código

- `hook`: `boot`.
- `router`: `(que`, `model`, `models`, `save`, `status`, `test`, `toggle`.

A lista é um inventário estático e pode incluir registros em testes; não garante disponibilidade sem os provedores do host.

Há imports relativos para diretórios superiores. A instalação isolada e a composição por perfil precisam resolver esses vínculos antes de remover a cópia da base.

