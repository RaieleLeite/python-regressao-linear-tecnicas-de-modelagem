# 🏘️ Análise de Preços de Imóveis com Regressão Linear

Este projeto realiza uma análise de dados do **mercado imobiliário do Rio de Janeiro**, aplicando o método de **Regressão Linear** para prever o preço de imóveis com base em variáveis como área, distância da praia e proximidade de farmácias.

---

## 📌 Objetivo do Projeto

O principal objetivo é desenvolver um modelo preditivo utilizando **Regressão Linear Simples e Múltipla**, com foco na:

- **Análise exploratória dos dados**;
- **Construção e interpretação de modelos de regressão**;
- **Avaliação da significância dos coeficientes**;
- **Interpretação estatística dos resultados**;
- **Validação das suposições da regressão linear**.

---

## 📊 Fonte dos Dados

- **Base utilizada**: amostra de 5000 imóveis à venda no município do **Rio de Janeiro**.
- **Formato**: CSV separado por `;`

### Variáveis no dataset:
| Variável         | Descrição                                        |
|------------------|--------------------------------------------------|
| `Valor`          | Preço do imóvel (em R$)                          |
| `Area`           | Área do imóvel (em m²)                           |
| `Dist_Praia`     | Distância até a praia mais próxima (em km)       |
| `Dist_Farmacia`  | Distância até a farmácia mais próxima (em km)    |

---

## 🛠️ Tecnologias e Bibliotecas Utilizadas

- [Python](https://www.python.org/)
- [Pandas](https://pandas.pydata.org/)
- [NumPy](https://numpy.org/)
- [Matplotlib](https://matplotlib.org/)
- [Seaborn](https://seaborn.pydata.org/)
- [Statsmodels](https://www.statsmodels.org/)

---

## 🔎 Etapas da Análise

### 1. Carregamento e inspeção dos dados
- Leitura do dataset
- Verificação do tamanho e tipos das variáveis
- Análise de dados ausentes

### 2. Análise Exploratória (EDA)
- Estatísticas descritivas
- Distribuições das variáveis com histograma
- Matriz de correlação para investigar relações lineares

### 3. Visualização Gráfica
- Gráficos de dispersão (`scatterplot`)
- Regressão linear visualizada com linha de tendência
- Boxplots para identificar outliers

### 4. 📐 Modelagem Estatística
- Regressão Linear Simples e Múltipla
- Estimativa dos coeficientes (β)
- Cálculo da reta de regressão

### 5. 📊 Teste de Hipóteses e Significância dos Parâmetros
- Interpretação dos **p-valores**
- Intervalos de confiança dos coeficientes
- Verificação das suposições:
  - Linearidade
  - Normalidade dos resíduos
  - Homocedasticidade (variância constante)
  - Ausência de multicolinearidade

### 6. ✅ Avaliação do Modelo
- **R² (Coeficiente de Determinação)**
- **MAE** (Erro Absoluto Médio)
- **MSE** (Erro Quadrático Médio)
- **RMSE** (Raiz do Erro Quadrático Médio)
- Análise dos resíduos

---

## 📈 Resultados Esperados

- Identificar quais variáveis têm maior impacto no **preço dos imóveis**;
- Interpretar a **significância estatística** de cada variável;
- Avaliar o **desempenho e aderência do modelo** às suposições da regressão;
- Sugerir possíveis melhorias no modelo com base nos resíduos e outliers.

---
## 🧪 Exemplo de Saída 

```
                            OLS Regression Results                            
==============================================================================
Dep. Variable:              log_Valor   R-squared:                       0.805
Model:                            OLS   Adj. R-squared:                  0.805
Method:                 Least Squares   F-statistic:                     8244.
Date:                Tue, 05 Aug 2025   Prob (F-statistic):               0.00
Time:                        22:11:01   Log-Likelihood:                -2045.1
No. Observations:                4000   AIC:                             4096.
Df Residuals:                    3997   BIC:                             4115.
Df Model:                           2                                         
Covariance Type:            nonrobust                                         
==================================================================================
                     coef    std err          t      P>|t|      [0.025      0.975]
----------------------------------------------------------------------------------
const              9.3349      0.059    158.353      0.000       9.219       9.450
log_Area           1.0581      0.012     89.345      0.000       1.035       1.081
log_Dist_Praia    -0.4906      0.009    -56.709      0.000      -0.508      -0.474
==============================================================================
Omnibus:                       65.115   Durbin-Watson:                   1.972
Prob(Omnibus):                  0.000   Jarque-Bera (JB):              107.712
Skew:                           0.136   Prob(JB):                     4.08e-24
Kurtosis:                       3.757   Cond. No.                         46.1
==============================================================================
```
---

## 📌 Conclusões
- A variável Área foi a mais significativa na explicação dos preços;
- Quanto maior a distância da praia, menor tende a ser o valor do imóvel;
- O modelo obedece razoavelmente bem as premissas da regressão linear;

