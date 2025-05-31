## Otimização de modelos de classificação</h2>

🎯 Sobre o Projeto
Este projeto teve como objetivo principal identificar clientes inadimplentes utilizando técnicas de aprendizado de máquina, com ênfase na comparação de diferentes métodos de classificação e técnicas de balanceamento de dados. A tarefa central era prever corretamente se um cliente seria inadimplente com base em características fornecidas pela empresa.

A base de dados original apresentava um sério desbalanceamento entre classes, com uma quantidade muito maior de clientes adimplentes em relação aos inadimplentes. Isso exigiu a aplicação de estratégias de balanceamento para garantir uma aprendizagem mais eficaz dos modelos.

Base de dados utilizada desponibvel em https://raw.githubusercontent.com/Nunes0220/Valida-o_de_Modelos/refs/heads/main/emp_automovel.csv

📊 Métodos de Classificação Avaliados

Foram avaliados quatro algoritmos supervisionados:

- DecisionTreeClassifier
- KNeighborsClassifier
- LogisticRegression
- RandomForestClassifier

Cada algoritmo foi testado em três cenários distintos de balanceamento de dados:

- SMOTE (oversampling da classe minoritária)
- NearMiss (undersampling da classe majoritária)
- SMOTEN (versão nominal do SMOTE)

Para cada combinação de algoritmo e técnica de balanceamento, foram calculadas as seguintes métricas de desempenho:

- Acurácia
- Precisão
- Recall (métrica principal)
- F1-score

✨ Destaque: KNeighborsClassifier com NearMiss

Dentre todas as combinações testadas, o modelo KNeighborsClassifier com balanceamento NearMiss apresentou o melhor resultado em recall (0.761), que era a principal métrica de interesse do projeto. Esse bom desempenho pode ser explicado por dois fatores principais: 

Comportamento do KNeighborsClassifier: O KNN é um algoritmo baseado na proximidade entre os exemplos. Ele classifica uma nova instância com base nas classes dos exemplos mais próximos no conjunto de treinamento. Quando as classes estão bem separadas ou equilibradas, o KNN tende a ser mais eficaz.

Efeito do Balanceamento NearMiss: O NearMiss é uma técnica de under-sampling que reduz a classe majoritária (clientes adimplentes), mantendo apenas os exemplos que estão mais próximos da classe minoritária (inadimplentes). Isso força o modelo a aprender melhor os padrões da classe minoritária, pois os dados ficam mais balanceados e a fronteira entre as classes mais bem definida.

Ao aplicar NearMiss antes do treinamento com KNN, o modelo se beneficia de uma distribuição de dados mais equilibrada e de vizinhanças mais representativas da realidade de inadimplência. Como resultado, ele consegue identificar inadimplentes com maior eficiência, mesmo que isso possa ocorrer às custas de alguma perda em precisão ou acurácia geral.


## 🎓 Autores
Lucas Nunes Assumpção

## 🗨️ Contacts

- **Email**: lucasnunes.ass1@gmail.com

[Back to top](#top)

