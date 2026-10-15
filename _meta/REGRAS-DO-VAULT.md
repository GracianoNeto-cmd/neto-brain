---
type: meta
status: ativo
sigilo: normal
created: 2026-10-15
updated: 2026-10-15
tags: [meta]
---
# Regras do vault

**Regra-mãe:** pasta diz **onde a nota mora**, cabeçalho diz **o que a nota é**,
tag diz **sobre o que ela fala**, link diz **com quem ela conversa**. Nunca use
dois desses para dizer a mesma coisa.

## 1. Estrutura

    _meta/          regras, modelos, log do Arrumador, anexos
    0. Inbox/       tudo que chega cru
      Capturas/     saída do "Encerrar sessão", fila do Arrumador
    1. Projetos/    tem prazo e resultado, então um dia termina
    2. Áreas/       responsabilidade contínua, nunca termina
      <Área>/Reuniões/   reuniões daquela área
    3. Recursos/    material de consulta
      Skills/       passo a passo reutilizável (type: skill)
      Temas/        ideia que atravessa frentes (type: concept)
    4. Pessoas/     uma nota por pessoa
      Círculos/     organizações e grupos (type: organization)
    5. Arquivo/     projetos terminados e áreas encerradas

**Teste de decisão, nesta ordem:**
1. Tem prazo e entregável? `1. Projetos`
2. É responsabilidade sem fim? `2. Áreas`
3. É material de consulta? `3. Recursos`
4. É ideia que aparece em várias frentes? `3. Recursos/Temas` (ver seção 6)
5. É sobre uma pessoa? `4. Pessoas`
6. Não sei? `0. Inbox`, com uma linha de contexto, nunca só o título.

**Áreas do Neto:** FIA Júnior, Faculdade, Carreira, Interesses, Saúde e treino.
Amigos e família não formam área: moram em `4. Pessoas` como nó mínimo.

**A FIA Júnior existe só como área**, nunca também como círculo, para não ter
duas notas com o mesmo nome. `Círculos/` guarda organização pela qual o Neto
conhece pessoas e que não é responsabilidade dele, como a FIA Business School e
cada cliente.

**Toda entidade nasce como arquivo único.** Vira pasta só quando ganha conteúdo
que não tem outro lugar: a primeira reunião, o primeiro entregável. Nunca
antecipe subpasta.

**Máximo de três níveis de pasta.** Exceção única: um quarto nível para agrupar
arquivos do mesmo tipo, como `Reuniões/Transcrições`.

## 2. Cabeçalho

Toda nota nasce com cabeçalho. Sem exceção. Nomes dos campos em inglês, para o
GBrain ler sem adaptação na fase 8.

    ---
    type: meeting | person | organization | project | area | resource |
          decision | skill | concept | meta
    status: ativo | concluido | perene
    sigilo: normal | alto
    area: fia-junior | faculdade | carreira | interesses | saude
    aliases: [variação de nome, apelido, grafia errada]
    created: AAAA-MM-DD
    updated: AAAA-MM-DD
    tags: []
    ---

- `type`, `status`, `sigilo`, `created` e `updated` são obrigatórios.
- `area` só existe se a nota pertence a uma área.
- `aliases` existe em `person`, `organization`, `project`, `area` e `concept`.
- `status: perene` é nota de referência sem ciclo: recurso, pessoa, skill, tema.
- `type: meeting` exige `event_date: AAAA-MM-DD`. Se a nota nasceu de convite de
  agenda, exige também `calendar_event_id`, que é o que impede nota duplicada.

## 3. Nomes de arquivo

| Tipo | Padrão | Exemplo |
|---|---|---|
| Reunião | `AAAA-MM-DD — Assunto` | `2026-10-16 — Diretoria` |
| Decisão | `Decisão — Objeto` | `Decisão — Skills` |
| Pessoa | Nome como o Neto chama | `Diego Coelho` |
| Organização | Nome como o Neto chama | `FIA Business School` |
| Projeto | Verbo + objeto | `Entregar diagnóstico do cliente X` |
| Área | Substantivo | `Carreira` |
| Skill | Verbo + objeto | `Montar proposta comercial` |
| Tema | Substantivo | `Gestão de pessoas` |
| Matéria | `Aula de {Matéria}` | `Aula de Logística` |

