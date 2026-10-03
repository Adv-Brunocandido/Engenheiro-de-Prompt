# PAS-DSL

Versão: 8.0  
Uso: notação compacta para especificar regras de prompts

PAS-DSL é uma convenção documental legível por humanos. Ela não é executável nem determinística por si só. Só chame uma regra de validada por máquina quando houver parser e verificação reais no destino.

## Estrutura de regra

```text
@rule ID {
  when: condição observável;
  action: ação específica;
  priority: CRITICAL | HIGH | NORMAL | LOW;
  requires: pré-condições opcionais;
  ensures: resultado esperado opcional;
  ref: regra/política relacionada opcional;
}
```

## Ações recomendadas

- `continue`: prossiga com a tarefa definida.
- `flag`: continue com ressalva visível.
- `hold`: não produza a parte dependente até obter dado/fonte/revisão.
- `block`: recuse a parte proibida e ofereça alternativa segura.
- `reroute`: use uma alternativa compatível com capacidades disponíveis.
- `ask`: formule pergunta curta sobre informação crítica.

## Exemplo

```text
@rule R017 {
  when: a plataforma não oferece validação nativa do schema;
  action: reroute para JSON textual e declarar validação externa pendente;
  priority: HIGH;
  ensures: nenhuma garantia de validade automática é prometida;
  ref: FS013_UNAVAILABLE_CAPABILITY;
}
```

## Conversão e revisão

1. Separe condição, ação e prioridade.
2. Use condição que possa ser observada em uma entrada ou resposta.
3. Defina ações compatíveis com a autoridade do agente.
4. Inclua comportamento quando a condição não puder ser determinada.
5. Compare a versão DSL com a regra em prosa para detectar perda semântica.
6. Adicione teste executável apenas quando houver pedido para criar/validar uma suite e ambiente capaz de executá-la.
