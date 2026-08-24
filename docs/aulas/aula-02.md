# Aula 2 — Cartografia sistemática: conceito e anatomia da folha

**Onde:** sala + laboratório (QGIS) · **Módulo:** I

## Objetivos

- Conceituar a Cartografia Sistemática e o mapeamento sistemático brasileiro.
- Reconhecer os elementos da moldura de uma folha topográfica.
- **Georreferenciar** a carta topográfica de Campinas (raster) no QGIS e descobrir a sua desatualização.

## Teoria

Cartografia **sistemática** é o mapeamento de um território inteiro segundo um padrão único — mesmas escalas, mesmo sistema de referência, mesmas convenções e um corte de folhas articulado. No Brasil, o esforço é dividido historicamente entre **IBGE** e a **DSG** (Exército) e organizado num encadeamento de escalas: 1:1.000.000 → 1:500.000 → 1:250.000 → 1:100.000 → 1:50.000 → 1:25.000, com nomenclatura derivada da Carta Internacional do Mundo ao Milionésimo (Fitz, 2000, cap. "Cartas, mapas e plantas"). Cada folha traz um índice que informa exatamente onde ela está no sistema.

A folha topográfica é um objeto codificado: escala numérica e gráfica, equidistância, **diagrama de declinação**, quadrícula UTM, articulação, legenda, **datum** e data. Esse conjunto é o que a torna utilizável por quem não a fez — a diferença entre um desenho e um documento cartográfico. Ler cada elemento não é decorar convenções: é o que permite **georreferenciar** a **carta de Campinas** (anos 1980), tarefa que abre o estudo de caso do semestre. Para pôr a imagem no lugar certo, o aluno lê as coordenadas da moldura, o datum e a projeção. E, ao sobrepor a carta georreferenciada à imagem de satélite atual, descobre que **ela não bate mais com a realidade** — a cidade cresceu. Essa desatualização é o gancho de todo o curso: a carta é um documento **datado**.

## Roteiro (3h)

| Bloco | Descrição |
|-------|-----------|
| Teoria | Cartografia sistemática; encadeamento de escalas e articulação; anatomia da folha |
| Prática | Georreferenciar a carta de Campinas no QGIS; sobrepor ao satélite e revelar a desatualização |
| PCC | A carta topográfica na Educação Básica; abertura do produto de PCC |

## Laboratório

**[Ex. 02 — Georreferenciar a carta de Campinas e descobrir a desatualização](../exercicios/ex-02-georreferenciamento.md)**

## Leituras

- FITZ, P. R. *Cartografia básica*, cap. "Cartas, mapas e plantas".
- IBGE. *Noções básicas de cartografia* — o mapeamento sistemático.
