# airbnb_pricing_prediction

a. Como foi a definição da sua estratégia de modelagem?
- Conhecer e entender a estrutura dos dados
- Data cleaning: onde gastei maior parte do tempo por conta da quantidade de variáveis para tratar. Como exemplo, a quantidade de banheiros que estava em formato texto, com várias features que separei em quantidade de banheiros (bathrooms) e se o banheiro é compartilhado (shared_bathroom)
- Exploration data analysis: gostaria de ter tido mais tempo para explorar e analisar os dados
- Preparação dos dados para modelagem (normalização, padronização, criação de dummies)
- E por fim, a modelagem 
 
b. Como foi definida a função de custo utilizada?

Foi definida pelo XGBoost que é um algoritmo de machine learning bastante utilizado para dados estruturados. Uma implementação de árvores de decisão com aumento de gradiente, projetados para ganho de velocidade e desempenho.

c. Qual foi o critério utilizado na seleção do modelo final?

Ideal seria ter mais de um modelo para comparação do desempenho do XGBoost (apesar de ter um desempenho satisfatório, precisando apenas de ajustes), porém não tive tempo suficiente para isso.

d. Qual foi o critério utilizado para validação do modelo?

Por que escolheu utilizar este método?
Os métodos de validação foram o Mean Square Error e o R-square. Porque o MSE é uma boa métrica para medir o quão bem o modelo está predizendo a resposta, já que é a soma da diferença média quadrática entre os valores estimados e o valor real. e o R-square expressa a quantidade da variância dos dados que é explicada pelo modelo a partir da variáveis independentes selecionadas para o modelo.

e. Quais evidências você possui de que seu modelo é
suficientemente bom?

MSE pequeno e R-Square que explica grande parte da variabilidade dos dados, no entanto, apesar do modelo ter performado bem na base de testes (R-Square=0,82) apresentou significativa diferença na validação(R-Square=0,64), indicando que o modelo precisa de ajustes.
