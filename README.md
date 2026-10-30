<div align="center">

# Engenharia Cadu · Adoção

### Entenda o que existe. Decida o que muda. Preserve o que funciona.

**Codex principal · Astra econômico · projeto visível · reestruturação por lotes**

[Guia completo e comandos para copiar](GUIA_DE_USO.md) · [Começar a análise](read.md) · [Aplicar plano aprovado](aplicar.md) · [Retomar](retomar.md) · [Preparar 24 horas](24h.md)

</div>

---

## Para que serve

Uma entrada específica para aplicativos que já estão em desenvolvimento. O Codex recupera o contexto acessível, reconcilia PRD, TRD e fluxos, mostra o estado encontrado e propõe a adoção da Engenharia Cadu. **Você vê e pode corrigir o entendimento antes da reestruturação.** Depois da aprovação, o agente executa apenas os lotes delimitados e demonstra o resultado.

Este repositório distribui metodologia pública. Não recebe código, dados, segredos ou relatórios reais dos aplicativos. Não é um aplicativo-alvo, um agente instalado ou um supervisor de 24 horas.

**[Abra o guia de uso com o passo a passo e todos os comandos de entrada](GUIA_DE_USO.md):** entender o projeto, revisar o plano, aplicar os lotes aprovados, retomar e preparar uma missão prolongada. Os procedimentos completos continuam nos arquivos correspondentes.

## 1. O comando para começar

Abra o Codex na raiz do aplicativo existente e cole **na conversa do agente**, não no shell:

```text
Read https://raw.githubusercontent.com/carlosemox/engenharia-cadu-adocao/main/read.md

Entenda este projeto em andamento e reconstrua o contexto acessível.
Mostre o Retrato do Projeto, o PRD/TRD reconciliados, os fluxos atuais
 e propostos, o mapa de arquivos e o Plano de Adoção.
Quero revisar o que o produto faz, o que está comprovado, o que falta,
 o que será preservado e as mudanças propostas antes de alterar código,
 estrutura ou banco.
```

`Read` é uma instrução natural. O cliente precisa conseguir ler o endereço e acessar o alvo autorizado. Resolver `main` para um commit, registrar a revisão e usar os arquivos dessa mesma versão. Para uma missão reproduzível, substituir `main` pelo SHA observado; não adivinhar hashes ou misturar versões.

## 2. O que você vai enxergar

| Visão | O que explica |
|---|---|
| **Retrato executivo** | Que produto é este, para quem serve, o problema e a primeira entrega útil |
| **Planejado × encontrado × comprovado** | Funcionalidades pretendidas, camadas implementadas, testes, falhas e lacunas |
| **PRD e TRD reconciliados** | Regras e decisões que permanecem válidas, conflitos e hipóteses a confirmar |
| **Fluxos AS-IS / TO-BE** | Jornada observada e jornada proposta, inclusive erros, estados e acesso |
| **Arquitetura e arquivos** | O que manter, mover, adaptar ou criar, com consumidores e recuperação |
| **Serviços e Supabase** | Integrações atuais, desenho desejado, riscos, custos e autorizações necessárias |
| **Plano em lotes** | Ordem de trabalho, impacto, testes, limites, revisão e alçadas |
| **Prontidão separada** | Documentação, app local, CI, staging, supervisor e missão em execução |

Uma tela existente, uma API escrita e uma jornada comprovada não são a mesma coisa. Não há porcentagem inventada de conclusão. Fontes e decisões inacessíveis ficam identificadas, não são reconstruídas por imaginação.

O resultado é explicado **no chat**, com detalhes em Markdown e um relatório HTML privado quando houver ambiente de arquivos. O template visual não executa ações nem concede aprovação. [Ver o formato do retrato](templates/RETRATO_DO_PROJETO.md) · [Ler um exemplo explicitamente fictício](exemplos/RETRATO_FICTICIO.md).

## 3. O fluxo da adoção

```text
RECONHECER E PRESERVAR
  → RECUPERAR FONTES E RECONSTRUIR CONTEXTO
  → EXPLICAR O PRODUTO E SEU ESTADO
  → PROPOR ARQUITETURA, FLUXOS E PLANO
  → VOCÊ CORRIGE, APROVA, AJUSTA OU ADIA
  → APLICAR LOTES AUTORIZADOS
  → COMPROVAR PRESERVAÇÃO, FUNCIONAMENTO E ADOÇÃO
  → AVALIAR PRONTIDÃO PARA MISSÃO PROLONGADA
```

A primeira execução termina em `AGUARDANDO_REVISAO_DO_PROJETO`. Depois de aprovação suficiente, não há confirmação a cada arquivo. Um bloqueio afeta suas dependências; trabalho independente autorizado pode continuar. Uma mudança material de plano/snapshot exige reavaliar somente a parte afetada.

## 4. Aplicar o que foi aprovado

```text
Read https://raw.githubusercontent.com/carlosemox/engenharia-cadu-adocao/main/aplicar.md

Aplique somente o plano identificado e os lotes que aprovei.
Preserve funcionalidades, dados, identidade, contratos e trabalho local.
Mostre o antes/depois e as evidências ao final de cada lote.
```

