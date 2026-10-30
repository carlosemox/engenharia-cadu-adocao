# Guia de uso — trazer um projeto existente para a Engenharia Cadu

**Comece pelo entendimento. Revise o plano. Aplique somente os lotes aprovados.**

Este guia reúne os comandos de entrada e explica o resultado de cada fase. Os procedimentos completos continuam em [read.md](read.md), [aplicar.md](aplicar.md), [retomar.md](retomar.md) e [24h.md](24h.md); não há uma segunda cópia concorrente das regras.

Abra o **Codex na pasta do aplicativo existente** e cole os comandos **na conversa do agente, não diretamente no shell**. O alvo é o aplicativo, não esta biblioteca. O agente precisa de acesso autorizado aos arquivos; conversas, contas e histórico inacessíveis não podem ser reconstruídos por imaginação.

`Read` é linguagem natural, não um executável instalado. Os endereços com `main` facilitam o início; o agente deve resolver a revisão, registrar o SHA observado e consultar arquivos da mesma revisão durante a missão. Não modificar cliente, modelo, autenticação ou cobrança por consequência de ler um prompt.

## 1. Entender o projeto e apresentar o redesenho

Copie este comando para começar:

```text
Read https://raw.githubusercontent.com/carlosemox/engenharia-cadu-adocao/main/read.md

Quero trazer este projeto existente para a Engenharia Cadu.
Comece em ENTENDER_E_PROPOR.

Recupere o contexto acessível nos documentos, no código,
no histórico e nas evidências disponíveis, sem inventar
as decisões ou conversas que você não consegue consultar.

Apresente:
- o que este produto é, para quem serve e o que deve entregar;
- funcionalidades planejadas, encontradas e comprovadas;
- PRD e TRD reconciliados;
- fluxos atuais e propostos;
- arquitetura atual e proposta;
- mapa dos arquivos que serão mantidos, movidos ou adaptados;
- integrações, GitHub e desenho de adoção do Supabase;
- plano de reestruturação por lotes, com testes e recuperação;
- condições que faltam para uma futura missão de 24 horas.

Explique o resultado no chat e produza o Retrato do Projeto
em destino privado, quando houver acesso a arquivos.

Preserve meu trabalho. Não altere código, estrutura ou banco
antes de apresentar o plano e receber minha decisão.

Use Codex como principal e aplique a política de economia
no Astra, sem trocar modelo, provedor ou cobrança silenciosamente.
```

### O que deve aparecer antes de qualquer reestruturação

| Entrega | O que precisa ficar compreensível |
|---|---|
| **Retrato executivo** | Que produto é este, quem utiliza, qual problema resolve e qual é a primeira entrega útil. |
| **Planejado × encontrado × comprovado** | Funcionalidades pretendidas, camadas existentes, testes efetivos, falhas e lacunas. |
| **PRD e TRD reconciliados** | Regras e decisões preservadas, divergências e hipóteses ainda não confirmadas. |
| **Fluxos atuais e propostos** | Jornadas, permissões, exceções, estados e dependências. |
| **Arquitetura e arquivos** | O que manter, mover, adaptar ou criar; motivos, consumidores, testes e recuperação. |
| **Dados e integrações** | Situação atual, desenho Supabase, serviços externos, custos pendentes e alçadas. |
| **Plano por lotes** | Ordem de execução, entregas, limites, riscos, critérios de aceite e recuperação. |
| **Decisões do responsável** | O que pode ser corrigido, aprovado, ajustado, adiado ou recusado. |

O agente deve explicar no chat: **“Este projeto é…; foi pensado para…; encontrei…; comprovei…; falta…; preservaremos…; proponho mudar…”**. Não basta entregar caminhos de arquivos ou uma árvore técnica sem contexto de negócio.

Uma tela existente não comprova persistência, autorização ou jornada completa. Não inventar percentual de conclusão. Documentos e código contraditórios devem ser apresentados como conflito, não corrigidos silenciosamente por suposição.

A primeira execução termina em **AGUARDANDO_REVISAO_DO_PROJETO**. O material detalhado pode utilizar o [Retrato do Projeto](templates/RETRATO_DO_PROJETO.md), o [mapa documental](templates/DOCUMENTOS_RECONCILIADOS.md) e o [template visual offline](templates/RELATORIO_VISUAL.html). Relatórios reais ficam privados, fora deste repositório público.

## 2. Revisar e aprovar o plano

Você pode corrigir o entendimento, mudar a prioridade, preservar um módulo, adiar uma integração ou aprovar lotes específicos. O plano deve ter identidade, versão e snapshot do aplicativo.

Exemplo de resposta, a preencher com os identificadores realmente apresentados:

```text
O entendimento do produto está correto, com estes ajustes:
[descreva somente os ajustes necessários].

Aprovo o plano [ID e versão] para o projeto [alvo],
restrito aos lotes [IDs dos lotes aprovados].

Mantenha as exclusões e os limites registrados no plano.
Não inclua migração remota, mudança de credenciais,
produção ou novos gastos sem autorização específica.
```

O exemplo não concede aprovação por existir. O [registro de decisão](templates/APROVACAO.md) deve refletir uma decisão real do responsável. Uma alteração material no aplicativo ou no plano exige reconciliar apenas os lotes afetados.

## 3. Aplicar a adoção aprovada

Depois de revisar e aprovar o plano, use:

