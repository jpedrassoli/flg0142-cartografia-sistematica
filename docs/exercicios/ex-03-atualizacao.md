# Ex. 03 — SR + SIG: atualizar a mancha urbana com Landsat 9 e limites do IBGE

**Aula:** 3 · **Ferramenta:** QGIS · **Duração:** ~3h

## Objetivo

Combinar três fontes sobre a mesma área — a **carta de Campinas de 1980** (base sistemática), uma imagem **Landsat 9 de 2025** (SR) e os **limites municipais do IBGE** (SIG) — para atualizar a **mancha urbana na escala da carta (1:50.000)** e medir a expansão regional de Campinas.

## Material / dados

- `campinas_georref.tif` (Ex. 02, ou versão de referência do docente).
- **Cena Landsat 9 (2025)** que cobre Campinas — bandas multiespectrais (30 m). O docente baixa uma vez e distribui (ver nota).
- **Malha municipal do IBGE** (ex.: `BR_Municipios_2023`), em shapefile/GeoPackage.
- Projeto QGIS em **SIRGAS 2000 / UTM 23S (EPSG:31983)**.

!!! note "De onde vem o Landsat (docente)"
    Baixe uma cena no **USGS EarthExplorer** (earthexplorer.usgs.gov, conta gratuita) — busque por Campinas e filtre *Landsat 9 OLI/TIRS C2 L2*, 2025, com baixa cobertura de nuvens. Alternativa: o complemento **Semi-Automatic Classification Plugin (SCP)** baixa Landsat dentro do QGIS. Distribua as bandas 2–7 para os alunos (evita 40 downloads).

## Parte A — SIG: recortar Campinas pelos limites do IBGE (30 min)

1. Carregue a **malha municipal do IBGE**.
2. Selecione Campinas: **Selecionar feições por expressão** → `"NM_MUN" = 'Campinas' AND "SIGLA_UF" = 'SP'` (ou `"CD_MUN" = '3509502'`).
3. **Botão direito → Exportar → Salvar feições selecionadas como** → `campinas_limite.gpkg`, SRC **EPSG:31983**.
4. Este polígono é a **máscara** de recorte e a moldura do trabalho.

## Parte B — SR: compor a imagem Landsat 9 (50 min)

5. Carregue as bandas do Landsat (cada banda é um raster). Se vierem separadas, empilhe: **Raster → Miscelânea → Mesclar** com *"Colocar cada arquivo de entrada em uma banda separada"* marcado → `landsat_stack.tif`.
6. Estilize como **cor multibanda** (*Propriedades → Simbologia*):
   - **Cor natural (4-3-2):** R=B4, G=B3, B=B2 → a cidade aparece cinza.
   - **Falsa-cor urbana (6-5-4):** R=B6 (SWIR1), G=B5 (NIR), B=B4 → a vegetação fica verde-viva, o **construído** fica em tons rosa/magenta, a água escura. É a melhor para ver a mancha urbana.
7. *(Opcional, SR quantitativo)* **NDBI** na Calculadora raster: `("B6" - "B5") / ("B6" + "B5")`. Valores altos = construído. Ajuda a delimitar a mancha.

## Parte C — SIG: recortar tudo por Campinas (20 min)

8. **Raster → Extração → Recortar raster por camada de máscara** → entrada = Landsat (stack); máscara = `campinas_limite`. Repita para a carta de 1980, se quiser.
9. Agora Landsat e carta estão restritos ao município — a leitura fica limpa.

## Parte D — Atualizar a mancha urbana (50 min)

10. Crie uma camada de polígonos `mancha_urbana` (EPSG:31983) com um campo `ano` (inteiro).
11. **Mancha de 1980:** sobre a carta, contorne a área urbana de então (lendo a simbologia da folha). `ano = 1980`.
12. **Mancha de 2025:** sobre a **falsa-cor 6-5-4** (ou guiando-se pelo NDBI), contorne a área urbana atual. Trabalhe na escala **1:50.000** — você mapeia a **extensão** urbana, não quadras. `ano = 2025`.
13. Estilize por `ano` (*Categorizado*): 1980 tracejado, 2025 sólido translúcido.

> A resolução de 30 m limita o detalhe — e isso é correto para 1:50.000. Um contorno "liso demais" na borda é honesto nessa escala.

## Parte E — Medir a expansão regional (30 min)

14. Calculadora de campo → `area_km2` = `$area/1000000`.

| Ano | Área urbana (km²) |
|-----|-------------------|
| 1980 | |
| 2025 | |

15. Calcule: crescimento absoluto (km²), relativo (%) e taxa anual média (÷ ~45 anos).
16. Compare com a área total do município (do limite IBGE): que fração de Campinas era urbana em 1980? E em 2025?

## Discussão

- Que papel teve cada fonte? (carta = base 1980; Landsat = estado atual/SR; IBGE = recorte/SIG)
- Por que o Landsat serve a 1:50.000 e **não** a 1:2.000? Relacione com o pixel de 30 m e o limite gráfico.
- A falsa-cor 6-5-4 separou o construído da vegetação melhor que a cor natural? Por quê (resposta espectral do SWIR)?

## Entrega

- [ ] `campinas_limite` recortado do IBGE.
- [ ] Composições Landsat (natural e falsa-cor) e, se fez, o NDBI.
- [ ] Camada `mancha_urbana` com 1980 e 2025, recortada por Campinas.
- [ ] Tabela de áreas + crescimento absoluto, relativo e taxa anual.

!!! note "Duas escalas"
    Aqui a atualização é **regional**, na escala da carta (Landsat, 1:50.000). O detalhe fino — **vias e pontos** sobre imagem de alta resolução — vem na **sub-região** (Ex. 06), em escala maior. Guarde as manchas: elas serão cruzadas com o relevo (Aula 13).
