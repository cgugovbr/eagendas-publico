# e-Agendas - API Consulta

Esta é uma API pública, disponível para qualquer cidadão.

## URL da API
- Ambiente de Produção: https://eagendas.cgu.gov.br/api
- Ambiente de Treinamento: https://eagendastreinamento.cgu.gov.br/api

## Pré-requisitos

1. Token de acesso 

Para utilizar a API, é necessário um token. 
Siga as instruções abaixo para gerar seu próprio token:

## Testes

É possível testar a API por meio do swagger ou qualquer sistema de teste de API, 
ou ainda diretamente usando _curl_.

### Swagger

Para utilizar o swagger, siga os passos abaixo:

1. Acessar a documentação por meio da página (/api/docs): https://eagendastreinamento.cgu.gov.br/api/docs

2. Autorize o acesso utilizando o token do usuário, conforme instruções abaixo:

3. Teste uma requisição.

### Postman

Você também pode utilizar o [Postman](https://www.postman.com/), 
que oferece uma versão pessoal gratuita, para testar a API do e-Agendas. 

Para facilitar os testes, disponibilizamos arquivos a serem importados no Postman:

- [Variáveis](./e-Agendas%20-%20v2%20-%20Consulta.postman_collection.json)
- [Rotas da API](./e-Agendas%20-%20v2%20-%20Consulta.postman_collection.json)

Siga os passos abaixo para importar e configurar o Postman:

1. Importe os arquivos
2. Configure o token
3. Teste uma requisição

### Curl

Para testar a API via _curl_, utilize o código abaixo com o seu token de acesso.

```bash
curl -XGET http://eagendastreinamento.cgu.gov.br/api/v2/objetivos-compromissos -H "Accept: application/json" -H "Authorization: Bearer SEU_TOKEN_AQUI"
```

> Caso tenha um _jq_ instalado para visualizar os dados forma mais clara poderia utilizar "| jq" ao final:
