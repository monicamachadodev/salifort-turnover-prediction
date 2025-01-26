# Análise e Previsão de Churn de Talentos da Salifort Motors 🚗 

## Visão Geral

Este projeto foi desenvolvido para ajudar o departamento de Recursos Humanos da Salifort Motors a entender os fatores que influenciam a retenção de funcionários. Utilizando análise exploratória e aprendizado de máquina, criamos um modelo preditivo capaz de identificar os colaboradores com maior risco de deixar a empresa. Isso fornece insights para implementar estratégias de retenção mais eficazes.

Objetivo: Identificar padrões nos dados para prever a saída e propor soluções estratégicas.
Ferramentas Utilizadas: Python, pandas, scikit-learn, XGBoost, matplotlib, seaborn.


## Compreensão do Negócio 🏢

A rotatividade de funcionários pode gerar altos custos operacionais e perda de conhecimento institucional. O projeto aborda questões críticas como:

- Identificar quais departamentos apresentam maior turnover.
- Analisar a relação entre carga de trabalho e saída dos funcionários.
- Propor intervenções baseadas em dados.


## Compreensão dos Dados 📊

A análise deste projeto utiliza dados históricos de funcionários da Salifort Motors, incluindo:
- department: Departamento do funcionário.
- average_monthly_hours: Média de horas trabalhadas por mês.
- tenure: Tempo de empresa (anos).
- work_accident: Registro de acidentes de trabalho.
- promotion_last_5years: Promoção nos últimos 5 anos.
- left: Indicador binário de saída do funcionário (1 = sim, 0 = não).

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
- **XGBoost**.

### Métricas de Avaliação

Os modelos foram avaliados com base em:
- **Acurácia**: Proporção de previsões corretas.
- **Precisão**: Capacidade de prever corretamente funcionários propensos a sair.
- **Recall**: Capacidade de identificar todos os funcionários que saíram.
- **F1-Score**: Harmonia entre precisão e recall.
- **AUC-ROC**: Desempenho geral do modelo em prever as classes.

Resultados:
- O modelo **[inserir XGBoost]** apresentou o melhor desempenho com:
  - Acurácia: XX%.
  - Recall: XX%.
  - F1-Score: XX%.


## Conclusão e Próximos Passos 📈

### Conclusão
O modelo identifica com precisão os funcionários mais propensos a deixar a empresa, possibilitando intervenções direcionadas, como:
- Redução de carga de trabalho em departamentos críticos, oferecendo suporte aos funcionários com sobrecarga.
- Aumento de benefícios para grupos de salários baixos, estabelecendo programas de retenção específicos para os departamentos mais afetados.
- Programas de desenvolvimento de carreira, oferecendo promoções e oportunidades de crescimento interno, especialmente para funcionários com mais de 3 anos de casa.

Essas ações podem reduzir a rotatividade e melhorar a satisfação dos colaboradores. No futuro, seria interessante incluir fatores adicionais, como feedback dos funcionários e avaliações de desempenho, para refinar ainda mais as previsões.

### Próximos Passos

1. **Integração com sistemas internos**:
   - Implementar o modelo para monitorar funcionários em tempo real.
2. **Análise mais aprofundada**:
   - Incorporar novas variáveis, como feedbacks de funcionários e avaliações de desempenho.
3. **Validação do modelo**:
   - Testar o modelo em dados futuros para validar sua eficácia.


## Como Executar 🚀

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu_usuario/salifort-motors-retention.git

2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   
3. Execute o Jupyter Notebook:
   ```bash
   jupyter notebook Salifort_Motors.ipynb
   

## Tecnologias Utilizadas 🛠️

- Python (pandas, numpy, matplotlib, seaborn)
- Scikit-learn
- XGBoost
- Jupyter Notebook

## Contato 📬

Se tiver dúvidas ou sugestões, sinta-se à vontade para entrar em contato:

LinkedIn: https://www.linkedin.com/in/monicaalessandra

