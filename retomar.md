# Retomar a adoção sem recomeçar

Leia o plano, o registro de aprovação e o último checkpoint disponíveis. Use a mesma revisão do kit indicada na missão; se não estiver acessível, registrar a limitação, sem trocar silenciosamente o procedimento.

1. Confirme alvo, raiz Git, HEAD, staged/unstaged/untracked, worktrees e artefatos do lote. Não resetar, limpar, fazer stash nem reaplicar scaffold. Preserve trabalho novo.
2. Confira processos, supervisor, lease, fila e quem ainda escreve. PID isolado não prova identidade nem saúde. Não matar worker saudável ou assumir seus arquivos sem reconciliação.
3. Compare checkpoint com fatos. Identifique o último resultado realmente comprovado, o que apenas foi planejado, mudanças depois da aprovação e verificações invalidadas. Não confiar em um resumo antigo que diz GREEN.
4. Consulte efeitos externos antes de repetição: migration, commit, push, publicação, criação de recurso ou envio. Resultado desconhecido não é falha autorizando retry automático.
5. Mostre no chat: onde paramos; o que mudou; o que ficou intacto; evidências válidas; impedimento; próxima ação. Atualize o Retrato do Projeto com esse delta, não reconstruir todo o histórico por hábito.
6. Com aprovação ainda válida e recursos livres, retome somente a menor etapa do lote necessário em `aplicar.md`. Se houver drift material ou decisão nova, apresente apenas o trecho afetado para revisão. Sem checkpoint, use `read.md` de forma focal para recuperar fontes e delimitar incertezas.
7. Execução prolongada depende de `24h.md`; sem supervisor observado, não alegar retomada automática. Fila vazia pode ser ausência legítima de trabalho.

Sem ferramentas, entregue a análise documental e o que falta verificar. Não simule consultas, continuidade ou recuperação.

[Entrada](read.md) · [Aplicar](aplicar.md) · [Prontidão prolongada](24h.md)
