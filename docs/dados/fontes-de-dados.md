# Fontes de dados

O curso é organizado como um **estudo de caso de Campinas**: a carta topográfica dos anos 1980 é georreferenciada, recortada e atualizada sobre imagem recente. Alguns exercícios conceituais (projeções) usam dados globais.

## Estudo de caso — Campinas

| Dado | Fonte | Uso |
|------|-------|-----|
| **Carta topográfica de Campinas** (IBGE, 1:50.000, anos 1980) | IBGE (Cartas Topográficas) | georreferenciamento, leitura da folha, **mancha urbana de 1980** (Aulas 2, 3) |
| **Landsat 9 (2025)**, bandas multiespectrais (30 m) | USGS EarthExplorer / SCP | SR: atualização da **mancha urbana na escala da carta (1:50.000)** (Aula 3) |
| **Malha municipal do IBGE** (limites) | IBGE (Malhas Territoriais) | SIG: **recorte de Campinas** e área temática (Aula 3) |
| **Imagem de satélite de alta resolução** (Google/Esri) | XYZ Tiles | detalhe da **sub-região**: vias e pontos, escala grande (Aula 6) — ver [XYZ Tiles](../ambiente/setup-xyz-tiles.md) |
| **MDE aberto** de Campinas | Copernicus GLO-30 (via QGIS/OpenTopography) ou MDT-SP (DataGEO) | relevo, curvas, hipsometria, clinografia, bacia (Aulas 11–13) |
| **Fotos aéreas para estereoscopia** | acervo do Departamento (LASERE) ou par-amostra | par estéreo no estereoscópio (Aula 11) |
| **Malhas IBGE** (município/setores de Campinas) | IBGE (malhas territoriais) | Cartografia Temática (Aula 3) |

> **Convergência meridiana de Campinas:** a cidade está em ≈ **47°03' W**, ainda no **fuso 23 S** (MC 45° W) — dá um valor de γ próprio do caso (Aula 9).

## Dados globais (conceituais)

- **Natural Earth** (naturalearthdata.com): países e grid para o exercício de projeções (Aula 5).

## Recurso didático (Aula 14)

- **Google Earth Pro** — imagens históricas de Campinas e Timelapse (a série temporal que confirma a expansão digitalizada à mão).
- **Google Earth na Sala de Aula** (mapasnasaladeaula.org) — mapas KML didáticos.

## Nota ao docente — produto de referência a cada etapa

Para que ninguém trave, tenha salvo e disponível (pen drive / rede / link):

- a **carta de Campinas já georreferenciada** (GeoTIFF) — quem faltou à Aula 2 continua;
- as **bandas Landsat 9 (2025)** já baixadas e o **limite municipal de Campinas** (IBGE) recortado, para não repetir 40 downloads;
- um **GeoPackage** com as camadas de atualização já criadas e vazias (polígono, linha, ponto), em EPSG:31983;
- um **MDE recortado** da sub-região e uma **malha de pontos cotados** para a interpolação manual (Aula 12).

A sequência é encadeada (a narrativa de Campinas atravessa o curso), mas a dependência técnica não: cada etapa tem um insumo pronto.
