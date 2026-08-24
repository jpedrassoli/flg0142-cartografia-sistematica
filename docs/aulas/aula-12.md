# Aula 12 — Curvas de nível e perfil topográfico

**Onde:** prancheta (analógico) + laboratório (QGIS) · **Módulo:** III — A carta e suas leituras

## Objetivos

- Compreender a curva de nível, suas propriedades e a interpolação.
- Traçar curvas à mão e gerá-las no QGIS a partir do MDT, comparando.
- Construir o perfil topográfico nos dois formatos.

## Teoria

Uma **curva de nível** é o lugar dos pontos de mesma altitude — a interseção do terreno com um plano horizontal. Suas propriedades decorrem da definição: não se cruzam, fecham-se sobre si mesmas, adensam-se onde o declive é forte e apontam para montante nos vales (Fitz, 2000, cap. "Altimetria"). A **equidistância** é uma escolha ligada à escala e à amplitude do terreno; as **curvas mestras** (a cada quinta) são cotadas. O traçado à mão é uma **interpolação linear** entre pontos cotados vizinhos — uma regra de três, ponto a ponto.

![Interpolação de curvas](../figuras/fig-interpolacao.svg)

Este é o momento de unir **analógico e digital** (objetivo 3 da ementa). O aluno interpola à mão uma malha de pontos cotados extraída do MDE de Campinas e, em seguida, gera as curvas automaticamente no QGIS (Raster → Extração → Curvas de nível), sobrepondo os dois resultados. A mesma suposição de linearidade está nos dois; o software é mais rápido e consistente, mas herda as mesmas cegueiras. Do mesmo modo, o **perfil topográfico** — corte vertical ao longo de uma linha — é construído à mão em papel milimetrado e no QGIS (complemento *Terrain Profile*), com atenção ao **exagero vertical**, que deve ser sempre declarado.

![Perfil topográfico](../figuras/fig-perfil.svg)

## Roteiro (3h)

| Bloco | Descrição |
|-------|-----------|
| Teoria | Curvas: conceito, propriedades, equidistância, interpolação; o perfil e o exagero vertical |
| Prática (analógico) | Interpolar curvas à mão a partir de pontos cotados do MDT |
| Prática (QGIS) | Gerar curvas do MDT e o perfil (Terrain Profile); comparar com o traçado manual |
| PCC | O perfil e a maquete como recursos didáticos |

## Laboratório

**[Ex. 12 — Curvas de nível e perfil (analógico + QGIS)](../exercicios/ex-12-curvas-perfil.md)**

## Leituras

- FITZ, P. R. *Cartografia básica*, cap. "Cartografia temática" (altimetria) e "Uso prático das cartas topográficas" (perfil).
