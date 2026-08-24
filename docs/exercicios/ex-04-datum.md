# Ex. 04 — O mesmo ponto, dois data (na carta de Campinas)

**Aula:** 4 · **Ferramenta:** QGIS · **Duração:** ~1h30

## Objetivo

Constatar e medir, no QGIS, que mudar o datum muda as coordenadas do mesmo ponto — usando a carta de Campinas, que é de um datum antigo.

## Material / dados

- `campinas_georref.tif` e a imagem de satélite.

## Passo a passo

### Parte A — O ponto (15 min)
1. Projeto em **SIRGAS 2000 / UTM 23S (EPSG:31983)**.
2. Crie uma camada de pontos (EPSG:31983) e marque um ponto sobre uma feição nítida e permanente que exista **na carta e na imagem** (um cruzamento antigo, um vértice de quadra do centro).
3. Anote E e N em SIRGAS 2000.

### Parte B — Reprojetar para o datum da carta (30 min)
4. **Vetor → Ferramentas de gestão → Reprojetar camada** → SRC de destino = o **datum da carta** (Córrego Alegre / UTM 23S, **EPSG:22523**, ou SAD-69, **EPSG:29193**).
5. Anote E e N no datum antigo.

| Datum | E (m) | N (m) |
|-------|-------|-------|
| SIRGAS 2000 (31983) | | |
| Córrego Alegre (22523) | | |
| **Diferença** | ΔE = | ΔN = |

### Parte C — Medir e interpretar (25 min)
6. **d = √(ΔE² + ΔN²)**. De que ordem? (dezenas de metros)
7. **Ligação com o Ex. 02:** aquele pequeno deslocamento sistemático entre a carta e a imagem era, em parte, **isto** — a diferença de datum. O resto era mudança real do território.
8. Distinga: quanto do descolamento observado no Ex. 02 é datum (uniforme, dezenas de metros) e quanto é a cidade que cresceu?

## Discussão

- Nenhuma coordenada está "errada". O que isso significa?
- O GPS mostra "altitude" — elipsoidal ou ortométrica? Por que importa?

## Entrega

- [ ] Tabela de coordenadas nos dois data + deslocamento.
- [ ] Datum que a carta final vai adotar (SIRGAS 2000), justificado.
- [ ] Distinção entre deslocamento de datum e mudança real (ligação com Ex. 02).
