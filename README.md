# Ponto Web API Requests

Artefatos revisados da integração externa do Secullum Ponto Web, validados contra o Swagger vivo e o manual PDF oficial.

Modelos disponíveis:
- Postman: [postman](./postman/)
- Bruno/OpenCollection YAML: [bruno](./bruno/)

Conteúdo da pasta `postman/`:
- `secullum-ponto-web.postman_collection.json`
- `secullum-ponto-web.postman_environment.json`

Links úteis:
- Swagger UI: [https://pontowebintegracaoexterna.secullum.com.br/docs/index.html](https://pontowebintegracaoexterna.secullum.com.br/docs/index.html)
- Swagger JSON: [https://pontowebintegracaoexterna.secullum.com.br/swagger/v1/swagger.json](https://pontowebintegracaoexterna.secullum.com.br/swagger/v1/swagger.json)
- Manual PDF: [https://github.com/Secullum/PontoWebIntegracaoExternaExemplo/blob/master/Integracao_Externa_Ponto_Web.pdf](https://github.com/Secullum/PontoWebIntegracaoExternaExemplo/blob/master/Integracao_Externa_Ponto_Web.pdf)
- Wiki do repositório: [https://github.com/luizGDpulz/ponto-web-api-requests/wiki](https://github.com/luizGDpulz/ponto-web-api-requests/wiki)

Notas rápidas:
- A collection prioriza o Swagger atual como fonte de verdade quando houver divergência com o PDF.
- O PDF ainda cita `IntegracaoExterna/Pendencias`, mas essa rota não aparece no Swagger atual.
- O Swagger atual expõe `GravarLogsIniciarBkp` e `PontoOffline/AssinaturaArquivo/Assinar`, que não aparecem no PDF.

## Uso rápido no Postman

1. Importe `postman/secullum-ponto-web.postman_collection.json`.
2. Importe `postman/secullum-ponto-web.postman_environment.json`.
3. Selecione o environment importado e preencha pelo menos `username` e `password`.
4. Execute `Autenticação e Seleção de Banco / Token`.
5. Execute `Autenticação e Seleção de Banco / Listar Bancos`.
6. Rode as demais requests da API.

Fluxo automático:
- `Token` grava `access_token` automaticamente na collection e também no environment ativo.
- `Listar Bancos` grava `selected_bank_id`, `selected_bank_identificador` e `selected_bank_name` automaticamente na collection e também no environment ativo.
- As demais requests já herdam `Authorization: Bearer {{access_token}}` e enviam `secullumidbancoselecionado: {{selected_bank_id}}`.
- Se você não selecionar environment, a collection ainda funciona via collection variables; com environment ativo, os valores ficam persistidos nele também.

## Uso no Bruno

Abra a pasta `bruno/` como collection no Bruno 3.x.

Documentação expandida e guias de uso devem ficar na wiki do repositório.
