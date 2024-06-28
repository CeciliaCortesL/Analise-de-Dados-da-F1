# Análise de Dados da Fórmula 1

Neste repositório, utilizamos uma base de dados real da Fórmula 1, obtida da fonte [Ergast API](https://ergast.com/api/f1?limit=30&offset=60), que registra detalhes históricos sobre as corridas, pilotos e equipes. A base de dados é composta por dois arquivos principais: `results.csv` e `drivers.csv`. O arquivo `results.csv` foi processado e convertido em `results_limpa.csv` para corrigir problemas de dados e facilitar a análise.

A base de dados contém informações abrangentes sobre diversas corridas ao longo dos anos, fornecendo atributos como identificadores de corrida, identificadores de pilotos, posições de largada e chegada, pontuações, tempos de volta mais rápidos, entre outros. Com mais de 26000 linhas de dados e uma mistura de atributos numéricos e categóricos, essa base de dados oferece uma complexidade significativa, ideal para análises exploratórias e aplicação de técnicas de machine learning.

## Objetivo

Realizar uma análise detalhada da base de dados e aplicar técnicas de machine learning para prever resultados de corridas futuras.

## Etapas do Trabalho

1. **Carga Correta dos Dados e Análise Exploratória Inicial**:
   - Carregamos os dados corretamente e realizamos uma análise exploratória inicial utilizando funções como `head`, `info`, `describe` e contagem de valores nulos para entender a estrutura e as características dos dados.

2. **Correção de Problemas da Base**:
   - Realizamos a conversão de tipos de dados, eliminamos valores faltantes e corrigimos quaisquer inconsistências presentes nos dados brutos.

3. **Profiling**:
   - Utilizamos ferramentas de profiling para obter uma visão detalhada dos dados, identificando padrões, anomalias e distribuições das variáveis.

4. **Estatística Descritiva com Apresentação de Gráficos Relevantes**:
   - Aplicamos técnicas de estatística descritiva e visualizamos os dados utilizando gráficos relevantes criados com `matplotlib` e `seaborn`. Exploramos distribuições, correlações e tendências nos dados.

5. **Aplicação de Machine Learning**:
   - Utilizamos um modelo de classificação, especificamente o Random Forest, para prever as posições finais dos pilotos em corridas futuras. Treinamos o modelo com dados históricos e avaliamos sua performance utilizando métricas apropriadas.
   - Justificamos a escolha do modelo de classificação em vez de clusterização, dado que estamos lidando com uma tarefa de previsão de rótulos conhecidos (posições finais).

6. **Previsão de Resultados**:
   - Usando o modelo treinado, realizamos previsões para determinar as posições finais dos pilotos em uma corrida hipotética. Garantimos que cada piloto tenha uma posição única prevista na classificação final.

7. **Documentação e Explicações Claras**:
   - Documentamos todas as etapas do trabalho, explicando claramente as fontes de dados, os métodos utilizados, os resultados obtidos e as interpretações feitas ao longo da análise.

## Conteúdos

### 1. Datasets
- **datasets/results.csv**: Dados brutos das corridas.
- **datasets/drivers.csv**: Informações detalhadas sobre os pilotos.
- **datasets/results_limpa.csv**: Dados processados para análise.

### 2. Notebooks
- **Análise de Dados F1.ipynb**: Notebook principal contendo a análise exploratória dos dados, incluindo visualizações de tendências ao longo dos anos, desempenho de equipes e pilotos, e insights sobre as corridas. Este notebook foi desenvolvido para rodar no Google Colab.

### 3. Scripts
- **scripts/limpeza_dados.py**: Scripts para limpeza e pré-processamento dos dados.
- **scripts/visualizacoes.py**: Funções para criação de gráficos e visualizações interativas.
- **scripts/modelos_predicao.py**: Implementação de modelos de machine learning para previsão de resultados de corridas e desempenho de pilotos.

### 4. Relatórios
- **relatorios/relatorio_analise_geral.pdf**: Relatório detalhado da análise exploratória e principais descobertas.
- **relatorios/relatorio_previsoes.pdf**: Resultados e análises dos modelos de predição.

## Requisitos
- Python 3.8+
- Bibliotecas: pandas, numpy, matplotlib, seaborn, scikit-learn, jupyter

## Como Usar
1. Clone este repositório: `git clone https://github.com/seuusuario/analise-f1.git`
2. Navegue até o diretório do projeto: `cd analise-f1`
3. Instale as dependências: `pip install -r requirements.txt`
4. Certifique-se de que os seguintes arquivos estão presentes no diretório `datasets/`:
   - `results.csv`
   - `drivers.csv`
   - `results_limpa.csv`
5. Abra e execute o notebook no Jupyter Colab: `jupyter notebook "Análise de Dados F1.ipynb"`

## Contribuições
Contribuições são bem-vindas! Sinta-se à vontade para abrir issues para relatar bugs ou sugerir melhorias. Para contribuir com código, faça um fork do repositório e envie um pull request com suas alterações.
---

Com este repositório, esperamos fornecer ferramentas e insights valiosos para entusiastas e analistas de dados interessados no fascinante mundo da Fórmula 1.
