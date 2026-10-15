---
type: decision
status: perene
sigilo: normal
created: 2026-10-15
updated: 2026-10-15
tags: [setup, sigilo]
---
# Decisão — GitHub e sigilo

**Decidido em:** 2026-10-07, confirmado em 2026-10-15
**Quem aprovou:** Neto

## O que foi decidido
- O vault inteiro sobe para um repositório privado no GitHub, exceto as notas com `sigilo: alto`.
- Conteúdo de cliente da FIA Júnior nasce `sigilo: alto`: nota e transcrição de reunião com cliente, dado, número, documento e qualquer informação não pública. Fica no vault e aparece no grafo, fica fora do GitHub e não é copiado para outra conversa.
- Conhecimento gerado pelo Neto entra `sigilo: normal`: método, framework, lição aprendida, decisão de gestão, skill, reflexão sobre a própria atuação. Antes de marcar normal, aplicar o teste do portfólio: se esta nota aparecesse num portfólio público, algum cliente seria exposto? Se sim, sanitizar (o nome do cliente vira uma descrição genérica, número vira ordem de grandeza ou sai) ou marcar alto. Na dúvida, `sigilo: alto` com a linha `❓ dúvida: sanitizar ou manter alto?`.
- Pessoas entram no vault e sobem para o GitHub. De ninguém, inclusive do Neto, se guarda senha, chave de acesso, documento, número de conta, dado de saúde ou de finanças.
- Valor exato continua na planilha ou no sistema onde já mora. A nota aponta para lá.
- O mecanismo que impede o envio de nota `sigilo: alto` é escolhido na fase 2. O `.gitignore` filtra por nome e caminho e não lê cabeçalho.

## Por quê
O GitHub privado é o cofre de versões: histórico de tudo, qualquer erro pode ser desfeito e existe cópia fora do computador. Conteúdo de cliente não é do Neto, então não sai do computador dele.

## Base
Decisão do Neto em 2026-10-07, confirmada em 2026-10-15. A FIA Júnior tem termo de confidencialidade que, segundo o Neto, veda divulgação a terceiros e não veda cópia local para o próprio trabalho.

## Assumido (não confirmado)
- O conteúdo do termo. Veio da lembrança do Neto, não do texto.

## Pendências
- ❓ dúvida: confirmar no texto do termo que a cópia local é permitida. Se o termo for mais restritivo, esta decisão se ajusta ao termo, não o contrário.

---
## Timeline
- **2026-10-07** | decisão do Neto — sigilo definido
- **2026-10-15** | conversa com o Claude — confirmado e registrado
