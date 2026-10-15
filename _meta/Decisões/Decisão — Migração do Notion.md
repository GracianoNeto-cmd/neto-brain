---
type: decision
status: perene
sigilo: normal
created: 2026-10-15
updated: 2026-10-15
tags: [setup, notion]
---
# Decisão — Migração do Notion

**Decidido em:** 2026-10-15
**Quem aprovou:** Neto

## O que foi decidido
O conhecimento do Notion que tinha substância na própria fonte veio para o
vault. O Notion não foi alterado em nada e segue congelado como fonte histórica,
pela [[Decisão — Vault, Notion e memória do Claude]].

### O que entrou
Cinco notas novas e uma nota existente ampliada.

| Nota | Tipo | Origem no Notion |
|---|---|---|
| [[Avaliar desempenho de membro]] | skill | Sistema de Avaliação de Desempenho |
| [[Playbooks e processos da Diretoria de Projetos]] | resource | Playbooks & Processos |
| [[Entregar o MVP do Peter Pan]] | project | Projeto Peter Pan e a linha dele no database de projetos |
| [[Executar o PE2026 da Diretoria de Projetos]] | project | PE2026, mais o database de OKRs Q2 |
| [[Curso de UI e UX Design]] | resource | UI \| UX Design e a aula 1 do M1 |
| [[FIA Júnior]] | area, ampliada | Hub da Diretoria de Projetos e Pessoas & PDI |

Mais dois anexos em `_meta/anexos`, os dois diagramas de design thinking da aula
1, baixados porque o link de arquivo do Notion expira.

### O que ficou de fora, e por quê

| Item | Motivo |
|---|---|
| Controle Financeiro, com cinco databases | O `CLAUDE.md` proíbe guardar dado de finanças, de qualquer pessoa, inclusive do Neto. Nenhuma linha dessas tabelas chegou a ser aberta. |
| Projeto "Hub Notion DP" | Este vault o substitui. Virou uma linha de Timeline em [[FIA Júnior]], não nota de projeto. |
| Database "Tarefas DP" | Zero linhas. |
| Database "Avaliações de Desempenho" | Zero linhas em seis meses. A estrutura virou a skill; não havia avaliação para migrar. |
| Aula 2 do M1 e uma terceira linha sem título | Páginas em branco. Sem conteúdo, sem nota. |
| Módulos M2 a M7 do curso | Listas de aula vazias. O M5 não pôde ser conferido. |
| Os 6 playbooks, as 6 trilhas de PDI e os ~10 processos | O conteúdo não está no Notion. A fonte só lista os nomes, e os arquivos vivem na pasta local "DP Projetos". Entrou o índice, não o acervo. |

## Por quê
O Notion era uma das quatro ilhas de conhecimento do Neto, e a decisão da fase 0
determinou que o vault passa a ser dono de todo conhecimento. Sem migrar, a
decisão ficava no papel.

## Base
Inventário completo do workspace `Neto´s Home`, feito pelo conector do Notion em
2026-10-15, somente leitura. Três páginas privadas de topo, 15 páginas de
conteúdo e 16 databases, dos quais 11 vazios.

Quatro achados sustentaram as escolhas:

1. **Não existe base compartilhada da FIA Júnior no Notion.** Zero teamspaces,
   zero páginas compartilhadas nos dois sentidos. Confirma, do lado do Notion, a
   hipótese do `CONTEXTO.md` de que a equipe não compartilha material por lá.
2. **Não existe conteúdo de cliente.** O database de projetos tem a opção
   `Tipo: Cliente` e nenhuma das três linhas a usa. Por isso nada do Notion
   nasceu `sigilo: alto`.
3. **Todo o conteúdo da FIA Júnior é um retrato de 21/03 a 01/04 de 2026.** Os
   OKRs eram do Q2, o prazo do Peter Pan era junho, e as "próximas ocorrências"
   de ritual eram de abril. Por isso cada nota de projeto diz, no Resumo e no
   Estado, que é retrato datado.
4. **O Notion funcionava como catálogo, não como acervo.** Playbooks, trilhas,
   processos e dashboards estão citados em tabela, com o conteúdo em `.docx` e
   `.html` numa pasta local sem cópia fora do computador.

## O que foi descartado
- **Gravar o Peter Pan e o PE2026 como projeto ativo**, tratando o estado de
  abril como o de hoje. Custo que a derrubou: poria no vault progresso de 8% e
  35% que podem estar errados, e mostraria prazo vencido como vivo. É o erro que
  o second brain existe para evitar.
- **Mandar os dois para `5. Arquivo`.** Custo: se o Peter Pan ainda está de pé,
  ele sai do grafo e do panorama.
- **Migrar só a estrutura de categorias do Controle Financeiro, sem valor.**
  Custo: abriria porta que a regra fechou, para uma nota quase sem utilidade.
- **Deixar as duas imagens da aula 1 só como link do Notion.** Custo: o link de
  arquivo do Notion expira, então na prática as imagens se perderiam.
- **Marcar as notas de projeto como `sigilo: alto` até conferir o termo de
  confidencialidade.** Custo: as duas sairiam do único backup fora do
  computador. Ficaram `normal`, com a dúvida registrada como pendência na nota
  do Peter Pan.

## O que isto revoga
Nada. Confirma e executa a [[Decisão — Vault, Notion e memória do Claude]], e
fecha a pendência "migração do conteúdo do Notion para o vault" que ela abriu.

## Assumido (não confirmado)
- Que o estado de abril de 2026 é o último que existe. Se houve atualização
  fora do Notion, ela não foi vista.
- Que o módulo M5 do curso de UI e UX está vazio como os outros seis. Não foi
  conferido, por limite de uso do conector.
- Que a pasta local "DP Projetos" ainda existe e contém os arquivos citados.

## Contradições encontradas e não resolvidas
Nenhuma destas foi decidida pelo Claude. Todas viraram pendência.

1. **Working day, quinta ou sexta.** A entrevista da fase 1 diz quinta; o
   Notion, em 01/04/2026, diz sexta. Pendência em [[FIA Júnior]].
2. **Duas versões divergentes dos OKRs do Q2**, em quatro dos nove KRs, entre o
   database de tracking e a página de texto do PE2026. Pendência em
   [[Executar o PE2026 da Diretoria de Projetos]].
3. **Início do PE2026.** A página diz dezembro de 2025; o database de projetos
   diz 15/01/2026.

## Candidatos a tema, listados e não criados
Pela seção 6 das regras, candidato aparece na revisão semanal sem virar nota.

- **Gestão do conhecimento:** aparece no Peter Pan, neste vault e no Mapa de
  Conhecimento da diretoria.
- **Gestão de pessoas:** aparece no PDI e na avaliação de desempenho.

## Ver também
- [[Decisão — Vault, Notion e memória do Claude]]
- [[Decisão — GitHub e sigilo]]
- [[FIA Júnior]]

---
## Timeline
- **2026-10-15** | inventário do Notion — workspace mapeado inteiro, somente leitura
- **2026-10-15** | conversa com o Claude — decisão tomada e migração executada em três grupos
