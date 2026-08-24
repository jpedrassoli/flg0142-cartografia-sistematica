# Ex. 11 — Estereoscopia, paralaxe e o relevo de Campinas

**Aula:** 11 · **Ferramenta:** estereoscópio de bolso + QGIS · **Duração:** ~2h30

## Objetivo

Ver o relevo em um par de fotos aéreas e medir alturas por paralaxe; visualizar o relevo de Campinas no MDE e começar a relacioná-lo com a expansão urbana (Ex. 03).

## Material / dados

- **Estereoscópio de bolso** (1 por dupla).
- Um **par de fotos aéreas** com recobrimento (acervo do Departamento/LASERE, ou par-amostra do docente).
- QGIS + **MDE aberto** da sub-região de Campinas (Copernicus GLO-30 ou MDT-SP).
- Régua milimetrada.

![Paralaxe](../figuras/fig-paralaxe.svg)

## Parte A — Ver o relevo no par (50 min)

1. Marque o **ponto principal (PP)** de cada foto e o **transferido (PPT)** na foto vizinha.
2. Alinhe as fotos numa reta (linha de voo), separadas ~6 cm; posicione o estereoscópio.
3. Olhe relaxando os olhos: **o relevo salta em 3D**.
4. Meça a **base fotográfica b** (média de PP–PPT), em mm.

!!! tip "Se não fundir"
    Confira o alinhamento e a separação; a foto da esquerda deve estar à esquerda (senão o relevo inverte).

## Parte B — Medir altura por paralaxe (40 min)

5. Escolha um objeto de altura conhecível (edifício com nº de andares) e um talude.
6. Meça a paralaxe do **topo** e da **base**; **Δp = p_topo − p_base**.
7. Com H (altura de voo, da ficha da foto) e b: **Δh = H·Δp/(b+Δp)**.
8. Compare com o valor conhecido. Qual a incerteza do método nas suas mãos?

## Parte C — O relevo de Campinas no MDE (50 min)

9. No QGIS, carregue o **MDE** da sub-região. Estilize com **Sombreamento (hillshade)** ou abra uma **Vista 3D** (*Ver → Novas Vistas do Mapa 3D*), com o MDE como terreno.
10. Sobreponha as **manchas urbanas** (1980 e atual, do Ex. 03).
11. **Observação-chave:** a expansão urbana (a diferença entre as duas manchas) ocupou terrenos planos? Evitou encostas? Avançou sobre fundos de vale? Anote a hipótese — a Aula 13 vai testá-la com a declividade.

## Discussão

- O que só apareceu em estéreo, que uma foto isolada não mostra?
- Analógico (par no estereoscópio) × digital (MDE em 3D): o que cada um mede melhor?
- Por que o relevo ajuda a explicar **onde** a cidade cresceu?

## Entrega

- [ ] Par orientado (PP, PPT, linha de voo) e **b** medido.
- [ ] Cálculo de Δh e comparação com o valor conhecido.
- [ ] Hipótese escrita: relação entre relevo e a expansão urbana (para testar na Aula 13).
