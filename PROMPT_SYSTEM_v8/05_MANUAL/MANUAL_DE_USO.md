# Manual de uso do PROMPT SYSTEM v8

## Para que serve

O pacote constrói prompts para vários domínios e tarefas. Ele atua como arquiteto de instruções: cria, melhora, audita, refatora e documenta prompts. Não executa por padrão as tarefas de domínio descritas no material que está projetando.

## Instalação sugerida

### Instruções centrais

Inclua, na ordem, os cinco arquivos de `00_RUNTIME`:

1. `01_L0_KERNEL.md`
2. `02_L1_CORE.md`
3. `03_L2_OPERATIONAL.md`
4. `04_ORCHESTRATOR_PROMPT.md`
5. `05_PROMPT_COMPILER.md`

Se o campo de instruções da plataforma não comportar tudo, mantenha L0, L1, L2 e o roteamento central nas instruções e disponibilize o compilador e os módulos como conhecimento consultável. Confira como o destino carrega arquivos antes de depender de ativação automática.

### Arquivos de conhecimento

Adicione `L3_MODULES.md`, `PROMPT_TYPE_PROFILES.md`, `ADVANCED_PROMPT_ENGINEERING.md`, os pacotes de domínio pertinentes, `OUTPUT_SCHEMAS.json`, `FAIL_STATES.md`, `PAS_DSL.md` e `EVALUATION_FRAMEWORK.md` como referências acionadas por necessidade.

`MANUAL_DE_USO.md`, `SOURCE_TRACEABILITY.md` e `TECHNOLOGY_REFERENCES.md` são documentação humana. Não os injete como instruções operacionais padrão.

## Solicitações de ativação

### Criar um prompt simples

```text
Crie um prompt para [objetivo], usado por [público], no destino [modelo/plataforma ou portátil].
Saída desejada: [formato].
Restrições: [limites importantes].
```

### Auditar e melhorar

```text
Audite e melhore o prompt abaixo. Preserve [requisitos], resolva conflitos, aponte pressupostos e entregue uma versão pronta para uso.
[cole o prompt]
```

### Criar um tutor educacional

```text
Crie um prompt de tutor para [disciplina/tema], etapa [ano/faixa], com objetivo [aprendizagem observável].
O tutor deve [estilo de apoio], considerar [materiais/acessibilidade] e seguir [política de avaliação e uso de IA].
```

### Criar um prompt jurídico

```text
Crie um prompt para [tarefa jurídica/judicial], na jurisdição [indicar], para uso por [público].
Fontes autorizadas: [listar]. Ferramentas disponíveis: [listar].
Saída: [formato]. Exija fonte para afirmações materiais, declare lacunas e encaminhe para revisão profissional.
```

### Pacote de produção

```text
Monte o pacote de produção para [objetivo]. Destino: [plataforma].
Inclua core, módulos necessários, contrato de saída, condições de falha e manual.
Limite informado: [se houver]. Indique pressupostos e capacidades não confirmadas.
```

## Como escolher o modo

- `FAST`: uma tarefa simples e baixo risco.
- `MODULAR`: várias funções, reutilização ou necessidade de manutenção.
- `AUDIT`: prompt existente para revisar.
- `DOMAIN`: domínio especializado, jurídico ou educacional.
- `DSL`: regra formal compacta.
- `PRODUCTION`: arquivos de implantação e documentação.

O agente deve escolher o modo se você não indicar um. Peça avaliação comparativa ou plano de avaliação quando precisar demonstrar qualidade. A criação do plano não significa que a avaliação foi executada.

## Boas práticas

- Informe o destino e suas ferramentas reais quando conhecidos.
- Dê fontes, critérios de qualidade, exemplos representativos e limites de dados.
- Compartilhe modelos institucionais com dados identificadores removidos quando possível.
- Em jurídico, especifique jurisdição, data/corte temporal e base de fontes autorizadas.
- Em educação, informe etapa, objetivo de aprendizagem, conhecimento prévio, acessibilidade e papel do professor.
- Para catalogar, diga se há registro central de IDs; sem ele, o agente deixará o ID como nulo/pendente.
- Evite pedir uma persona sofisticada sem definir comportamento observável.
- Peça que o pacote diferencie instruções de runtime e documentação humana.

## Atualização do pacote

Registre mudança de versão, motivo, arquivos afetados, pressupostos e evidência de validação. Revise referências técnicas dependentes de fornecedor antes de cada implantação. Não altere os arquivos originais de `sources/`; eles são referências somente de leitura.

Antes de substituir uma versão anterior, consulte `COMPARATIVE_READINESS_V7_V8.md`. Uma revisão de arquitetura não comprova desempenho. Para uma decisão de migração, compare versões no mesmo destino, com tarefas pareadas, rubrica comum e revisão especializada nos casos de alto impacto.
