# lab-actions-artefatos

Repositório do desafio prático de GitHub Actions — Controle de Fluxos e Sobrevivência de Arquivos.

## Estrutura

```
.github/workflows/pipeline-inteligente.yml  ← Workflow principal
src/
  codigo/script.js     ← Código-fonte
  docs/manual.md       ← Documentação (alterações aqui NÃO disparam o workflow)
testes/suite.test.js   ← Suite de testes
```

## Gatilhos configurados

| Regra | Trigger | Comportamento |
|-------|---------|---------------|
| 1 | `workflow_dispatch` | Execução manual pelo botão no GitHub |
| 2 | `schedule: cron 0 2 * * *` | Toda noite às 02:00 UTC |
| 3 | `push → branches: feature/**` | Somente em branches `feature/...` |
| 4 | `push → paths: src/** + !src/docs/**` | Monitora `src/`, ignora `src/docs/` |
teste
