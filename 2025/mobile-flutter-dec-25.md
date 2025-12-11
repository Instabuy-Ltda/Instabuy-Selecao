# Processo Seletivo - Desenvolvedor Mobile Flutter

Olá, candidato(a)!

Nesta etapa, você terá a oportunidade de demonstrar seus conhecimentos técnicos através de um desafio prático. Recomendamos que utilize boas práticas de programação e desenvolva um código bem estruturado e legível.

## Prazo de Entrega

**Conforme orientado a você por e-mail.**

Não serão aceitos testes entregues fora do prazo estabelecido.

## O Que Entregar

Você deverá enviar o **código-fonte completo** do projeto desenvolvido. 

### Requisitos Técnicos

- O projeto deve ser desenvolvido em **Flutter (Dart)**
- Não utilize frameworks que exijam instalação adicional pelo avaliador
- Você pode utilizar bibliotecas de terceiros (pub.dev) desde que não seja necessário nenhum passo adicional além dos comandos padrão do Flutter
- **Projetos que não executem corretamente com `flutter run` serão desclassificados**

### Como Enviar

Envie um e-mail para **paulo.rezende@instabuy.com.br** com:
- **Assunto:** "PS Dev Mobile" (e-mails com outro assunto serão desconsiderados)
- **Nome completo e telefone** para contato
- **Currículo e/ou portfólio**
- **Link do repositório** (GitHub, GitLab, etc.) contendo o projeto

A Instabuy deseja boa sorte a todos! Estamos ansiosos para trabalharmos juntos!

---

# Desafio Técnico

## Objetivo

Desenvolver um aplicativo Flutter que consuma a API da Instabuy e exiba uma tela contendo **banners e produtos**.

### Requisitos da Interface

Cada card de produto deve conter:
- Imagem do produto
- Nome do produto
- Preço

Você pode utilizar bibliotecas de terceiros, desde que não exijam instalação manual por parte do avaliador.

## Especificações da API

### Endpoint Principal
```
URL Base: https://api.instabuy.com.br/apiv3/
Endpoint: layout
Método: GET
Parâmetro: subdomain=bigboxdelivery
```

### Estrutura da Response

Todas as respostas contêm três campos:

- **status**: `'success'` ou `'error'`
- **data**: conteúdo da resposta (pode ser objeto, lista, string, etc.)
- **type**: tipo do valor em `data`

📖 **Documentação completa:** https://docs.instabuy.com.br/#layout

### URLs das Imagens

**Banners:**
```
https://assets.instabuy.com.br/ib.store.banner/bnr-{{banner.image}}
```

**Produtos:**
```
https://assets.instabuy.com.br/ib.item.image.{RESOLUÇÃO}/{PREFIXO}-{{product.photo}}
```

**Resoluções disponíveis:**
- Small: `ib.item.image.small` / prefixo `s-`
- Medium: `ib.item.image.medium` / prefixo `m-`
- Big: `ib.item.image.big` / prefixo `b-`
- Large: `ib.item.image.large` / prefixo `l-`

**Exemplo:**
Para uma imagem com `thumb = 20161023214840752541600349dcf4284c2592bd49355774b7b1.jpg` em resolução média:
```
https://assets.instabuy.com.br/ib.item.image.medium/m-20161023214840752541600349dcf4284c2592bd49355774b7b1.jpg
```

**Sinta-se à vontade para ir além do solicitado e demonstrar suas habilidades! Consulte a documentação da nossa API para descobrir outros recursos.**