# Aula 3 — Sensoriamento Remoto e SIG: atualizar a mancha urbana

**Onde:** laboratório (QGIS) · **Módulo:** I

## Objetivos

- Definir SR e SIG e sua relação com a cartografia sistemática.
- Compor e interpretar uma imagem **Landsat 9 (2025)**; extrair a mancha urbana na escala da carta (1:50.000).
- Usar os **limites municipais do IBGE** (SIG) para recortar Campinas e combinar as fontes.

## Teoria

O **Sensoriamento Remoto** é a captação de informação à distância. O satélite **Landsat 9** (sensor OLI-2) registra o terreno em faixas do espectro — azul, verde, vermelho, infravermelho próximo (NIR), infravermelho de ondas curtas (SWIR) — a **30 m** por pixel (Fitz, 2000, cap. "Aerofotogrametria e sensoriamento remoto"; resolução espacial e espectral). Combinando bandas em **composições coloridas**, realçam-se alvos: em cor natural (4-3-2) a cidade é cinza; numa composição SWIR-NIR-Vermelho (6-5-4), o construído destaca-se da vegetação. Índices como o **NDBI** = (SWIR−NIR)/(SWIR+NIR) medem o quão "construído" é cada pixel.

Há uma coerência de escala que organiza a aula: um pixel de 30 m corresponde a ~0,6 mm numa folha 1:50.000 — próximo do limite gráfico. Ou seja, o Landsat é adequado para atualizar a **extensão urbana** na escala da carta, **não** o lote a lote (isso virá na sub-região, em alta resolução). Atualizar "nesta escala" é honesto: mapeia-se a mancha, não a quadra.

O **SIG** é o que combina as fontes. Com os **limites municipais do IBGE** (uma camada vetorial oficial), recorta-se Campinas e restringe-se o trabalho ao município — a operação de *recorte por máscara* é típica de SIG. Ao final, três camadas conversam sobre a mesma área: a **carta sistemática de 1980** (a mancha de então), a **imagem Landsat de 2025** (SR, a mancha de agora) e o **limite do IBGE** (SIG, o recorte). A diferença entre as duas manchas é a **expansão urbana de Campinas** na escala regional.

## Roteiro (3h)

| Bloco | Descrição |
|-------|-----------|
| Teoria | SR (bandas, composições, índices) e SIG (camadas, recorte); relação com a base sistemática |
| Prática | Recortar Campinas pelos limites do IBGE; compor o Landsat 9 (2025); extrair a mancha 2025 e comparar com a de 1980 (carta) |
| PCC | A imagem de satélite como recurso de leitura da cidade |

## Laboratório

**[Ex. 03 — SR + SIG: atualizar a mancha urbana com Landsat 9 e limites do IBGE](../exercicios/ex-03-atualizacao.md)**

## Leituras

- FITZ, P. R. *Cartografia básica*, cap. "Aerofotogrametria e sensoriamento remoto" (resolução espacial/espectral, composições) e "Cartografia assistida por computador" (SIG).
- FITZ, P. R. *Geoprocessamento sem complicação*.
