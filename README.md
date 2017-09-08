# Processo seletivo desenvolvedor Instabuy #

Nós da Instabuy estamos expandindo e buscando profissionais para vagas de desenvolvimento. 
A vaga é para estágio e o profissional deve ser proativo, ter boa relação interpessoal e vontade de aprender e desenvolver novos conhecimentos.

O processo será divido em 3 etapas: inscrição, testinho e entrevistas.
Estamos procurando desenvolvedores para 4 areas: front-end, back-end, iOS, Android.

Voce poderá se increver em mais de uma area para realização dos testes, porem o prazo para entrega será o mesmo independente das areas em que você se increveu.

Carga horaria: 25 horas
Bolsa: a combinar (acima da média do mercado)


## Inscrição ##

Para se inscrever no processo, voce deverá fazer o cadastro em nosso servidor. Para tal siga os proximos passos

- Fazer uma request para o endpoint **https://instabuy.com.br/apiv2_2/selecao.json** utlizando o method **POST**.
- Enviar na request, via body, os seguintes paramentros: **name, email, jobs**.
	- name - String : Nome completo do candidato
	- email - String : Email do candidato
	- jobs - [String] Array with Strings : Lista contendo as areas que o candidato deseja se inscrever. Os valores devem ser: **front, back, ios, android**.

Ao fazer a requisicao corretamente voce estará automaticamente na fase 2(testinho). Na fase 2 iremos enviar um email para todos os inscritos contendo as informacoes necessarias para execucao do testinho.
Para validar se voce se inscreveu corretamente basta analisar a chave **status** da response. A mesma deverá ser **success**. 

## Areas ##

### 1. Front-end ###
Requisitos necessarios:
- HTML
- CSS
- JS
- Logica de programacao
- Orientacao a objeto
- Ingles intermediario (necessário conseguir ler textos tecnicos e assistir video aulas em ingles) 

Diferenciais:
- Angular 2 ou algum framework (AngularJS, React, Vue, etc)
- Git
- MVC
- Typescript
- jQuery
- WordPress


### 2. Back-end ###
Requisitos necessarios:
- Python ou Ruby
- Banco de dados SQL
- Banco de dados NOSQL
- Logica de programacao
- Orientacao a objeto
- Linux
- Ingles intermediario (necessário conseguir ler textos tecnicos e assistir video aulas em ingles) 

Diferencias:
- Web2py, Flask, Rails ou algum framework (Express, Django, etc)
- Git
- MVC
- MongoDB
- MySQL
- REST API
- JSON
- AWS


### 3. Android ###
Requisitos necessarios:
- Android Studio
- Java
- Gradle
- Logica de programacao
- Orientacao a objeto
- Ingles intermediario (necessário conseguir ler textos tecnicos e assistir video aulas em ingles) 

Diferencias:
- Git
- MVC ou MVP
- REST API
- JSON


### 4. iOS ###
Requisitos necessarios:
- Xcode
- Swift ou Objective-C
- Cocoa Pods
- Logica de programacao
- Orientacao a objeto
- Ingles intermediario (necessário conseguir ler textos tecnicos e assistir video aulas em ingles) 

Diferencias:
- Git
- MVC
- REST API
- JSON