<img src="https://github.com/monicamachadodev/salifort-turnover-prediction/blob/main/capa-previsao-turnover.jpg">

# Modelagem Preditiva Baseada em Dados - Previsão de Turnover de Talentos 

## 📌 Compreendendo o Cenário e o Problema do Negócio
O departamento de RH da Salifort Motors está em busca de soluções para aumentar a satisfação dos funcionários e reduzir a rotatividade. Eles coletaram dados valiosos sobre seus colaboradores, mas agora enfrentam um desafio: como transformar esses dados em ações eficazes?

Utilizando técnicas de análise de dados e machine learning, o projeto visa prever quais funcionários têm maior probabilidade de deixar a empresa e sugerir ações estratégicas para reduzir a rotatividade. Se conseguirmos prever quais funcionários estão propensos a sair, será possível entender os fatores críticos que contribuem para a rotatividade. Isso permitirá que a empresa tome medidas preventivas, reduzindo custos associados à perda de talentos, processos seletivos e treinamentos de novos colaboradores.

Para ajudar a decifrar essas informações e fornecer insights orientados por dados. A pergunta central que precisamos responder é:
O que faz um funcionário decidir sair da empresa?

## 🎯 Objetivo do Projeto

O objetivo principal é prever a probabilidade de um funcionário deixar a empresa e identificar os principais fatores que contribuem para essa decisão. 

Com base nisso, foram propostas recomendações acionáveis para melhorar a satisfação e a retenção dos funcionários.

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

## 🛠️ Ferramentas e Tecnologias

- **Linguagem de Programação:** `Python`

- **Bibliotecas:** `Pandas`, `NumPy`, `Scikit-learn`, `Matplotlib`, `Seaborn`

- **Ferramentas de Visualização:** `Matplotlib`, `Seaborn`

- **Modelos de Machine Learning:** `Regressão Logística`, `Decision Tree`, `Random Forest`

## 📊 Metodologia e Passo a Passo do Projeto

O projeto foi estruturado seguindo a metodologia **PACE** (Plano, Análise, Construção e Execução):

### 1. Plano

- **Entendimento do Problema:** Identificar os fatores que levam os funcionários a deixar a empresa.

- **Coleta de Dados:** Utilização de um dataset com 14.999 linhas e 10 variáveis, incluindo `satisfaction_level`, `last_evaluation`, `number_project`, `average_monthly_hours`, entre outras.

- **Limpeza e Preparação dos Dados:**
   - Remoção de duplicatas,
   - Tratamento de outliers,
   - Codificação de variáveis categóricas (`salary` e `department`)..

### 2. Análise

- **Análise Exploratória de Dados (EDA):**
   - Visualização da distribuição das variáveis.
   - Identificação de outliers.
   - Análise de correlação entre variáveis.

- **Visualizações:**
   - Gráficos de dispersão,
   - Boxplots,
   - Histogramas,
   - Mapas de calor para entender as correlações entre as variáveis.

### 3. Construção

- **Modelagem:**
  
   - Divisão dos dados em conjuntos de treino e teste.
  
   - Treinamento de modelos como `Regressão Logística`, `Decision Tree` e `Random Forest`.
  
   - Ajuste de hiperparâmetros com `GridSearchCV`.
  
   - Avaliação dos modelos usando métricas como AUC, precisão, recall e F1-score.

- **Engenharia de Features:** Criação da variável `overworked` para capturar funcionários sobrecarregados.

### 4. Execução

- **Interpretação do Modelo:** Identificação dos principais fatores que influenciam a saída dos funcionários, como carga de trabalho excessiva e falta de promoções.

- **Recomendações:** Sugestões de ações para melhorar a retenção, como ajustes na carga horária e políticas de reconhecimento.

### Resumo dos Resultados dos Modelos:

Avaliação  |Regressão Logistica |Decision Tree  |Random Forest |
-----|-----|-----|-----|
**Acurácia** | 82% | 94,4%| 96.2% |
**Precisão** | 79% | 78,4% | 87.0% |
**Recall** | 82% | 91,8% | 90.4% |
**F1-Score** | 80% | 84,5% | 88.7% |
**AUC-ROC** |   | 93,4% | 93.8% |

## 📊 Resultados e Insights

### Principais Fatores que Influenciam a Saída dos Funcionários:

- **Sobrecarga de Trabalho:** Funcionários com mais projetos e horas trabalhadas têm maior probabilidade de sair.

- **Tempo de Serviço:** Funcionários com 4 anos de empresa têm níveis de satisfação excepcionalmente baixos.

- **Falta de Promoções:** Funcionários que trabalham muitas horas, mas não são promovidos, têm maior probabilidade de sair.

- **Avaliação de Desempenho:** Funcionários com altas pontuações de avaliação, mas que trabalham muitas horas, também têm maior probabilidade de sair.

- Os 3 departamentos com as maiores taxas de rotatividade são: *Vendas, Tecnologia e Suporte*.

## 💡 Recomendações para a Empresa:

- Implementar programas de engajamento para aumentar a satisfação dos funcionários.
  
- Ajustar a carga de trabalho para evitar excesso de horas.
  
- Revisar políticas salariais para garantir competitividade no mercado.
  
- Esclarecer políticas de pagamento de horas extras e expectativas de carga de trabalho.
  
- Oferecer oportunidades de desenvolvimento profissional.

## 📌 Conclusão

Este projeto demonstra como a análise de dados pode fornecer insights valiosos para a gestão de pessoas, ajudando empresas a reduzir a rotatividade de funcionários com estratégias baseadas em evidências. Os modelos desenvolvidos têm um bom desempenho preditivo e podem ser utilizados para identificar funcionários em risco de saída.

## 🚀 Próximos Passos

- **Testar sem `last_evaluation`:** Verificar se há vazamento de dados e como isso afeta o desempenho do modelo.

- **Análise de Agrupamento (K-means):** Identificar grupos de funcionários com características semelhantes.

- **Implementação do Modelo:** Integrar o modelo em um sistema que o RH possa usar para monitorar funcionários em risco de sair.

## 📝 Considerações Éticas

- **Privacidade dos Dados:** Garantir que os dados dos funcionários sejam tratados com confidencialidade.

- **Viés no Modelo:** Verificar se o modelo não está perpetuando ou amplificando vieses existentes.

## 📚 Recursos

[Documentação do Pandas](https://pandas.pydata.org/docs/)

[Documentação do Scikit-learn](https://scikit-learn.org/stable/)

[Documentação do Matplotlib](https://matplotlib.org/stable/users/index.html)


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
   
## 👥 Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests com sugestões de melhorias.

Se tiver dúvidas ou sugestões, sinta-se à vontade para entrar em contato:

LinkedIn: [![Linkedin](https://img.shields.io/badge/-monicaalessandra-blue?style=flat-square&logo=Linkedin&logoColor=white&link=LINK-DO-SEU-LINKEDIN)](https://www.linkedin.com/in/monicaalessandra/)
