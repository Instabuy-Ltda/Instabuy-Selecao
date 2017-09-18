# Processo seletivo desenvolvedor front-end Instabuy #

Olá candidato, nessa fase você terá seus conhecimentos testados. Recomendamos que utilize boas praticas de programação e desenvolva um código bem estruturado. 
Caso você queira se candidatar para mais de uma área basta enviar os testes das áreas desejadas. Note que o prazo será o mesmo independentemente de quantas áreas foram escolhidas.

## Prazo para entrega ##
**24 de setembro de 2017, Domingo, até 23:59.** Sob hipótese alguma serão aceitos testes fora do prazo.


## O que enviar ##

O candidato deverá enviar o **código** que foi desenvolvido juntamente com uma **documentação** explicando como executar o projeto.
Projetos que não executem apos seguir os passos da documentação serão desconsiderados.
O candidato deverá um email para **cayke@instabuy.com.br** até o prazo determinado acima. No email o assunto deverá ser **"Seleção Dev Instabuy"**. Emails com outro assunto serão desconsiderados.
Caso esteja fazendo o teste para mais de uma área, enviar todos os testes no mesmo email.
No email explicitar a(s) área(s) de interesse bem como seu **nome e telefone para contato**.
Os melhores de cada área serão selecionados para a ultima fase da seleção que será uma entrevista presencial.

O Instabuy deseja boa sorte a todos. Estamos ansiosos para trabalharmos juntos!!!


# Testinho Front-end #

O teste consiste em fazer uma request para a API do Instabuy e montar uma **tela mostrando a lista de produtos** presentes na response.
Cada celula de produto deverá conter: **imagem, marca, nome, preco**.
O candidato poderá utilizar frameworks e libs de terceiros desde que **não** seja necessario nenhuma instalacao por parte do avaliador.


## Request ##

URL:  **https://instabuy.com.br/apiv2_2/**
ENDPOINT: **product.json**
METHOD: **GET**
Params: **subcategory_id = 57eec92f072d415b67c24175**

## Response ##

Todas as responses possuem 3 campos : status, data, type.
- Status: ’success’ ou ‘error’
- data: conteudo da response (pode ser dictionary, list, string, …)
- type: tipo do valor em data

Dados revelantes request product.json:
- id : id do produto
- name: nome do produto
- brand: marcar do produto
- thumb: foto principal do produtophotos: array com fotos do produto
- pc: Array de controllers de preço
	-valid_price : valor do produto
	
Para fazer download das imagens deve-se fazer o append da url do bucket da amazon com a chave da imagem.
Download foto do produto:
**https://s3-us-west-2.amazonaws.com/ib.image.YYYY/X-{{product.photo}}**
Onde os pares YYYY e X podem ser: small e s, medium e m, big e b, large e l. Essa chaves sao utilizadas para identificar qual resolucao da imagem.

Exemplo de url da imagem do produto com resoulucao media cuja thumb = 20161023214840752541600349dcf4284c2592bd49355774b7b1.jpg
https://s3-us-west-2.amazonaws.com/ib.image.medium/m-20161023214840752541600349dcf4284c2592bd49355774b7b1.jpg




