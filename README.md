# JEVaaS skills

Skills para agentes de código construírem com o [JEVaaS](https://jevaas.com.br): decisão
tipada, roteada e auditável. O modelo que escreve continua escrevendo; o JEV responde às
perguntas que não geram texto.

## Instalar

Claude Code:

```bash
claude plugin marketplace add vertikon/jevaas-skills
claude plugin install jevaas@jevaas
```

Outros agentes:

```bash
npx skills add vertikon/jevaas-skills --skill jevaas
```

A skill ensina o agente a usar a API, o SDK e o servidor MCP. Ela não é o JEV: as chamadas
precisam de uma chave `jev_sk_…` de https://dashboard.jevaas.com.br/chaves-api.

## Servidor MCP

```json
{ "mcpServers": { "jevaas": { "command": "npx", "args": ["-y", "@jevaas/mcp"],
  "env": { "JEVAAAS_API_KEY": "${JEVAAAS_API_KEY}" } } } }
```

## Licença

MIT
