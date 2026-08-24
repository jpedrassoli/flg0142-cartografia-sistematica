# Aula 13 — Leitura de cartas: planimetria, altimetria, hipsometria e clinografia

**Onde:** laboratório (QGIS) + prancheta · **Módulo:** III

## Objetivos

- Ler de forma integrada planimetria e altimetria.
- Produzir cartas hipsométrica e clinográfica a partir do MDT.
- Delimitar uma bacia; cruzar a declividade com as manchas urbanas para explicar a expansão.

## Teoria

Ler uma carta é integrar **planimetria** (o que está no plano: vias, edificações, hidrografia) e **altimetria** (o relevo, pelas curvas). Duas leituras derivadas tornam o relevo imediato. A **hipsometria** responde "quão alto?", agrupando altitudes em classes de cor (dos verdes aos marrons); a escolha das classes muda a aparência sem que nenhum dado mude — antessala da Cartografia Temática (Fitz, 2000, cap. "Cartografia temática"). A **clinografia** responde "quão íngreme?": a declividade está implícita no **espaçamento** das curvas (tg α = e/D), lida à mão pelo **ábaco** de De Biasi ou calculada no QGIS.

![Ábaco clinográfico](../figuras/fig-abaco.svg)

No QGIS, a partir do **MDE de Campinas**, o aluno gera a **carta hipsométrica** (estilo de classes de altitude), a **carta de declividade** (Raster → Análise → Declividade; classes 5/12/20/30%, com significado legal e de aptidão) e delimita uma **bacia hidrográfica** pela linha divisora de águas — uma das aplicações clássicas da carta topográfica na Geografia (Fitz, 2000, cap. "Uso prático das cartas topográficas"). E fecha-se o estudo de caso: cruzando as **manchas urbanas** (Ex. 03) com a declividade, testa-se com números a hipótese da Aula 11 — a expansão de Campinas ocupou terrenos planos, subiu encostas, avançou sobre fundos de vale? A hipsométrica e a clinográfica descrevem o mesmo relevo e produzem imagens que não se parecem.

## Roteiro (3h)

| Bloco | Descrição |
|-------|-----------|
| Teoria | Planimetria e altimetria; hipsometria e classes; clinografia e o ábaco; bacia hidrográfica |
| Prática (QGIS) | Carta hipsométrica; carta de declividade; delimitação de bacia |
| PCC | Escolha de classes como decisão didática |

## Laboratório

**[Ex. 13 — Hipsometria, clinografia e a expansão sobre o relevo](../exercicios/ex-13-hipsometria-clinografia.md)**

## Leituras

- FITZ, P. R. *Cartografia básica*, cap. "Cartografia temática" (hipsometria) e "Uso prático das cartas topográficas" (bacia, declividade).
- DE BIASI, M. Carta clinográfica (1992).
