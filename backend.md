# Processo seletivo desenvolvedor back-end Instabuy #

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


# Testinho Back-end #
O testinho consiste em desenvolver um sistema **(aplicação, banco de dados e API)** que rodará localmente. Para tal o candidato podera utlizar as linguagens de programacao **Python ou Ruby**.

O candidato poderá utilizar frameworks e libs de terceiros desde que seja documentado todos os passos necessarios para instalacao dos pacotes.

A aplicacao deverá rodar em ambientes **UNIX**, MacOS ou Ubuntu.


## O que fazer ##

Desenvolver sistema onde seja possivel executar CRUD de pessoas e endereços atraves de uma **API REST** com formato **JSON**


### Request Method e funcoes ###

Para cada method da request deverá ser feita uma funcao diferente.

- GET: retornar os dados de uma pessoa/endereço. Parametros enviados via query.
- PUT: adicionar uma pessoa/endereço. Parametros enviados via body.
- DELETE: remove uma pessoa/endereço. Parametros enviados via body.
- POST: atualiza os dados de uma pessoa/endereço. Parametros enviados via body.


#### Pessoa ####
Cada pessoa deverá ter os dados descritos abaixo. Na request os parametros terao o mesmo nome como descrito abaixo.

- id: (string ou int) Identificador do usuario gerado pelo sistema.
- name: (string) Nome da pessoa.
- age: (int) Idade da pessoa.
- cpf: (int) Cpf da pessoa. **o cpf deverá ser validado pela aplicacao. Caso cpf seja invalido, retornar uma mensagem de erro na response.**
- addresses: (list of address) Lista de endereços da pessoa.


#### Endereço ####
Cada endereço deverá ter os dados descritos abaixo. Na request os parametros terao o mesmo nome como descrito abaixo.

O endereço deverá ser relacionado a uma pessoa. Ao adicionar um endereço deverá ser passado o ID da pessoa em questao.

- id: (string ou int) Identificador do endereço gerado pelo sistema.
- zipcode: (string) Cep do endereço.
- state: (string) Estado.
- city: (string) Cidade.
- street: (string) Rua
- number: (int) numero da casa.
- person_id: (string ou int) Identificador da pessoa que cadastrou esse endereço.


### Exemplos praticos ###
Abaixo segue-se algums exemplos de comportamentos esperados.

#### 1. Adicionar pessoa ####
Request para adicionar uma pessoa nova:

		url: http://localhost/person
		method: PUT
		params: {
			name : "Cayke Prudente",
			age : 24,
			cpf : 03487448114,
		}

Resposta esperada:

		Identificacao de sucesso ou erro
		Em caso de sucesso, retornar o ID da pessoa. 
		

#### 2. Atualizar pessoa ####
Request para atualizar idade de uma pessoa cujo ID = 0001:

		url: http://localhost/person
		method: POST
		params: {
			id : 0001,
			age : 25
		}

Resposta esperada:

		Identificacao de sucesso ou erro
		
#### 3. Adicionar endereço ####
Request para adicionar um endereço para uma pessoa cujo ID = 0001:

		url: http://localhost/person
		method: PUT
		params: {
			zipcode: "70200-020",
			state: "DF",
			city: "Brasilia",
			street: "Sqs 404 bloco B",
			number: 107,
			person_id: 0001
		}

Resposta esperada:

		Identificacao de sucesso ou erro
		Em caso de sucesso, retornar o ID do endereço. 
