---
type: meta
status: ativo
sigilo: normal
created: 2026-10-15
updated: 2026-10-15
tags: [setup]
---
# Andamento do setup

**Fase atual:** fase 3 concluída em 2026-10-15. Próxima: fase 4, contexto de reuniões.

Leia este arquivo antes de tudo no começo de cada sessão nova.

## Ambiente confirmado
- Windows 11 Home, 64 bits, usuário `gneto`.
- Vault em `C:\Users\gneto\Obsidian\Neto Brain`, Obsidian 1.14.4. Antes desta sessão continha apenas `.obsidian`.
- A pasta Documentos do Neto está no OneDrive. O vault fica fora dela e nunca entra em OneDrive, iCloud, Google Drive ou Dropbox.
- Git 2.53.0.windows.2. `user.name` e `user.email` globais configurados em 2026-10-15 como Graciano Neto e gnetosouza2009@gmail.com.
- Kit de referência do Heitor em `C:\Users\gneto\Downloads\kit-second-brain-helio`, com LEIA-ME e 13 arquivos em agentes, regras, rotinas e skills. Somente leitura, nunca escrito.
- Aparelhos: só o notebook. Sincronização com celular desligada por ora (fase 2, opção "só no computador").

## Conectores vistos nesta sessão (2026-10-15)
- Google Calendar: conta gnetosouza2009@gmail.com. Enxerga também fiajrconsultoria22@gmail.com e os calendários "Reunião Geral" e "Eventos EJ".
- Google Drive: mesma conta. Arquivos recentes de um projeto ABRAEC.
- Conector de reuniões e transcrições (Wispr Flow): ativo, identifica o Neto como "Graciano Neto". Candidato a fonte na fase 4.
- Também ativos: Notion, Gmail, ClickUp, Canva, Figma.
- GitHub e Slack exigem autorização e não estão disponíveis. O GitHub da fase 2 usa o `git` de linha de comando, então não depende disso.
- Memória da conta do Claude: vazia sobre o Neto no início desta sessão.

## Onde o conhecimento mora hoje
Notion, Google Drive, memória e skills do Claude, e arquivos soltos no PC. O Notion opera hoje tarefa com prazo, bases da FIA Júnior, notas de estudo e conhecimento e método.

## Fase 2: ambiente de versionamento (2026-10-15)
- Sincronização: nenhuma. Só notebook, por decisão do bloco 0. Reabrir se o Neto quiser o celular, confirmando preço e recursos no site do Obsidian na hora.
- Git local: repositório na pasta do vault, branch `main`, `core.quotepath false` para nome com acento aparecer legível.
- Permissões em `.claude/settings.json`, com sintaxe conferida em code.claude.com/docs/en/permissions: `ask` antes de `git push`, de remoção de arquivo (`rm`, `rmdir`, `Remove-Item`, `Clear-Content`, `find -delete`), de `git clean`, `git reset --hard` e `git rebase`, em Bash e PowerShell. `deny` em force push, apagar branch e `filter-branch`. Limite conhecido e documentado: regra de Bash compara texto, então `/bin/rm` ou `bash -c 'rm ...'` escapam. É rede de segurança, não parede; a garantia são as regras do `CLAUDE.md` e o histórico do git.
- Mecanismo de sigilo escolhido: hook de pre-commit. Fica em `.githooks/pre-commit`, apontado por `core.hooksPath .githooks`, então sobrevive a um clone. Ele lê o cabeçalho de cada nota que está no index e bloqueia o commit se achar `sigilo: alto`. Testado em 2026-10-15 nos dois sentidos: bloqueou com a nota de sigilo no stage e liberou sem ela.
- Corpo de prova: `_meta/Teste de sigilo.md`, ignorado no `.gitignore` para não travar commit de rotina. Para retestar o hook: `git add -f "_meta/Teste de sigilo.md"` e rodar `bash .githooks/pre-commit`.
- Fora do GitHub pelo `.gitignore`: `_meta/setup/` (entrevista bruta), `.obsidian/workspace*`, `.claude/settings.local.json`, nomes com `(sigilo)` e o corpo de prova.
- Remoto: `https://github.com/GracianoNeto-cmd/neto-brain.git`, privado e vazio na criação.
- Primeiro commit: `4b9d899`, 10 arquivos, enviado em 2026-10-15.

