---
tipo: bussola
gaveta: raiz
status: rascunho
autor: claude
atualizado: 2026-11-18
---
# AGENTS.md — Bússola para ChatGPT / Codex e outros agentes

> Este arquivo é lido automaticamente pelo Codex. Qualquer IA que não seja o Claude começa por aqui.

## Regra única
**As regras do cofre estão em [`CLAUDE.md`](CLAUDE.md) e valem para todos os agentes**, não só para o Claude. Leia esse arquivo inteiro e siga a mesma ordem de leitura:
1. `CLAUDE.md` → 2. `aprendizados.md` → 3. `hot.md` → 4. `QUADRO.md` → 5. notas sob demanda.

## O que muda para você (ChatGPT / Codex)
| Área | Pode? |
|---|---|
| `_CELSO/` | **Somente leitura.** |
| Gavetas `00`…`99` | Criar e atualizar notas com `autor: chatgpt` e `status: rascunho`. Nunca apagar: mover para `99_ARQUIVO/`. |
| `_CLAUDE/` | **Não escrever** (área do Claude). Pode ler. |
| `_CODEX/` | Sua área de trabalho: logs, rascunhos, pesquisas. Autonomia total. |
| `QUADRO.md` | Ler sempre no início; escrever recados e passagens de turno. |
| `CLAUDE.md`, `AGENTS.md`, `aprendizados.md` | Não editar. Propor mudanças no `QUADRO.md`. |

## Convivência com o Claude
- **Antes de editar uma nota**, veja no `QUADRO.md` se ela está "em uso" pelo outro agente.
- **Ao terminar**, registre no `QUADRO.md`: o que fez, o que falta e o que precisa de revisão.
- Papel padrão do ChatGPT neste cofre: **auditor e segunda opinião** (revisar propostas, cálculos, riscos fiscais e planos feitos pelo Claude). Pode também produzir conteúdo quando o Celso pedir.
- Em divergência com o Claude, não sobrescreva: descreva a divergência no `QUADRO.md` para o Celso decidir.

## Git
Se tiver acesso ao git: commits pequenos, mensagem começando com `[chatgpt]`. Nunca forçar push nem reescrever histórico.