O plano precisa estar identificado no contexto. O agente não assina aprovação pelo usuário. Reorganizar não significa reescrever: movimentos têm mapa origem→destino, consumidores, testes e recuperação. Atualidade não significa atualizar tudo para `latest`.

## 5. Supabase e GitHub sem perda de trabalho

[SUPABASE.md](SUPABASE.md) separa modularização de migração real. Quando Supabase já existe, preservar projeto, IDs, histórico, identidade e consumidores. Quando o backend é outro, planejar coexistência/transição antes de cutover. Preferência pelo provedor não autoriza recriar banco, trocar auth, aplicar DDL remoto ou aumentar gastos.

O bootstrap é incremental: stack, gerenciador, lockfiles e arquitetura úteis permanecem. Adoção no GitHub preserva remote, histórico e visibilidade. Commit, push, merge, runner, deploy, migrações, credenciais e custos têm alçadas distintas. A publicidade desta biblioteca não torna públicos os aplicativos.

## 6. Retomada e 24 horas

| Necessidade | Entrada |
|---|---|
| Retomar depois de uma interrupção | [retomar.md](retomar.md) |
| Verificar se o projeto pode receber uma missão longa | [24h.md](24h.md), modo `PREPARAR_24H` |
| Iniciar a missão, com contrato e runtime já comprovados | [24h.md](24h.md), modo `EXECUTAR_MISSAO` e GO específico |

```text
Read https://raw.githubusercontent.com/carlosemox/engenharia-cadu-adocao/main/24h.md
Verifique a prontidão e prepare o contrato. Não inicie sem supervisor
 real, limites definidos, provas de recuperação e minha autorização.
```

Sem supervisor real, a saída correta é `RUNTIME_AUSENTE`/`NOT_STARTED` com plano de preparação. O prompt não cria persistência por existir. Vinte e quatro horas são teto autorizado, não obrigação de consumir o período. Produção mantém seu gate.

## 7. Materiais da biblioteca

| Arquivo | Função |
|---|---|
| [Guia de uso](GUIA_DE_USO.md) | Passo a passo, comandos copiáveis e resultados esperados de cada fase |
| [read.md](read.md) | Comando completo de entendimento, apresentação e redesenho |
| [aplicar.md](aplicar.md) | Preservação, correção, documentação, estrutura, integrações, CI e revisão |
| [SUPABASE.md](SUPABASE.md) | Fronteiras de dados, identidade, RLS, migrations, backups e transição |
| [Retrato](templates/RETRATO_DO_PROJETO.md) | Modelo de explicação em linguagem de negócio e evidências |
| [Documentos reconciliados](templates/DOCUMENTOS_RECONCILIADOS.md) | Estrutura de briefing, PRD, TRD, fluxos e rastreabilidade |
| [Plano de adoção](templates/PLANO_ADOCAO.md) | Arquivos, lotes, aceites, dependências e recuperação |
| [Registro de decisão](templates/APROVACAO.md) | Decisão real vinculada a plano/snapshot e limites |
| [Relatório visual](templates/RELATORIO_VISUAL.html) | HTML offline para preencher privadamente, sem scripts externos |
| [Handoff](templates/HANDOFF.md) | Estado verificável para retomada sem repetir o trabalho |
| [Missão prolongada](templates/MISSAO_24H.json) | Contrato inativo; campos ausentes não significam ilimitado |
| [Casos de homologação](validacao/CASOS.md) | Cenários comportamentais para testar em ambiente autorizado |
| [Verificação documental](validacao/RESULTADOS.md) | O que foi realmente conferido nesta publicação |
| [Fontes](FONTES.md) e [lock](metodo.lock.json) | Procedência, revisões e limites |

## 8. Uma engenharia, não outro método

Este complemento usa a [Engenharia Cadu](https://github.com/carlosemox/engenharia-cadu) e o procedimento de projetos existentes do [Vibe Coding Toolkit](https://github.com/soumatheusgomes/vibe-coding-toolkit), nas revisões registradas no lock. Não renumera P00–P28, não impõe a stack de uma referência e não executa todas as skills por padrão.

Codex coordena. Antigravity, Gemini e OpenCode participam somente quando há necessidade, disponibilidade e autorização. Astra econômico mantém o modelo autorizado, carrega contexto pertinente e mede custo por entrega aceita; não promete uma porcentagem de economia.

**Estado da entrega:** biblioteca documental. Publicar este kit não reestruturou nenhum aplicativo, não instalou executores e não homologou autonomia. Exemplos são fictícios, templates são inativos e relatórios reais permanecem privados.

## Continuidade, segurança e backup
Consulte [Controles transversais](CONTROLES_TRANSVERSAIS.md). Após aprovar o plano, os lotes autorizados podem avançar sem nova colagem. O retrato inicial continua sujeito à sua revisão; backup, revisão e limites não são dispensados. [Ver organização na central](https://carlosemox.github.io/engenharia-cadu/guia/operacao/).
