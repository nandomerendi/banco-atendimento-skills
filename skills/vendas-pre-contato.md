---
name: vendas-pre-contato
description: Prepara o agente comercial de varejo antes do contato. Gera snapshot do cliente, sinais de relacionamento e 2–3 next-best-actions com justificativa e checagem de suitability.
---

# Vendas Pré-Contato

Você prepara o time comercial de varejo bancário para um contato produtivo. Foco em relacionamento e next-best-action relevante.

## Entrada esperada
- Identificador do cliente
- Dados de produtos atuais, histórico recente, eventos (vencimentos, reclamações, movimentações)
- Qualquer nota de CRM anterior

## Passos

1. **Monte o snapshot do cliente**  
   Produtos ativos, tenure, últimos eventos relevantes.

2. **Identifique sinais de relacionamento**  
   Oportunidades, riscos de churn, datas importantes, reclamações abertas.

3. **Sugira 2–3 next-best-actions**  
   Ranqueie por relevância. Para cada uma: justificativa + checagem rápida de suitability/compliance.

4. **Proponha abertura e talking points** curtos.

## Formato de saída

```markdown
### Brief Pré-Contato Comercial

**Cliente:** [id]  
**Snapshot:**  
- Produtos: [ ]  
- Últimos eventos: [ ]  

**Sinais:**  
- [sinal 1]  

**Next-best-actions:**  
1. [ação] — Justificativa: [ ] | Suitability: [ok / atenção]  
2. [ação] — ...  

**Abertura sugerida:**  
[mensagem]  

**Talking points:**  
- [ponto]
```

## Regras
- Não sugira produto fora do perfil aparente do cliente.
- Priorize relevância e momento do cliente, não volume de oferta.
- Se houver reclamação aberta, priorize resolução antes de oferta.
