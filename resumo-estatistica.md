# Resumo do processo de análise estatítica

*Bibliografia de referência: Statistics the art and science of learning from data*

*Contexto de negócio utilizado para exemplos: Operações de uma padaria*

O processo de análise estatítica segue 4 etapas fundamentais:

1. **Pergunta Estatística** → 2. **Coleta de Dados** → 3. **Análise** → 4. **Interpretação**

### 🎯 Capítulo 1: Mentalidade Estatística para Negócios

**Problema Real na Padaria:** "Vale a pena continuar produzindo o novo pão 'Ciabatta Especial'?"

**Pergunta Estatística Transformada:** 
- *Qual é o número médio de unidades vendidas por dia?*
- *Há diferença significativa nas vendas entre dias úteis e fins de semana?*

```python
# Exemplo: Coletando dados básicos de vendas
import pandas as pd
import numpy as np

# Simulando dados de vendas por 30 dias
vendas_ciabatta = {
    'data': pd.date_range('2024-01-01', periods=30),
    'vendas': [45, 52, 48, 60, 55, 58, 42, 53, 61, 57, 
               49, 54, 59, 56, 50, 62, 47, 53, 58, 55,
               51, 49, 63, 56, 52, 59, 54, 57, 50, 61],
    'dia_semana': ['seg', 'ter', 'qua', 'qui', 'sex', 'sab', 'dom'] * 4 + ['seg', 'ter']
}

df_vendas = pd.DataFrame(vendas_ciabatta)
media_vendas = df_vendas['vendas'].mean()
print(f"Média de vendas: {media_vendas:.1f} unidades/dia")
```

---

## 📊 Análise Exploratória de Dados (AED)

### Capítulo 2: Entendendo Seus Dados

**Variáveis comuns em uma padaria:**
- **Quantitativas:** Tempo de espera, faturamento, peso do pão
- **Categóricas:** Tipo de pão, forma de pagamento, período do dia

```python
# Análise exploratória completa
import matplotlib.pyplot as plt
import seaborn as sns

# Dados de exemplo: tempo de espera na fila
tempos_espera = [2.5, 3.1, 1.8, 4.2, 2.9, 3.5, 2.1, 3.8, 2.7, 3.9,
                 2.3, 3.2, 1.9, 4.1, 2.8, 3.6, 2.2, 3.7, 2.6, 3.4]

print(f"Estatísticas descritivas:")
print(f"Média: {np.mean(tempos_espera):.2f} min")
print(f"Mediana: {np.median(tempos_espera):.2f} min")
print(f"Desvio padrão: {np.std(tempos_espera):.2f} min")

# Visualização
fig, (ax1, ax2) = plt.subplots(1, 2, figsize=(12, 4))

# Histograma
ax1.hist(tempos_espera, bins=8, alpha=0.7, color='skyblue')
ax1.set_xlabel('Tempo de Espera (min)')
ax1.set_ylabel('Frequência')
ax1.set_title('Distribuição do Tempo de Espera')

# Box plot
ax2.boxplot(tempos_espera)
ax2.set_ylabel('Tempo de Espera (min)')
ax2.set_title('Box Plot - Tempo de Espera')

plt.tight_layout()
plt.show()
```

---

## 🔗 Análise de Relacionamentos

### Capítulo 3: Correlações e Associações

**Problema:** "O preço do pão especial afeta as vendas?"

```python
# Análise de correlação entre preço e vendas
dados_correlacao = {
    'preco': [8.50, 8.00, 9.00, 8.20, 8.80, 8.30, 9.20, 8.60, 8.10, 8.90],
    'vendas': [45, 52, 38, 50, 42, 48, 35, 44, 51, 40]
}

df_correlacao = pd.DataFrame(dados_correlacao)
correlacao = df_correlacao['preco'].corr(df_correlacao['vendas'])
print(f"Correlação entre preço e vendas: {correlacao:.3f}")

# Gráfico de dispersão
plt.figure(figsize=(8, 5))
plt.scatter(df_correlacao['preco'], df_correlacao['vendas'], alpha=0.7)
plt.xlabel('Preço (R$)')
plt.ylabel('Vendas (unidades)')
plt.title('Relação entre Preço e Vendas do Pão Especial')
plt.grid(True, alpha=0.3)
plt.show()
```

---

## 📈 Inferência Estatística na Prática

### Capítulo 8: Estimando com Confiança

**Problema:** "Qual é o tempo médio real que clientes passam na padaria?"

```python
# Intervalo de confiança para tempo de permanência
from scipy import stats

# Amostra de 40 clientes
tempo_permanencia = np.random.normal(7.5, 3.0, 40)

n = len(tempo_permanencia)
media_amostral = np.mean(tempo_permanencia)
desvio_padrao = np.std(tempo_permanencia, ddof=1)  # ddof=1 para amostra

# Calculando intervalo de confiança 95%
erro_padrao = desvio_padrao / np.sqrt(n)
intervalo_confianca = stats.t.interval(0.95, df=n-1, loc=media_amostral, scale=erro_padrao)

print(f"Média amostral: {media_amostral:.2f} minutos")
print(f"Intervalo de 95% confiança: ({intervalo_confianca[0]:.2f}, {intervalo_confianca[1]:.2f}) minutos")
```

