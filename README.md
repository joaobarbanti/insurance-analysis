##  📂 Análise de empréstimos 

### Projeto com o intuito de utilizar modelos de machine learning para aprovar ou reprovar empréstimos a partir de dados chave como renda, idade, escolaridade, sexo e etc.

## 💻 Processo Técnico

####  Antes de inserir os dados nos modelos(e começar a diversão) precisei realizar um pequeno tratamento no conjunto. Primeiro preenchi os dados faltantes com a média ou mediana dos dados restantes de mesma categoria, pude fazer isso sem alterar de forma demasiada o resultado, pois a porcentagem de tais dados missing ficava em torno de 8% a 10%(porcentagem pequena) caso esse número fosse maior aplicaria outra estratégia. 
#### Logo em seguida peguei os dados em forma de texto e converti os mesmos para modelo binário utilizando a função get_dummies do pandas, essa etapa é necessária pois modelos de machine learning são basicamente técnicas de estatística e para as mesmas operarem elas precisam de dados númericos por isso é necessário a etapa de conversão. 
#### Com os dados ajustados, testei alguns modelos padrões sem nenhum tipo de refinamento para ver o resultado(ficou em torno de 80% superior do que se utilizasse a média para previsão) e logo depois projetei uma pipeline que pega cada modelo e seus parâmetros e os testa na função GridSearchCv e depois retorna o melhor modelo com seus melhores parâmetros, depois disso é só conferir esse modelo com os dados de teste e ver o resultado que nesse caso foi 93% melhor que se tivesse usado a média como previsão e teve 17544 verdadeiros positivos e 3622 verdadeiros negativos um resultado o tanto quanto satisfatório

## 💻 Tecnologias Usadas

##### Todos modelos utilizados foram modelos de classificação por se tratar de um problema de aprovar ou não aprovar(1,0)
##### Utilizei a biblioteca pandas e scikit-learn
##### O modelo que mais performou foi o modelo gradient-boosting a qual sua principal função é aprender com seus erros de previsão e assim criar árvores de decisões aprimoradas com os erros de suas anteriores









