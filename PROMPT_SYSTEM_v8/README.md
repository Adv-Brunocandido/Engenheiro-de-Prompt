# PROMPT SYSTEM v8

Agente modular para criar, revisar, auditar, refatorar e compilar prompts para diferentes modelos e contextos.

## Comece por aqui

1. Leia `05_MANUAL/MANUAL_DE_USO.md` para instalar e operar o sistema.
2. Antes de substituir uma versão anterior, leia `05_MANUAL/COMPARATIVE_READINESS_V7_V8.md` e faça a comparação no destino real.
3. Para o runtime, use os cinco arquivos de `00_RUNTIME` na ordem numérica.
4. Carregue módulos, políticas e schemas somente quando a tarefa exigir.
5. Preserve os arquivos em `sources/` do projeto de origem como referências somente de leitura. Este pacote é uma edição nova e independente.

## Estrutura

```text
PROMPT_SYSTEM_v8/
  00_RUNTIME/
    01_L0_KERNEL.md
    02_L1_CORE.md
    03_L2_OPERATIONAL.md
    04_ORCHESTRATOR_PROMPT.md
    05_PROMPT_COMPILER.md
  01_MODULES/
    L3_MODULES.md
    DOMAIN_PACK_LEGAL_JUDICIAL.md
    DOMAIN_PACK_EDUCATIONAL.md
    ADVANCED_PROMPT_ENGINEERING.md
    PROMPT_TYPE_PROFILES.md
  02_SCHEMAS/
    OUTPUT_SCHEMAS.json
  03_POLICIES/
    FAIL_STATES.md
    PAS_DSL.md
    EVALUATION_FRAMEWORK.md
  05_MANUAL/
    MANUAL_DE_USO.md
    COMPARATIVE_READINESS_V7_V8.md
    SOURCE_TRACEABILITY.md
    TECHNOLOGY_REFERENCES.md
```

## Ordem e classificação

| Camada | Arquivos | Uso |
|---|---|---|
| Runtime obrigatório | L0, L1, L2, Orquestrador, Compilador | Instruções centrais do agente |
| Módulos | L3, tecnologia avançada, perfis de tarefa e pacotes de domínio | Carregamento condicional |
| Contratos | Schemas e fail states | Quando houver saída estruturada, risco ou auditoria |
| Avaliação e DSL | Framework de avaliação e PAS-DSL | Quando houver otimização, validação ou formalização |
| Documentação humana | Manual e rastreabilidade | Nunca inserir no runtime normal |

O agente deste pacote projeta prompts. Ele não executa automaticamente o trabalho especializado descrito nos prompts que cria.

## Princípios de montagem

- Comece com o menor conjunto de instruções que cobre a tarefa.
- Produza um prompt único para tarefas simples e uma arquitetura modular apenas quando ela trouxer manutenção, segurança ou reutilização concretas.
- Não invente detalhes de implantação, ferramentas, fontes, regras de negócio ou autoridade jurídica.
- Declare pressupostos relevantes e lacunas que alterem o comportamento do prompt.
- Não trate estimativas de tokens como limites garantidos. Ajuste o tamanho ao limite real informado para a plataforma-alvo.
- Consulte `SOURCE_TRACEABILITY.md` para ver como as referências foram consolidadas e quais conflitos foram resolvidos.
