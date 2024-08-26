##  📂 Previsão preço de seguros de saúde

### Projeto com o intuito de utilizar modelos de machine learning para prever preços de seguros de saúde a partir de dados chave como renda, idade, fumante e etc

## 💻 Processo Técnico

####  Antes de inserir os dados nos modelos(e começar a diversão) precisei realizar um pequeno tratamento no conjunto. Primeiro preenchi os dados faltantes com a média ou mediana dos dados restantes de mesma categoria, pude fazer isso sem alterar de forma demasiada o resultado, pois a porcentagem de tais dados missing ficava em torno de 2 a 3%.
#### Logo em seguida peguei os dados em forma de texto e converti os mesmos para modelo númerico, apenas assim podem ser inseridos no modelo.
#### Com os dados ajustados, testei alguns modelos padrões sem nenhum tipo de refinamento para ver o resultado(ficou em torno de 80% superior do que se utilizasse a média para previsão). Logo depois projetei uma simples pipeline que defini um intervalo de valores a serem testados no modelo e os roda na função GridSearchCV, que retorna os melhores parâmetros e resultado do modelo. Depois disso é só conferir esse modelo com os dados de teste e ver o resultado que nesse caso foi 87% melhor do que se tivesse usado a média como previsão.
#### Utilizei o algoritmo SELECTKBEST junto da função f-regression para reduzir o consumo de dados do modelo, permitindo assim maior velocidade em seu uso em situações de produção.

## 💻 Gráficos importantes dos dados:

### Preço do seguro por sexo:
![download (2)](https://github.com/user-attachments/assets/24e29fff-c0e8-43c2-9cbf-e9f51a1eb9da)

### Gráficos de fumantes por sexo:
![download (4)](https://github.com/user-attachments/assets/90a64636-aad5-4b67-aa5c-4aa5897c5b13)
![download (5)](https://github.com/user-attachments/assets/a1d437b1-dcbe-449c-8dfb-774cb80fc5c8)

### Preço do seguro para pessoas fumantes e não fumantes:
![download (3)](https://github.com/user-attachments/assets/ed1ffd4f-d6f5-445c-83a7-9dec9fa0260d)

## 💻 Tecnologias Usadas

##### Todos modelos utilizados foram modelos de regressão.
##### Utilizei as bibliotecas pandas,scikit-learn e numpy.
##### O modelo que mais performou foi o modelo gradient-boosting a qual sua principal função é aprender com seus erros de previsão e assim criar árvores de decisões aprimoradas com os erros de suas anteriores.
##### Utilizei o algoritmo SELECTKBEST para diminuir o consumo de dados mantendo a eficiência do modelo.









