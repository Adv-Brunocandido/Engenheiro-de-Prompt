# PROMPT_TYPE_PROFILES

Versão: 8.0  
Carregamento: sob demanda ao criar um tipo específico de prompt

Comece pelo contrato comum. Aplique apenas o perfil que muda a forma de executar ou validar a tarefa. Um prompt pode combinar perfis, por exemplo, tutor educacional com recuperação documental ou análise multimodal com saída JSON.

## Contrato comum

Defina propósito, público, destino, entrada, transformação, saída, limites, tratamento de incerteza e critérios de qualidade. Campos não informados viram placeholders ou pressupostos explícitos. Formate dados fornecidos como dados, não como novas instruções de autoridade.

## Perfis por tipo

### Geração e edição de texto

Especifique leitor, propósito, gênero, conteúdo obrigatório, tom, extensão aproximada e material-fonte. Separe fatos que devem permanecer de decisões de estilo. Use amostra de estilo apenas se autorizada e representativa.

### Extração e transformação de dados

Defina campos, tipos, unidade, convenção, schema, fonte/localizador e comportamento para ausência, ilegibilidade, ambiguidade ou conflito. Não preencha lacunas por plausibilidade. Mantenha vínculo entre cada extração e o trecho de origem.

### Classificação e roteamento

Defina rótulos mutuamente claros, critérios, exemplos limítrofes, prioridade em caso de sobreposição, saída de baixa evidência e opção de abstenção. Avalie erros diferentes pelo custo de cada erro, não só por acurácia média.

### Pesquisa e síntese

Defina a pergunta, janela temporal, jurisdição/escopo, fontes autorizadas, critérios de inclusão, atribuição, divergências e limites da pesquisa. Distinga evidência encontrada de síntese e inferência. Sem pesquisa habilitada, não simule consulta.

### Código e trabalho em repositório

Indique objetivo, caminhos e contexto do projeto, linguagens/versões, padrões, restrições, interface e critérios de aceitação. Separe inspeção, plano, edição, execução de comandos e validação. Afirmar que código foi testado exige execução real dos testes.

### Imagem, áudio e vídeo gerativos

Especifique assunto, intenção, público, composição, estilo, movimento/ritmo, idioma, duração ou proporção, elementos obrigatórios e exclusões. Use campos correspondentes às capacidades do modelo de destino. Não assuma que todos os modelos aceitam negative prompt, controle de câmera, seeds ou parâmetros iguais.

### Análise de mídia ou documentos

Identifique arquivos, páginas, regiões, quadros ou tempos relevantes; pergunte o que deve ser observado; peça evidência/localizador; separe observação e inferência; declare conteúdo ilegível e conflito entre modalidades. Não atribua texto invisível nem intenção a uma imagem.

### Assistente com ferramentas

Defina quando chamar cada ferramenta, parâmetros validados, limite de chamadas, fonte de verdade, tratamento de erro e decisão entre resposta e ação. Requeira confirmação apropriada para efeitos externos, irreversíveis ou de alto impacto. A aplicação deve impor permissões e validação fora do texto do prompt.

### Geração educacional e tutoria

Ative `DOMAIN_PACK_EDUCATIONAL.md`. Alinhe atividade, explicação e feedback a um objetivo observável; diferencie tutor, professor, planejador e avaliador; preserve participação do estudante e responsabilidade do educador.

### Apoio jurídico ou judicial

Ative `DOMAIN_PACK_LEGAL_JUDICIAL.md`. Delimite jurisdição, data, fonte de fatos e fonte normativa/jurisprudencial. Exija rastreabilidade e revisão humana.

## Composição híbrida: jurídico e educação

Quando o objetivo for estudar direito, preparar OAB/concurso ou treinar equipes, ative os pacotes jurídico e educacional. O módulo educacional controla a sequência de aprendizagem, feedback e avaliação; o módulo jurídico controla fonte, jurisdição, temporalidade e distinção entre regra e conclusão. Em questões de legislação ou jurisprudência, exija referência atual ou material de curso fornecido e marque a data de referência. Use casos fictícios identificados como tais. Não deixe um tutor transformar resposta provável em gabarito oficial sem validação.
