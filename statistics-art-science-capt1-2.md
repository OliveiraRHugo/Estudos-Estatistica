# A Arte e Ciência de Aprender com Dados
---

## Capítulo 1: Estatística: A Arte e Ciência de Aprender com Dados

### 1. O que é Estatística?
  *  É a ciência de **aprender a partir de dados**. **Nos ajuda a planejar estudos e a analisar informações, visando a tomada de boas decisões diante da incerteza**.

### 2. Três Componentes Principais da Estatística:
  * Planejamento (Design): Esta é a fase de definir o objetivo ou a pergunta estatística de interesse e planejar como obter os dados que a responderão.
  * Descrição (Description): Consiste em resumir e analisar os dados coletados. Os resumos geralmente incluem gráficos e números, como médias e porcentagens. A estatística descritiva é útil mesmo quando temos dados de toda a população (por exemplo, em um censo).
  * Inferência (Inference): É o processo de tomar decisões e fazer previsões sobre uma população maior com base nos dados de uma amostra.

### 3. Amostra vs. População
  * População: Refere-se a todos os sujeitos de interesse em um estudo. Por exemplo, todos os 9,5 milhões de eleitores que votaram em uma eleição.
  * Amostra: É um subconjunto da população. Por exemplo, 3.889 eleitores pesquisados em uma pesquisa de boca de urna.
  * Parâmetros: São as medidas que resumem uma característica de uma população. Eles são geralmente desconhecidos e, em capítulos posteriores, serão denotados por letras gregas (como μ para a média da população ou σ para o desvio padrão da população).
  * Estatísticas: São as medidas que resumem uma característica de uma amostra.

### 4. Significância Estatística
Os resultados de um estudo são considerados estatisticamente significativos se eles raramente seriam observados apenas pela variação aleatória comum. Em outras palavras, a diferença observada é provavelmente devido a um efeito real e não apenas ao acaso.

### 5. O Papel da Tecnologia
Calculadoras e softwares estatísticos (como MINITAB, JMP, StatCrunch, SPSS, R e calculadoras TI) são ferramentas populares para realizar análises.
  * Arquivos de dados: Organizam grandes conjuntos de dados em formato de planilha, com cada linha representando um sujeito e cada coluna uma característica.
  * Web apps: São ferramentas interativas baseadas na web que ajudam a entender conceitos estatísticos e realizar inferências.

É crucial entender que, embora a tecnologia faça os cálculos, você precisará de uma boa base em estatística para saber qual método usar, quais opções escolher e como interpretar e tirar conclusões válidas da saída do computador [17, 25].

### 6. A Importância de Pensar Estatisticamente
A estatística é uma arte e uma ciência. O objetivo é formar alunos estatisticamente alfabetizados, que desenvolvam a alfabetização estatística e a capacidade de pensar estatisticamente [28]. Isso significa enfatizar a compreensão conceitual, usar dados reais e promover a aprendizagem ativa [29].

---

## Capítulo 2: Explorando Dados com Gráficos e Resumos Numéricos

### 1. Diferentes Tipos de Dados (Variáveis)
As variáveis são características que variam entre os sujeitos. Podemos classificá-las em dois tipos principais:
  * Variável Categórica: As observações se encaixam em um conjunto de categorias.
    * Exemplos: Gênero, grupo étnico-racial, filiação partidária, estado civil.
* Variável Quantitativa: Assume valores numéricos que representam diferentes magnitudes.
    * Discreta: Tem valores possíveis separados (como números inteiros para contagens). Exemplo: Número de filhos [35].
    * Contínua: Seus valores possíveis formam um intervalo. Exemplo: Idade (em anos), GPA da faculdade, horas assistindo TV [20]. Dados contínuos podem ser registrados como números inteiros, mas ainda são analisados como contínuos [36].

### 2. Resumos Gráficos de Dados
Gráficos são uma maneira poderosa de visualizar e entender a distribuição de uma variável.
  * **Para Variáveis Categóricas**:
    * Gráfico de Barras (Bar Graph): Usa barras para exibir as proporções ou frequências de cada categoria [38, 39]. Pode ser usado para comparar duas variáveis categóricas (gráficos de barras lado a lado ou empilhados) [39, 40].
    * Gráfico de Pizza (Pie Chart): Mostra as categorias como fatias de um círculo, representando suas proporções em relação ao todo [38].
    * Gráfico de Pareto (Pareto Chart): É um gráfico de barras que ordena as categorias por frequência, da maior para a menor [41].
