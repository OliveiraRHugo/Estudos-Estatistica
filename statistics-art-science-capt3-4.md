# Capítulo 3: Associação: Contingência, Correlação e Regressão
Este capítulo foca em métodos descritivos para estudar a associação entre duas variáveis, explorando como o valor de uma variável de resposta se relaciona com o valor de uma variável explicativa.

## 1. A Associação Entre Duas Variáveis Categóricas
  * Para resumir a associação entre duas variáveis categóricas, utilizam-se tabelas de contingência, que mostram as contagens de observações para as diversas combinações de categorias das variáveis.
  * As proporções ou porcentagens condicionais são usadas para comparar as distribuições da variável de resposta em diferentes categorias da variável explicativa.
  * Gráficos de barras lado a lado (side-by-side bar charts) e gráficos de barras empilhadas (stacked bar charts) são displays gráficos eficazes para visualizar essas relações .
  * Medidas como a diferença de proporções, a razão de proporções (risco relativo) e a razão de chances (odds ratio) descrevem a força da associação.
  * Exemplos notáveis incluem a análise de pesticidas em alimentos orgânicos  e a relação entre felicidade e renda familiar .

## 2. A Associação Entre Duas Variáveis Quantitativas
  * Para duas variáveis quantitativas, um gráfico de dispersão (scatterplot) é o display gráfico padrão, onde a variável de resposta (y) é plotada no eixo y e a variável explicativa (x) no eixo x .
  * O coeficiente de correlação (r) mede a força e a direção da associação linear entre as variáveis, variando de -1 a +1.
  * Exemplos abordam o uso da internet e do Facebook , e votos em eleições .

## 3 Previsão do Resultado de uma Variável
  * Uma linha de regressão (yn = a + bx) é usada para prever o valor de uma variável de resposta (y) a partir de uma variável explicativa (x).
  * O intercepto y (a) representa o valor previsto de y quando x é zero, e a inclinação (b) indica a mudança prevista em y para um aumento de uma unidade em x .
  * Resíduos são as diferenças entre os valores observados e previstos de y.
  * O quadrado do coeficiente de correlação (r²) descreve a proporção da variabilidade na variável de resposta que é explicada pela relação linear com a variável explicativa.

## Cuidados na Análise de Associações
  * Extrapolação, ou seja, fazer previsões muito além da faixa dos valores de x observados, é frequentemente não confiável .
  * Outliers e observações influentes podem distorcer significativamente a linha de regressão e o coeficiente de correlação .
  * A correlação não implica causalidade; variáveis ocultas (lurking variables) podem ser a verdadeira causa de uma associação observada.
  * O Paradoxo de Simpson é um fenômeno onde uma associação pode mudar de direção ou desaparecer quando uma terceira variável é controlada.
  * Aplicativos web como "Guess the Correlation" e "Explore Linear Regression" são introduzidos para permitir a interação com esses conceitos .

---

## Capítulo 4: Coleta de Dados
Este capítulo aborda a importância do planejamento cuidadoso do estudo para coletar dados que respondam a perguntas estatísticas de forma eficaz e evitar resultados enganosos .

### 1 Estudo Experimental Versus Observacional
  * Em um estudo observacional, o pesquisador observa os resultados em uma variável de resposta para sujeitos em grupos definidos por uma variável explicativa sem impor tratamentos .
  * Em um estudo experimental (experimento), o pesquisador atribui sujeitos a certas condições experimentais (tratamentos) e então observa os resultados .
  * Experimentos são geralmente preferidos quando viáveis, pois permitem inferência mais forte sobre a causalidade, controlando variáveis ocultas através da randomização .
  * Evidências anedóticas são consideradas não confiáveis para tirar conclusões .

