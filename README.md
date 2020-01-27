# Análise de dados - Airbnb

Os dados são referentes ao Estado do Rio de Janeiro e foram extraídos da [página inside Airbnb](http://insideairbnb.com/get-the-data.html). Essa análise terá o objetivo de realizar uma regressão para realizar a previsão do preço de uma noite da estadia.

1. Estratégia de Modelagem
    
    Pela análise exploratória foram encontradas algumas inconsistências:
    
        1. Alugueis com valor zerados que navegando pela página da Airbnb não foram encontrados esse valor,
        2. Alugueis com valores muito altos e sem nenhum review.

    Para contornar estes problemas foram realizados alguns filtros, então nesta análise, serão considerados estadias com pelo menos um review e que possua o valor de aluguel diário.


2. Função de Custo

    O modelo Random Forest do pacote sklearn utiliza Mean Squared Error como função do erro padrão a ser minimizada. O interessante do MSE é que os grandes erros possuem pesos maiores por conta da elevação ao quadrado.

3. Seleção do Modelo Final

    Para a seleção do modelo foi utilizado a Otimização Bayesiana para definição do melhor conjunto de hiperparâmetros.

 
4. Validação do Modelo

    Para a validação modelo foi utilizada a validação cruazada com a base separada em 5 folds, foi observado o MSE médio para compreender a média dos erros(mesmo que fora de escala) e o desvião padrão para avaliar a estabilidade do modelo.


5. Evidências de um bom modelo

    O modelo não parece tão bem ajustado, pois além do aumento da variabilidade das previsões com o aumento do preço, o modelo aumenta o erro também.
    Provavelmente falta a identificação de alguma variável para a melhor identificação dos alugueis mais caros.
