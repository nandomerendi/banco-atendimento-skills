# Banco Atendimento Skills

Skills de atendimento assistido para times humanos de banco (Customer Service e Comercial de varejo).

Formato **SKILL.md** pronto para injeção em tempo de execução em um Harness LangGraph.

## Skills incluídas

### Customer Service (Dúvidas / Resolutividade)
- `cs-pre-atendimento.md` — Brief antes da conversa
- `cs-durante-resolucao.md` — Assistência em tempo real (foco FCR)
- `cs-pos-atendimento.md` — Fechamento + classificação FCR + CRM

### Vendas / Comercial
- `vendas-pre-contato.md` — Snapshot + next-best-action
- `vendas-durante.md` — Assistência durante a conversa
- `vendas-pos-contato.md` — Nota de CRM + follow-up

## Como usar

No seu nó LangGraph, carregue o conteúdo do SKILL.md correspondente e use como system prompt / instruction do agente daquele passo.

```python
def load_skill(skill_name: str) -> str:
    with open(f"skills/{skill_name}.md") as f:
        return f.read()
```

## Princípios

- FCR primeiro (resolução real no primeiro contato)
- TMA como consequência, não meta primária
- Grounding em política/sistema (não inventar)
- Alçada clara do humano
- Histórico viaja entre etapas
