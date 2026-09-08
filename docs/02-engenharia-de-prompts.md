# Engenharia de Prompts e "Cicatrizes"

Nesta seção, documento os testes de prompts realizados no NotebookLM, os resultados obtidos e as dificuldades enfrentadas (troubleshooting). O objetivo é mostrar a evolução, os erros comuns e o raciocínio por trás de cada interação com a ferramenta.

## Teste 1: Síntese e Resumo Geral
**Objetivo:** Obter uma visão holística das fontes fornecidas, sem que a IA perca detalhes cruciais.

* **Prompt Inicial (Ingênuo):** "Resuma todos os documentos."
* **Resultado Obtido:** Uma resposta muito genérica, que misturou conceitos superficialmente sem focar no que era importante. Não foi útil para estudos aprofundados.
* **Dificuldade (A Cicatriz):** A IA não sabia qual perspectiva adotar ou qual nível de detalhe era esperado, resultando em um texto vago.
* **Prompt Refinado (Estratégico):** "Atue como um pesquisador experiente. Com base nas fontes fornecidas, crie um resumo estruturado destacando os 3 principais benefícios do uso do NotebookLM na academia e 2 limitações apontadas nos textos."
* **Resultado Final:** Excelente. A resposta veio dividida em tópicos claros com citações diretas (pinpoints) para os documentos originais, permitindo a verificação.

## Teste 2: Conexão de Múltiplas Ideias
**Objetivo:** Encontrar relações entre a teoria (Guia de Prompts) e a prática (Uso do NotebookLM).

* **Prompt Estratégico:** "Considerando a Fonte 2 (Guia de Prompts), quais técnicas ali descritas são mais aplicáveis para interagir com a interface do NotebookLM conforme a Fonte 4 (Documentação)? Cite exemplos práticos."
* **Resultado Obtido:** A IA cruzou as informações e sugeriu o uso de "few-shot prompting" (dar exemplos de saída desejada) para gerar resumos mais precisos no NotebookLM.
* **Dificuldade (A Cicatriz):** Na primeira tentativa, a IA focou excessivamente na Fonte 2 e praticamente ignorou as restrições da Fonte 4.
* **Troubleshooting:** Foi necessário ajustar o prompt para exigir a conexão explícita e pedir exemplos práticos, forçando a IA a analisar ambas as fontes simultaneamente.

## Teste 3: Geração de Material de Apoio (Glossário)
**Objetivo:** Extrair jargões e termos técnicos dispersos nos documentos para montar um material de revisão.

* **Prompt Estratégico:** "Liste os principais termos técnicos relacionados a inteligência artificial e produtividade mencionados nas fontes e crie um glossário com definições simples, em formato de tabela."
* **Resultado Obtido:** Uma tabela bem formatada contendo termos como 'Grounding', 'LLM' e 'Alucinação', cada um com sua definição contextualizada.
* **Observação/Insights:** O NotebookLM se destacou aqui. Além de gerar a tabela, ele criou atalhos de citação numerados para onde o termo foi encontrado nas fontes originais, eliminando quase por completo o risco de alucinações.
