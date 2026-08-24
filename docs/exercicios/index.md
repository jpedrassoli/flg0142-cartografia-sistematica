# Exercícios

O curso é um **estudo de caso de Campinas**: a carta topográfica dos anos 1980 é georreferenciada (Ex. 02), atualizada sobre imagem de satélite (Ex. 03) e cruzada com o relevo, até a carta de atualização final. Cada exercício produz insumo para os seguintes — mas há **produto de referência pronto** a cada etapa, para ninguém travar.

| # | Exercício | Aula | Ferramenta | Caso |
|---|-----------|------|-----------|------|
| 02 | [Georreferenciar a carta de Campinas](ex-02-georreferenciamento.md) | 2 | QGIS | **Campinas** |
| 03 | [**SR + SIG**: mancha urbana com Landsat 9 e IBGE](ex-03-atualizacao.md) | 3 | QGIS + Landsat | **Campinas** |
| 04 | [O mesmo ponto, dois data](ex-04-datum.md) | 4 | QGIS | **Campinas** |
| 05 | [Projeções e distorção](ex-05-projecoes.md) | 5 | QGIS | mundo |
| 06 | [A sub-região: coordenadas e GPS](ex-06-coordenadas-gps.md) | 6 | QGIS + GPS | **Campinas** |
| 07 | [Escala, medições e escala da foto](ex-07-escala.md) | 7 | QGIS | **Campinas** |
| 09 | [Os três nortes e o azimute](ex-09-nortes-azimute.md) | 9 | QGIS | **Campinas** |
| 10 | [Fotogrametria com o celular](ex-10-fotogrametria-celular.md) | 10 | KIRI Engine | objeto |
| 11 | [Estereoscopia, paralaxe e relevo](ex-11-estereoscopia.md) | 11 | estéreo + QGIS | **Campinas** |
| 12 | [Curvas de nível e perfil](ex-12-curvas-perfil.md) | 12 | analógico + QGIS | **Campinas** |
| 13 | [Hipsometria, clinografia e expansão](ex-13-hipsometria-clinografia.md) | 13 | QGIS | **Campinas** |
| 14 | [SIG, Google Earth e série histórica](ex-14-sig-google-earth.md) | 14 | Google Earth + QGIS | **Campinas** |

## A espinha de Campinas

```
Ex. 02 georreferenciar a carta 1980 ── descobre a desatualização
   │
Ex. 03 SR+SIG: mancha 1980 (carta) + mancha 2025 (Landsat), recorte IBGE → expansão regional (1:50.000)
   │
Ex. 06 sub-região (alta resolução): vias + pontos · coordenadas · GPS    Ex. 07 escalas e áreas
   │
Ex. 09 diagrama de declinação de Campinas → moldura da carta
   │
Ex. 11–13 o RELEVO explica a expansão (estéreo, curvas, declividade × mancha)
   │
Ex. 14 confronta a atualização manual com a série histórica do Google Earth
   │
Aula 15 CARTA DE ATUALIZAÇÃO FINAL (analógica + digital) + PCC
```

Ficam **globais** (o conceito pede o mundo): Ex. 05 (projeções). O Ex. 10 (fotogrametria) usa um objeto para ensinar o princípio.

> Antes de começar: instale as ferramentas ([QGIS](../ambiente/setup-qgis.md), [XYZ Tiles](../ambiente/setup-xyz-tiles.md), [Google Earth](../ambiente/setup-google-earth.md), [apps](../ambiente/setup-apps-celular.md)) e veja as [fontes de dados](../dados/fontes-de-dados.md).
