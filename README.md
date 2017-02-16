# CEPs

Este projeto busca manter uma base de dados de contribuição coletiva (do inglês,
_croudsourcing database_) para códigos de endereçamento postal (CEP) do Brasil.

Através de uma estrutura de dados no formato `JSON` e arquivos com nomenclatura
padronizada, esta base de dados pode ser utilizada como dependência em projetos
que necessitam de informações atualizadas relacionadas a CEPs no país.

## Formato

Todos os arquivos com informações sobre CEPs estão armazenados no diretório
`data/` e nomeados com o padrão `/^[0-9]{8}\.json$/`. Este arquivo contém um
documento no formato `JSON` com atributos que descrevem o endereço relacionado
ao CEP. Por exemplo, o primeiro código postal do Brasil, segundo a
[Wikipédia](https://pt.wikipedia.org/wiki/C%C3%B3digo_de_Endere%C3%A7amento_Postal),
está armazenado no arquivo `data/01001000.json` e possui o seguinte conteúdo.

```json
{
    "_id": "01001000",
    "tipo": "Praça",
    "logradouro": "da Sé",
    "bairro": "Sé",
    "cidade": "São Paulo",
    "estado": "SP"
}
```

## Contribuindo

Você pode contribuir com este projeto, adicionando ou atualizando informações
através de _Patch Requests_ (PRs). Caso esteja interessado, por favor, acesse o
arquivo
[`CONTRIBUTING.md`](https://github.com/carteiro/ceps/blob/master/CONTRIBUTING.md)
para mais detalhes sobre o assunto.

## Finalidade

A criação deste projeto surgiu com a necessidade de criar uma base de dados
atualizada para CEPs, independente de Correios ou qualquer tipo de Web Services.

Muitos projetos necessitam de informações sobre endereços a partir dos CEPs,
todavia, nem todos possuem a capacidade de conexão com servidores que
centralizam estes dados. Ainda, bases de dados _offline_ podem ser adquiridas de
empresas especializadas, porém nem sempre projetos de código-fonte aberto
possuem capital para isto.

Tendo isto em mente, o atual projeto busca centralizar uma base de dados,
independente de empresas, no formato de contribuição coletiva, onde os próprios
usuários podem manter as informações atualizadas.

## Licença

Esta base de dados é _opensource_ e está disponível sob a licença MIT, descrita
no arquivo [`LICENSE`](https://github.com/carteiro/ceps/blob/master/LICENSE).
