# Banco Atendimento Skills

Skills de atendimento assistido para times humanos de banco (Customer Service e Comercial de varejo).

Formato **SKILL.md** pronto para injeção em tempo de execução em um Harness LangGraph.

## Estrutura do repositório

```
skills/
├── pattern-skill-cs.md          # Template CS
├── pattern-skill-sales.md       # Template Vendas
├── cs-pre-atendimento.md
├── cs-durante-resolucao.md
├── cs-pos-atendimento.md
├── vendas-pre-contato.md
├── vendas-durante.md
└── vendas-pos-contato.md
```

## Skills incluídas

### Customer Service (Dúvidas / Resolutividade)
- `pattern-skill-cs.md` — Template padrão CS
- `cs-pre-atendimento.md` — Brief antes da conversa
- `cs-durante-resolucao.md` — Assistência em tempo real (foco FCR)
- `cs-pos-atendimento.md` — Fechamento + classificação FCR + CRM

### Vendas / Comercial
- `pattern-skill-sales.md` — Template padrão Comercial
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
- Suitability e compliance nas ofertas comerciais