- Nunca `v2`, `final`, `novo`. Se mudou, edite e atualize `updated`.
- Data sempre `AAAA-MM-DD`.
- Português correto, com acento.
- Nota de matéria abre com a frase fixa, na linha abaixo do H1:
  `Matéria da [[FIA Business School]] ministrada pelo professor [[Nome]].`
  Os dois links são obrigatórios. Se a nota do professor não existe, crie o
  esboço em `4. Pessoas`. A frase idêntica permite achar todas as matérias.

## 4. Tags

- Máximo 4 por nota. Se precisa de mais, a nota está fazendo duas coisas.
- Nunca com o nome de uma pasta.
- Tudo minúsculo, singular, sem acento.
- Status nunca vira tag: está no cabeçalho.
- Antes de criar tag, procure uma parecida, com e sem acento, singular e plural.
- Tema não é tag. Tema é nota.
- Sinalizadores, vocabulário fechado e transversal: `#ideia`, `#pergunta`,
  `#decisao`, `#risco`, `#permanente`. `#permanente` marca conhecimento
  destilado do Neto, não cópia de fonte externa.

## 5. Links de fato

`[[Nome]]` para relação concreta e verificável na fonte: pessoa que estava na
reunião, decisão tomada na reunião, projeto que pertence a uma área, skill usada
num projeto. Livre, sempre que a relação estiver na fonte.

Link para nota que não existe é dívida: na revisão semanal, ou cria a nota ou
tira o colchete.

## 6. Links de tema

Liga uma nota a uma nota de `3. Recursos/Temas/`. Regra de nascimento:

1. Uma ocorrência: não é nada. Fica como observação.
2. Duas ocorrências em frentes diferentes, cada uma com nota de origem:
   candidato. Aparece listado na revisão semanal, sem virar nota.
3. Três ou mais ocorrências em pelo menos duas frentes diferentes: o Claude
   propõe a nota de tema, com as ocorrências e as fontes na mesa.

O Claude nunca cria nota de tema sozinho. Frentes diferentes quer dizer duas
áreas, ou projetos de áreas diferentes.

**Nunca crie link de tema para enriquecer o grafo.** O grafo mostra os links que
foram escritos, então link inventado polui exatamente a leitura que o Neto quer
fazer. Link faltando é menos grave que link inventado.

Formato da nota de tema: Resumo em uma frase; "Onde aparece", uma linha por
frente com link para a nota de origem e o que ela diz; "Tensões e perguntas
abertas"; linha `---`; `## Timeline`.

**Critério provisório:** depois de quatro semanas, revisar com o Neto se o número
3 está rígido demais (sinal: bons candidatos parados) ou frouxo demais (sinal:
tema com ligação forçada).

## 7. Dedupe

Antes de criar pessoa, organização, projeto, área ou tema, procure o nome e os
`aliases` existentes. Achou, acrescente o apelido novo na nota que já existe.
Nunca crie uma segunda.

## 8. Página viva

Pessoa, organização, projeto, área e tema seguem o mesmo corte. Acima da linha é
reescrito quando chega informação nova. Abaixo da linha só cresce.

    # Nome

    **Resumo:** uma frase com o estado atual.

    ## Estado
    - Fato confirmado, com fonte quando houver.

    ## Assumido (não confirmado)
    - Inferência do Claude, nunca misturada ao Estado.

    ## Pendências
    - [ ] O que falta fazer. Sai da lista quando resolve, e o que foi decidido
          desce para a Timeline.

    ## Ver também
    - [[nota relacionada]]

    ---
    ## Timeline
    - **AAAA-MM-DD** | fonte — evento

**Estado e Assumido nunca se misturam.** Um é fato, o outro é incerteza. E
Assumido não é Pendência: Assumido é o que o Claude não confirmou, Pendência é
trabalho que falta.

**A linha de Timeline tem formato fixo, não estético:**
`- **AAAA-MM-DD** | fonte — evento`. A data em negrito e o `|` são o que o
parser do GBrain reconhece na fase 8. Sem isso, a linha existe no Obsidian e o
GBrain não a lê como evento.

