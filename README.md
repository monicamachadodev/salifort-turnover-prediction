# Modelagem Preditiva Baseada em Dados - Previsão de Turnover de Talentos

## Visão Geral 🔎 

Este projeto foi desenvolvido para ajudar o departamento de Recursos Humanos da Salifort Motors a entender os fatores que influenciam a retenção de funcionários. Utilizando análise exploratória e aprendizado de máquina, criamos um modelo preditivo capaz de identificar os colaboradores com maior risco de deixar a empresa. Isso fornece insights para implementar estratégias de retenção mais eficazes.

### Objetivo: 

Identificar padrões nos dados para prever a saída de funcionários e propor soluções estratégicas.


## Compreensão do Negócio 🏢

A rotatividade de funcionários pode gerar altos custos operacionais e perda de conhecimento institucional. 

O projeto aborda questões críticas como:

- Identificar quais departamentos apresentam maior turnover.
- Analisar a relação entre carga de trabalho e saída dos funcionários.
- Propor intervenções baseadas em dados.


## Compreensão dos Dados 📊

Os dados foram obtidos do Kaggle [dataset](https://www.kaggle.com/datasets/mfaisalqureshi/hr-analytics-and-job-prediction?select=HR_comma_sep.csv), há 14,999 linhas, 10 columas e essas variáveis: 

Variável  |Descrição |
-----|-----| 
satisfaction_level|Nível de satisfação no trabalho relatado pelo funcionário (0-1)|
last_evaluation|Pontuação da última avaliação de desempenho do funcionário (0-1)|
number_project|Número de projetos para os quais o funcionário contribui|
average_monthly_hours|Número médio de horas trabalhadas pelo funcionário por mês|
time_spend_company|Há quanto tempo o funcionário está na empresa (anos)
Work_accident|Se o funcionário sofreu ou não um acidente durante o trabalho
left|Se o funcionário saiu ou não da empresa (1 = sim, 0 = não)
promotion_last_5years|Se o funcionário foi promovido ou não nos últimos 5 anos
Department|Departamento do funcionário
salary|Salário do funcionário (dólares americanos)

### Pré-processamento dos Dados
- Colunas renomeadas para maior clareza.
- Exclusão de valores redundantes ou inconsistentes.
- Normalização de variáveis numéricas para otimizar a modelagem.

Os dados foram pré-processados para garantir sua integridade e relevância:
1. **Variáveis categóricas**:
   - A coluna `department` foi convertida para variáveis dummy.
   - A coluna `salary` foi codificada ordinalmente (`low = 0`, `medium = 1`, `high = 2`).
   
2. **Análise de correlação**:
   - Um mapa de calor foi gerado para entender as relações entre as variáveis numéricas.
   - Variáveis redundantes ou irrelevantes foram removidas.

3. **Divisão dos dados**:
   - O conjunto foi dividido em treinamento (70%) e teste (30%).


## Avaliação do Modelo 🤖

Vários modelos foram testados para prever a rotatividade, incluindo:
- **Regressão Logística**.
- **Classificadores baseados em Árvores (Decision Tree, Random Forest)**.

### Métricas de Avaliação

Os modelos foram avaliados com base em:
- **Acurácia**: Proporção de previsões corretas.
- **Precisão**: Capacidade de prever corretamente funcionários propensos a sair.
- **Recall**: Capacidade de identificar todos os funcionários que saíram.
- **F1-Score**: Harmonia entre precisão e recall.
- **AUC-ROC**: Desempenho geral do modelo em prever as classes.

### Resumo dos Resultados dos Modelos:
- Regressão logística

O modelo de regressão logística obteve precisão de 80%, recall de 83%, pontuação f1 de 80% (todas as médias ponderadas) e acurácia de 83% no conjunto de teste.

- Aprendizado de máquina baseado em árvore

Depois de realizar a engenharia de recursos, o modelo de árvore de decisão obteve AUC de 93,8%, precisão de 87,0%, recall de 90,4%, pontuação f1 de 88,7% e acurácia de 96,2% no conjunto de teste. A floresta randômica superou modestamente o modelo de árvore de decisão.


## 🔄  Resultados

### Principais descobertas
- Departamentos com as maiores taxas de rotatividade: *[Adicionar percepções]*.
- Os funcionários que trabalham mais de *[Adicionar número]* horas por mês têm maior probabilidade de sair.
- Altas cargas de projeto foram fortemente correlacionadas com a rotatividade.

**Desempenho do modelo**
- **Melhor modelo**: *[Adicionar modelo]*
- Métricas**:
  - Accuracy: *[Add]*
  - F1-Score: *[Add]*

## 💡 Recomendações
- Gerenciamento da carga de trabalho: Implementar limites nas atribuições de projetos.
- Programas de reconhecimento: Recompensar os funcionários de departamentos com alta rotatividade.
- Ferramentas de monitoramento: Avalie regularmente a satisfação dos funcionários e o equilíbrio da carga de trabalho


## Como Executar 🚀

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu_usuario/salifort-turnover-prediction.git

2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   
3. Execute o Jupyter Notebook:
   ```bash
   jupyter notebook salifort.ipynb
   

## Tecnologias Utilizadas 🛠️

- Python (pandas, numpy, matplotlib, seaborn)
- Scikit-learn
- XGBoost
- Jupyter Notebook

## Contato 📬

Se tiver dúvidas ou sugestões, sinta-se à vontade para entrar em contato:

LinkedIn: https://www.linkedin.com/in/monicaalessandra