### Capítulo 9: Testes de Hipótese

**Problema:** "A nova campanha de marketing realmente aumentou as vendas?"

```python
# Teste A/B para campanhas de marketing
from scipy.stats import ttest_ind

# Dados das campanhas
vendas_antiga = np.random.normal(50, 8, 30)  # Campanha antiga
vendas_nova = np.random.normal(55, 8, 30)    # Campanha nova

# Teste t para duas amostras independentes
t_stat, p_value = ttest_ind(vendas_nova, vendas_antiga, alternative='greater')

print(f"Estatística t: {t_stat:.3f}")
print(f"Valor-p: {p_value:.4f}")

if p_value < 0.05:
    print("✅ Resultado significativo: A nova campanha aumentou as vendas!")
else:
    print("❌ Não há evidências suficientes: A campanha não teve efeito significativo")
```

---

## 🧠 Análises Avançadas para Tomada de Decisão

### Capítulo 12: Regressão Linear para Previsões

**Problema:** "Como prever o faturamento baseado no número de clientes?"

```python
from sklearn.linear_model import LinearRegression
from sklearn.metrics import r2_score

# Dados históricos
dados_regressao = {
    'clientes': [120, 150, 130, 180, 160, 140, 170, 190, 155, 165],
    'faturamento': [2400, 3000, 2600, 3600, 3200, 2800, 3400, 3800, 3100, 3300]
}

df_regressao = pd.DataFrame(dados_regressao)

# Modelo de regressão
X = df_regressao[['clientes']]
y = df_regressao['faturamento']

modelo = LinearRegression()
modelo.fit(X, y)

# Previsões
y_pred = modelo.predict(X)
r2 = r2_score(y, y_pred)

print(f"Coeficiente (slope): R$ {modelo.coef_[0]:.2f} por cliente")
print(f"Intercepto: R$ {modelo.intercept_:.2f}")
print(f"R²: {r2:.3f} ({r2*100:.1f}% da variabilidade explicada)")

# Previsão para 200 clientes
faturamento_previsto = modelo.predict([[200]])
print(f"Previsão para 200 clientes: R$ {faturamento_previsto[0]:.2f}")
```

### Capítulo 14: ANOVA para Comparação Múltipla

**Problema:** "Qual fornecedor de farinha produz os melhores pães?"

```python
from scipy.stats import f_oneway

# Dados de volume dos pães por fornecedor (em cm³)
fornecedor_A = [125, 128, 122, 130, 127, 124, 129, 126]
fornecedor_B = [118, 120, 115, 122, 119, 117, 121, 116]
fornecedor_C = [132, 135, 130, 137, 133, 131, 136, 134]

# Teste ANOVA
f_stat, p_value = f_oneway(fornecedor_A, fornecedor_B, fornecedor_C)

print(f"Estatística F: {f_stat:.3f}")
print(f"Valor-p: {p_value:.4f}")

if p_value < 0.05:
    print("✅ Há diferença significativa entre os fornecedores")
    # Para identificar qual é melhor, precisaríamos de teste post-hoc (Tukey)
else:
    print("❌ Não há diferença significativa entre os fornecedores")
```

---

## 💡 Framework de Decisão para Iniciantes

### Como Escolher a Análise Correta:

| Seu Problema de Negócio | Tipo de Análise Recomendada |
|------------------------|-----------------------------|
| **Comparar 2 grupos** (ex: duas campanhas) | Teste t, Teste de proporções |
| **Comparar 3+ grupos** (ex: múltiplos fornecedores) | ANOVA |
| **Prever valor numérico** (ex: faturamento) | Regressão Linear |
| **Verificar relacionamento** entre variáveis | Correlação |
| **Analisar categorias** (ex: preferência por pagamento) | Qui-Quadrado |
| **Estimar intervalo** (ex: tempo médio) | Intervalo de Confiança |

### 📝 Checklist do Analista Iniciante:

1. **Defina claramente** o problema de negócio
2. **Identifique** variáveis relevantes (o que medir)
3. **Escolha** a análise apropriada (use a tabela acima)
4. **Verifique premissas** da análise escolhida
5. **Interprete resultados** no contexto do negócio
6. **Comunique insights** de forma simples e clara

### Como exercitar estas habilidades?:

1. Comece com análises descritivas simples (médias, medianas)
2. Pratique visualizações básicas (histogramas, box plots)
3. Avance para testes de hipótese simples (teste t)
4. Explore correlações entre variáveis do seu negócio
5. Quando confortável, experimente modelos de regressão

Lembre-se: a análise de dados é um processo iterativo. Comece simples, valide seus resultados e gradualmente incorpore técnicas mais sofisticadas conforme ganha confiança!

**Dica Final:** Sempre conecte seus resultados estatísticos às decisões de negócio. Um valor-p significa pouco sem a pergunta de negócio que o originou.
