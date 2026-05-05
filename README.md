# Mapa de Árvores — Flores da Cunha

Mapa interativo das 100 árvores plantadas em comemoração aos 100 anos do município de Flores da Cunha. Projeto da equipe **MARCOLINA** para a gincana municipal.

## Estrutura

```
mapa-arvores/
├── index.html       # página principal (Leaflet + OpenStreetMap)
├── arvores.json     # base de dados das árvores
└── img/             # fotos das placas (arvore_NN.jpg)
```

## Como adicionar uma árvore

Edite `arvores.json` e adicione um objeto no array:

```json
{
  "numero": 47,
  "nome": "Ipê-amarelo",
  "nome_cientifico": "Handroanthus albus",
  "ano_fato": 1971,
  "fato": "É inaugurado um novo centro de saúde em Flores da Cunha.",
  "local": "Praça da Bandeira",
  "latitude": -29.0294,
  "longitude": -51.1817,
  "foto": "img/arvore_47.jpg"
}
```

Coloque a foto correspondente em `img/arvore_47.jpg` (ou ajuste o caminho no campo `foto`). Se a foto não existir, o card mostra um placeholder automaticamente.

## Coordenadas

Para pegar latitude/longitude de cada árvore: abra o [Google Maps](https://maps.google.com), clique com botão direito no ponto exato, e copie as coordenadas que aparecem no menu.

## Publicar no GitHub Pages

1. Faça push do repositório para o GitHub.
2. Em **Settings → Pages**, selecione a branch `main` e a pasta `/ (root)`.
3. O mapa fica disponível em `https://<usuario>.github.io/<repositorio>/`.

## Tecnologia

- [Leaflet](https://leafletjs.com/) (mapa)
- [OpenStreetMap](https://www.openstreetmap.org/) (tiles, gratuito, sem chave de API)
- HTML/CSS/JS puro, sem build step
