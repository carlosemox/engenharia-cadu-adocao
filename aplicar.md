# Aplicar o plano de adoção aprovado

**Modo: APLICAR_PLANO_APROVADO.** Este comando transforma um plano revisado em mudanças verificáveis; não aprova por conta própria o que o diagnóstico sugeriu.

## Entrada e alçada
Leia as instruções aplicáveis do alvo, `AGENTS.md` desta biblioteca, plano identificado, registro da decisão do usuário, baseline, mapas de arquivos e dados. Use a revisão única do kit e `metodo.lock.json`. Se faltam alvo, plano, lotes ou autorizações, faça apenas a parte documental independente e peça a decisão material. Não recomece toda a entrevista.

Revalide HEAD e alterações locais. Drift material exige atualizar o trecho afetado; preserve trabalho posterior. Aprovação antiga de outra revisão não autoriza aplicar um patch incompatível. Registro de aprovação é evidência de decisão real, não credencial, assinatura criptográfica ou controle suficiente de segurança.

Codex coordena. Colaboradores recebem escopo/arquivos/recursos/aceites/retorno específicos e modelo/provedor autorizados; não se cria painel por hábito. Revisor é somente leitura. Não atribua a um colaborador ferramentas que não possui. Nunca altere preferências globais, autenticação ou cobrança apenas para delegar.

## Lote 0 — Preservação e baseline
1. Confirme alvo, recursos e ausência de escritor concorrente. Não matar processo com identidade não verificada. Branch/worktree conforme política do projeto; proteger main/master. Worktree não isola banco, portas, builds ou credenciais.
2. Faça checkpoint privado do estado pertinente dentro da autorização: arquivos versionados, staged/unstaged/untracked úteis, dados e recursos que poderão ser afetados. Um bundle Git não contém alterações locais não commitadas nem dados. Não versionar credenciais, caches pessoais ou dumps de produção. Verifique recuperação antes de mudanças arriscadas.
3. Leia scripts/hooks e efeitos antes de executar checks. Baseline controlado em cópia/recurso descartável sem produção, com testes e dados sintéticos. Registre comandos, versão, ambiente, falhas anteriores e verificações NOT_RUN. Não use um comando chamado check sem verificar se migra ou publica.

## Lote 1 — Restaurar o primeiro resultado útil
4. Quando o app estiver quebrado, reproduza a causa e faça a menor correção autorizada antes de uma reforma estrutural. Defina teste de regressão e demonstre antes/depois. Falta de credencial, runner ou quota não é automaticamente bug no código.
5. Não misture a correção com atualização geral, mudança de banco/ORM ou nova arquitetura. Sem causa demonstrada, formule hipótese testável; não acumule remendos sem nova informação. Respeite tentativas e orçamento. Bloqueio externo afeta só etapas dependentes.

## Lote 2 — Documentação e contexto canônicos
6. Incorpore PRD/TRD/fluxos/design revisados nos destinos aprovados. Reuse equivalentes em vez de criar documentos concorrentes. Preserve requisitos e decisões; não substituir produto pretendido por comportamento defeituoso do código.
7. Considere consertado apenas o que foi implementado/verificado. Rascunho de arquitetura-alvo continua proposto. Atualize índice de contexto curto e memória com fonte, validade e motivo. Handoff temporário separado das decisões duráveis. Não copiar toda a biblioteca para o produto.

## Lote 3 — Arquivos e modularização
8. Execute o mapa origem→destino aprovado, por unidade testável. Atualize imports/exports, aliases, rotas, scripts, testes, build, CI/deploy e caminhos sensíveis a maiúsculas. Preserve APIs/contratos, ou trate compatibilidade explicitamente aprovada. Não excluir arquivo por ser desconhecido.
9. Separe movimento de mudança de comportamento quando útil. Não impor uma árvore universal, microserviço ou stack de referência. A menor solução completa pode ser manter arquivos onde estão e melhorar fronteiras/documentação. Lote sem benefício demonstrado deve ser revisto, não aplicado por estética.
10. Execute checks focais e de integração afetados. Regressões introduzidas bloqueiam dependentes; não diminuir regras ou excluir testes para obter GREEN. Recuperação incide apenas sobre alterações próprias e aprovadas, sem resetar o trabalho do usuário.

