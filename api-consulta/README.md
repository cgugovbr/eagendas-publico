# e-Agendas - API Consulta

Esta é uma API pública, disponível para qualquer cidadão.

## URL da API
- Ambiente de Produção: https://eagendas.cgu.gov.br/api
- Ambiente de Treinamento: https://eagendastreinamento.cgu.gov.br/api

## Pré-requisitos

- Token de acesso 

Para utilizar a API, é necessário um token. 
Siga as instruções abaixo para gerar seu próprio token:

1. Faça login no sistema
2. Acesso a página de perfil do usuário
   ![image](https://github.com/cgugovbr/eagendas-publico/assets/905951/70737104-ad13-4f23-9959-67e981a14456)

3. Acesse o menu 'Meus tokens' e gere um novo token
   ![image](https://github.com/cgugovbr/eagendas-publico/assets/905951/b174bbfd-a3ac-465c-b1b3-f48cc2a9e5fc)
  
> Lembre-se de guardar esse token, pois ele não poderá ser mostrado novamente.

## Testes

É possível testar a API por meio do swagger ou qualquer sistema de teste de API, 
ou ainda diretamente usando _curl_.

### Swagger

Para utilizar o swagger, siga os passos abaixo:

1. Acessar a documentação por meio da página (/api/docs): https://eagendastreinamento.cgu.gov.br/api/docs
   ![image](https://github.com/cgugovbr/eagendas-publico/assets/905951/fa5719bc-de71-40ae-a64f-cedb3451dfd8)

2. Autorize o acesso utilizando o token do usuário, conforme instruções abaixo:
  - Clique em Authorize:
     ![image](https://github.com/cgugovbr/eagendas-publico/assets/905951/a55713d9-9e20-412b-a2d6-69d5bd44f042)

  - Insira o token no campo 'value' e clique em '_Authorize_'
     ![image](https://github.com/cgugovbr/eagendas-publico/assets/905951/6bf4cd30-c818-4cc9-b726-60bbdf0d0ec5)

3. Teste uma requisição:
  - clique na requisição desejada e clique em '_Try it out_':
    ![image](https://github.com/cgugovbr/eagendas-publico/assets/905951/43369518-a6ca-40d1-ad18-cfbe5e0b06d7)

  - Clique em '_Execute_'
    ![image](https://github.com/cgugovbr/eagendas-publico/assets/905951/90249192-8127-41a0-b6e3-a371cef3a8a2) 

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
