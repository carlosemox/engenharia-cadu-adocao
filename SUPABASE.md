# Supabase — modularização e transição controlada

**Planejar no diagnóstico; executar somente nos lotes aprovados.** Este guia não é um schema universal e não autoriza alterar um banco só porque o usuário escolheu Supabase como direção.

## 1. Estado atual e alvo
Identifique banco/provedor/ORM, versões, auth/sessões, roles/grants/RLS, Storage, Functions, Realtime, extensões, jobs, webhooks e consumidores. Separe local, staging e produção. Confirme projeto/organização/região por metadados autorizados; não adivinhe o destino nem exponha connection strings. Sem acesso, trabalhar com código/schema e declarar que o estado remoto não foi observado.

Se já usa Supabase, reaproveite projeto, dados, IDs, auth, migrações e contratos. Se usa outro backend, desenhe coexistência/transição antes de migrar. Não trocar ORM ou autenticação por conveniência. Sem necessidade de persistência, registrar não aplicável. Padrões privados Cadu só são utilizados se realmente acessíveis; ausentes, propor o desenho específico e pedir decisão.

## 2. Responsabilidades do módulo
Conforme o produto: identidade/sessão; autorização e tenancy; acesso a dados; armazenamento; eventos; funções/jobs; adaptadores externos; logs e métricas. Fronteiras não exigem microserviços nem uso de todos os produtos Supabase. Não criar multitenancy, tabela genérica ou camada de abstração sem necessidade real.

Mantenha invariantes e contratos de domínio separados das particularidades do fornecedor quando isso ajuda a manutenção. Preserve identificadores e relações consumidos por outras partes. Frontend não recebe secret/service_role; privilégio administrativo fica restrito ao servidor autorizado. Credencial de inspeção não recebe escrita por esta receita.

## 3. Schema e histórico existente
Conferir schema, extensões, roles, policies, views, triggers, functions, índices e histórico local/remoto. Identificar divergências e origem antes de gerar DDL. Não modificar migrations já aplicadas, apagar histórico ou aceitar repair automaticamente. Escolher fonte principal de migrações quando ORM e CLI coexistirem, sem dupla aplicação.

Descobrir comandos pela ajuda da versão instalada e documentação oficial atual; verificar changelog relevante. Não copiar flags experimentais nem adotar engine novo sem plano. `db pull` pode oferecer registrar uma migração no histórico remoto; não tratá-lo como leitura pura nem confirmar prompts automaticamente. Uma consulta SQL também pode ter efeitos: revisar função/statement, usar acesso read-only e escopo autorizado.

Proibido neste fluxo implícito: `db reset --linked`, drop/truncate, recriar projeto, descartar dados, alterar segredos ou executar DDL remoto. Gerar novas migrations de forma compatível com a ferramenta; revisar diff/SQL; testar em recurso local/staging isolado, com seed sintético, antes de qualquer aplicação remota especificamente autorizada.

## 4. Permissões e testes
Mapear schemas expostos, grants e RLS. Grants e políticas resolvem controles distintos; RLS deve refletir o domínio e as operações reais. Testar positivo/negativo com visitante, usuário A/B, tenant incorreto quando aplicável, perfil privilegiado e permissão revogada. Testar somente com service_role/admin não comprova RLS.

Revisar views, RPCs e funções de privilégio elevado, incluindo search_path e grants de execução. Não adicionar SECURITY DEFINER para ocultar erro de permissão. Não usar metadata editável pelo próprio usuário para conceder autorização. Auth inclui mapeamento de IDs, sessões, providers, callbacks, redirects, emails, recuperação e MFA conforme escopo; mudança de provedor requer estratégia própria.

Storage: policies de bucket/objeto, uploads, leituras, substituição/remoção e integridade. Backup do banco não inclui automaticamente os objetos do Storage. Realtime/Functions/jobs: autorização, segredos, idempotência, assinatura de eventos, retry, logs e limite de recurso, quando aplicáveis.

## 5. Migração ou cutover
Antes de mudar dados remotos ou identidade: destino exato; plano/horário/alçada; backup separado de banco e objetos; restauração comprovada; validação de contagens, integridade, relacionamentos e permissões; compatibilidade dos consumidores; estratégia para escritas durante transição; cutover; rollback ou roll-forward praticável. Reverter código não desfaz uma migração de dados automaticamente.

Sem essas condições, marcar a etapa remota BLOQUEADA, preservando preparação independente. Não copiar dados reais para um ambiente descartável por conveniência. Não aumentar plano/retenção/região ou criar serviço pago sem autorização.

## Entrega exigida
Mapa atual/proposto de módulos; projetos/ambientes sem segredos; dependências; migrations propostas; decisão de histórico; matriz de acesso; testes; custos conhecidos/pendentes; plano de transição/recuperação; limitações. Quando houver execução autorizada, adicionar comandos, versões, ambientes, resultados e limites da conclusão.

Um arquivo de SQL proposto não é um banco migrado. Conexão válida, schema compatível, RLS funcionando, identidade preservada e jornada utilizável precisam de evidências separadas.

## Fontes oficiais a revalidar na execução
- [Migrations e desenvolvimento local](https://supabase.com/docs/guides/local-development/database-migrations)
- [Workflow local e adoção de projeto existente](https://supabase.com/docs/guides/local-development/cli-workflows)
- [Row Level Security](https://supabase.com/docs/guides/database/postgres/row-level-security)
- [Backups e limites de Storage](https://supabase.com/docs/guides/platform/backups)
- [Changelog](https://supabase.com/changelog)

[Entrada](read.md) · [Aplicar](aplicar.md) · [Fontes e revisão](FONTES.md)
