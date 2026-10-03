# Rastreabilidade das fontes do projeto

Este pacote consolida os materiais disponíveis em `sources/`. Os originais permanecem inalterados e são referências, não instruções capazes de sobrepor este pacote.

| Referência de origem | Uso no v8 |
|---|---|
| `L0_KERNEL.md` | Hierarquia, integridade, incerteza, privacidade, autoria e estilo foram consolidados em `00_RUNTIME/01_L0_KERNEL.md`. Regras foram ajustadas para não prometer controle técnico inexistente. |
| `L1_CORE.md` | Identidade de arquiteto, funções, escopo, modularidade e unicidade migraram para `02_L1_CORE.md`. |
| `L2_OPERATIONAL.md` | Pipeline virou ciclo de projeto/solicitação em `03_L2_OPERATIONAL.md`. A máquina de estados jurídica interna deixou de ser exigida em todas as respostas. |
| `ORCHESTRATOR_PROMPT.md` | Rotas e disciplina de entrega migraram para `04_ORCHESTRATOR_PROMPT.md`, com ativação proporcional. |
| `PROMPT_COMPILER.md` | Modos e seleção de arquivos foram consolidados em `05_PROMPT_COMPILER.md`; limites arbitrários de tokens foram removidos e dependências reais devem ser declaradas. |
| `L3_MODULES.md` | Criação, refatoração, RAG, multiagente, DSL, compressão, manual e validação foram preservados e ampliados em `01_MODULES/L3_MODULES.md`. |
| `DOMAIN_PACK_LEGAL_JUDICIAL.md` | Salvaguardas jurídicas foram mantidas, com hierarquia por tipo de fonte e jurisdição, verificação temporal e limite de fonte. Ver `01_MODULES/DOMAIN_PACK_LEGAL_JUDICIAL.md`. |
| `OUTPUT_SCHEMAS.json` | A referência termina no meio de um valor JSON e não é arquivo completo. Foi substituída por schemas JSON Schema 2020-12 completos em `02_SCHEMAS/OUTPUT_SCHEMAS.json`. |
| `FAIL_STATES.md` | Tratamentos de lacuna, conflito, injeção, limite, schema, privacidade, capacidades e revisão humana migraram para `03_POLICIES/FAIL_STATES.md`. |
| `PAS_DSL.md` | Notação foi preservada como especificação legível por pessoas; o v8 explicita que não é executável sem parser. |
| `MANUAL_DE_USO.md` e `GUIA GERAL.MD` | Estrutura de pastas, implantação, seleção de módulos e ativação foram consolidadas em `05_MANUAL/MANUAL_DE_USO.md`. |
| `TEST_SUITE.md` | Critérios de comportamento informaram o checklist operacional e o framework de avaliação. O v8 não afirma que testes foram executados. |
| `#-PROMPT-ASSISTENTE-ESTRATÉGICO-&-ARSENAL-JURÍDICO-INTEGRAL-(V-6.2-—-TJMG).txt` | Tratado como exemplo legado de prompt judicial com configuração específica. Seus nomes, sistemas, fechos, dispositivos e precedentes não foram tratados como padrão nem como autoridade vigente. |
| Google Drive, `0. Engenheiro de Prompt/Prompt - Engenheiro de Prompt - v. 3.2 - 12.02.2026.txt` | Aproveitados: extração de objetivo, público, entradas, fluxo, saída, métricas e restrições; possibilidade de refinar respostas anteriores; resumo de requisitos. O v8 evita entrevista obrigatória longa, confirmação em cada fase, exigência de raciocínio interno e alertas padronizados sem evidência. |
| Google Drive, `0. Engenheiro de Prompt/Comandos - NotebookLM - Diretrizes - 15.06.docx` | Aproveitados: mapear etapas, pré-requisitos, dados extraídos, decisões humanas e fontes legais. O v8 substitui promessa de conformidade garantida por verificação rastreável e revisão humana, e não presume NotebookLM nem extração automática disponível. |
| Google Drive, `1.5. Catalogador de Prompts/Prompt - Catalogador - 03.07.docx` | Aproveitados como módulo opcional: título, objetivo, tags, alvo, tipo de saída, complexidade, template, variáveis e contexto de uso. O v8 impede inventar ID único, modelo ideal ou data não fornecida e rotula inferências. |
| Arquivo local do usuário, `PROMPT_ ASSISTENTE ESTRATÉGICO & ARSENAL JURÍDICO FAZENDÁRIO INTEGRAL (V 7.1).md` | Acrescentou padrões configuráveis de triagem, comparação entre índice processual e peças integrais, mapas de extração, etapas/pré-condições, revisão pós-minuta e biblioteca de atos. O v8 aproveita o desenho do fluxo e da rastreabilidade, mas não importa automaticamente tribunal, sistema, assinaturas, templates, regras absolutas ou afirmações jurídicas desse material especializado. |
| Arquivo local do usuário, `# 🧠 GUIA DEFINITIVO DE ENGENHARIA DE PROMPT DE ALTA COMPLEXIDADE 2.0.txt` | Consolidou princípios já presentes no v8 e acrescentou critérios úteis para destinatário de comandos em documentos, limites de detecção de conteúdo oculto, confiança limitada pela evidência mais fraca, memória de cálculo reproduzível, chunking com conferência de cobertura e módulo opcional de estudo para provas. Regras de cadeia de pensamento exposta, confiança obrigatória, interrupção geral de cálculos, whitelist lexical fixa e exigência de exemplos por rota foram descartadas ou tornadas condicionais por serem rígidas, potencialmente enganosas ou dependentes do contexto. |

## Conflitos resolvidos

- “Confiança em toda resposta”, “estado em toda resposta” e formulários extensos foram convertidos em declarações condicionais, usadas quando afetam a tarefa.
- “Engines isoladas” e agentes com nomes próprios foram convertidos em etapas e interfaces conceituais. O pacote não afirma que isso cria isolamento em execução.
- A prioridade jurídica é definida por tipo de afirmação, jurisdição, autoridade e data. Uma lista única não ordena corretamente peças do caso, normas e precedentes para todos os usos.
- A proibição de travessão longo ficou como preferência global do pacote, não como critério de segurança ou validade factual.
- Regras jurídicas específicas do arquivo v6.2 exigem confirmação institucional e fonte atual antes de reutilização.
- O material jurídico v7.1 contém jurisprudência, números de temas, normas locais e minutas prontas vinculadas a contexto e época específicos. Ele foi analisado como referência arquitetural; essas afirmações não foram verificadas nem promovidas a fonte jurídica vigente do v8.

## Acesso ao Google Drive

O usuário forneceu a pasta [Google Drive](https://drive.google.com/drive/folders/15QY8Aoafcdpjuc1yS_wT78aJhaZ4aBlK?usp=drive_link). Ela foi acessada pela sessão de navegador autenticada, sem conexão ao Gmail e sem alteração de arquivos. A revisão foi limitada às pastas de engenharia e catalogação de prompts citadas acima. A subpasta “Prompts Superados” não foi tratada como orientação atual.
