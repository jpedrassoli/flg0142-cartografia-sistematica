# Ex. 05 — Projeções e distorção no QGIS

**Aula:** 5 · **Ferramenta:** QGIS · **Duração:** ~2h

## Objetivo

Medir a deformação das projeções e situar São Paulo no sistema UTM.

## Material / dados

- **Natural Earth** (países e um grid, de naturalearthdata.com) ou a malha de países do IBGE.

## Passo a passo

### Parte A — A mesma camada, várias projeções (40 min)
1. Carregue a camada de **países** (projeto pode começar em WGS84 / EPSG:4326).
2. Troque o SRC do **projeto** (barra inferior direita) e observe a mudança de forma:
   - **Mercator** (EPSG:3857) — conforme.
   - **Mollweide** ou **Eckert IV** — equivalente (busque "World Mollweide", ESRI:54009).
   - **Robinson** (ESRI:54030) — de compromisso.
3. Para cada uma, observe: a Groenlândia cresce ou encolhe em relação ao Brasil?

### Parte B — Medir a distorção de área (40 min)
4. Com o projeto em cada projeção, use **Vetor → Geometria → Adicionar atributos de geometria** (ou o campo calculador com `$area`) para medir a **área aparente** de Groenlândia e Brasil **na projeção**.
5. Compare a razão Groenlândia/Brasil em cada projeção com a **real** (Groenlândia ≈ 2,2 mi km²; Brasil ≈ 8,5 mi km² → razão ≈ 0,26).

| Projeção | Razão GRO/BRA medida | Real | Classificação |
|----------|----------------------|------|---------------|
| Mercator | | 0,26 | conforme |
| Mollweide | | 0,26 | equivalente |
| Robinson | | 0,26 | compromisso |

> Para medir área "de verdade" (não a aparente da projeção), use um SRC equivalente. A diferença entre a área aparente e a real **é** a distorção.

### Parte C — O fuso de São Paulo (40 min)
6. Determine o **fuso UTM** de São Paulo (longitude ≈ 46°44' W). Mostre a conta: fuso = parte inteira de (183 − |MC|)/6... ou use a regra prática (São Paulo → **fuso 23 S**). Confirme carregando a ortofoto do GeoSampa em EPSG:31983.
7. Qual o **meridiano central** do fuso 23? (**45° W**). Anote — reaparece na Aula 9.
8. No QGIS, com o projeto em EPSG:31983, verifique: as coordenadas E ficam em torno de qual valor no centro do fuso? (perto de 500.000 no MC).

## Discussão

- Mercator foi feita para navegar. Isso a torna "boa"? Boa para quê?
- Por que um planisfério equivalente parece "errado" ao olho?
- Por que o mapeamento sistemático usa UTM (cilíndrica transversa conforme, por fusos)?

## Entrega

- [ ] Capturas das três projeções da mesma camada.
- [ ] Tabela de distorção preenchida.
- [ ] Conta do fuso de São Paulo e do meridiano central.
