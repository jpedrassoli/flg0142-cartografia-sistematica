# Ex. 07 — Escala, medições na sub-região e escala da foto

**Aula:** 7 · **Ferramenta:** QGIS · **Duração:** ~2h

## Objetivo

Medir sobre a carta e a atualização de Campinas, discutir generalização e erro gráfico, e calcular a escala da fotografia aérea (ponte para a fotogrametria).

## Material / dados

- Projeto de Campinas (carta + imagem + camadas do Ex. 03).

## Parte A — Medições na sub-região (40 min)

1. **Medir linha:** meça a extensão da mancha urbana atual no sentido de maior crescimento; compare com a de 1980.
2. Trave a escala do projeto em **1:2.000** e depois **1:25.000** (a da carta). O que é legível em cada uma? Um lote cabe em 1:25.000?
3. **Medir área** (ou `$area`): confirme a área das manchas do Ex. 03. As contas batem?

## Parte B — Generalização e erro gráfico (30 min)

4. Preencha (limite gráfico 0,2 mm; Fitz, 2000):

| Escala | 0,2 mm no terreno | Cabe um lote (~20 m)? | Cabe uma quadra? |
|--------|-------------------|------------------------|------------------|
| 1:50.000 | 10 m | | |
| 1:25.000 | 5 m | | |
| 1:2.000 | 0,4 m | | |

5. A carta de 1980 é 1:50.000. Que nível de detalhe da mancha urbana ela **pode** representar? Isso explica por que a mancha de 1980 é generalizada?

## Parte C — Escala da foto aérea (50 min)

Exercício numérico (modelo Fitz, cap. Aerofotogrametria):

- f = **150 mm**; H = **6.000 m**; formato **23×23 cm**.

1. **E = f/H** = 150 mm / 6.000.000 mm = **1:40.000**.
2. Terreno por foto: 0,23 m × 40.000 = **9.200 m** de lado.
3. Aerobase 3.700 m → recobrimento = (9.200−3.700)/9.200 ≈ **60%**.
4. Refaça com outros f e H (o docente varia); confira se o recobrimento fica ~60% — a condição da estereoscopia (Aula 11).

![Geometria da foto](../figuras/fig-geometria-voo.svg)

## Discussão

- Por que a escala gráfica sobrevive à fotocópia e a numérica não?
- Por que "a escala pode ser reduzida, nunca ampliada" (Fitz)? Relacione com a carta de 1980 usada em zoom.

## Entrega

- [ ] Medições na sub-região (extensão e área das manchas).
- [ ] Tabela de generalização por escala.
- [ ] Cálculo completo da escala da foto e do recobrimento.
