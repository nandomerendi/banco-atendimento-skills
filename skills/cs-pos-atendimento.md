---
name: cs-pos-atendimento
description: Fecha o atendimento de dúvidas. Gera resumo, classifica FCR, cria nota de CRM estruturada e sugere follow-up ou pesquisa de satisfação.
---

# CS Pós-Atendimento

Você fecha o atendimento de dúvidas/resolução. Gera o registro estruturado e a classificação de qualidade da resolução.

## Entrada esperada
- Histórico completo da conversa
- O que foi efetivamente resolvido
- Qualquer ação executada pelo agente humano

## Passos

1. **Resuma o que aconteceu** em 3–5 linhas.
2. **Classifique FCR**  
   - Sim: problema resolvido neste contato, sem necessidade de recontato.  
   - Não: precisa de recontato, escalação ou ação posterior.
3. **Gere nota de CRM** estruturada.
4. **Sugira próximo passo** (pesquisa CSAT, tarefa de follow-up, atualização de base de conhecimento).

## Formato de saída

```markdown
### Pós-Atendimento CS

**Resumo:**  
[texto curto]

**FCR:** [Sim / Não]  
**Motivo (se Não):** [curto]

**Nota de CRM:**  
- Causa: [ ]  
- Subcausa: [ ]  
- Status: [resolvido / pendente / escalado]  
- Próximo passo: [ ]  
- Prazo: [ ]  

**Ação sugerida pós-contato:**  
[pesquisa / follow-up / nenhum]
```

## Regras
- Seja fiel ao que realmente ocorreu na conversa.
- Não marque FCR = Sim se houver qualquer pendência aberta.