* **Para Variáveis Quantitativas**:
    * Gráfico de Pontos (Dot Plot): Exibe cada observação individual como um ponto acima de uma linha numérica [36, 42]. Útil para conjuntos de dados pequenos, pois permite reconstruir os dados originais [43].
    * Gráfico de Caule e Folhas (Stem-and-Leaf Plot): Semelhante ao gráfico de pontos, separa cada valor em "caule" (dígitos iniciais) e "folha" (último dígito) [44, 45]. Também permite ver as observações individuais [46].
    * Histograma (Histogram): Usa barras para exibir as frequências das observações dentro de intervalos (ou "bins") de valores [46, 47].
      * Diferença do Gráfico de Barras: Histogramas são para variáveis quantitativas, enquanto gráficos de barras são para variáveis categóricas [48].
      * Intervalos: Para variáveis contínuas ou discretas com muitos valores, os dados são agrupados em intervalos de largura igual [48, 49]. Geralmente, 5 a 10 intervalos são adequados [50].
      * Altura das Barras: Representa a frequência (ou frequência relativa/porcentagem) das observações em cada intervalo [48, 50].
      * Convenção de Ponto Final à Esquerda: Se uma observação cair exatamente no limite entre dois intervalos, ela pertence ao intervalo onde é o ponto final esquerdo [51].

### 3. Formas das Distribuições
Ao analisar gráficos, observe a forma da distribuição:
* Simétrica: A distribuição é espelhada em torno de seu centro [52].
* Assimétrica à Direita (Skewed to the Right): A cauda da distribuição se estende mais para os valores mais altos (à direita) [21, 52-55]. Nesses casos, a média é geralmente maior que a mediana.
* Assimétrica à Esquerda (Skewed to the Left): A cauda da distribuição se estende mais para os valores mais baixos (à esquerda) [21, 52, 54, 55]. Nesses casos, a média é geralmente menor que a mediana.
* Bimodal: A distribuição tem dois "montes" ou picos distintos [25].

### 4. Resumos Numéricos: Medidas de Centro
* Média (Mean - $\bar{x}$): É a soma de todas as observações dividida pelo número total de observações [56]. A média da população é denotada por μ [14]. É sensível a valores extremos (outliers) [57].
* Mediana (Median): É o valor do meio quando os dados são ordenados do menor para o maior [56]. Metade das observações são menores ou iguais à mediana, e metade são maiores ou iguais [56]. É resistente a outliers [57, 58].
* Moda (Mode): É o valor (ou valores) que aparece com mais frequência na distribuição [57].

### 5. Resumos Numéricos: Medidas de Variabilidade (Dispersão)
* Amplitude (Range): É a diferença entre o valor máximo e o valor mínimo dos dados [38]. É uma medida simples, mas sensível a extremos.
* Desvio Padrão (Standard Deviation - s): Mede a variabilidade típica das observações em torno da média [36, 38]. Um desvio padrão maior indica maior dispersão dos dados [36]. O desvio padrão da população é denotado por σ [14].
    * Regra Empírica (Empirical Rule): Para distribuições em forma de sino (aproximadamente normais), cerca de 68% das observações estão dentro de 1 desvio padrão da média, 95% dentro de 2 desvios padrão e quase todas (99.7%) dentro de 3 desvios padrão [43, 44, 59].
* Amplitude Interquartil (Interquartile Range - IQR): É a diferença entre o terceiro quartil (Q3) e o primeiro quartil (Q1) (IQR = Q3 - Q1) [49, 60]. Representa a amplitude dos 50% centrais dos dados e é resistente a outliers.

### 6. Medidas de Posição e Identificação de Outliers
* Quartis (Quartiles): Dividem os dados ordenados em quatro partes iguais [49, 60].
    * Q1 (Primeiro Quartil): O valor abaixo do qual 25% dos dados se encontram [49].
    * Q2 (Segundo Quartil): É a mediana, o valor abaixo do qual 50% dos dados se encontram [49, 60].
    * Q3 (Terceiro Quartil): O valor abaixo do qual 75% dos dados se encontram [49].
* Cinco Números Resumo (Five-Number Summary): Consiste no Mínimo, Q1, Mediana, Q3 e Máximo [61, 62].
* Outliers: São observações que se desviam significativamente do padrão geral dos dados [61, 62]. Uma regra comum para identificar potenciais outliers é: valores que estão mais de 1.5 * IQR abaixo de Q1 ou acima de Q3 [61-64].
* Z-score: Indica o número de desvios padrão que uma observação está da média [65-67]. Um z-score com valor absoluto grande (por exemplo, |z| > 3) pode indicar um outlier [65].

### 7. Box Plot (Gráfico de Caixa)
O Box Plot é um gráfico que resume visualmente o cinco números resumo e mostra potenciais outliers [61, 62, 68]. A caixa central representa os 50% centrais dos dados (de Q1 a Q3), com uma linha dentro indicando a mediana. Os "bigodes" se estendem da caixa até os valores mínimo e máximo que não são considerados outliers. Outliers são marcados separadamente (geralmente com asteriscos) [62, 68].

### 8. Reconhecendo e Evitando Maus Usos de Resumos Gráficos
Gráficos mal construídos podem enganar [69, 70]. Para gráficos eficazes, siga estas diretrizes:
* Rótulos Claros: Sempre rotule ambos os eixos e forneça um título claro [71].
* Eixo Vertical a Partir do Zero: O eixo vertical deve começar em 0 para comparações visuais precisas [71].
* Clareza e Simplicidade: Evite figuras que distorçam as proporções ou que sejam difíceis de interpretar [70, 72].
### 9. Tecnologia para Resumos
Softwares estatísticos e calculadoras gráficas facilitam a construção de gráficos e resumos numéricos [61]. O foco deve ser na interpretação da saída, e não nos passos de teclado para gerá-los [73].
---

