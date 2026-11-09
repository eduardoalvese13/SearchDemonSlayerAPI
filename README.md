# SearchDemonSlayerAPI

Atividade da Lista 25 da UC Usabilidade, Desenvolvimento Web, Mobile e Jogos (UniBH), professor Daniel Henrique Matos de Paiva.

Aplicação simples em **Blazor WebAssembly e .NET 10** que lista personagens de Demon Slayer, com navegação entre páginas. Exibe os campos solicitados: nome (`name`), idade (`age`), raça (`race`), citação (`quote`) e imagem (`img`). Campos vazios aparecem como “Não informado”.

## Como executar

É necessário ter o [SDK do .NET 10](https://dotnet.microsoft.com/download/dotnet/10.0) instalado e acesso à internet.

Na pasta do projeto:

```bash
dotnet restore
dotnet run --urls http://localhost:5000
```

Abra `http://localhost:5000` no navegador. Os botões **Anterior** e **Próxima** percorrem as páginas. Em caso de falha, use **Tentar novamente**. Não é necessário banco de dados, chave de API ou servidor próprio de backend.

## API utilizada

- [Documentação](https://www.demonslayer-api.com/documentation)
- Endpoint: `https://www.demonslayer-api.com/api/v1/characters?page=1`

As consultas são feitas diretamente pelo navegador. A API precisa estar disponível e permitir acesso entre origens (CORS).

## Compilar

```bash
dotnet build
dotnet publish -c Release
```

A publicação estática fica em `bin/Release/net10.0/publish/wwwroot`.

## Validação

Validações realizadas: compilação sem erros ou avisos, publicação em Release e teste no Chromium dos campos, imagem, paginação, campos vazios, falha HTTP e nova tentativa, usando respostas simuladas. Nesta implementação, a consulta à API real ficou limitada pelo bloqueio do domínio na rede do ambiente de desenvolvimento; isso não comprova indisponibilidade da API. Testes com respostas simuladas verificam a interface, mas não substituem a conferência com a API real.

## Entrega

Repositório: https://github.com/eduardoalvese13/SearchDemonSlayerAPI

O link deve ser entregue individualmente no Google Classroom, conforme solicitado na atividade.
