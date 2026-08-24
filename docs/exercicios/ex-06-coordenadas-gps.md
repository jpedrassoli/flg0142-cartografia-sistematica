# Ex. 06 — A sub-região: coordenadas, recorte e GPS

**Aula:** 6 · **Ferramenta:** QGIS + app de GPS · **Duração:** ~2h30

## Objetivo

Formalizar a sub-região do estudo de caso lendo suas coordenadas UTM; converter coordenadas; e coletar pontos com o celular, avaliando a precisão — o GPS que a atualização (Ex. 03) ainda não tinha.

## Material / dados

- Projeto de Campinas (carta + imagem + camadas de atualização do Ex. 03).
- Celular com **GPS & Maps** (ou *GPS Test* + *UTM Geo Map*). Ver [apps](../ambiente/setup-apps-celular.md).

## Parte A — Converter (20 min)

Aritmética (1' = 1/60°, 1" = 1/3600°). Campinas ≈ 22°54' S, 47°03' W:

| Item | Converter |
|------|-----------|
| 22° 54' 30" S | → decimal |
| −47,0608° | → GMS |

## Parte B — Ler o recorte da sub-região (40 min)

1. Enquadre a sub-região da atualização (Ex. 03). Painel **Coordenada** (barra inferior) para ler E/N ao passar o mouse.
2. Anote os **limites UTM** do recorte (West/South/East/North) — esses quatro números definem oficialmente a área de trabalho.
3. Que **dimensões** tem o recorte (largura × altura, em metros)? Que **escala** ele comporta em uma folha A3? (relembre o limite gráfico de 0,2 mm)
4. *(Opcional)* Recorte a carta na sub-região: **Raster → Extração → Recortar raster pela extensão**, usando os limites lidos.

## Parte C — Detalhar a sub-região: vias e pontos (40 min)

A atualização regional (Ex. 03, Landsat, 1:50.000) fica grosseira demais para vias e marcadores. Na sub-região, em **escala grande** sobre a imagem de alta resolução (Google/Esri), digitalize o detalhe.

1. Adicione a camada **Esri World Imagery / Google Satellite** ([XYZ](../ambiente/setup-xyz-tiles.md)) e enquadre a sub-região.
2. Crie `vias` (linha; campos `nome`, `tipo`) e `pontos` (ponto; campos `nome`, `tipo`), em **EPSG:31983**.
3. Digitalize as **vias novas** (que a carta de 1980 não traz) e **marcadores** (shopping, campus, viaduto).
4. Comprimento total das vias: campo `$length`; some em *Estatísticas*.

> Mesma cidade, duas escalas: a mancha regional (Landsat, Ex. 03) e o detalhe local (alta resolução, aqui). É a lição de escala e generalização em ato.

## Parte C — No pátio/campo, com o celular (50 min)

5. App em formato **UTM**; em 4 pontos identificáveis:
   - 5 leituras (~30 s de intervalo); anote a **dispersão** (máx−mín);
   - a **precisão (accuracy)** informada;
   - em UTM **e** Lat/Long.

| Ponto | E médio | N médio | Dispersão (m) | Precisão (m) |
|-------|---------|---------|---------------|--------------|

## Parte D — Importar no QGIS (40 min)

6. Monte um CSV `nome,E,N` → **Camada → Adicionar camada de texto delimitado** → X=E, Y=N, SRC **EPSG:31983**.
7. Sobreponha à imagem. Caíram no lugar? De quantos metros é o descolamento?
8. Junte esses pontos à camada `pontos` da atualização, se forem marcadores úteis.

## Discussão

- A dispersão que você mediu é compatível com 1:2.000 (0,4 m)? E com a escala do seu recorte?
- Por que a incerteza do GPS de navegação é o **gargalo** da exatidão da carta de atualização?

## Entrega

- [ ] Conversões.
- [ ] Limites UTM do recorte + escala que ele comporta.
- [ ] Tabela de coleta (dispersão, precisão) + pontos importados.
