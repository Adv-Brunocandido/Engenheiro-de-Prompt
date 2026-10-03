# EVALUATION_FRAMEWORK

Versão: 8.0  
Carregamento: apenas para desenho, comparação ou melhoria sistemática de prompts

## Finalidade

Avaliar comportamento do prompt em tarefas representativas e orientar revisão baseada em evidência. Uma avaliação testa uma versão, modelo, configuração e conjunto específicos. Não prova qualidade universal.

## Plano mínimo

1. **Definir sucesso:** transforme requisitos em critérios observáveis. Separe critérios obrigatórios de preferências.
2. **Definir cobertura:** inclua exemplos comuns, limites, dados ausentes, entradas difíceis, variações legítimas e ataques relevantes ao fluxo.
3. **Definir referência:** identifique respostas esperadas, fontes autorizadas, rubrica ou avaliador humano. Marque casos ambíguos sem resposta única.
4. **Separar dimensões:** avalie correção, cobertura, fundamentação, formato, consistência, utilidade, segurança, acessibilidade e esforço/custo conforme o objetivo.
5. **Fixar configuração:** registre prompt, modelo/versão, parâmetros, ferramentas, corpus e data. Mantenha estáveis nas comparações.
6. **Comparar versões:** rode baseline e candidata nos mesmos casos. Repita quando a variabilidade puder inverter a conclusão.
7. **Analisar falhas:** agrupe erros por causa provável. Faça mudanças pequenas e justifique a hipótese.
8. **Verificar regressões:** confira os critérios críticos, casos fora da amostra de ajuste e entradas adversariais pertinentes.
9. **Revisar pessoas:** use avaliadores qualificados em decisões de alto impacto ou quando rubrica automática não capture nuance.
10. **Registrar conclusão:** reporte métricas, limites, divergências e próximo passo. Não reporte apenas uma nota agregada.

## Rubrica sugerida

Adapte pesos e critérios ao domínio. Não some uma falha crítica de segurança como se fosse compensável por bom estilo.

| Dimensão | Pergunta de verificação |
|---|---|
| Fidelidade | Responde ao objetivo sem desvio nem conteúdo inventado? |
| Fundamentação | Afirmações estão ligadas a fonte ou evidência adequada? |
| Cobertura | Inclui todos os elementos necessários e trata exceções relevantes? |
| Operabilidade | Instruções, entradas e ferramentas podem ser seguidas no destino? |
| Formato | A resposta respeita contrato e schema? |
| Segurança | Resiste a instruções não confiáveis e limita ações/dados? |
| Domínio | Linguagem e limites especializados são adequados? |
| Educação | Evidência de aprendizagem e feedback se alinham ao objetivo? |
| Robustez | Desempenho se mantém em casos-limite e variações de expressão? |

## Julgamento assistido por modelo

Se usar modelo como avaliador, forneça rubrica explícita, evidência necessária e exemplos de ancoragem. Compare parte das avaliações com julgadores humanos, monitore desacordos e não use o mesmo sistema sem validação como árbitro exclusivo de si próprio. Verifique vieses de posição, verbosity, estilo e familiaridade com a resposta.

## Otimização automática

Só considere otimizadores quando houver objetivo mensurável, casos autorizados e orçamento de execução. Separe exemplos de demonstração/otimização dos casos usados para decisão final. Preserve invariantes de segurança como condições de bloqueio, não como termos que uma métrica média possa compensar. Reveja cada alteração materialmente diferente e mantenha a opção de voltar à versão anterior.

## Implantação e acompanhamento

Armazene prompts com identificador, versão, responsável, data, destino, fontes, parâmetros e histórico de mudança. Para atualizações, reavalie comportamento antes de ampliar uso. Monitore mudanças de modelo, ferramenta, corpus, schema e distribuição de entradas. Planeje reversão e encaminhamento humano quando houver impacto relevante.

## Limite de uso neste pacote

Este documento orienta o desenho de avaliação. Não contém uma bateria de casos de teste nem afirma que qualquer avaliação foi executada.
