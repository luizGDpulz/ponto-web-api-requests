# Ponto Web API Requests

Collection da integração externa do Secullum Ponto Web, revisada contra o Swagger vivo e o manual PDF oficial.

Modelos disponíveis:
- Postman: [pontoweb_integracao_externa_postman_collection.json](./pontoweb_integracao_externa_postman_collection.json)
- Bruno/OpenCollection YAML: [bruno](./bruno/)

Links úteis:
- Swagger UI: [https://pontowebintegracaoexterna.secullum.com.br/docs/index.html](https://pontowebintegracaoexterna.secullum.com.br/docs/index.html)
- Swagger JSON: [https://pontowebintegracaoexterna.secullum.com.br/swagger/v1/swagger.json](https://pontowebintegracaoexterna.secullum.com.br/swagger/v1/swagger.json)
- Manual PDF: [https://github.com/Secullum/PontoWebIntegracaoExternaExemplo/blob/master/Integracao_Externa_Ponto_Web.pdf](https://github.com/Secullum/PontoWebIntegracaoExternaExemplo/blob/master/Integracao_Externa_Ponto_Web.pdf)
- Wiki do repositório: [https://github.com/luizGDpulz/ponto-web-api-requests/wiki](https://github.com/luizGDpulz/ponto-web-api-requests/wiki)

Notas rápidas:
- A collection prioriza o Swagger atual como fonte de verdade quando houver divergência com o PDF.
- O PDF ainda cita `IntegracaoExterna/Pendencias`, mas essa rota não aparece no Swagger atual.
- O Swagger atual expõe `GravarLogsIniciarBkp` e `PontoOffline/AssinaturaArquivo/Assinar`, que não aparecem no PDF.

Documentação expandida e guias de uso devem ficar na wiki do repositório.

Para usar no Bruno 3.x, abra a pasta `bruno/` como collection.
