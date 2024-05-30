# Podcast Manager

## Descrição

O Podcast Manager é um aplicativo ao estilo Netflix, onde você pode centralizar diferentes episódios de podcasts separados por categorias. Ideal para organizar e assistir seus podcasts favoritos de vídeo.

## Features

-   Listar os episódios de podcasts em seções de categorias
    -   Categorias: saúde, bodybuilder, mentalidade, humor
-   Filtrar episódios por nome de Podcast

## Tecnologias

Este projeto utiliza as seguintes tecnologias:

-   [Node.js](https://nodejs.org/): Plataforma de execução de JavaScript no servidor.
-   [TypeScript](https://www.typescriptlang.org/): Um superconjunto de JavaScript que adiciona tipagem estática.
-   [tsx](https://github.com/esbuild-kit/tsx): Um executor TypeScript rápido e moderno.
-   [tsup](https://tsup.egoist.dev/): Um empacotador de código TypeScript para JavaScript.

### Features

#### Listar os episódios de podcasts em seções de categorias

**Endpoint:**

GET `/api/episodes`

**Response:**

```json
[
    {
        "podcastName": "flow",
        "episode": "IGORFINA - Extra Flow",
        "videoId": "vhykXU7PPVc",
        "category": ["humor", "bodybuilder"]
    },
    {
        "podcastName": "flow",
        "episode": "MC LAN - Flow #358",
        "videoId": "gMVFtfY6NRs",
        "category": ["humor", "música"]
    }
]
```

### Como vou implementar:

#### Listar os episódios de podcasts em seções de categorias

1. Criar um endpoint GET `/api/episodes` que retorna a lista de episódios de podcasts.
2. A resposta será uma lista de objetos, onde cada objeto representa um episódio de podcast com os seguintes campos:
    - `podcastName`: Nome do podcast
    - `episode`: Título do episódio
    - `videoId`: ID do vídeo
    - `category`: Lista de categorias às quais o episódio pertence

#### Filtrar episódios por nome de Podcast

**Endpoint:**

GET `/api/episodes?name={podcastName}`

**Descrição:**

Este endpoint retorna a lista de episódios baseado em um parâmetro enviado pelo cliente do nome do podcast.

**Exemplo de Uso:**

Para buscar episódios do podcast "flow":

```
GET /api/episodes?p=flow
```

**Response:**

```json
[
    {
        "podcastName": "flow",
        "episode": "IGORFINA - Extra Flow",
        "videoId": "vhykXU7PPVc",
        "category": ["humor", "bodybuilder"]
    },
    {
        "podcastName": "flow",
        "episode": "MC LAN - Flow #358",
        "videoId": "gMVFtfY6NRs",
        "category": ["humor", "música"]
    }
]
```

## Inicialização do Projeto

Para inicializar o projeto, siga os passos abaixo:

### Pré-requisitos

-   [Node.js](https://nodejs.org/) instalado
-   [npm](https://www.npmjs.com/) instalado

### Instalação

1. Clone o repositório:
    ```sh
    git clone https://github.com/seu-usuario/projeto_app_podcast.git
    ```
2. Navegue até o diretório do projeto:
    ```sh
    cd projeto_app_podcast
    ```
3. Instale as dependências:
    ```sh
    npm install
    ```

### Scripts Disponíveis

-   **Desenvolvimento:**

    ```sh
    npm run start:dev
    ```

    Este script inicia o servidor em ambiente de desenvolvimento usando `tsx`.

-   **Desenvolvimento com Watch:**

    ```sh
    npm run start:watch
    ```

    Este script inicia o servidor em ambiente de desenvolvimento com watch mode usando `tsx`.

-   **Construção para Produção:**

    ```sh
    npm run dist
    ```

    Este script compila o código TypeScript para JavaScript usando `tsup`.

-   **Iniciar em Produção:**
    ```sh
    npm run start:dist
    ```
    Este script compila o código e inicia o servidor usando o código compilado.

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir uma issue ou enviar um pull request.
