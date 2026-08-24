# Aula 6 — Coordenadas geográficas e UTM; introdução ao GPS

**Onde:** sala + laboratório (QGIS) + pátio (app de GPS) · **Módulo:** I

## Objetivos

- Ler, plotar e converter coordenadas geográficas e UTM.
- Compreender o princípio do posicionamento por GPS/GNSS e a incerteza do receptor de navegação.
- Ler as coordenadas UTM do recorte da sub-região de Campinas; coletar coordenadas com o celular.

## Teoria

Coordenadas **geográficas** (latitude e longitude) localizam um ponto por dois ângulos; são universais, mas incômodas para calcular distâncias. Coordenadas **planas UTM** (E, N), em metros dentro de um fuso, resolvem esse incômodo: distâncias e áreas saem por Pitágoras. O **E** parte do falso leste de 500.000 m no meridiano central; o **N**, no hemisfério sul, parte de 10.000.000 m no equador e diminui para o sul (Fitz, 2000, cap. "Sistemas de coordenadas"). Converter GMS ↔ decimal é aritmética simples, e é preciso saber que **a precisão declarada tem de ser compatível com a fonte**: cada dígito descartado multiplica por dez a incerteza.

O **GPS/GNSS** determina posição por um processo semelhante à triangulação, a partir de satélites. Fitz (2000) classifica os receptores em **navegação** (precisão planimétrica de dezenas de metros, método absoluto), métrico, submétrico e geodésico. O receptor do celular é de navegação: adequado para localizar-se, insuficiente para apoio geodésico. No pátio, coletando pontos com o app e observando a **flutuação** da leitura e a **precisão** informada, o aluno mede na prática essa incerteza — e a leva para a discussão de exatidão que percorre o curso.

## Roteiro (3h)

| Bloco | Descrição |
|-------|-----------|
| Teoria | Coordenadas geográficas e UTM; conversões; princípio do GPS e classes de receptor |
| Prática (QGIS) | Ler, plotar e converter coordenadas sobre a ortofoto/folha |
| Prática (pátio) | Coletar pontos com o app de GPS; avaliar flutuação e precisão; importar no QGIS |

## Laboratório

**[Ex. 06 — A sub-região: coordenadas, recorte e GPS](../exercicios/ex-06-coordenadas-gps.md)**

## Leituras

- FITZ, P. R. *Cartografia básica*, cap. "Sistemas de coordenadas" (inclui obtenção de coordenadas em campo e classificação dos receptores GPS).