Glossário dos Capítulo 1 e 2:

* Estatística: A arte e ciência de aprender a partir de dados [1, 2].
* Dados: Informações coletadas para um estudo [4, 30].
* População: O grupo total de indivíduos ou objetos de interesse em um estudo [4, 11].
* Amostra: Um subconjunto da população, coletado para obter informações sobre a população [4, 11].
* Parâmetro: Uma medida numérica que descreve uma característica da população [4, 13].
* Estatística (medida amostral): Uma medida numérica que descreve uma característica da amostra [4, 13].
* Planejamento (Design): A fase de planejamento de um estudo para coletar dados [4, 8].
* Estatística Descritiva (Description): Métodos para resumir e analisar dados coletados (gráficos, médias, porcentagens) [4, 8].
* Estatística Inferencial (Inference): Métodos para tomar decisões e fazer previsões sobre uma população com base nos dados de uma amostra [4, 8].
* Significância Estatística: Ocorre quando os resultados observados em uma amostra são tão extremos que dificilmente aconteceriam por variação aleatória, sugerindo um efeito real na população [15, 17].
* Arquivo de Dados: Um conjunto de dados organizado em formato de planilha, com linhas para sujeitos e colunas para características [17, 18].
* Variabilidade: A extensão em que os valores de uma característica ou medida diferem entre os sujeitos ou ao longo do tempo [31].
* Variável Categórica: Variável cujas observações pertencem a categorias [8, 32].
* Variável Quantitativa: Variável que assume valores numéricos que representam magnitudes [8, 32].
* Variável Discreta: Variável quantitativa com valores possíveis separados (ex: 0, 1, 2...) [32, 33].
* Variável Contínua: Variável quantitativa cujos valores possíveis formam um intervalo [32, 33].
* Distribuição: A forma como os valores de uma variável se espalham, incluindo seus valores possíveis e suas frequências [32, 34].
* Frequência: O número de vezes que um determinado valor ou categoria ocorre [33, 48].
* Gráfico de Pizza: Gráfico para variáveis categóricas que mostra as proporções das categorias em um círculo [38].
* Gráfico de Barras: Gráfico para variáveis categóricas que usa barras para representar as frequências ou proporções das categorias [38].
* Gráfico de Pareto: Gráfico de barras para variáveis categóricas, onde as barras são ordenadas por frequência decrescente [41].
* Gráfico de Pontos (Dot Plot): Gráfico para variáveis quantitativas que mostra cada observação como um ponto acima de uma linha numérica [36].
* Gráfico de Caule e Folhas (Stem-and-Leaf Plot): Gráfico para variáveis quantitativas que organiza os dados separando cada valor em um "caule" e uma "folha" [44].
* Histograma: Gráfico para variáveis quantitativas que usa barras para exibir as frequências de observações dentro de intervalos de valores [46, 47].
* Forma Simétrica: Distribuição onde os lados esquerdo e direito são imagens espelhadas um do outro [52].
* Assimétrica à Direita (Skewed to the Right): Distribuição com uma cauda mais longa para os valores mais altos [21].
* Assimétrica à Esquerda (Skewed to the Left): Distribuição com uma cauda mais longa para os valores mais baixos [21].
* Bimodal: Distribuição que apresenta dois picos ou modas [25].
* Outlier: Uma observação que está muito distante dos outros valores de um conjunto de dados [61, 62].
* Média (Mean): O valor médio de um conjunto de dados [56].
* Mediana (Median): O valor do meio em um conjunto de dados ordenado [56].
* Moda (Mode): O valor mais frequente em um conjunto de dados [57].
* Amplitude (Range): A diferença entre o valor máximo e o valor mínimo em um conjunto de dados [38].
* Desvio Padrão (Standard Deviation): Uma medida da dispersão dos dados em torno da média [38].
* Regra Empírica: Descreve a proporção de dados dentro de 1, 2 e 3 desvios padrão da média em distribuições em forma de sino [43, 44].
* Quartis (Quartiles): Três valores (Q1, Q2, Q3) que dividem um conjunto de dados ordenado em quatro partes iguais [49].
* Amplitude Interquartil (Interquartile Range - IQR): A diferença entre o terceiro e o primeiro quartil (Q3 - Q1), representando a amplitude dos 50% centrais dos dados [49].
* Cinco Números Resumo (Five-Number Summary): Os valores mínimo, Q1, mediana, Q3 e máximo de um conjunto de dados [61].
* Z-score: Uma medida padronizada que indica quantos desvios padrão uma observação está da média [65, 66].
* Box Plot (Gráfico de Caixa): Uma representação gráfica do cinco números resumo, útil para visualizar a distribuição e identificar outliers [61, 68].
