# Previsão do Percentual de Inadimplência no Brasil a partir de Indicadores Macroeconômicos

## Sobre o Projeto
Projeto final da formação em Ciência de Dados pela EBAC, realizado em parceria com uma empresa do setor financeiro. O objetivo é construir um modelo preditivo capaz de estimar o percentual de inadimplência no Brasil, utilizando séries temporais de indicadores macroeconômicos e socioeconômicos públicos (BACEN e IBGE). O projeto une fundamentos de economia aplicada, engenharia de dados e inteligência artificial para propor uma abordagem eficiente e realista de previsão de risco no cenário macroeconômico brasileiro.

## Objetivo
Desenvolver um modelo de machine learning capaz de prever a taxa de inadimplência no Brasil com base em dados agregados de crédito e indicadores econômicos, como taxa de juros, inflação, comprometimento de renda e desemprego. O foco está em antecipar tendências nacionais, subsidiando decisões estratégicas de instituições financeiras, órgãos reguladores e formuladores de políticas públicas.

## Base de Dados
- **dados_pf_bacen.csv**: Séries históricas de crédito, inadimplência e juros do Banco Central do Brasil (BACEN).
- **df_features.csv / df_features_v2.csv**: Bases processadas com variáveis derivadas e lags temporais.
- **ipca_mes_1737.xlsx, desocupacao_6381.xlsx, ocupacao_4092.xlsx, rendimento_5436.xlsx**: Indicadores socioeconômicos do IBGE (inflação, desemprego, ocupação, renda).

## Estrutura do Projeto
```
├── Projeto_Semantix-Versao_final-Ana_Paula.ipynb  # Notebook principal com todo o pipeline
├── dados_pf_bacen.csv                            # Séries históricas BACEN
├── df_features.csv / df_features_v2.csv          # Features processadas e variáveis derivadas
├── arquivos .xlsx                                # Indicadores econômicos IBGE
```

## Resultados
- Construção de modelos de regressão para previsão do percentual de inadimplência nacional.
- Engenharia de variáveis para capturar tendências, variações e eventos de crise (recessão, pandemia).
- Validação robusta com TimeSeriesSplit, respeitando a ordem temporal dos dados.
- Modelo LightGBM otimizado apresentou maior robustez e menor erro absoluto médio (MAE) no conjunto de teste, superando XGBoost e RandomForest.

## Tecnologias e Bibliotecas
- Python (Pandas, NumPy, Scikit-learn, XGBoost, LightGBM, Matplotlib, Seaborn, Plotly)
- Jupyter Notebook
- Visual Studio Code

## Insights
- O tempo (trimestre) exerce forte influência sobre todas as variáveis, exigindo técnicas para neutralizar tendências espúrias.
- Variáveis de eventos de crise (recessão 2014-2016, pandemia pós-2020) são cruciais para explicar saltos na inadimplência.
- O modelo LightGBM, ao incorporar variações percentuais e lags, mostrou-se mais robusto para prever cenários futuros e lidar com concept drift.
- O XGBoost apresentou overfitting, com bom desempenho em validação cruzada mas queda acentuada no teste.
- A explicabilidade dos modelos permitiu identificar os principais determinantes macroeconômicos da inadimplência nacional.

## Como Rodar
1. Clone este repositório:
   ```bash
   git clone https://github.com/anapaulads/Previsao_Inadiplencia_Br.git
   ```
2. Instale as dependências (recomenda-se uso de ambiente virtual):
   ```bash
   pip install -r requirements.txt
   ```
3. Abra o notebook `Projeto_Semantix-Versao_final-Ana_Paula.ipynb` e execute as células sequencialmente.

## Contribuições
Sugestões, melhorias e novas ideias são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests.

## Autoria
Projeto desenvolvido por Ana Paula Dias, como projeto final da formação em Ciência de Dados pela EBAC.

---


---

> Este projeto demonstra habilidades em análise de dados, engenharia de variáveis, modelagem preditiva, explicabilidade e comunicação de resultados, sendo um diferencial competitivo para desafios reais do mercado financeiro e de políticas públicas.
