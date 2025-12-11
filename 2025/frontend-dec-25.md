# Processo Seletivo - Desenvolvedor Front-End (Estágio)

Olá, candidato(a)! Bem-vindo(a) ao processo seletivo da **Instabuy**.

Nesta etapa, avaliaremos suas habilidades técnicas através de um desafio prático. Recomendamos que você utilize boas práticas de programação e desenvolva um código bem estruturado.

---

## Prazo de Entrega

**17 de dezembro de 2025 (quarta-feira) às 23:59**

> ⚠️ Sob nenhuma hipótese serão aceitos testes enviados após o prazo.

---

## O que você deve entregar

### 1. Repositório no GitHub
- Código-fonte do projeto desenvolvido
- Framework recomendado: **React** ou **Angular** (outras opções também são aceitas)
- README explicando como rodar o projeto localmente

### 2. Projeto Hospedado (Deploy)
O projeto deve estar **hospedado e acessível** em algum serviço de sua escolha, como:
- [Vercel](https://vercel.com)
- [Netlify](https://netlify.com)
- [Railway](https://railway.app)
- AWS S3 + CloudFront
- Ou qualquer outro serviço de hospedagem

> 📌 **Importante:** Precisamos acessar tanto o código-fonte quanto o projeto funcionando online.

### 3. Envio por E-mail
Envie um e-mail para **cayke@instabuy.com.br** e **joao.jorge@instabuy.com.br** com:

| Campo | Informação |
|-------|------------|
| **Assunto** | PS Dev Front |
| **Conteúdo** | Seu nome completo |
| | Telefone para contato |
| | Link do repositório GitHub |
| | Link do projeto hospedado |
| | Portfólio (se tiver) |

> ⚠️ E-mails com assunto diferente de "PS Dev Front" serão desconsiderados.

---

## O que será avaliado

- **Qualidade do código:** organização, boas práticas, legibilidade
- **CSS e Layout:** boas práticas de CSS, visual agradável, responsividade
- **Raciocínio:** como você estruturou o projeto e resolveu os problemas

> 💡 **Dica:** Os links de referência servem apenas para você entender o contexto e os dados que deve exibir. Não é necessário replicar o design — sinta-se livre para criar seu próprio layout!

---

## O Desafio

Desenvolva duas telas de um **e-commerce** consumindo a API da Instabuy:

### Tela 1: Home

Exiba os **banners** e **produtos** retornados pela API.

Cada card de produto deve conter:
- Imagem
- Nome
- Preço

**Referência de design:** https://supermercado.instabuy.com.br/

#### Endpoint

| | |
|---|---|
| **Base URL** | `https://api.instabuy.com.br/apiv3/` |
| **Endpoint** | `layout` |
| **Método** | `GET` |
| **Parâmetros** | `subdomain=supermercado` |
| **Documentação** | https://docs.instabuy.com.br/#layout |

---

### Tela 2: Detalhes do Produto

Ao clicar em um produto, exiba uma tela com:
- Nome
- Preço
- Imagens
- Descrição
- Botão "Adicionar ao carrinho"

**Referência de design:** https://supermercado.instabuy.com.br/p/Iogurte-Integral-Morango-Batavo-Pedacos-Pote-500g

#### Endpoint

| | |
|---|---|
| **Base URL** | `https://api.instabuy.com.br/apiv3/` |
| **Endpoint** | `item` |
| **Método** | `GET` |
| **Parâmetros** | `subdomain=supermercado` e `slug={slug-do-produto}` |
| **Documentação** | https://docs.instabuy.com.br/#item |

---

## Informações Técnicas

### Estrutura da Response

Todas as respostas da API possuem a seguinte estrutura:

```json
{
  "status": "success", // ou "error"
  "data": { ... }      // conteúdo da resposta
}
```

### URLs das Imagens

#### Imagem do Banner
```
https://ibassets.com.br/ib.store.banner/bnr-{banner.image}
```

#### Imagem do Produto
```
https://ibassets.com.br/ib.item.image.{tamanho}/{prefixo}-{product.photo}
```

| Tamanho | Prefixo | Uso recomendado |
|---------|---------|-----------------|
| `small` | `s` | Miniaturas |
| `medium` | `m` | Cards de produto |
| `big` | `b` | Página de detalhes |
| `large` | `l` | Visualização ampliada |

**Exemplo:**
```
https://ibassets.com.br/ib.item.image.medium/m-5b586ad8c98945c597d3d3240c633df5.jpeg
```

---

## Boa sorte!

Estamos ansiosos para conhecer seu trabalho e, quem sabe, trabalharmos juntos!

**Equipe Instabuy**




