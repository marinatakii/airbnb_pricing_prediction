# airbnb_pricing_prediction

a. Como foi a definição da sua estratégia de modelagem?
- Conhecer e entender a estrutura dos dados
- Data cleaning: onde gastei maior parte do tempo por conta da quantidade de variáveis para tratar. Como exemplo, a quantidade de banheiros que estava em formato texto, com várias features que separei em quantidade de banheiros (bathrooms) e se o banheiro é compartilhado (shared_bathroom). 
- Exploration data analysis: gostaria de ter tido mais tempo para explorar e analisar os dados
- Preparação dos dados para modelagem (normalização, padronização, criação de dummies)
- Modelagem dos dados
- Validação do modelo
 
b. Como foi definida a função de custo utilizada?

Foi definida pelo XGBoost que é um algoritmo de machine learning bastante utilizado para dados estruturados. Uma implementação de árvores de decisão com aumento de gradiente, projetados para ganho de velocidade e desempenho.

c. Qual foi o critério utilizado na seleção do modelo final?

Utilizei uma otimização manual dos parâmetros (Grid search) que considerou como critério de seleção do modelo final o MSE (mean square errors).

d. Qual foi o critério utilizado para validação do modelo?

Por que escolheu utilizar este método?
Para validação do modelo utilizei o grid search com kfold cross validation, porque garante uma boa avaliação de desempenho de modelos de machine learning. A utilização do cross validation aumenta as chances de detectar se o modelo está sofrendo overfitting.
A avaliação das métricas foram a partir do MSE que e o R-square. O MSE é uma medida para qualificar o quão bem o modelo está predizendo a resposta, já que é a soma da diferença média quadrática entre os valores estimados e o valor real (o quanto o modelo está errando),  e o R-square expressa a quantidade da variância dos dados que é explicada pelo modelo a partir da variáveis independentes selecionadas para o modelo.

e. Quais evidências você possui de que seu modelo é
suficientemente bom?

MSE aprox. 0,01 (quanto mais próximo de zero, melhor) e R-Square aprox. 0,58 (quanto mais próximo de 1, mais o modelo se ajustou aos dados), explicando parte da variabilidade dos dados. No entanto, o modelo precisa de melhorias no tratamento dos dados e na seleção das variáveis, já que são muitas e algumas fortemente correlacionadas. Apesar dos modelos de árvore não serem afetados pela multicolinearidade, é uma boa prática retirar variáveis redundantes.
