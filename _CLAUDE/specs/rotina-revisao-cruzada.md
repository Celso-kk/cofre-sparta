---
tipo: spec
gaveta: _CLAUDE
status: rascunho
autor: claude
atualizado: 2026-11-18
---
# Rotina 1 — Revisão cruzada de propostas (Claude faz, ChatGPT audita)

## Objetivo
Nenhuma proposta comercial sai sem uma segunda opinião independente sobre **fiscal, preço e cláusulas**.

## Fluxo
| # | Quem | O quê |
|---|---|---|
| 1 | Claude | Gera a proposta (.docx, skill `proposta-comercial-sparta`) e cria a nota em `03_COMERCIAL/` com o `_MODELOS/Modelo - Proposta`, com todos os números da formação de preço e o tratamento fiscal. |
| 2 | Claude | Abre o pedido no `QUADRO.md`: `Claude → ChatGPT · Revisar fiscal e preço · [[nota]] · aberto`. |
| 3 | Celso | No app ChatGPT, projeto **cofre-sparta**: *"Faça as revisões abertas do QUADRO"*. |
| 4 | ChatGPT | Aplica o checklist abaixo e escreve a seção `## Revisão ChatGPT` **no fim da nota da proposta**. Não altera valores nem o .docx. |
| 5 | ChatGPT | Muda o pedido para `revisado` no quadro e o campo `revisao_chatgpt` da nota para `ok` ou `ajustar`. Se achar erro **crítico**, registra também em "Divergências para o Celso decidir". |
| 6 | Celso | Decide. Se houver ajuste: `Claude execute registrar: …` e o Claude corrige a proposta e a nota. |

## Checklist do ChatGPT (cada item: ✅ ok · ⚠️ atenção · ❌ erro)
1. **Fiscal:** UF de destino, contribuinte ou não de ICMS, alíquota interestadual, DIFAL (quem recolhe), NCM (8436.80.00 / 8432.80.00 para Prinoth).
2. **Preço:** soma da formação de preço (EXW → custo importado → margem → venda) refeita do zero; câmbio e data da cotação informados.
3. **Margem:** margem real calculada × margem-alvo da nota.
4. **Condições:** parcelamento, sinal, prazo de entrega, validade da proposta, reserva de domínio.
5. **Coerência com `aprendizados.md`:** regras do Celso (nomenclatura do arquivo, ICMS com redução de base, etc.).
6. **Risco comercial:** algo que o cliente pode questionar ou que deixa a SPARTA exposta.

## Formato da seção na nota
```
## Revisão ChatGPT — AAAA-MM-DD
| Item | Resultado | Comentário |
|---|---|---|
| Fiscal | ✅/⚠️/❌ | … |
…
**Veredito:** pode enviar / enviar após ajustes / não enviar
```
