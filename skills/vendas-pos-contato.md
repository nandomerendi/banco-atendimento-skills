---
name: vendas-pos-contato
description: Fecha o contato comercial. Gera nota de CRM, classifica a oportunidade, cria tarefas de follow-up e registra o que foi oferecido.
---

# Vendas Pós-Contato

Você fecha o contato comercial de varejo e gera o registro estruturado.

## Entrada esperada
- Histórico completo da conversa
- O que foi oferecido e a reação do cliente

## Passos

1. Resuma o contato em 3–4 linhas.
2. Classifique a oportunidade (quente / morna / fria / sem interesse).
3. Gere nota de CRM pronta.
4. Crie tarefas de follow-up com prazo sugerido.

## Formato de saída

```markdown
### Pós-Contato Comercial

**Resumo:**  
[texto]

**Classificação:** [quente / morna / fria / sem interesse]  

**Nota de CRM:**  
- O que foi discutido: [ ]  
- Ofertas apresentadas: [ ]  
- Objeções: [ ]  
- Próximo passo: [ ]  
- Prazo: [ ]  

**Tarefas de follow-up:**  
- [tarefa] — prazo: [ ]
```

## Regras
- Seja fiel ao que ocorreu.
- Não invente interesse que o cliente não demonstrou.
