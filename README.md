# bootcamp_how
Repositório destinado as atividades do bootcamp de engenharia de dados da How.

Um curso mais prático do que teórico.

Pré-requisitos:
- Familiaridade com alguma linguagem de programação(Python principalmente)
- Familiaridade com SQL
- Pacote Pandas do Python é desejável

## Fundamentos de engenharia de dados

O primeiro módulo do curso é o fundamentos de engenharia de dados, onde é apresentado um problema de extrair os dados de um site, fazer o tratamento e a análise desses dados.

### **Exercício do módulo**
Extrair todos os resultados da [lotofácil no site](https://loterias.caixa.gov.br/Paginas/Download-Resultados.aspx) para fazer algumas analises como
- Qual o número que foi mais sorteado?
- Qual o número que foi menos sorteado?
- Qual a combinação de números pares, impares e primos mais frequentes?

### **Resumo da resolução**
 Fazer uma requisição ao site da caixa, mas para isso foi pego a url através do inspecionar elemento porque a requisição direta não nos traz os dados, após isso pegamos o código html resultante e tratamos com o pandas.
 Para executar o código precisamos instalar os pacotes necessários, foi sugerido utilizar o virtualenv. Vou deixar as dependências no arquivo requirements.txt da pasta desse módulo. Para executar o código precisamos passar a url como parametro do código, por exemplo 

 >python minha_resolucao.py 'site_da_caixa'

 Outra curiosidade legal desse exercício é que podemos pegar outros concursos como mega-sena mudando o parametro modalidade da url.

Alguns problemas que surgiram, o site mudou do vídeo para os dias atuais então o código de solução proposto não funciona diretamente, precisando de alguns ajustes.
Outro problema enfrentado foi tentar mapear o trafego de rede do site, quando atualizo a página com a ferramenta de inspeção aberta o site não termina de carregar, mas o botcamp tem um vídeo de atualização da resolução que nos mostra essa parte e é pega uma url na qual devemos fazer a requisição para termos a página[https://servicebus2.caixa.gov.br/portaldeloterias/api/resultados?modalidade=Lotofácil].