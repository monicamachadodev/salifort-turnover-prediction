<img src="https://github.com/monicamachadodev/salifort-turnover-prediction/blob/main/capa-previsao-turnover.jpg">

# Modelagem Preditiva Baseada em Dados - Previsão de Turnover de Talentos 

Este projeto tem como objetivo analisar os fatores que influenciam a saída de funcionários da empresa fictícia **Salifort Motors**. Utilizando técnicas de análise exploratória de dados (EDA) e modelagem preditiva, buscamos identificar padrões e propor estratégias para melhorar a retenção de colaboradores.


## 📌 Visão Geral

O projeto é dividido nas seguintes etapas utilizando o método PACE (Planejamento, Analize, Construção e Execução ):
1. **Exploração dos Dados**: Análise das variáveis e identificação de padrões.
2. **Limpeza e Preparação dos Dados**: Tratamento de valores nulos, duplicatas e codificação de variáveis categóricas.
3. **Modelagem Preditiva**: Treinamento e avaliação de modelos de machine learning para prever a saída de funcionários.
4. **Interpretação dos Resultados**: Identificação dos principais fatores que impactam a retenção e sugestões de ações para a empresa.

## Compreensão do Negócio

A rotatividade de funcionários pode gerar altos custos operacionais e perda de conhecimento institucional. 

O projeto aborda questões críticas como:

- Identificar quais departamentos apresentam maior turnover.
- Analisar a relação entre carga de trabalho e saída dos funcionários.
- Propor intervenções baseadas em dados.


## 📂 Compreensão dos Dados 

Os dados foram obtidos do Kaggle [dataset](https://www.kaggle.com/datasets/mfaisalqureshi/hr-analytics-and-job-prediction?select=HR_comma_sep.csv), há 14,999 linhas, 10 colunas e essas variáveis: 

Variável  |Descrição |
-----|-----| 
satisfaction_level|Nível de satisfação do funcionário (0 a 1).|
last_evaluation|Resultado da última avaliação de desempenho (0 a 1).|
number_project|Número de projetos em que o funcionário está envolvido.|
average_monthly_hours|Média de horas trabalhadas por mês.||
time_spend_company|Tempo de permanência na empresa (em anos).|
Work_accident|Indica se o funcionário sofreu um acidente de trabalho (0 ou 1).|
left|Indica se o funcionário saiu da empresa (0 ou 1).|
promotion_last_5years|SIndica se o funcionário foi promovido nos últimos 5 anos (0 ou 1).|
Department|Departamento em que o funcionário trabalha.|
salary|Nível salarial (baixo, médio, alto).

## 🛠️ Tecnologias Utilizadas 

- Python (pandas, numpy, matplotlib, seaborn)
- Scikit-learn
- XGBoost
- Jupyter Notebook

## 📖 Passo a Passo do Projeto

### 1️⃣ Importação de Bibliotecas
Foram utilizadas bibliotecas como `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn` e `xgboost` para análise, visualização e modelagem.

### 2️⃣ Carregamento e Inspeção dos Dados
- Leitura do dataset `HR.csv`.
- Renomeação de colunas para facilitar a manipulação.
- Verificação de valores nulos e duplicados.

### 3️⃣ Análise Exploratória de Dados (EDA)
- Visualização da distribuição das variáveis.
- Identificação de outliers.
- Análise de correlação entre variáveis.
- Criação de gráficos para entender a relação entre as variáveis e a saída de funcionários.

### 4️⃣ Limpeza e Preparação dos Dados
- Remoção de duplicatas.
- Codificação de variáveis categóricas (`salary` e `department`).
- Criação de novas features, como `overworked` (funcionários que trabalham mais de 175 horas por mês).

### 5️⃣ Modelagem Preditiva
- Divisão dos dados em conjuntos de treino e teste.
- Treinamento de modelos como Regressão Logística, Árvore de Decisão e Random Forest.
- Ajuste de hiperparâmetros com `GridSearchCV`.
- Avaliação dos modelos usando métricas como AUC, precisão, recall e F1-score.

### 6️⃣ Interpretação dos Resultados
- Identificação dos principais fatores que influenciam a saída de funcionários.
- Sugestões de ações para melhorar a retenção, como ajustes na carga horária e políticas de reconhecimento.

### Resumo dos Resultados dos Modelos:

- Regressão logística

O modelo de Regressão logística obteve precisão de 80%, recall de 83%, pontuação f1 de 80% (todas as médias ponderadas) e acurácia de 83% no conjunto de teste.

- Aprendizado de máquina baseado em árvore

Depois de realizar a engenharia de recursos, o modelo de Árvore de decisão obteve AUC de 93,8%, precisão de 87,0%, recall de 90,4%, pontuação f1 de 88,7% e acurácia de 96,2% no conjunto de teste. Random Forest superou modestamente o modelo de Árvore de decisão.

## 📊 Resultados e Insights

### Principais Fatores que Impactam a Retenção:
- Baixa satisfação no trabalho: Funcionários insatisfeitos têm maior probabilidade de sair.
- Carga horária elevada: Trabalhar muitas horas por mês aumenta o risco de burnout.
- Número de projetos: Funcionários com poucos ou muitos projetos são mais propensos a sair.
- Salário: Colaboradores com salários mais altos tendem a permanecer na empresa.
- Os 3 departamentos com as maiores taxas de rotatividade são: *Vendas, Tecnologia e Suporte*.

## 💡 Recomendações para a Empresa:
- Implementar programas de engajamento para aumentar a satisfação dos funcionários.
- Ajustar a carga de trabalho para evitar excesso de horas.
- Revisar políticas salariais para garantir competitividade no mercado.
- Oferecer oportunidades de desenvolvimento profissional.

## 📌 Conclusão

Este projeto demonstra como a análise de dados pode fornecer insights valiosos para a gestão de pessoas, ajudando empresas a reduzir a rotatividade de funcionários com estratégias baseadas em evidências. Os modelos desenvolvidos têm um bom desempenho preditivo e podem ser utilizados para identificar funcionários em risco de saída.

## 🚀 Como Executar 

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu_usuario/salifort-turnover-prediction.git

2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   
3. Execute o Jupyter Notebook:
   ```bash
   jupyter notebook salifort.ipynb
   
## 📬 Contato 

Se tiver dúvidas ou sugestões, sinta-se à vontade para entrar em contato:

LinkedIn: [![Linkedin](https://img.shields.io/badge/-monicaalessandra-blue?style=flat-square&logo=Linkedin&logoColor=white&link=LINK-DO-SEU-LINKEDIN)](https://www.linkedin.com/in/monicaalessandra/)
