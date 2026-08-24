# Aula 4 — Referenciais cartográficos: geoide, elipsoide, datum

**Onde:** sala + laboratório (QGIS) · **Módulo:** I

## Objetivos

- Distinguir superfície topográfica, geoide e elipsoide.
- Compreender datum e as consequências de mudá-lo.
- Medir, no QGIS, o deslocamento de um mesmo ponto entre data diferentes.

## Teoria

Medir posições exige decidir **qual Terra**. A **superfície topográfica** é a real, irregular e intratável. O **geoide** é a superfície equipotencial que mais se aproxima do nível médio dos mares — o "nível zero" físico das altitudes, ondulado porque a massa terrestre não é homogênea. O **elipsoide** é a figura matemática sobre a qual se calcula (Fitz, 2000, cap. "A representação cartográfica"). Um **datum** amarra o elipsoide à Terra: escolhe qual elipsoide usar e como posicioná-lo. Data locais (**Córrego Alegre**, **SAD-69**) serviram ao Brasil; data geocêntricos (**SIRGAS 2000**, oficial desde 2005; **WGS84**, do GPS) centram o elipsoide no centro de massa e servem ao mundo.

A consequência é concreta: **o mesmo ponto físico tem coordenadas diferentes em data diferentes** — no Brasil, a diferença entre Córrego Alegre e SIRGAS 2000 chega à ordem de dezenas de metros. Uma folha antiga e um GPS moderno discordam, e nenhum está errado. Há ainda a armadilha da altitude: o GPS entrega altitude **elipsoidal**, enquanto a carta traz altitude **ortométrica** (referida ao geoide) — e a diferença, a ondulação geoidal, importa. No QGIS, reprojetar um ponto entre SIRGAS 2000 e o datum da **carta de Campinas** (anos 1980) e medir o deslocamento torna isso palpável — e explica parte do descolamento visto no Ex. 02.

## Roteiro (3h)

| Bloco | Descrição |
|-------|-----------|
| Teoria | Geoide, elipsoide, datum; data locais × geocêntricos; altitude elipsoidal × ortométrica |
| Prática | No QGIS, comparar o mesmo ponto em SIRGAS 2000 e Córrego Alegre; medir o deslocamento |

## Laboratório

**[Ex. 04 — O mesmo ponto, dois data (na carta de Campinas)](../exercicios/ex-04-datum.md)**

## Leituras

- FITZ, P. R. *Cartografia básica*, cap. "A representação cartográfica" (forma da Terra e sistemas geodésicos).
- IBGE. *Noções básicas de cartografia* — referenciais geodésicos.
