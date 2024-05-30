# Podcast Manager

### Descrição

App ao estilo Netflix, aonde possa centralizar diferentes episódios de podcasts separados por categorias

### Domínio

Podcast feitos em Vídeo

### Features

-   Listar os episódios de podcasts em seções de categorias
    -   [saúde, bodybuilder, mentalidade, humor]
-   Filtrar episódios por nome de Podcast

## Como

#### Features

-   Listar os episódios de podcasts em seções de categorias

### Como vou implementar:

GET: Retorna lista de episódios

response:

```js
[
    {
        podcastName: "flow",
        episode: "IGORFINA - Extra Flow",
        videoId: "vhykXU7PPVc",
        cover: "https://i.ytimg.com/vi/vhykXU7PPVc/maxresdefault.jpg",
        link: "https://www.youtube.com/watch?v=vhykXU7PPVc",
        category: ["humor", "bodybuilder"],
    },
    {
        podcastName: "flow",
        episode: "MC LAN - Flow #358",
        videoId: "gMVFtfY6NRs",
        cover: "https://i.ytimg.com/vi/gMVFtfY6NRs/maxresdefault.jpg",
        link: "https://www.youtube.com/watch?v=gMVFtfY6NRs",
        category: ["humor", "música"],
    },
];
```

GET: Retorna a lista de episódios baseado em um parâmetro enviado pelo cliente do nome do podcast
