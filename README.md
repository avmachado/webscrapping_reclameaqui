# Web Scrapping no site do Reclame Aqui - Coleta de Scores

### Descrição
Este projeto é parte de um trabalho para previsão das notas de consumidores em relação à reclamação aberta no Portal [Consumidor.gov](https://www.consumidor.gov.br/pages/principal/?1653940320598). Aqui foi realizada uma coleta dos Scores (pontuações) no Reclame Aqui das empresas participantes do portal público utilizando <b>Automação Web com Selenium</b>.

É interessante ressaltar que a forma de realizar essa busca foi a que considerei mais eficiente, uma vez que a automação consiste em: 
- Digitar o nome da empresa na seção de busca;
- Aguardar o site do Reclame Aqui retornar com o resultado;
- Armazenar o nome da primeira empresa e o Score.

Desse jeito, mesmo que o site do Reclame Aqui retorne um resultado de busca diferente da empresa que foi usada originalmente para fazer a busca, é possível posteriormente tratar isso, seja excluindo a linha ou coletando o Score correto. E mesmo sujeito a esses erros, essa solução acaba se tornando mais viável do que passar o nome da empresa na URL do Reclame Aqui, já que o nome fantasia na base do portal Consumidor.gov muitas vezes é diferente do nome no site do Reclame Aqui. Como eu precisava de uma solução rápida, e não necessariamente elegante, dessa forma já me serviu bastante!

A única preocupação aqui é verificar se foi encontrado o <i>match</i> correto entre o nome da empresa na base e o nome no Reclame Aqui, além de avaliar as empresas cuja tag é 'Não Encontrado'.

É importante escalerecer também que o Score extraído é o equivalente aos últimos 30 dias (que é o Score principal mostrado no site). Para extrair o Score total da empresa, seria necessário entrar na página da empresa no site, e aí sim extrair o Score total.

Por fim, deixo aqui a recomendação de melhoria nesse script para deixar a automação mais elegante e eficiente.
