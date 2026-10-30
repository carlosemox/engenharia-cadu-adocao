# Continuidade, segurança e backup na adoção

Complemento de coordenação da trilha de projetos existentes. Base editorial: Engenharia Cadu, revisão `0d01db8df3efc103ac586e2c4d830023b11931c7`. As referências originais de `metodo.lock.json` permanecem preservadas; esta seção acrescenta apenas as políticas transversais aprovadas para organização.

| Assunto | Fonte fixada | Página explicativa |
|---|---|---|
| Continuidade por etapa | [CONTINUIDADE.md](https://github.com/carlosemox/engenharia-cadu/blob/0d01db8df3efc103ac586e2c4d830023b11931c7/politicas/CONTINUIDADE.md) | [Fluxo contínuo](https://carlosemox.github.io/engenharia-cadu/guia/continuidade/) |
| Revisão e segurança | [SEGURANCA_ENGENHARIA.md](https://github.com/carlosemox/engenharia-cadu/blob/0d01db8df3efc103ac586e2c4d830023b11931c7/politicas/SEGURANCA_ENGENHARIA.md) | [Segurança](https://carlosemox.github.io/engenharia-cadu/guia/seguranca/) |
| Backup por projeto | [BACKUP_DRIVE.md](https://github.com/carlosemox/engenharia-cadu/blob/0d01db8df3efc103ac586e2c4d830023b11931c7/politicas/BACKUP_DRIVE.md) | [Backup](https://carlosemox.github.io/engenharia-cadu/guia/backup/) |
| Implantação e limites | [OPERACAO.md](https://github.com/carlosemox/engenharia-cadu/blob/0d01db8df3efc103ac586e2c4d830023b11931c7/OPERACAO.md) | [Estado documental](https://carlosemox.github.io/engenharia-cadu/guia/operacao/) |

## Antes de aplicar
`read.md` continua em ENTENDER_E_PROPOR: reconstruir e mostrar o produto, os conflitos e o plano. O agente não modifica código, pastas ou banco antes da decisão material. Continuidade não remove esse gate nem transforma todas as sugestões em trabalho aprovado.

## Depois da aprovação
No modo contínuo já autorizado, o coordenador conduz os lotes de `aplicar.md`, verifica a entrega, a revisão, a segurança, o backup aplicável e o checkpoint, e segue para o próximo trabalho elegível sem exigir nova colagem de comandos. Falhas e decisões pendentes bloqueiam apenas suas dependências. Plano ou alvo alterado exige reconciliação do delta.

## Segurança e preservação
Antes de mudança arriscada, proteger o estado anterior com prova pertinente; ao fechar uma entrega, preservar os novos artefatos. Destino privado: `Projetos 2026/Backup/<nome-do-projeto>`. Não enviar relatórios reais ou snapshots do aplicativo ao kit público. Código, histórico, arquivos locais, banco e objetos têm cobertura separada; segredos exigem proteção própria.

Revisão de segurança acompanha a adoção e o candidato final. Nenhuma inspeção garante ausência de invasão; achados bloqueantes impedem a ação dependente. A revisão independente precisa de outra execução real quando exigida pelo risco, não de uma declaração do implementador.

## Continuidade não é supervisor
`24h.md` permanece uma verificação/receita. Sem runtime, limites, conexão Drive e testes de retomada no host, não declarar READY_UNATTENDED ou RUNNING. As políticas são consultadas uma vez por revisão; carregar somente as seções pertinentes. O alvo e suas permissões continuam sendo os do projeto.
