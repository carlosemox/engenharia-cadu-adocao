# Plano de Adoção — template inativo

ID e versão do plano:
Alvo/repositório/raiz privados:
Baseline: commit + staged/unstaged/untracked pertinentes:
Revisão da biblioteca e método-base:
Referência do Retrato do Projeto e fontes:
Primeiro resultado útil:
Fora do escopo:
Pendências que realmente impedem execução:

## Estratégia
Arquitetura útil a preservar; problema observado; menor adaptação completa; alternativas rejeitadas e motivo; mudanças comerciais não incluídas; direção de Supabase separada das autorizações de migração.

## Preservação
| Recurso | Estado anterior | Cópia/checkpoint privado | Como verificar recuperação | Risco residual |
|---|---|---|---|---|

Incluir alterações não commitadas/untracked úteis e dados atingidos. Não incluir valores de segredos. Bundle Git não preserva todo o estado. Restauração e rollback de dados precisam de prova própria.

## Arquitetura e caminhos
| Origem | Destino/permanência | Operação | Contratos/consumidores | Teste | Recuperação |
|---|---|---|---|---|---|

Marcar MANTER/MOVER/ADAPTAR/NOVO/ADIAR. Arquivos desconhecidos permanecem preservados. Separar movimento de alteração comportamental quando útil.

## Um contrato por lote
- ID, objetivo e requisitos:
- Pré-condições e lotes dependentes:
- Caminhos e recursos permitidos:
- Dados/serviços/ambiente:
- O que obrigatoriamente permanece funcionando:
- Executor e revisor realmente disponíveis:
- Alçadas exigidas e já concedidas:
- Baseline e teste capaz de detectar regressão:
- Procedimento delimitado:
- Critérios de aceite e comandos entendidos:
- Recuperação/rollback/roll-forward e limitações:
- Limites de tempo, tentativas, chamadas, concorrência e custo observável:
- Condições de espera/parada:
- Decisão do usuário e sua origem:
- Resultado, evidências e testes NOT_RUN após execução:

## Sequência sugerida, adaptar às dependências
L0 preservação e baseline → L1 funcionamento → L2 documentos/contexto → L3 arquitetura/arquivos → L4 dados/serviços → L5 ambiente/GitHub/CI → L6 validação e revisão → L7 preparação de continuidade.

Nenhum lote está aprovado por constar desta tabela. Migração remota, novos recursos pagos, alteração de auth/segredos e produção têm decisão específica.

## Revisão do plano
Registrar alteração, motivo, fontes afetadas, lotes invalidados e decisões preservadas. Sem reiniciar a concepção do produto a cada ajuste. Mudança material de snapshot exige reconciliação antes de aplicar.

## Encerramento
ADOTADO_NO_ESCOPO / PARCIAL / BLOQUEADO. Separar aplicação recuperada, engenharia adotada, supervisor validado e missão iniciada. Próximo resultado utilizável e dependências.
