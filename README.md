##  📂 Previsão preço de seguros de saúde

### Projeto com o intuito de utilizar modelos de machine learning para prever preços de seguros de saúde a partir de dados chave como renda, idade, se é fumante ou não e etc

## 💻 Processo Técnico

####  Antes de inserir os dados nos modelos(e começar a diversão) precisei realizar um pequeno tratamento no conjunto. Primeiro preenchi os dados faltantes com a média ou mediana dos dados restantes de mesma categoria, pude fazer isso sem alterar de forma demasiada o resultado, pois a porcentagem de tais dados missing ficava em torno de 2 a 3%.
#### Logo em seguida peguei os dados em forma de texto e converti os mesmos para modelo númerico, apenas assim podem ser inseridos no modelo.
#### Com os dados ajustados, testei alguns modelos padrões sem nenhum tipo de refinamento para ver o resultado(ficou em torno de 80% superior do que se utilizasse a média para previsão) e logo depois projetei uma pipeline que pega cada modelo e seus parâmetros e os testa na função GridSearchCv e depois retorna o melhor modelo com seus melhores parâmetros, depois disso é só conferir esse modelo com os dados de teste e ver o resultado que nesse caso foi 87% melhor que se tivesse usado a média como previsão.

## 💻 Tecnologias Usadas

##### Todos modelos utilizados foram modelos de regressão
##### Utilizei a biblioteca pandas e scikit-learn
##### O modelo que mais performou foi o modelo gradient-boosting a qual sua principal função é aprender com seus erros de previsão e assim criar árvores de decisões aprimoradas com os erros de suas anteriores









