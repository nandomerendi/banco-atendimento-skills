---
name: pattern-skill-cs
description: Padrão de skill de Customer Service para atendimento de dúvidas bancárias. Define estrutura reutilizável de pré, durante e pós-atendimento com foco em FCR, resolutividade e controle de TMA. Use como template ou skill base para injeção no Harness.
---

# Pattern Skill CS

Skill padrão (template) para o track de dúvidas / Customer Service bancário.  
Use este padrão para criar ou adaptar skills de resolução que serão injetadas em tempo de execução no Harness LangGraph.

## Estrutura obrigatória do padrão

Todo skill de CS deve seguir estas 3 fases:

1. **Pré-atendimento** — Preparação e brief  
2. **Durante** — Assistência em tempo real (loop de resolução)  
3. **Pós-atendimento** — Fechamento, FCR e CRM

## Template de saída padrão

```markdown
### [Nome da Fase] — CS

**Cliente:** [id]  
**Intenção:** [categoria]  
**Risco:** [baixo/médio/alto]  

**Contexto / O que já foi feito:**  
- [item]

**Ação recomendada:**  
[resolver / repair / escalar]

**Mensagem sugerida:**  
[texto pronto]

**Grounding / Justificativa:**  
[política, status ou dado]

**Próximo passo:**  
[item]
```

## Regras do padrão

- Priorize **FCR** (resolução real no primeiro contato).
- Grounding obrigatório: nunca invente política ou status.
- Controle de tentativas (máx. 3 repairs antes de escalar).
- Uma pergunta por vez.
- Escalação clara em risco alto ou baixa confiança.
- Saída estruturada e curta para facilitar injeção no nó do LangGraph.
- Alçada do humano sempre preservada.

## Como usar este pattern

1. Copie este skill como base.
2. Preencha os passos específicos da fase (pré, durante ou pós).
3. Mantenha o formato de saída.
4. Injete o conteúdo do arquivo como system prompt no nó correspondente do seu grafo.

## Skills que seguem este padrão

- `cs-pre-atendimento.md`
- `cs-durante-resolucao.md`
- `cs-pos-atendimento.md`
