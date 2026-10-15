---
type: project
status: ativo
sigilo: normal
area: fia-junior
aliases: [Peter Pan, Projeto Peter Pan, MVP Interno]
created: 2026-10-15
updated: 2026-10-15
tags: [ia, conhecimento]
---
# Entregar o MVP do Peter Pan

**Resumo:** sistema de gestão do conhecimento institucional da [[FIA Júnior]]
baseado em IA, que permite a qualquer membro consultar o histórico da EJ em
linguagem natural por um bot no Telegram. Tudo abaixo é retrato do Notion em
01/04/2026, quando o projeto estava com 8% de progresso. O que aconteceu nos
seis meses seguintes não consta.

## Estado
Retrato em 2026-04-01, segundo o Notion.

- Codename: Peter Pan. Tipo: projeto interno. Prioridade: P0, crítica.
- Início em 07/04/2026, entrega prevista em 30/06/2026. Treze semanas.
- Progresso registrado: 8%. A conta por trás desse número não consta na fonte.
- Papel do Neto: coordenador e co-tech lead.

### Objetivo do MVP
Provar que membro recupera conhecimento institucional em linguagem natural, sem
precisar perguntar para ninguém. Dois casos de uso prioritários:

1. Histórico de cliente: quem foi atendido, o que foi entregue, como foi.
2. Como a EJ funciona por dentro: processo, ritual, onboarding.

### Stack técnico
| Camada | Escolha |
|---|---|
| LLM | GPT-4o-mini, da OpenAI |
| Embeddings | OpenAI Embeddings |
| Vector store | FAISS, local |
| Orquestração | LangChain |
| Interface | Telegram Bot API, com python-telegram-bot |
| Hospedagem | Railway, free tier |
| Custo | cerca de R$ 20 por mês, só a API da OpenAI |

### Time
Por papel. O Notion não nomeia ninguém.

| Papel | Quem |
|---|---|
| Coordenador e co-tech lead | Neto |
| Tech lead principal | Especialista técnica |
| Dev de suporte e sucessor técnico | Analista sênior 1 do DP |
| QA, documentação e teste | Analista sênior 2 do DP |
| Fichas de cliente | Analista júnior do Comercial |
| Comunicação interna | VP e analista júnior de MKT |
| Docs de onboarding e processo | Diretora de G&G e analista sênior de G&G |
| Beta testers | Trainees, em número de 15 |
| Advisory técnico quinzenal | Professor |

### Cronograma de treze semanas
| Fase | Período | Entregável |
|---|---|---|
| Semanas 1 e 2 | 1ª quinzena de abril | Setup técnico: pipeline RAG e bot no Telegram |
| Semanas 3 e 4 | 2ª quinzena de abril | Base de conhecimento mínima, de 10 a 15 docs |
| Semanas 5 e 6 | 1ª quinzena de maio | Teste interno com o DP |
| Semanas 7 e 8 | 2ª quinzena de maio | Teste com trainees e material de comunicação |
| Semanas 9 e 10 | 1ª quinzena de junho | Rollout geral interno |
| Semanas 11 a 13 | 2ª quinzena de junho | Fechamento, métricas, documentação, decisão de continuidade |

**Marco go ou no-go, semana 6:** bot funcionando com base mínima respondendo três
perguntas-teste. Se não atingido, escopo reduzido ou prazo estendido.

### Riscos registrados
Cinco riscos, com o nível que a fonte deu. Nenhum avalia uma pessoa: todos são
estruturais.

| # | Risco | Nível |
|---|---|---|
| 1 | Dependência de uma única pessoa no papel de tech lead | alto |
| 2 | Ausência de adoção cultural pelos membros | alto |
| 3 | Qualidade insuficiente dos documentos indexados | médio |
| 4 | Sobrecarga do Neto, que é coordenador e tech lead ao mesmo tempo | médio |
| 5 | Prazo de treze semanas não cumprido | médio |

### Métricas de sucesso
- Pelo menos 80% das perguntas respondidas com precisão, por avaliação humana.
- Pelo menos 70% dos membros usando o bot ao menos uma vez por semana depois do
  rollout.
- Coordenador e diretor respondendo 50% menos pergunta recorrente.
- NPS interno do bot de pelo menos 8 em 10.

### Próximas fases previstas, depois do MVP validado
- **MVP+:** controle de acesso por papel e integração automática com o Google Drive.
- **V2.0:** interface web administrativa.
- **Produto:** versão comercializável para outras EJs, validando demanda com
  cinco EJs antes.

## Assumido (não confirmado)
- Que o projeto ainda está de pé. O prazo era 30/06/2026 e hoje é 15/10/2026. Se
  entregou, se escorregou ou se morreu, não consta em lugar nenhum.
- Que o Neto continua coordenador e co-tech lead.
- Que "Professor", no advisory técnico quinzenal, é [[Diego Coelho]]. A fonte
  não dá nome.
- Que o risco 1 se refere à mesma pessoa que a página de Pessoas e PDI chama de
  "Especialista Técnica". Reescrevi o risco sem o cargo para não ligar nível de
  risco a uma pessoa identificável.

## Pendências
- [ ] Dizer o que de fato aconteceu com o projeto entre abril e outubro de 2026.
      Até isso, esta nota é história, não estado.
- [ ] Localizar `peter_pan_mvp_dp.docx`, com 14 seções e 560 parágrafos, citado
      na fonte como estando na pasta local "DP Projetos". É onde está o
      conteúdo de verdade.
- [ ] ❓ dúvida: sanitizar ou manter alto? Esta nota tem stack, custo, estrutura
      de time e matriz de risco interna da FIA Júnior. Nenhum cliente é
      exposto, então pelo teste do portfólio ela é `sigilo: normal`. Mas o
      texto do termo de confidencialidade ainda não foi conferido, e é ele que
      diz se informação interna da EJ pode sair do computador.
- [ ] Decidir o que fazer com a sobreposição entre este projeto e este vault.
      Os dois resolvem o mesmo problema, recuperar conhecimento em linguagem
      natural, um para a EJ e outro para o Neto.

## Ver também
- [[FIA Júnior]]
- [[Executar o PE2026 da Diretoria de Projetos]]
- [[Playbooks e processos da Diretoria de Projetos]]
- [[Decisão — Migração do Notion]]

## Fonte
- Página `🤖 Projeto Peter Pan — MVP Interno` do Notion, lida em 2026-10-15:
  https://app.notion.com/p/33298a1c476681a4a9b3d7b2bd908311
  Última edição da fonte: 2026-03-29.
- Linha `Peter Pan — MVP Interno` do database `📁 Projetos DP`, de onde vêm as
  datas, a prioridade e o progresso de 8%:
  https://app.notion.com/p/33598a1c476681da88dae44549fe727c

---
## Timeline
- **2026-03-29** | Notion — página do projeto escrita, com escopo, stack, time, cronograma e riscos
- **2026-04-01** | Notion — projeto registrado no database de Projetos DP com 8% de progresso
- **2026-10-15** | migração do Notion — projeto trazido para o vault como retrato de abril