```text
Read https://raw.githubusercontent.com/carlosemox/engenharia-cadu-adocao/main/aplicar.md

Aplique somente o plano identificado e os lotes que aprovei.

Preserve funcionalidades, dados, identidade, contratos
e alterações locais.

Execute as etapas autorizadas sem repetir confirmações
a cada arquivo. Apresente o antes/depois, os testes
e as pendências ao final de cada lote.

Não amplie o escopo nem altere produção, credenciais,
banco remoto ou gastos fora das autorizações registradas.
```

O procedimento cobre preservação e baseline, correção de bloqueios, documentação, organização de arquivos, dados e serviços, bootstrap incremental, GitHub/CI e revisão. Não aplica scaffold de produto novo sobre a aplicação existente.

O [guia Supabase](SUPABASE.md) separa modularização de migração: preservar dados, IDs, identidade e contratos; planejar transição quando necessária; exigir autorização específica antes de mudanças remotas. Estar no plano técnico não equivale a estar aprovado para execução.

**Resultado esperado:** lotes aplicados e comprovados no escopo autorizado, com mapa antes/depois e limitações. Estados possíveis: ADOTADO_NO_ESCOPO, PARCIAL ou BLOQUEADO. Adoção documental não comprova funcionamento integral nem supervisor instalado.

## 4. Retomar depois de uma interrupção

```text
Read https://raw.githubusercontent.com/carlosemox/engenharia-cadu-adocao/main/retomar.md

Retome a adoção deste projeto a partir do plano e do checkpoint
existentes, conferindo o estado real antes de continuar.

Mostre onde paramos, o que foi aplicado, as evidências ainda
válidas, o que falta e a próxima ação autorizada.

Preserve alterações locais e processos saudáveis.
Não duplique tarefas, migrações ou publicações.
```

A retomada confronta resumo, arquivos, revisão, recursos e efeitos externos. Resultado desconhecido de uma operação externa exige reconciliação antes de repetição. Fila vazia não prova falha. Sem ferramentas, a saída é documental, não continuidade simulada.

## 5. Preparar uma missão de até 24 horas

Após a adoção e a validação do projeto, use:

```text
Read https://raw.githubusercontent.com/carlosemox/engenharia-cadu-adocao/main/24h.md

Entre em PREPARAR_24H.
Verifique a prontidão deste projeto e prepare o contrato
para uma futura missão de até 24 horas.

Confira o supervisor real, backlog elegível, ambiente,
permissões, limites, checkpoints, exclusividade,
recuperação e mecanismo de parada.

Não inicie a missão nesta etapa.
Não declare READY_UNATTENDED sem evidências atuais.
Se faltar runtime ou qualquer condição necessária,
mostre o bloqueio e o próximo lote de preparação.
```

O [template de missão](templates/MISSAO_24H.json) vem desativado. Campos ausentes não significam limites infinitos. Ter um arquivo `24h.md` não implementa um supervisor; a prontidão precisa ser demonstrada no host e no escopo que serão utilizados.

### Iniciar somente após prontidão e GO específico

O comando abaixo é um modelo condicionado, não autorização geral. Substitua os campos por identificadores reais e use somente após conferir o contrato e seus limites:

```text
Read https://raw.githubusercontent.com/carlosemox/engenharia-cadu-adocao/main/24h.md

Solicito EXECUTAR_MISSAO para o contrato [ID e revisão],
no projeto [alvo], respeitando o backlog e os limites aprovados.

Confirme a validade das evidências de READY_UNATTENDED,
o destino, o orçamento, a exclusividade e a ausência
de outra missão conflitante antes de iniciar.

Use somente o supervisor e o comando realmente validados.
Se qualquer condição indispensável faltar, não inicie.

Registre identificador da execução, estado observado,
checkpoint e forma de parada. Não amplie permissões,
modelos, provedores, cobrança ou escopo para continuar.
```

Vinte e quatro horas são um teto autorizado, não uma obrigação de consumir o período. Sem runtime e início observáveis, a saída correta é NOT_STARTED ou RUNTIME_AUSENTE, não RUNNING.

## 6. Onde fica cada informação

| Destino | Conteúdo |
|---|---|
| **Esta biblioteca pública** | Procedimentos genéricos, templates inativos, referências e exemplos fictícios. |
| **Aplicativo-alvo** | Código, documentação canônica e alterações que seu plano autorizar. |
| **Destino privado de diagnóstico** | Retrato real, rascunhos, evidências e decisões específicas antes da incorporação aprovada. |
| **Operação privada autorizada** | Perfis e referências operacionais pertinentes, sem credenciais versionadas. |

Não enviar relatórios reais à página pública, não copiar todo o aplicativo para esta central e não usar a publicidade da metodologia como autorização de publicar projetos.

## 7. Uma única engenharia

A adoção complementa a [Engenharia Cadu principal](https://github.com/carlosemox/engenharia-cadu) e seus procedimentos P00–P28. Codex coordena; Antigravity, Gemini e OpenCode colaboram somente quando disponíveis, úteis e autorizados. A economia usa contexto suficiente por tarefa e verificações proporcionais, sem omitir requisitos nem prometer redução percentual.

**Estado do material:** comandos documentados para uso nos ambientes autorizados. A publicação deste guia não executou diagnóstico em aplicativo, migrou banco, instalou agente ou iniciou missão prolongada. Consulte [verificações](validacao/RESULTADOS.md), [cenários de homologação](validacao/CASOS.md) e [fontes](FONTES.md).

[Voltar ao início](README.md) · [Comando de análise](read.md) · [Aplicar](aplicar.md) · [Retomar](retomar.md) · [Preparar 24 horas](24h.md)
