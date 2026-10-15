---
type: skill
status: perene
sigilo: normal
created: 2026-10-15
updated: 2026-10-15
tags: [avaliacao, pessoas]
---
# Avaliar desempenho de membro

**Resumo:** conduz a avaliação de desempenho de um membro da Diretoria de
Projetos da [[FIA Júnior]], em dois ciclos, com seis dimensões e escala de 1 a
5. O método veio do Notion; o registro passa a morar no vault.

## Gatilho
Última semana de cada mês, para o ciclo mensal. Junho e dezembro, para o ciclo
semestral. Também quando o Neto diz "avaliar o time" ou prepara um 1:1.

## Entradas
- Nome do membro, o período de referência e o ciclo.
- Quem avalia. O método prevê quatro vozes: Diretor, Coordenador,
  Autoavaliação e Par.
- As entregas do membro no período, que não estão nesta nota: vêm do projeto.

## Passo a passo
1. Escolher o ciclo.
   - **Mensal:** pulso rápido, feito pelo Diretor, pelo Coordenador e pelo
     próprio membro ao fim do mês. Foco em entrega e comportamento recentes.
   - **Semestral:** 360° completa, com as quatro vozes. Foco em
     desenvolvimento, padrão ao longo do tempo e próximos passos.
2. Pontuar as seis dimensões, cada uma de 1 a 5:
   1. Qualidade técnica das entregas
   2. Cumprimento de prazos
   3. Comunicação e proatividade
   4. Trabalho em equipe
   5. Iniciação e aprendizado contínuo
   6. Alinhamento com a cultura da FIA JR
3. Ler a escala sempre pelo significado, nunca pelo número solto:

   | Nota | Significado |
   |---|---|
   | 1 | Abaixo do esperado |
   | 2 | Em desenvolvimento |
   | 3 | Atende ao esperado |
   | 4 | Acima do esperado |
   | 5 | Referência no time |

4. Escrever, em texto, os quatro campos que o número não carrega: pontos
   fortes, pontos de melhoria, plano de ação e período de referência.
5. Separar fato de julgamento na hora de gravar, como manda a seção 10 das
   regras do vault:
   - A ocorrência da avaliação, quem avaliou, quando e em que ciclo é fato:
     `sigilo: normal`.
   - As notas, os pontos de melhoria e qualquer leitura sobre maturidade ou
     limitação da pessoa avaliam uma pessoa: vão para nota própria com
     `sigilo: alto`, ligada por link.
6. Não escrever na nota da pessoa por conta própria. A avaliação propõe; o Neto
   aprova pelo [[Arrumador]].
7. Marcar o status: pendente, em andamento ou concluída.

## Conferências
O Neto confere se a nota de cada dimensão tem um fato por trás, não uma
impressão. Número sem origem é anti-regra do vault. A skill nunca decide a nota
sozinha, e nunca escreve avaliação sem o Neto ter dito a nota.

## Armadilhas
- No Notion, a estrutura existia e **nenhuma avaliação foi preenchida**: o
  database tem 16 propriedades, 5 visões e zero linhas, entre 28/03/2026 e hoje.
  A armadilha comprovada aqui é montar o instrumento e não rodar o ciclo. Isso é
  a "camada 2" do próprio diagnóstico da diretoria, consistência interrompida.
- Misturar a nota numérica com a justificativa na mesma nota `sigilo: normal`
  expõe julgamento sobre pessoa no que sobe para o GitHub.

## Exemplo real
- Não consta. Nenhuma avaliação foi registrada no Notion.

## Fonte
- Página `📊 Sistema de Avaliação de Desempenho — Diretoria de Projetos` do
  Notion, lida em 2026-10-15:
  https://app.notion.com/p/33198a1c4766811c8320ca304063d721
  Última edição da fonte: 2026-03-28.

## Assumido (não confirmado)
- Que o método ainda é o que vale. A fonte é de março de 2026 e o que mudou
  desde então não consta.
- Que "Coordenador" é um papel diferente do de Diretor dentro da diretoria. O
  Notion usa os dois termos sem definir a diferença.
- O desenho do passo 5, que separa fato de julgamento, é aplicação da regra do
  vault e não estava no Notion.

---
## Timeline
- **2026-03-28** | Notion — método criado na página do sistema de avaliação
- **2026-10-15** | migração do Notion — skill escrita a partir da página de origem
