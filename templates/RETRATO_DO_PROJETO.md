# Retrato do Projeto — template privado

**Modelo vazio, não diagnóstico realizado.** Preencher com fontes; não publicar relatório real neste kit. Campo desconhecido permanece DESCONHECIDO. Não utilizar o exemplo fictício como evidência.

## 1. O projeto em um minuto
- Nome e alvo observado:
- Snapshot/commit e alterações locais pertinentes:
- Data, escopo e fontes realmente acessadas:
- Este projeto é:
- Atende estas pessoas:
- Resolve este problema:
- A experiência principal deve ser:
- Primeiro resultado útil que devemos recuperar/entregar:
- Resumo da situação atual, em linguagem de negócio:

## 2. O que já decidimos e o que ainda é hipótese
| ID | Decisão/hipótese | Origem e revisão | Situação | Conflito ou confirmação necessária |
|---|---|---|---|---|

Distinguir relatado pelo usuário, aprovado em documento, inferido do código e proposta nova. Não substituir intenção por bug existente nem fabricar decisões passadas.

## 3. Planejado × encontrado × comprovado
| ID | Funcionalidade e público | Previsto no PRD | UI/API/dados/permissão encontrados | Evidência atual e ambiente | Estado | Lacuna | Ação proposta |
|---|---|---|---|---|---|---|---|

Estados: COMPROVADO / PARCIAL / FALHA / PLANEJADO / NAO_VERIFICADO / DESCONHECIDO / NAO_APLICAVEL. Uma função pode ter várias linhas para suas camadas. Não gerar percentual de conclusão sem critério definido.

## 4. Fluxos que o usuário percorre
Para cada jornada, preencher:
- Ator e pré-condições:
- AS-IS, observado: início → decisões → operações → resultado:
- Exceções, erros, falta de acesso, vazio e dependências encontradas:
- TO-BE, proposto: início → decisões → operações → resultado:
- O que muda para a pessoa:
- Fontes e testes; o que não foi observado:

Adicionar diagrama Mermaid apenas se útil e manter explicação em texto. Os elementos propostos precisam de legenda.

## 5. Documentação reconciliada
| Documento | Fonte atual | Autoridade/estado | Contradição | Destino proposto | Mudança necessária |
|---|---|---|---|---|---|

Relacionar briefing/escopo, PRD, TRD, fluxos, design, dados, plano, setup, qualidade e handoff. Rascunhos fora do código até aprovação; equivalentes existentes permanecem preferidos.

## 6. Arquitetura e arquivos
### Como está
Responsabilidades, módulos, dependências, contratos públicos e dados. Árvore relevante do estado observado, não milhares de arquivos.

### Como propomos deixar
Mesmas responsabilidades ou diferenças justificadas. Legenda MANTER/MOVER/ADAPTAR/NOVO/ADIAR. Mostrar benefício e impacto.

| Origem | Destino ou permanência | Motivo | Consumidores/contratos | Como preservar | Teste | Recuperação |
|---|---|---|---|---|---|---|

## 7. Experiência e design
- D0: direção de marca/uso disponível:
- D1: tokens/componentes/regras especificados:
- D2: componentes/telas verificados:
- O que preservar:
- Lacunas de experiência, responsividade e acessibilidade:
- Inspeção visual efetivamente realizada ou NOT_RUN:

## 8. Dados, Supabase e integrações
| Capacidade | Atual e fonte | Estado observado | Decisão proposta | Dados/risco | Custo conhecido ou pendente | Dependência/alçada | Contingência/saída |
|---|---|---|---|---|---|---|---|

Separar identidade, autorização, banco/migrações, Storage, eventos/functions e serviços externos. Explicar o que é harmonização e o que é migração/cutover. Referenciar plano de preservação e teste de restauração, sem colar segredos.

## 9. Nosso plano de mudança
| Lote | Resultado | Requisitos | Paths/recursos | Preservado | Risco | Aceite | Recuperação | Aprovação |
|---|---|---|---|---|---|---|---|---|

Mantenha funcionalidades novas fora da adoção estrutural, salvo aprovação explícita. Relacione dependências e ordem.

## 10. Decisões para você
| ID | Decisão | Minha proposta | Alternativas e impacto | Sua escolha | Evidência da escolha |
|---|---|---|---|---|---|

As escolhas são corrigir entendimento, aprovar, ajustar, adiar ou recusar um lote. O agente não preenche sua aprovação. Não solicitar confirmação de informações já disponíveis.

## 11. Prontidão sem ambiguidade
| Item | PASS/FAIL/NOT_RUN/BLOCKED/NAO_APLICAVEL | Evidência e versão | O que falta |
|---|---|---|---|
| Produto e escopo compreendidos | | | |
| Preservação/recuperação | | | |
| Desenvolvimento local | | | |
| CI pertinente ao backlog | | | |
| Staging pertinente ao backlog | | | |
| Integrações/Supabase | | | |
| Instruções e skills descobertas | | | |
| Supervisor real | | | |
| Retomada e exclusividade | | | |
| Limites e bloqueio de ações proibidas | | | |
| Contrato de missão | | | |

Adoção documental, aplicativo funcional, READY_UNATTENDED e RUNNING são estados distintos.

## 12. Evidências, lacunas e próximo passo
| Fonte ID | Arquivo/recurso | Revisão/data | O que sustenta | Limite da observação |
|---|---|---|---|---|

- Fontes inacessíveis e o efeito sobre a conclusão:
- Testes não realizados e por quê:
- Plano/snapshot que está sendo apresentado:
- Estado: AGUARDANDO_REVISAO_DO_PROJETO, ou estado observado da execução posterior.
- Próxima ação coberta pela autorização:

**Apresentar também no chat:** o que este produto é, onde está, o que será preservado, as mudanças propostas e as decisões materiais. Arquivo bonito não substitui a explicação.
