---
tipo: bussola
atualizado: 2026-11-15
---
# CLAUDE.md — Bússola do Cofre SPARTA

> Claude: leia este arquivo inteiro no início de toda sessão. Ele diz onde está cada coisa e o que você pode e não pode fazer aqui.

## 1. O que é este cofre
Segundo cérebro da **SPARTA BRASIL Máquinas Industriais Ltda.** (Jaguariúna/SP), que importa, revende e representa trituradores florestais, cabeçotes trituradores e destocadores (Prinoth, Dipperfox) para supressão vegetal mecanizada.

- Dono (100%) e Diretor Executivo: **Celso Kossaka**.
- **Território:** a SPARTA BRASIL vende **somente no Brasil**. Fora do Brasil (Uruguai, Costa Rica etc.) quem atua é **Celso Kossaka, representante oficial da Prinoth GmbH**. Toda nota de cliente indica a entidade.
- Meta-mãe: **R$ 15 MM de patrimônio líquido até nov/2031**, com a SPARTA vendável ou com novos sócios e Celso como conselheiro. Ver [[00_COMANDO/Plano 2031|Plano 2031]].
- O cofre pessoal do Celso é **outro** (`cofre-pessoal`). Nada pessoal entra aqui.

## 2. Ordem de leitura (economiza tempo e tokens)
1. `CLAUDE.md` (este arquivo)
2. `aprendizados.md`: regras que nasceram de correções. **Obrigatório.**
3. `hot.md`: o que está quente agora.
4. `mapa.md`: só quando precisar localizar algo.
5. Notas específicas: abrir sob demanda. **Nunca ler o cofre inteiro.**

## 3. Os três fluxos: quem escreve onde
| Área | Quem escreve | Regra para o Claude |
|---|---|---|
| `_CELSO/` | Só o Celso | **Somente leitura.** Nunca criar, editar, mover ou apagar. |
| Gavetas `00_COMANDO` … `99_ARQUIVO` | Celso e Claude | Pode criar e atualizar notas operacionais. Nota criada pelo Claude leva `autor: claude` e `status: rascunho` até o Celso validar (`status: validado`). Nunca apagar: mover para `99_ARQUIVO/`. |
| `_CLAUDE/` | Claude | Autonomia total: logs, specs, rascunhos, skills. Podagem mensal. |
| `_INBOX/` | Celso (captura rápida) | Ler e propor triagem. Mover para a gaveta certa só com OK do Celso ou via `Claude execute arquivar`. |
| `_MODELOS/` | Celso | Propor modelos novos em `_CLAUDE/specs/`. |

## 4. As gavetas
| Gaveta | O que guarda |
|---|---|
| `00_COMANDO` | Plano 2031, decisões estratégicas, metas, tom de voz, rotinas |
| `01_ADM_FINANCAS` | Finanças, contabilidade, fiscal, importação/despacho, bancos, seguros, RH, jurídico |
| `02_CLIENTES` | Uma nota por cliente: histórico, contatos, equipamentos, oportunidades |
| `03_COMERCIAL` | Propostas, precificação, tabela de custos EXW, negociações com fábricas |
| `04_TECNICO` | Equipamentos, compatibilidade, manuais, diagnósticos, consultas de peças |
| `05_MARKETING` | Site, SEO, newsletter, redes, feiras, identidade visual, concorrência digital |
| `06_COMPARTILHADOS` | Material de uso comum: anexos, apresentações, documentos institucionais |
| `07_NOVOS_NEGOCIOS` | Forestec, Prinoth Crawler, empresa no Canadá, novas linhas |
| `08_TEMP` | Trabalho em andamento sem gaveta definida (limpar todo mês) |
| `99_ARQUIVO` | Encerrados e superados. Nada é apagado, vem para cá |

## 5. Convenções
- **Datas:** AAAA-MM-DD.
- **Dinheiro:** sempre com moeda (R$, USD, EUR) e base (EXW, CIF, custo importado, preço de venda).
- **Links:** use `[[ ]]`. Nota de cliente sempre liga às pessoas e aos equipamentos.
- **Frontmatter mínimo:** `tipo`, `gaveta`, `status`, `autor`, `atualizado`.
- **Arquivos de proposta:** `MARCA_MODELO_AAMMDDHHMM_EMPRESA`.
- **Anexos** (PDF, fotos, planilhas): `06_COMPARTILHADOS/anexos/`.
- **Modelos** de nota: `_MODELOS/`.

## 6. Comandos do Celso
Mensagem que começa com **"Claude execute"** é comando. Sem o prefixo, é conversa.
*(Definições propostas, a validar no Bloco 6 da entrevista.)*

| Comando | O que o Claude faz no cofre |
|---|---|
| `Claude execute registrar: …` | Grava o fato ou decisão, com data, na nota da gaveta certa. Se for decisão, também em [[00_COMANDO/Decisoes]]. |
| `Claude execute peça: …` | Cria a consulta em `04_TECNICO/consultas/` com o modelo de consulta, para resgatar no futuro com fidelidade. |
| `Claude execute cliente: …` | Abre ou atualiza a nota do cliente e devolve um resumo da situação. |
| `Claude execute cruzar: A x B` | Cruza informações entre notas (ex.: cliente × equipamento × preço). |
| `Claude execute buscar: …` | Procura no cofre e lista as notas encontradas. |
| `Claude execute fechamento` | Resumo do dia ou da semana e atualização do `hot.md`. |
| `Claude execute arquivar: …` | Move a nota para `99_ARQUIVO/`, ou do `_INBOX/` para a gaveta certa. |
| `Claude execute semana` | Planejamento da semana: prioridades e agenda no `hot.md`. |

## 7. Estilo das respostas
- Português, direto e analítico.
- Tabelas e comparativos; mapas mentais para planos.
- Didático em tributário, contábil e finanças, com exemplos práticos.
- **Sem analogias hidráulicas.**
- Precisão técnica, sempre com as ressalvas práticas.

## 8. Segurança
Nunca gravar senhas, logins, tokens, nem números de conta bancária ou de cartão. Dados de terceiros: só o necessário para o negócio.

## 9. Fonte da verdade
- O **cofre** é a fonte da verdade detalhada.
- A **memória do Claude** (claude.ai) é o resumo curto.
- Em conflito, vale a nota `status: validado` mais recente. Registre a divergência em `aprendizados.md`.

## 10. Ao terminar uma sessão de trabalho
1. Atualizar `hot.md` se algo mudou de status.
2. Se o Celso corrigiu algo, registrar a regra nova em `aprendizados.md`.
3. Gravar um log curto em `_CLAUDE/logs/AAAA-MM-DD.md`.
