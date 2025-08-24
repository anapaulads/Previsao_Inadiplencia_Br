# Previsão do Percentual de Inadimplência no Brasil.

## Sobre o Projeto
Este projeto foi desenvolvido como trabalho final da formação em Ciência de Dados da EBAC.

O objetivo é analisar e prever a taxa de inadimplência de pessoas físicas no Brasil utilizando variáveis macroeconômicas e de crédito, integrando fundamentos de economia aplicada com técnicas avançadas de ciência de dados e machine learning.

A solução proposta visa apoiar instituições financeiras, órgãos reguladores e formuladores de políticas públicas na tomada de decisões estratégicas, ajudando a antecipar movimentos da inadimplência em resposta a mudanças econômicas.

## Objetivo
Desenvolver um modelo de machine learning capaz de prever a taxa de inadimplência no Brasil com base em dados agregados de crédito e indicadores econômicos, como taxa de juros, inflação, comprometimento de renda e desemprego. O foco está em antecipar tendências nacionais.

## Base de Dados

O projeto utilizou dados públicos do:
- Banco Central do Brasil (BACEN)  
**dados_pf_bacen.csv**: Séries históricas de crédito, inadimplência e juros do Banco Central do Brasil (BACEN).
- Instituto Brasileiro de Geografia e Estatística (IBGE)  
**ipca_mes_1737.xlsx, desocupacao_6381.xlsx, ocupacao_4092.xlsx, rendimento_5436.xlsx**: Indicadores socioeconômicos do IBGE (inflação, desemprego, ocupação, renda).  
**df_features.csv / df_features_v2.csv**: Bases processadas com variáveis derivadas e lags temporais.
  
Abrangendo o período de 2012 até os dados mais recentes disponíveis.

## Estrutura do Projeto
```
├── Projeto_Semantix-Versao_final-Ana_Paula.ipynb  # Notebook principal com todo o pipeline
├── dados_pf_bacen.csv                            # Séries históricas BACEN
├── df_features.csv / df_features_v2.csv          # Features processadas e variáveis derivadas
├── arquivos .xlsx                                # Indicadores econômicos IBGE
```
- Seção 1: Definição do problema e objetivos de negócio
- Seção 2: Preparação e integração dos dados
- Seção 3: Análise Exploratória de Dados (EDA)
- Seção 4: Engenharia de atributos e transformação de séries temporais
- Seção 5: Modelagem preditiva (Machine Learning)
- Seção 6: Novas estratérias e modelagem
- Seção 7: Avaliação dos resultados e insights obtidos

## Resultados
Na etapa de modelagem foram testados diferentes algoritmos, como: Random Forest, XGBoost e LightGBM, sempre utilizando validação adequada para séries temporais. O Random Forest serviu como baseline, mas apresentou limitação em generalizar, com erro médio absoluto (MAE) em torno de 26,9 p.p. no conjunto de teste. O XGBoost, mesmo mostrando bom desempenho em validação (MAE próximo de 11,3 p.p.), não manteve a performance em dados não vistos, também ficando em 26,9 p.p. no teste, evidenciando sobreajuste.

O LightGBM otimizado, por outro lado, foi o modelo que melhor equilibrou aprendizado e generalização. Incorporando variáveis de variação percentual, lags de curto prazo e marcadores de choques econômicos (como recessão e pandemia), reduziu o erro médio para 16,4 p.p. no teste — uma melhoria de aproximadamente 39% em relação ao baseline. Esse resultado mostra que modelos mais parsimoniosos e com variáveis que capturam a dinâmica temporal são mais robustos frente às mudanças estruturais da economia.

Em termos de negócio, isso significa que o modelo é capaz de antecipar tendências de inadimplência com maior confiabilidade, principalmente ao identificar o impacto do mercado de trabalho, da inflação e do custo do crédito, variáveis que se mostraram determinantes ao longo da análise.

## Tecnologias e Bibliotecas
- Python (Pandas, NumPy, Scikit-learn, XGBoost, LightGBM, Matplotlib, Seaborn, Plotly)
- Jupyter Notebook
- Visual Studio Code

## Insights
Durante a EDA, algumas descobertas importantes foram feitas:

- O tempo se mostrou a variável mais dominante, influenciando direta ou indiretamente quase todas as outras.
- Correlações bivariadas simples (ex.: entre rendimento médio e inadimplência) revelaram-se enganosas devido ao efeito do tempo, que atua como uma variável oculta.
- A inadimplência e o rendimento médio cresceram juntos ao longo dos anos, mas isso não significa relação causal direta — trata-se de uma correlação espúria.
- Para análises robustas, foi necessário ajustar variáveis econômicas (ex.: deflacionar rendimentos) e aplicar técnicas que neutralizem o efeito temporal.

**Conclusão principal:** Modelos que desconsiderem a forte influência do tempo tendem a gerar interpretações equivocadas
  
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
Sugestões, melhorias e novas ideias são bem-vindas!  
Sinta-se à vontade para abrir issues ou pull requests.

## Autoria
Projeto desenvolvido por Ana Paula Dias, como projeto final da formação em Ciência de Dados pela EBAC.

---

> Este projeto demonstra habilidades em análise de dados, engenharia de variáveis, modelagem preditiva, explicabilidade e comunicação de resultados, sendo um diferencial competitivo para desafios reais do mercado financeiro e de políticas públicas.
