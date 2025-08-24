# Previsão de Inadimplência de Clientes

## Sobre o Projeto
Este projeto foi desenvolvido como trabalho final do curso de Ciência de Dados da EBAC, em parceria com uma empresa do setor financeiro. O objetivo é construir uma solução preditiva robusta para identificar clientes com maior risco de inadimplência, utilizando dados reais e técnicas avançadas de Machine Learning.

## Objetivo
Desenvolver um modelo preditivo capaz de antecipar a inadimplência de clientes, auxiliando a empresa na tomada de decisões estratégicas, redução de perdas financeiras e aprimoramento do relacionamento com o cliente.

## Base de Dados
- **dados_pf_bacen.csv**: Dados cadastrais e financeiros dos clientes.
- **df_features.csv / df_features_v2.csv**: Conjuntos de dados com features engenheiradas.
- **ipca_mes_1737.xlsx, desocupacao_6381.xlsx, ocupacao_4092.xlsx, rendimento_5436.xlsx**: Indicadores macroeconômicos utilizados para enriquecer a análise.

## Estrutura do Projeto
```
├── Projeto_Semantix-Versao_final-Ana_Paula.ipynb  # Notebook principal com todo o pipeline
├── dados_pf_bacen.csv                            # Base de dados original
├── df_features.csv / df_features_v2.csv          # Features processadas
├── arquivos .xlsx                                # Indicadores econômicos
```

## Resultados
- Construção de modelos de classificação com alta acurácia e interpretabilidade.
- Identificação dos principais fatores de risco para inadimplência.
- Geração de insights estratégicos para o negócio.

## Tecnologias e Bibliotecas
- Python (Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn)
- Jupyter Notebook
- Visual Studio Code

## Insights
- Análise dos perfis de clientes mais propensos à inadimplência.
- Impacto de variáveis macroeconômicas no risco de crédito.
- Sugestões de políticas para mitigação de risco.

## Como Rodar
1. Clone este repositório:
   ```bash
   git clone https://github.com/anapaulads/Previsao_Inadiplencia_Br.git
   ```
2. Instale as dependências (recomenda-se uso de ambiente virtual):
   ```bash
   pip install -r requirements.txt
   ```
3. Abra o notebook `Projeto_Semantix-Versao_final-Ana_Paula.ipynb` e execute as células.

## Contribuições
Sugestões, melhorias e novas ideias são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests.

## Autoria
Projeto desenvolvido por Ana Paula Dias, como projeto final da formação em Ciência de Dados pela EBAC.

---

> Este projeto demonstra habilidades em análise de dados, engenharia de features, modelagem preditiva e comunicação de resultados, sendo um diferencial competitivo para desafios reais do mercado financeiro.
