# RadioPlan BR

Ferramenta web de planejamento de cobertura RF para radioamadores brasileiros. Estima a area de cobertura de sinais de transmissao utilizando modelos de propagacao e dados reais de elevacao do terreno.

## Funcionalidades

### Modelos de propagacao
- Friis (espaco livre)
- Okumura-Hata (urbano, suburbano, rural)
- COST-231
- ECC-33
- Ericsson

### Antenas
- **Omnidirecional** — irradiacao uniforme em 360 graus
- **Direcional** — Yagi ou Parabolica, com ganho e abertura configuraveis
- **Cardioide** — padrao cardioide com razao frente-costas ajustavel
- **Custom** — importacao de diagrama de irradiacao a partir de arquivo texto (angulo x ganho)
- Diagrama de irradiacao plotado diretamente no mapa, com rotacao por azimute

### Analise de Linha de Visada (LoS)
- Perfil de elevacao entre transmissor e ponto de interesse
- Zona de Fresnel com raio calculado para a frequencia selecionada

### Presets de faixas brasileiras
80m, 40m, 20m, 15m, 10m, 6m, 2m, 70cm, 23cm — com frequencias e modelos pre-configurados

### Visualizacao
- Poligono de cobertura
- Mapa de calor (heatmap)
- Combinado (poligono + mapa de calor)

### Terreno e mapa
- Elevacao real do terreno via Google Maps Elevation API
- Mapa inicializa em modo terrain (curvas de nivel)

### Exportacao
- **KML** para uso no Google Earth
- **Repetidoras (JSON)** — exportar e importar lista de repetidoras para compartilhamento

### Repetidoras
- Cadastro de repetidoras com nome, frequencia, shift e tom CTCSS
- Verificacao automatica de alcancabilidade (dentro ou fora do poligono de cobertura)
- Importar/exportar repetidoras em formato JSON
- Persistencia via localStorage

### Metricas
- Alcance maximo e medio
- Area de cobertura estimada
- Niveis de sinal

### Persistencia
- Configuracoes e repetidoras salvas automaticamente no localStorage do navegador

## Como usar

1. Acesse a aplicacao pelo navegador
2. Clique em **Carregar** para inicializar o mapa (a API Key ja esta configurada)
3. Clique no mapa para posicionar a antena
4. Ajuste os parametros de transmissao (potencia, frequencia, altura, ganho, etc.)
5. Selecione o tipo de antena e o modelo de propagacao adequado
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
