# Exemplo fictício — Plataforma de Treinamentos

**DEMONSTRAÇÃO INVENTADA PARA EXPLICAR O FORMATO. Não é diagnóstico de um projeto do usuário. Não foram lidos arquivos nem executados testes desta plataforma.**

## O projeto em um minuto
Este produto pretende organizar cursos e permitir que alunos matriculados encontrem conteúdos e aulas ao vivo. Administradores gerenciam cursos e professores conduzem as aulas. A primeira entrega proposta é uma jornada de matrícula autorizada → agenda → acesso à aula.

Neste exemplo, imaginamos que já existam telas de cursos e uma estrutura inicial de login, mas não há evidência de funcionamento de ponta a ponta. O primeiro trabalho não seria reescrever tudo: seria esclarecer contratos, identificar o que está conectado e verificar a jornada mínima.

## Planejado, encontrado e comprovado — situações ilustrativas
| Módulo | Intenção fictícia | Situação hipotética | Classificação ilustrativa | Próxima investigação |
|---|---|---|---|---|
| Cursos | Listar aulas disponíveis | Telas com dados locais | PARCIAL | Identificar origem dos dados e contrato |
| Acesso | Limitar conteúdo por matrícula | Estrutura de login sem teste observado | NAO_VERIFICADO | Rastrear autorização no servidor e casos negados |
| Aula ao vivo | Entrar na aula pela agenda | Nenhum fornecedor definido | PLANEJADO | Definir interação, acesso, gravação, custo e integração |
| Pagamentos | Registrar compra | Fora do recorte inicial neste exemplo | ADIAR, decisão proposta | Confirmar fronteira de escopo |

Um diagnóstico real substitui estas situações pelas fontes, caminhos, versões e evidências encontrados. Nenhum estado desta demonstração pode ser copiado para um relatório real.

## Fluxos para comparar
**Hipótese de AS-IS:** abrir a tela de curso → escolher aula → encontrar ação ainda não integrada.

**TO-BE proposto:** autenticar → conferir matrícula no servidor → consultar agenda → solicitar acesso autorizado → entrar na sala externa → apresentar erro/contingência se indisponível.

As duas descrições acima são fictícias. No aplicativo real, o agente deverá confirmar o fluxo atual e explicar o impacto de cada mudança.

## Preservar e redesenhar
Preservaríamos identidade, telas úteis, contratos válidos e código que cumpre sua função. Proporíamos separar regras de acesso e integração da aula em responsabilidades claras. Não migraríamos banco ou autenticação apenas porque queremos reorganizar arquivos.

| Responsabilidade hipotética | Decisão proposta | Motivo |
|---|---|---|
| Telas e identidade atuais | Preservar e conferir | Evitar refazer trabalho útil |
| Regra de matrícula | Identificar fonte e isolar contrato | Não depender de esconder botões no frontend |
| Serviço de aula ao vivo | Escolher fornecedor após requisitos | Lançar sem construir toda infraestrutura própria |
| Dados | Reconciliar backend atual e desenho Supabase | Preservar IDs, histórico e consumidores |

## Plano a discutir
L0: inventário/baseline e preservação.
L1: reconstruir PRD, TRD e jornada prioritária.
L2: verificar autorização de acesso e corrigir o que estiver aprovado.
L3: integrar aula ao vivo no ambiente de teste autorizado.
L4: conferir jornada completa e atualizar documentação.
L5: avaliar supervisor e condições para missão prolongada.

## Decisões que o responsável enxergará
- O produto e o público foram entendidos corretamente?
- A primeira versão precisa de transmissão ou encontro interativo?
- Pagamentos ficam fora deste primeiro recorte?
- Qual lote está aprovado e quais devem mudar?
- A transição de dados é necessária ou basta harmonizar o que já existe?

## Situação do exemplo
Relato fictício, plano não aprovado, testes NOT_RUN, supervisor não demonstrado. Não existe percentual de conclusão nem missão em execução.

[Voltar à entrada](../read.md) · [Template real](../templates/RETRATO_DO_PROJETO.md)