## Fase 3: arquitetura (2026-10-15)
- Estrutura de pastas criada conforme o teste de decisão, com `Reuniões/` em FIA Júnior e `Matérias/` em Faculdade. Nota de área mora em `2. Áreas/<Área>.md`, e a pasta existe ao lado só para subconteúdo.
- Raiz: `CLAUDE.md` (contrato do agente, 72 linhas, importa as regras por `@_meta/REGRAS-DO-VAULT.md`), `CONTEXTO.md` (resumo aprovado da entrevista, arquivo do Neto) e `INICIO.md` (porta de entrada, com a tabela de gatilhos marcando o que já existe).
- `_meta/REGRAS-DO-VAULT.md`: regras de nota, adaptadas das do Heitor. Sem Dataview, porque o plugin não está instalado. Com seções de sigilo e de decisão de alocação, que são do Neto e não existem no vault dele.
- Cinco áreas criadas: FIA Júnior, Faculdade, Carreira, Interesses, Saúde e treino.
- Seis modelos em `_meta/modelos/`: Reunião, Decisão, Pessoa, Skill, Tema e Captura.
- Cinco pessoas e um círculo: André Lima, Sophie Yumi, Diego Coelho, Edson Ito, Samantha e FIA Business School.
- Arrumador em três peças: `_meta/Arrumador.md` (especificação editável no Obsidian), `.claude/agents/arrumador.md` (ponteiro, sem modelo declarado) e `_meta/Log-do-Arrumador.md` (tabela vazia).
- Skill "Encerrar sessão" em `3. Recursos/Skills/`, com as quatro respostas mais Candidato a skill e Atualizações por pessoa, por escolha do Neto.
- Grafo configurado com o Neto: filtro `-path:"_meta" -path:"0. Inbox"`, cinco grupos de cor por frente usando `[area:...] OR path:"..."`, e órfãos ligados. Resultado conferido na tela: 16 nós.

## Fatos verificados em 2026-10-15
- O plugin Sync do Obsidian está habilitado, mas pede login: não existe cofre remoto conectado. Nenhuma nota sai do computador por esse caminho. Reconferir se o Neto um dia assinar o Sync.
- Existe `Sem título.canvas` na raiz, vazio, criado pelo Neto em 2026-10-15 às 14:44. O Claude não toca nele.

## Onde está o backup
1. Sincronização: nenhuma, por escolha. Não existe cópia em nuvem de arquivos.
2. GitHub privado `GracianoNeto-cmd/neto-brain`: tudo menos nota com `sigilo: alto` e `_meta/setup/`. É a única cópia fora do computador.
3. Cópia local: a própria pasta do vault, mais o histórico do git em `.git`.

Antes de qualquer operação em lote no futuro, o Claude pergunta se existe backup recente.

## Regras de git para o Claude
- Nunca forçar envio, nunca reescrever histórico, nunca apagar repositório ou branch.
- Antes de cada envio, dizer em uma frase o que vai subir e esperar o "pode".
- Nunca subir nota com `sigilo: alto`.

