# Fontes, procedência e limites

Revisão documental: 29/10/2026, horário de São Paulo. Este kit é uma especialização da Engenharia Cadu para projetos existentes; não substitui a central nem redistribui pacotes de skills. APIs e condições dos fornecedores devem ser revalidadas na execução.

## Base versionada

- [Engenharia Cadu, revisão b22931d](https://github.com/carlosemox/engenharia-cadu/tree/b22931d1be7a53f62092ecac16eba3a108420542): contratos de contexto, economia, implementação, revisão, retomada e alçadas; especialmente P20/P21 e P17/P18.
- [Matheus Gomes, projeto existente, revisão 21b71b6](https://github.com/soumatheusgomes/vibe-coding-toolkit/blob/21b71b68679c11184f49c23168852014bf6dde8b/docs/prompts/12-existing-project-setup.md): inventário, preservação da stack, adoção aplicável, documentação canônica, delegação delimitada, validação e revisão por evidências.
- Referências exatas em [metodo.lock.json](metodo.lock.json). A biblioteca não atualiza missões automaticamente.

## Adaptações específicas

| Tema da referência | Decisão nesta biblioteca |
|---|---|
| Adoção de app existente | Reconstrução explícita de produto e apresentação visível antes de mudanças |
| Brainstorming e plano | Gate do responsável com decisões por lote e delta de ajustes |
| Preservar contratos e arquitetura | Mapa origem→destino, baseline e recuperação de trabalho não commitado |
| Cobrir catálogo aplicável | Selecionar por necessidade/licença/compatibilidade, sem instalar tudo |
| Documentação canônica | Reconciliar PRD/TRD/fluxos existentes em vez de criar versões concorrentes |
| Dados e serviços | Guia Supabase próprio, sem migração remota implícita |
| Continuidade | Preparação condicionada a supervisor real; prompt não equivale a runtime |

As restrições de branches, publicação, gastos e produção da Engenharia Cadu não são removidas porque a referência de terceiros possui autorizações diferentes.

## Fontes oficiais consultadas

- [Supabase — migrations](https://supabase.com/docs/guides/local-development/database-migrations): versionar e testar mudanças; não confundir o tutorial local com autorização para reset remoto.
- [Supabase — workflow local](https://supabase.com/docs/guides/local-development/cli-workflows): projeto existente e histórico de migrações; conferir efeitos e prompts de comandos como db pull.
- [Supabase — RLS](https://supabase.com/docs/guides/database/postgres/row-level-security): grants e políticas, superfícies expostas e testes de autorização.
- [Supabase — backups](https://supabase.com/docs/guides/platform/backups): banco e objetos do Storage exigem tratamento de recuperação distinto.
- [Supabase — changelog](https://supabase.com/changelog): consultar alterações relevantes à versão antes de implementar. O índice Markdown não foi lido com sucesso nesta preparação; não se afirma auditoria completa de breaking changes.
- [OpenAI — Codex não interativo](https://developers.openai.com/codex/noninteractive/): interface de execução não equivale à implementação de um supervisor próprio.
- [OpenAI — harness engineering](https://openai.com/index/harness-engineering/): conhecimento acessível no repositório e ciclos de verificação.

Não foram acessados bancos, credenciais, código privado dos aplicativos ou contas Supabase na criação deste kit. As fontes sustentam decisões de procedimento, não certificam a implementação dos projetos ou a qualidade futura dos modelos.

## Licenciamento
Textos novos são material da Engenharia Cadu. A licença geral de redistribuição do material próprio permanece sem nova concessão nesta entrega; publicidade não significa licença automática para todos os componentes. Referências de terceiros mantêm seus termos. O aviso MIT do toolkit está em [fontes/LICENSE_MATHEUS.txt](fontes/LICENSE_MATHEUS.txt). Não incorporar skills restritas apenas porque foram recebidas num ZIP.
