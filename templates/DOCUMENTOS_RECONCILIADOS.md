# Mapa de documentação reconciliada

Template lógico, não obrigação de criar todos os arquivos. Reutilizar fontes canônicas existentes. Antes da aprovação, manter rascunhos privados fora do código; depois aplicar revisões nos destinos aprovados.

## Cabeçalho de cada documento proposto
Nome, responsável, status (RECONSTRUIDO_PARA_REVISAO / APROVADO / IMPLEMENTADO_PARCIAL / VERIFICADO_NO_ESCOPO), fonte original, revisão do alvo, data, evidências e lista de diferenças. Status não pode ser promovido pelo simples preenchimento do template.

## Contexto e briefing
Problema, público e comprador, operação anterior, intenção, jornada principal, resultado útil, negócio, restrições, primeira versão, exclusões, hipóteses, direção de design D0, serviços necessários e decisões ainda abertas. Histórico curto e fundamentado.

## PRD reconciliado
- Objetivo e público, escopo vigente e cancelamentos documentados.
- Requisitos identificados com origem, prioridade e dependências; preservar IDs existentes.
- Regras de negócio, perfis, autorização, estados, erros e exceções.
- Critérios positivos/negativos de aceite, sem transformar teste existente em toda a definição do produto.
- Serviços/APIs e limitações da primeira versão; não confundir plano de integração com integração comprovada.
- Requisitos não funcionais pertinentes: acessibilidade, privacidade, segurança, desempenho, disponibilidade e manutenção, com metas somente quando fundamentadas/aprovadas.
- Colunas: intenção normativa, implementação observada, evidência de teste, conflito/decisão.
- Requisito inferido do código deve estar marcado como tal e não prevalecer automaticamente sobre a intenção.

## TRD reconciliado
- Stack/versões/runtime/gerenciador atuais e compatibilidade verificada.
- Arquitetura atual com fronteiras, módulos, contratos e consumidores.
- Dados, schema, migrações, identidade, autorização, isolamento e serviços.
- Backend/frontend/jobs/build/CI/ambientes/observabilidade/recuperação.
- Arquitetura-alvo proposta e alternativas; motivos e tradeoffs, sem impor framework.
- Mapa de alterações em arquivos e impactos nos consumidores.
- Plano Supabase, preservação de dados/IDs/identidade, controle de migrations, teste e transição.
- ADRs para decisões materiais; restrições, riscos, dependências e custo pendente.
- Não apresentar propostas como desenho já implementado.

## Fluxos e design
AS-IS observado e TO-BE proposto, atores e decisões, sucesso, falha, falta de acesso, vazio, estados transitórios e dependências. Direção D0, especificação D1, componentes D2; marca e padrões úteis preservados. Inspeção visual precisa de execução real ou NOT_RUN.

## Implementação e operação
Backlog por incremento utilizável, dependências, contrato de tarefa, limites, testes, revisores, alçadas, setup, comandos reais, readiness por nível e runbook de recuperação. Missões prolongadas somente após supervisor validado e contrato específico.

## Rastreabilidade
| Necessidade/decisão | Requisito | Fluxo | Módulo/contrato | Tarefa/lote | Teste | Evidência/revisão |
|---|---|---|---|---|---|---|

## Reconciliação de destinos
| Informação | Fonte atual | Destino escolhido | Operação aprovada | Referências a corrigir | Por que não perde conteúdo |
|---|---|---|---|---|---|

Não apagar documentos antigos por idade. Consolidar preservando origem e decisões; arquivamento/exclusão depende de escopo. Código, schema e regras não são automaticamente reescritos por mudar os documentos.