## Regras combinadas durante a fase 1
- Amigos e família entram como nó mínimo e nascem `sigilo: alto`: nome como o Neto chama, vínculo em uma linha, e Timeline só com evento que envolve o Neto. Nada sobre a vida deles, nenhum dado pessoal. Não sobem para o GitHub. Decidido em 2026-10-15, bloco 2.
- Regra de saturação para tema, proposta pelo Neto: duas ocorrências em frentes diferentes fazem um candidato, que aparece listado na revisão semanal sem virar nota. Três ou mais ocorrências em pelo menos duas frentes diferentes fazem o Claude propor a nota de tema, com ocorrências e fontes. O Claude nunca cria tema sozinho. Revisar o número 3 depois de quatro semanas.
- Decisão de alocação de membro em projeto separa fato de julgamento: quem foi alocado onde, quando e o critério objetivo ficam `sigilo: normal`; a justificativa que avalia desempenho, maturidade ou limitação de uma pessoa vai para nota própria com `sigilo: alto`, ligada por link. Decidido em 2026-10-15, bloco 5.
- Voz do Neto: cinco regras dele valem mais que as amostras, e estão na íntegra em `_meta/setup/Entrevista bruta.md`, bloco 5. Sem travessão em texto corrido; `—` só em nome de arquivo e linha de Timeline. Criar e editar nota são livres; enviar para o GitHub pede ok toda vez.
- Informação sensível: vale a lista da fase 0 (senha, chave, documento, número de conta, saúde, finanças, de ninguém). Fora dela, o Claude para e pergunta antes de gravar. Decidido em 2026-10-15, bloco 6.
- Grafo: cores por frente. Leitura toda semana, dentro da revisão semanal. O Neto quer ver pessoas que ligam frentes, temas que se repetem, frentes isoladas e lugares onde investe tempo sem retorno. Decidido em 2026-10-15, bloco 7.

## Decisões tomadas
- [[Decisão — Vault, Notion e memória do Claude]]
- [[Decisão — GitHub e sigilo]]

## Pendências abertas
- Conteúdo da FIA Júnior que hoje vive na memória da conta do Claude e no ClickUp precisa vir para o vault (fase 4c). O Claude não lê a memória da conta daqui, então vai depender de exportação ou cópia pelo Neto.
- ❓ Confirmar no texto do termo de confidencialidade da FIA Júnior que a cópia local é permitida. Até então, conteúdo de cliente segue a regra mais restritiva.
- Migração do conteúdo do Notion para o vault: tarefa própria, depois da fase 3.
- Sincronização com o celular: reabrir se o Neto quiser o celular.
- Perguntar, depois do `CONTEXTO.md` aprovado na fase 3, se a entrevista bruta continua em `_meta/setup/` ou vai para `5. Arquivo/`. Em qualquer caso continua fora do GitHub.
- Definir na fase 4 o critério operacional de "reunião importante", que hoje é circular.
- Decidir se transcrição automática de reunião de cliente é viável, dado que exige avisar os participantes e existe termo de confidencialidade.
- Fase 3: decidir se decisão de vida fica na área correspondente, e não em `_meta/Decisões/`.
- Projetos ativos: o Neto ainda não informou quais são. `1. Projetos/` está vazia.
- TCC: candidato a projeto, sem data de início.
- ABRAEC: hipótese vinda do Drive, não confirmada pelo Neto. Se for projeto de cliente da FIA Júnior, nasce `sigilo: alto`.
- Criar as notas de matéria do semestre, que é onde os professores entram no grafo.
- Decidir o que fazer com `Sem título.canvas`.

## Fases
- Fase 0, ambiente, limites e sigilo: concluída em 2026-10-15.
- Fase 1, entrevista: concluída em 2026-10-15. Sete blocos respondidos, crus em `_meta/setup/Entrevista bruta.md`. O resumo de uma página foi aprovado pelo Neto sem correções e vira o `CONTEXTO.md` na fase 3.
- Fase 2, ambiente de versionamento: concluída em 2026-10-15.
- Fase 3, arquitetura: concluída em 2026-10-15.
- Fase 4, contexto de reuniões: próxima. Depende de resolver a falta de fonte: hoje nenhuma reunião do Neto gera transcrição.
- Fases 4b a 8: não iniciadas.

---
## Timeline
- **2026-10-15** | conversa com o Claude — fase 0 concluída, git configurado, duas decisões registradas
- **2026-10-15** | conversa com o Claude — fase 1 concluída, sete blocos de entrevista gravados e resumo aprovado
- **2026-10-15** | conversa com o Claude — fase 2 concluída, permissões, hook de sigilo, gitignore e primeiro envio ao GitHub
- **2026-10-15** | conversa com o Claude — fase 3 concluída, arquitetura criada e grafo configurado com 16 nós