## 9. Pessoa e organização

Pessoa (`4. Pessoas`), campos obrigatórios no Estado:
- **Vínculo:** como o Neto se relaciona com ela hoje.
- **Conheci via:** pessoa ou organização, sempre como link. Se não lembra,
  escreva `desconhecido`, nunca deixe em branco.

Organização (`4. Pessoas/Círculos`), campos obrigatórios no Estado:
- **Tipo:** empresa, escola, cliente, grupo.
- **Meu vínculo:** como o Neto se relaciona com ela hoje.
- Seção **Pessoas**, com link para quem ele conhece ali.

Amigo e familiar entram como nó mínimo e nascem `sigilo: alto`: nome, vínculo em
uma linha, e Timeline só com evento que envolve o Neto. Nada sobre a vida deles.

**O Claude não escreve em nota de pessoa por conta própria.** Ele propõe, e o
Neto aprova pelo Arrumador. "Atualizações por pessoa" fica dentro da nota da
reunião até ser aprovada.

## 10. Decisões

Decisão que fecha porta, reverte algo ou corrige premissa vira nota
`Decisão — Objeto`, com: o que foi decidido, por quê, base, quem aprovou, o que
foi descartado e o que revoga.

Decisão de alocação de membro separa fato de julgamento: quem foi alocado onde,
quando e o critério objetivo ficam `sigilo: normal`; a justificativa que avalia
desempenho, maturidade ou limitação de uma pessoa vai para nota própria com
`sigilo: alto`, ligada por link.

## 11. Ciclo de vida

- `0. Inbox` é temporário. Nenhuma nota mora ali em definitivo.
- Quem esvazia é o Arrumador, especificado em `_meta/Arrumador.md`.
- Item que o Claude não sabe classificar fica na caixa com a linha
  `❓ dúvida: X ou Y?` no topo. Chute calado corrompe o vault sem ninguém ver.
- Toda decisão automática entra em `_meta/Log-do-Arrumador.md`: data, item,
  destino, motivo. É isso que torna a automação auditável e reversível.
- Arquivar é mover para `5. Arquivo/`, preservando a estrutura de origem. Nunca
  apagar.
- Uma vez por semana, a revisão procura o que apodreceu: link quebrado,
  pendência esquecida, dúvida parada, tag parecida, regra que contradiz outra.

## 12. Sigilo na prática

- Conteúdo de cliente nasce `sigilo: alto`. Isso inclui nota e transcrição de
  reunião com cliente, dado, número e documento.
- Conhecimento do Neto é `sigilo: normal` depois do teste do portfólio: se esta
  nota aparecesse num portfólio público, algum cliente seria exposto? Se sim,
  sanitize (o nome do cliente vira uma descrição genérica como "cliente do setor
  de logística"; número vira ordem de grandeza ou sai) ou marque alto.
- Quem impede o envio é o hook `.githooks/pre-commit`, que lê este cabeçalho. A
  marca no cabeçalho não é decoração: é o mecanismo.

## 13. Anti-regras

- Nota sem cabeçalho.
- Pasta criada "para organizar depois".
- Anexo solto fora de `_meta/anexos`.
- Cópia de documento inteiro sem uma linha de "por que isto importa".
- Link de tema sem duas ocorrências com fonte.
- Tarefa com prazo vivendo só no vault.
- Número sem origem.

## 14. Evolução das regras

**Quem altera:** o Neto, a qualquer momento. O Claude, quando os quatro testes
passarem:
1. **Caso real.** Surgiu de um registro concreto que as regras atuais não
   resolvem. Nunca por hipótese.
2. **Sem sinônimo.** Nenhuma regra existente já cobre o caso.
3. **Sem conflito.** Não contradiz a regra-mãe nem as anti-regras.
4. **Sem destruição.** Não apaga nem move nota existente.

Como registrar: edite a seção afetada antes de usar a regra, acrescente uma linha
no changelog, atualize o `updated` e avise o Neto em uma linha na mesma resposta.

### Changelog das regras

| Data | Mudança | Motivo | Por |
|---|---|---|---|
| 2026-10-15 | Versão inicial, adaptada das regras do vault do Heitor | Fase 3 da construção | Pedido do Neto |
