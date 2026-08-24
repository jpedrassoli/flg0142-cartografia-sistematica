# Ex. 02 — Georreferenciar a carta de Campinas e descobrir a desatualização

**Aula:** 2 · **Ferramenta:** QGIS · **Duração:** ~2h

## Objetivo

Georreferenciar a carta topográfica de Campinas (IBGE, 1:50.000, anos 1980), lendo os elementos da moldura para isso, e descobrir a desatualização ao sobrepô-la à imagem de satélite atual. É o **ponto de partida do estudo de caso** do semestre.

## Material / dados

- **Carta topográfica de Campinas** (IBGE, 1:50.000) digitalizada (imagem/PDF).
- QGIS com o SRC do projeto em **SIRGAS 2000 / UTM 23S (EPSG:31983)**.
- Camada **Esri World Imagery** ou **Google Satellite** ([XYZ Tiles](../ambiente/setup-xyz-tiles.md)).

## Passo a passo

### Parte A — Ler a moldura (20 min)
1. Localize na moldura: escala, **datum** (a carta dos anos 1980 provavelmente está em **Córrego Alegre** ou **SAD-69**), **projeção** (UTM, fuso 23), e os **valores de coordenadas** impressos nos cantos e na quadrícula.
2. Anote o SRC da folha. Ex.: Córrego Alegre / UTM 23S ≈ **EPSG:22523**; SAD-69 / UTM 23S ≈ **EPSG:29193**.

> Sem ler datum, projeção e coordenadas, não há como georreferenciar — a "anatomia da folha" vira condição do trabalho.

### Parte B — Georreferenciador (10 min)
3. Menu **Camadas → Georreferenciador**.
4. **Abrir raster** → a carta.
5. **Configurações de transformação:** *Polinomial 1*; reamostragem *Vizinho mais próximo*; **SRC de destino = o SRC lido na Parte A**; raster de saída `campinas_georref.tif`; marque *Carregar no QGIS ao concluir*.

### Parte C — Pontos de controle (40 min)
6. Use **cruzamentos da quadrícula** (a coordenada é conhecida com exatidão).
7. **Adicionar ponto** → clique no cruzamento na imagem → digite E e N lidos na moldura. Repita.
8. **Pelo menos 4 pontos**, bem distribuídos (cantos + centro).
9. Acompanhe o **resíduo** de cada ponto; refaça os que destoarem.

### Parte D — Georreferenciar e revelar a desatualização (40 min)
10. **Iniciar georreferenciamento**. A carta entra no projeto.
11. Adicione a **Esri World Imagery / Google Satellite** por baixo (ou por cima com transparência).
12. Reduza a **opacidade** da carta (*Propriedades → Simbologia → Opacidade ~50%*) e sobreponha à imagem atual.
13. **Observe:** onde a carta de 1980 e a imagem de hoje **não batem**? A mancha urbana da carta é muito menor. Vias que não existiam. Loteamentos onde a carta mostra vazio. **Anote e discuta** — é o gancho do estudo de caso.

### Parte E — Datum (20 min)
14. Se a carta estiver em Córrego Alegre e a imagem em Web Mercator/SIRGAS, haverá um pequeno deslocamento sistemático além da desatualização real. Distinga os dois: o deslocamento de **datum** (poucas dezenas de metros, uniforme) × a **mudança real** do território (a cidade cresceu). Registre.

## Discussão

- Por que a carta "não bate mais" com a realidade? (ela é datada — anos 1980)
- Qual parte do descolamento é **datum** e qual é **mudança real**?
- Que elementos da moldura foram indispensáveis?

## Entrega

- [ ] `campinas_georref.tif` sobre a imagem de satélite.
- [ ] Tabela de pontos de controle com resíduos.
- [ ] Anotação: datum lido + 3 lugares onde a desatualização é evidente.

!!! note "Guarde"
    Esta carta georreferenciada é a base de **todo o estudo de caso**. Se você faltou, use a versão de referência do docente.
