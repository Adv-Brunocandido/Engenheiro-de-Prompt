# PROMPT_COMPILER

## Objetivo

Montar a menor composição de instruções que preserve os requisitos do pedido. Este compilador é um procedimento de seleção para o agente, não um executável nem uma garantia de limite de tokens.

## Ficha de compilação

Preencha internamente os campos que estiverem disponíveis. Pergunte ou marque como pressuposto o que for relevante e ausente.

```text
TASK: objetivo do prompt
DOMAIN: geral, técnico, corporativo, educacional, institucional ou especializado
PROMPT_TYPE: texto, extração, classificação, pesquisa, código, mídia, educação, jurídico ou agente
AUDIENCE: quem configura e quem usa
TARGET: modelo, plataforma ou portátil
OUTPUT: prompt único, modular, auditoria, manual, DSL ou pacote
RISK: baixo, moderado, alto ou crítico
SOURCES: materiais autorizados e sua função
TOOLS: ferramentas realmente disponíveis no destino
MODALITIES: texto, imagem, áudio, vídeo, arquivos ou outras entradas reais
CONSTRAINTS: segurança, privacidade, linguagem, tamanho e operação
ACCEPTANCE: sinais observáveis de que o prompt atende ao pedido
TOKEN_LIMIT: limite informado, se houver
```

## Perfis de montagem

### FAST

Carregue L0, L1, L2 e Orquestrador. Use criação e validação essenciais. Entregue um prompt simples, sem schemas ou módulos que não alterem o comportamento.

### MODULAR

Carregue runtime, L3, fail states e schemas se houver saídas estruturadas. Divida o core, processo, módulos reutilizáveis e contratos de saída. Inclua manual apenas quando pedido ou necessário para implantação.

### EDUCATIONAL

Carregue `DOMAIN_PACK_EDUCATIONAL.md` e `ADVANCED_PROMPT_ENGINEERING.md` quando o prompt atuar como tutor, professor, planejador de aula, autor de avaliação ou gerador de feedback. Defina público/idade, objetivo de aprendizagem, conhecimento prévio, papel do educador, evidência de aprendizagem e política de integridade. Não trate uma técnica pedagógica como universal.

### AUDIT

Carregue runtime, módulos de auditoria/refatoração e fail states. Compare intenção com comportamento descrito, localize conflitos, lacunas, riscos, redundância e dependências. Preserve conteúdo útil e entregue a revisão solicitada.

### DOMAIN

Carregue runtime, L3, política de falhas e o pacote do domínio correspondente. Inclua somente fontes fornecidas ou explicitamente disponíveis. No domínio jurídico/judicial, nunca trate o prompt jurídico legado como autoridade normativa.

### DSL

Carregue runtime e PAS-DSL. Converta apenas regras que possam ser expressas sem perda material. Declare se o resultado é especificação para leitura ou se existe um parser executável no destino.

### PRODUCTION

Monte os arquivos que o destino realmente comporta: runtime essencial, módulos requeridos, schemas necessários, fail states e manual humano. Inclua manifesto de carregamento e pressupostos de implantação. Omita suites de teste do runtime.

## Seleção de componentes

| Componente | Selecione quando |
|---|---|
| `L3_MODULES.md` | Há arquitetura modular, auditoria ou especialização |
| `DOMAIN_PACK_LEGAL_JUDICIAL.md` | O prompt criado opera em função jurídica/judicial |
| `DOMAIN_PACK_EDUCATIONAL.md` | O prompt criado atua no ensino, tutoria, avaliação ou feedback |
| `ADVANCED_PROMPT_ENGINEERING.md` | A tarefa exige técnica especializada, multimodalidade, agente ou desenho de contexto |
| `PROMPT_TYPE_PROFILES.md` | O prompt se enquadra em um tipo específico ou combina tipos |
| `OUTPUT_SCHEMAS.json` | O usuário pede JSON ou validação estruturada |
| `FAIL_STATES.md` | Há risco, dependência crítica, auditoria ou necessidade de resposta a bloqueios |
| `EVALUATION_FRAMEWORK.md` | O usuário pede avaliação, comparação, otimização ou plano de qualidade |
| `PAS_DSL.md` | O usuário pede DSL ou a sintaxe compacta tem benefício claro |
| Manual | O pacote será instalado/operado por humanos ou o usuário o pede |

## Política de tamanho

Use o limite real fornecido. Preserve regras de segurança, objetivo, fluxo, dados e contrato de saída. Comprima explicações e exemplos primeiro. Se ainda exceder o limite, proponha dividir o pacote ou peça escolha sobre requisitos concorrentes. Não alegue contagem exata de tokens sem ferramenta de contagem compatível.

## Relatório de compilação

Inclua somente em pacote de produção, auditoria ou quando solicitado:

```text
BUILD: modo escolhido
TASK: objetivo resumido
FILES: arquivos incluídos
OPTIONAL: arquivos carregados sob demanda
OMITTED: componentes que não alteram o comportamento
ASSUMPTIONS: escolhas feitas por falta de dado
LIMITATIONS: capacidades ou fontes não confirmadas
```
