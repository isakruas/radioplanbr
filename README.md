# RadioPlan BR

Ferramenta web de planejamento de cobertura RF para radioamadores brasileiros. Estima a area de cobertura de sinais de transmissao utilizando modelos de propagacao e dados reais de elevacao do terreno.

## Funcionalidades

- **Modelos de propagacao**: Friis, Okumura-Hata (urbano, suburbano, rural), COST-231, ECC-33, Ericsson
- **Analise de linha de visada (LoS)** com opcao de zona de Fresnel
- **Presets de faixas brasileiras**: 80m, 40m, 20m, 15m, 10m, 6m, 2m, 70cm, 23cm
- **Visualizacao**: poligono de cobertura, mapa de calor ou combinado
- **Elevacao real do terreno** via Google Maps Elevation API
- **Exportacao KML** para uso no Google Earth
- **Metricas**: alcance maximo, alcance medio, area de cobertura, niveis de sinal

## Como usar

1. Acesse a aplicacao pelo navegador
2. Clique em **Carregar** para inicializar o mapa (a API Key ja esta configurada)
3. Clique no mapa para posicionar a antena
4. Ajuste os parametros de transmissao (potencia, frequencia, altura, ganho, etc.)
5. Selecione o modelo de propagacao adequado
6. Clique em **Calcular Cobertura**
7. Analise os resultados no mapa e exporte em KML se desejar

## Tecnologias

- Vue.js 3 (CDN)
- Bootstrap 5.3
- Google Maps JavaScript API + Elevation API

## Deploy

A aplicacao e publicada automaticamente via GitHub Actions no GitHub Pages a cada push na branch `master`.

## Estrutura

```
index.html          # Aplicacao completa (SPA single-file)
.github/workflows/  # Workflow de deploy para GitHub Pages
```

## Licenca

Uso pessoal / radioamadorismo.
