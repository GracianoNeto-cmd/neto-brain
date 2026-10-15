---
type: skill
status: perene
sigilo: normal
created: 2026-10-15
updated: 2026-10-15
tags: []
---
# Encerrar sessão

**Resumo:** ao fim de uma conversa que gerou decisão, aprendizado ou tarefa
nova, escreve uma captura em `0. Inbox/Capturas/` com quatro respostas, mais
duas seções quando houver conteúdo para elas. Conversa sem nada disso não gera
nota.

## Gatilho
Quando o Neto diz "encerra" ou "salva o que aprendemos", e ao fim de uma sessão
longa de trabalho.

## Entradas
A própria conversa. Nada mais.

## Passo a passo
1. Decidir se cabe nota: houve decisão, aprendizado ou tarefa nova? Se não
   houve, não escreva nada e diga em uma linha que não havia o que salvar.
2. Escrever em `0. Inbox/Capturas/AAAA-MM-DD — Assunto.md`, usando
   `_meta/modelos/Captura.md`.
3. Responder as quatro perguntas: o que foi pedido; o que foi produzido e onde
   está; o que o Neto corrigiu; o que ficou em aberto.
4. Acrescentar, só quando houver conteúdo de verdade:
   - **Candidato a skill:** processo que se repete e vai ser feito de novo, com
     gatilho e ação.
   - **Atualizações por pessoa:** fato ou decisão que pertence à Timeline de
     alguém. A captura só propõe; quem aplica é o [[Arrumador]], com o ok do
     Neto.
   Seção sem conteúdo é omitida inteira. Título vazio é ruído.
5. Não decidir destino final. A captura nasce em `Capturas/` e o [[Arrumador]]
   roteia depois, com o ok do Neto.
6. Nunca inventar. Inferência vai em "Assumido (não confirmado)", nunca
   misturada ao que foi de fato decidido.

## Conferências
O Neto confere se "o que o Neto corrigiu" está fiel. É a parte que mais ensina,
porque é ali que aparece o erro que eu repeti.

## Armadilhas
- Nada deu errado aqui ainda: a skill é nova. A armadilha herdada do vault do
  Heitor é decidir o destino final na hora da captura, o que trava a escrita.
  Por isso a captura não escolhe pasta.
- Escrever captura de conversa que não produziu nada enche a caixa de entrada de
  ruído e faz o Arrumador trabalhar de graça.
- Aplicar "Atualizações por pessoa" direto na nota da pessoa, sem passar pelo
  Neto, quebra a regra de que o Claude não escreve em nota de pessoa por conta
  própria.

## Exemplo real
- A captura desta própria construção, quando for escrita no fim da sessão.

## Assumido (não confirmado)
- Nada.

---
## Timeline
- **2026-10-15** | fase 3 da construção — skill criada, adaptada de "Salvar
  Conhecimento de Projeto" do vault do Heitor
