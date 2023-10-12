# arima-temperature

Análise de Séries Temporais e Previsão de Temperatura Mínima Diária

Este projeto tem como objetivo realizar uma análise de séries temporais em um conjunto de dados que registra a temperatura mínima diária de 1981 a 1990. Ele também abrange a previsão da temperatura mínima diária usando modelos ARIMA (Modelo Autorregressivo Integrado de Médias Móveis) e SARIMA (Modelo Autorregressivo Integrado de Médias Móveis com Componente Sazonal).

Bibliotecas Utilizadas:

pandas: para manipulação dos dados.
numpy: para operações matemáticas.
matplotlib: para plotagem de gráficos.
statsmodels: para modelagem estatística e previsão de séries temporais.
pmdarima: para auxiliar na seleção de hiperparâmetros do modelo ARIMA.
Passos Realizados:

Carregamento dos Dados:

Os dados de temperatura mínima diária são lidos a partir de um arquivo Excel e são convertidos em um DataFrame do pandas.
Os dados são indexados pela coluna de datas e as datas são parseadas para o formato apropriado.
Pré-Processamento:

Uma nova coluna chamada "New Column" é criada, contendo os valores de temperatura mínima diária como floats.
O DataFrame é ordenado pelo índice de datas.
Análise Exploratória:

O conjunto de dados é explorado por meio de visualizações, como gráficos de séries temporais.
Decomposição da Série Temporal:

A decomposição sazonal da série temporal é realizada usando o método de decomposição aditiva.
Teste de Estacionariedade:

O teste ADF (Augmented Dickey-Fuller) é aplicado à série temporal original e à série temporal diferenciada para verificar a estacionariedade.
Modelagem ARIMA:

Utilizando a biblioteca pmdarima, um modelo ARIMA é ajustado aos dados, otimizando automaticamente os hiperparâmetros.
Modelagem SARIMA:

Um modelo SARIMA (Modelo Autorregressivo Integrado de Médias Móveis com Componente Sazonal) é ajustado aos dados.
Previsão:

O modelo SARIMA é usado para fazer previsões da temperatura mínima diária.
Visualização das Previsões:

As previsões são visualizadas juntamente com os dados reais em um gráfico.
Avaliação do Modelo:

O RMSE (Erro Quadrático Médio) é calculado para avaliar o desempenho do modelo de previsão.
Para executar este código, você deve ter as bibliotecas mencionadas no início instaladas em seu ambiente Python. Certifique-se de ter o arquivo 'temperature.xlsx' com os dados de temperatura mínima diária no mesmo diretório.

Observações:

A estacionariedade da série temporal é importante para a aplicação de modelos ARIMA. Foram feitos testes ADF para verificar a estacionariedade.
O modelo SARIMA é ajustado para prever os próximos valores da temperatura mínima com base nos dados históricos.
