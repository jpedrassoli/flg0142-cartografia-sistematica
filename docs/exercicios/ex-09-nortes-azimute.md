# Ex. 09 — Os três nortes e o azimute (Campinas)

**Aula:** 9 · **Ferramenta:** QGIS + cálculo · **Duração:** ~2h

## Objetivo

Calcular a convergência meridiana e a declinação de Campinas, desenhar o diagrama de declinação da carta de atualização e medir azimutes.

## Material / dados

- Calculadora; transferidor e régua; projeto de Campinas.

![Os três nortes](../figuras/fig-tres-nortes.svg)

## Parte A — Convergência meridiana de Campinas (30 min)

1. Dados: λ ≈ **47°03' W**; meridiano central do fuso 23 = **45° W**; φ ≈ **22°54' S**.
2. Converta para decimais; Δλ = λ − λ₀ (≈ −2,05°).
3. **c ≈ Δλ · sen φ**. Calcule (deve dar ~**0°48'**, um pouco maior que o de São Paulo, porque Campinas está mais longe do MC).
4. Para que lado o NQ se inclina? Confira pelo sinal e pelo desenho.

## Parte B — Declinação magnética (20 min)

5. Obtenha δ do **ano corrente** para Campinas (modelo IGRF/WMM; ordem de 21°–22° W). O docente fornece ou consulta antes.
6. Leia a declinação e a data no diagrama da **carta de 1980** (Ex. 02). Com a variação anual, calcule δ **hoje**. Bate com o item 5? De quanto mudou em 40 anos?

## Parte C — Diagrama da carta de atualização (30 min)

7. Desenhe, em **escala angular correta** (transferidor): NG vertical; NQ deslocado por γ; NM deslocado por δ; ângulos cotados, data e variação anual.
8. Guarde: vai para a carta final (Aula 15).

## Parte D — Azimutes no QGIS (40 min)

9. Meça o azimute de 3 alinhamentos da sua sub-região (ex.: a direção de uma via nova, do Ex. 03).
10. O QGIS dá o azimute em relação ao **NQ**. Converta para **verdadeiro** (aplicando γ) e **magnético** (aplicando δ).

!!! danger "O erro clássico é o sinal"
    Desenhe o diagrama e olhe. Declinação W → NM à esquerda do NG.

## Entrega

- [ ] Cálculo de γ e δ (hoje) de Campinas, com as contas.
- [ ] Diagrama de declinação em escala angular (para a carta final).
- [ ] Tabela de 3 azimutes com as conversões.