### 2 Amostragem Aleatória
  * Uma amostra aleatória simples (AAS) garante que cada amostra possível de um dado tamanho tenha a mesma chance de ser selecionada .
  * Um quadro de amostragem é uma lista de todos os sujeitos na população .
  * Viéss (bias) podem ocorrer na amostragem:
      * Viés de amostragem (sampling bias) ocorre quando o método de amostragem favorece sistematicamente certos resultados (ex: amostras de conveniência, amostras voluntárias) .
      * Viés de resposta (response bias) ocorre quando os sujeitos fornecem respostas imprecisas .
      * Viés de não resposta (nonresponse bias) ocorre quando uma parte substancial dos sujeitos selecionados se recusa a participar .
  * Um tamanho de amostra grande não garante uma amostra não viciada se o método de amostragem for falho .
  * Os métodos comuns de coleta de dados incluem entrevistas pessoais, entrevistas por telefone e questionários .

### 3 Experimentação e Causalidade
  * A randomização na atribuição de tratamentos é crucial para equilibrar os grupos de comparação em relação a variáveis ocultas e para permitir inferências causais .
  * Um grupo de controle é usado para comparação, não recebendo o tratamento ativo .
  * Cegamento (blinding), onde os sujeitos (cego simples) ou ambos os sujeitos e os pesquisadores (duplo-cego) desconhecem o tratamento atribuído, ajuda a evitar vieses .
  * O efeito placebo é a resposta de um sujeito a um tratamento inativo .
  * Delineamentos experimentais incluem o delineamento completamente aleatorizado e o delineamento de pares combinados (matched-pairs design) . Um delineamento de blocos envolve a randomização dentro de blocos de sujeitos semelhantes .
  * A replicação de estudos aumenta a confiança nas conclusões .

### 4 Outros Delineamentos de Amostragem e Experimentais
  * Amostragem aleatória estratificada divide a população em estratos e coleta uma AAS de cada um .
  * Amostragem por conglomerados (cluster sampling) envolve a amostragem de conglomerados e a observação de todos os sujeitos nos conglomerados selecionados .
  * A amostragem aleatória sistemática seleciona cada k-ésimo sujeito de um quadro de amostragem .
  * A randomização é fundamental para a validade da inferência estatística .
  * A generalização das conclusões de um estudo depende do seu delineamento .
  * O aplicativo web "Random Numbers" é uma ferramenta para gerar números aleatórios para fins de amostragem .
  
---

Glossário dos Capítulo 3 e 4:
* Associação: Estudar como o valor de uma variável de resposta se relaciona com o valor de uma variável explicativa.
* Tabelas de contingência: Mostram as contagens de observações para as diversas combinações de categorias das variáveis.
* Coeficiente de correlação (r): Mede a força e a direção da associação linear entre duas variáveis quantitativas.
* Linha de regressão: Usada para prever o valor de uma variável de resposta (y) a partir de uma variável explicativa (x).
* Resíduos: As diferenças entre os valores observados e previstos de y.
* Estudo observacional: O pesquisador observa os resultados em uma variável de resposta para sujeitos em grupos definidos por uma variável explicativa sem impor tratamentos .
* Estudo experimental (experimento): O pesquisador atribui sujeitos a certas condições experimentais (tratamentos) e então observa os resultados .
* Amostra aleatória simples (AAS): Garante que cada amostra possível de um dado tamanho tenha a mesma chance de ser selecionada .
* Viéss (bias): Podem ocorrer na amostragem, como Viés de amostragem, Viés de resposta ou Viés de não resposta .
* Randomização: Crucial para equilibrar os grupos de comparação em relação a variáveis ocultas e para permitir inferências causais, especialmente em experimentos .
* Cegamento (blinding): Ajuda a evitar vieses, onde os sujeitos (cego simples) ou ambos os sujeitos e os pesquisadores (duplo-cego) desconhecem o tratamento atribuído .
* Efeito placebo: A resposta de um sujeito a um tratamento inativo .
* Variáveis ocultas (lurking variables): Podem ser a verdadeira causa de uma associação observada, onde correlação não implica causalidade.
* Paradoxo de Simpson: Fenômeno onde uma associação pode mudar de direção ou desaparecer quando uma terceira variável é controlada
