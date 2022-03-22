# Processo Seletivo Desenvolvedor Mobile Flutter #

Olá candidato, nessa fase você terá seus conhecimentos testados. 
Recomendamos que utilize boas práticas de programação e desenvolva um código bem estruturado. 


## Prazo para entrega ##
**Conforme orientado a você por email.** 

Sob hipótese alguma serão aceitos testes fora do prazo.


## O que enviar ##

O candidato deverá enviar o **código** que foi desenvolvido. Não será permitida utilização de frameworks que necessitem instalação por parte do avaliador. 
Pode-se utilizar bibliotecas(maven/cocoa pods) desde que não seja necessário nenhum passo adicional para execução do projeto pelo avaliador.
Projetos que não executem ao rodar o RUN no Android Studio/Xcode serão desconsiderados.
Códigos aceitos:
- **Flutter (Dart)**


O candidato deverá enviar um email para **cayke@instabuy.com.br** até o prazo determinado acima. No email o assunto deverá ser **"PS Dev Mobile"**. 
Emails com outro assunto serão desconsiderados.
No email explicitar seu **nome e telefone para contato**.
Tambem é necessário enviar seu **curriculo e/ou portfolio**.

A Instabuy deseja boa sorte a todos. Estamos ansiosos para trabalharmos juntos!!!


# Testinho Mobile #

O teste consiste em fazer uma request para a API do Instabuy e montar uma **tela mostrando os banners e produtos** presentes na response.
Cada célula de produto deverá conter: **imagem,nome e preço**.
O candidato poderá utilizar frameworks e libs de terceiros desde que **não** seja necessário nenhuma instalação por parte do avaliador.


## Request ##

- URL:  **https://api.instabuy.com.br/apiv3/**
- ENDPOINT: **layout**
- METHOD: **GET**
- Params: **subdomain = bigboxdelivery**

## Response ##

Todas as responses possuem 3 campos : status, data, type.

- Status: ’success’ ou ‘error’
- data: conteudo da response (pode ser dictionary, list, string, …)
- type: tipo do valor em data

Dados revelantes da request podem ser consultados pela documentação:
https://docs.instabuy.com.br/#layout
	
### Para fazer download das imagens deve-se fazer o append da url padrão com a chave da imagem. ###
Download foto banner:
**https://assets.instabuy.com.br/ib.store.banner/bnr-{{banner.image}}**

Download foto do produto:

**https://assets.instabuy.com.br/ib.item.image.YYYY/X-{{product.photo}}**

Onde os pares YYYY e X podem ser: small e s, medium e m, big e b, large e l. Essa chaves sao utilizadas para identificar qual resolucao da imagem.

Exemplo de url da imagem do produto com resolucao media cuja thumb = 20161023214840752541600349dcf4284c2592bd49355774b7b1.jpg

**https://assets.instabuy.com.br/ib.item.image.medium/m-20161023214840752541600349dcf4284c2592bd49355774b7b1.jpg**




