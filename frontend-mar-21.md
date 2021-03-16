# Processo seletivo Desenvolvedor Front-End Instabuy Março 2021 #

Olá candidato, nessa fase você terá seus conhecimentos testados. 

Recomendamos que utilize boas práticas de programação e desenvolva um código bem estruturado. 


## Prazo para entrega ##

**23 de março de 2021, terça-feira, até 23:59.** 

Sob hipótese alguma serão aceitos testes fora do prazo.


## O que enviar ##

O candidato deverá enviar o **código** que foi desenvolvido, **preferencialmente em Angular**. 
Não será permitida utilização de frameworks que necessitem instalação por parte do avaliador. 

Pode-se utilizar bibliotecas js desde que não seja necessário nenhum passo adicional para execução do projeto.
Projetos que não executem ao abrir o index.html serão desconsiderados.

O candidato deverá enviar um email para **cayke@instabuy.com.br** até o prazo determinado acima. No email o assunto deverá ser **"Dev Front Mar-21"**. 
Emails com outro assunto serão desconsiderados.
No email explicitar seu **nome e telefone para contato**.
Tambem é necessário enviar seu **currículo e/ou portfólio**.

A Instabuy deseja boa sorte a todos. Estamos ansiosos para trabalharmos juntos!!!


# Testinho Front-end #

O teste consiste em fazer desenvolver duas telas de um site e-commerce. 

Você deverá consumir a API do Instabuy e montar uma tela de **home** e uma tela de **produtos**.


## Home screen ##
Essa é a tela que será montada ao acessar a raiz do projeto. Nela você deverá **mostrar os banners e produtos** presentes na response.

Cada célula de produto deverá conter: **imagem, nome e preço**.

Referencia de design: https://supermercado.instabuy.com.br/

### Request ###

- BASE_URL:  **https://api.instabuy.com.br/apiv3/**
- ENDPOINT: **layout**
- METHOD: **GET**
- Params: **subdomain = supermercado**
- DOCS: https://docs.instabuy.com.br/#layout


## Product screen ##
Essa é a tela que será montada ao clicar em algum produto. Nela você deverá mostrar **as informações do produto** presentes na response.

A tela deverá conter: **nome, preço, imagens, descricao, botão de adicionar ao carrinho**.

Referencia de design: https://supermercado.instabuy.com.br/p/Iogurte-Integral-Morango-Batavo-Pedacos-Pote-500g

### Request ###

- BASE_URL:  **https://api.instabuy.com.br/apiv3/**
- ENDPOINT: **item**
- METHOD: **GET**
- Params: **subdomain = supermercado** e **slug = {product slug}**
- DOCS: https://docs.instabuy.com.br/#layout



## Response e path images ##

Todas as responses possuem ao menos 2 campos : status, data.

- Status: ’success’ ou ‘error’
- data: conteudo da response (pode ser dictionary, list, string, …)
	
Para fazer download das imagens deve-se fazer o append da url padrão com a chave da imagem.
Download foto banner:
**https://assets.instabuy.com.br/ib.store.banner/bnr-{{banner.image}}**

Download foto do produto:

**https://assets.instabuy.com.br/ib.item.image.YYYY/X-{{product.photo}}**

Onde os pares YYYY e X podem ser: small e s, medium e m, big e b, large e l. Essa chaves sao utilizadas para identificar qual resolucao da imagem.

Exemplo de url da imagem do produto com resoulucao media cuja thumb = 20161023214840752541600349dcf4284c2592bd49355774b7b1.jpg

**https://assets.instabuy.com.br/ib.item.image.medium/m-20161023214840752541600349dcf4284c2592bd49355774b7b1.jpg**