## Lote 4 — Supabase e serviços do produto
11. Use `SUPABASE.md`. Preparar código, schema proposto e teste local não autoriza aplicar migração remota. Preserve IDs, dados, auth, providers e consumidores até um plano de transição aprovado. Diferenciar conexão, histórico de migração, RLS, identidade e jornada real. Backup de banco e objetos têm escopos diferentes.
12. Para APIs externas, valide contrato, ambiente, autorização, custo, evento, retry e recuperação no escopo aprovado. Não inventar endpoint/chave/fornecedor. Soluções provisórias têm condição de revisão/saída. Serviços já contratados não implicam permissões de API ou liberdade de aumentar plano.

## Lote 5 — Bootstrap incremental e GitHub
13. Preserve runtime, package manager, lockfiles, framework e ferramentas funcionais. Atualizações compatíveis precisam de necessidade, documentação atual e verificação; major/stack migration é decisão separada. Não usar force ou downgrade automático por auditoria de dependências.
14. Integre as capacidades pertinentes da central/Matheus. Cada item recebe decisão: manter, equivalente, adaptar, testar, não aplicável ou bloqueado. Conferir fonte, licença, versão, instruções, dependências, descoberta e uso real; não instalar todos os catálogos.
15. AGENTS.md deve conter invariantes, comandos e mapa; clientes adicionais usam seu formato documentado e observado. Não duplicar hooks/MCPs, importar caches/credenciais ou alterar globais por padrão. Incompatibilidade bloqueia só a capacidade dependente.
16. No GitHub, preservar remote, visibilidade, histórico, PRs, workflows e regras reais. Criar repo, mudar branch default/proteção, executar workflow, push/PR/merge ou habilitar runner têm alçadas específicas. Uma autorização para publicar esta biblioteca não se aplica aos apps. Não ligar código de PR não confiável a runner com credenciais internas.
17. Quando autorizado, conectar CI aos comandos canônicos e distinguir lint/tipos/teste/build/deploy/migração. Registrar SHA e artefatos. Build/check não aplica migrations remotas nem acessa produção. Segredos ficam fora do Git. Commit seleciona paths exatos e HEAD atual; nada de git add . indiscriminado, force-push ou commit de trabalho alheio.

## Lote 6 — Validação e revisão
18. Compare funcionalidades e fluxos antes/depois. Cobrir regressão, dados, permissões, isolamento, erros, contratos e interface quando pertinentes. Código existente ou build não comprova fluxo funcional. Rever design renderizado em dispositivos pertinentes; sem navegador, revisão visual NOT_RUN.
19. Provar reaplicação segura do setup nos componentes alterados: sem seções/hooks/servers/skills duplicados. Não reinstalar tudo nem repetir migrations para provar idempotência. Examinar todos os caminhos alterados e consumidores.
20. Fixe o candidato e aplique revisão independente P14 da base Cadu quando disponível. Achados precisam de localização, cenário e evidência. Deduplicar; corrigir dentro da alçada; repetir testes afetados. Sem outro executor real, declarar auto-revisão, não fingir independência.
21. Atualize o Retrato do Projeto visível: o que mudou, o que ficou intacto, o que está comprovado, o que falta, riscos e próximos passos. Relatórios privados fora deste kit público. Prontidão da aplicação e do harness são estados diferentes.

## Prontidão e encerramento
Use `24h.md` para preparar os próximos gates, sem iniciar a missão por consequência. Se houver runtime ausente, desenhe um incremento de supervisor/reuso e registre a dependência. Não declare READY_UNATTENDED com base em documentação preenchida.

Saída: ADOTADO_NO_ESCOPO / PARCIAL / BLOQUEADO, plano e revisão aplicados, mapa antes/depois, evidências por lote, recursos criados, recuperação, testes NOT_RUN e próximos itens autorizados. Continue etapas independentes já autorizadas sem pedir confirmação a cada arquivo; pare nas decisões materiais e limites verdadeiros.

[Entrada](read.md) · [Supabase](SUPABASE.md) · [Retomada](retomar.md) · [Plano](templates/PLANO_ADOCAO.md)
