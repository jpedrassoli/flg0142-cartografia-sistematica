# Ex. 10 — Fotogrametria com o celular (KIRI Engine)

**Aula:** 10 · **Ferramenta:** KIRI Engine (celular/web) · **Duração:** ~2h

## Objetivo

Gerar um modelo 3D a partir de fotos de um objeto para entender, com as próprias mãos, como fotos sobrepostas contêm a terceira dimensão — o princípio das fotos aéreas.

## Material / dados

- Celular com o app **KIRI Engine** (ou o site kiriengine.app), conta gratuita. Ver [apps do celular](../ambiente/setup-apps-celular.md).
- Um **objeto** com relevo e textura: uma pedra, um tênis, uma miniatura, ou uma **pequena maquete de relevo** (massa de modelar/isopor). Evite objetos lisos, brilhantes ou transparentes (falham na fotogrametria).

## Passo a passo

### Parte A — Capturar (40 min)
1. Ponha o objeto num lugar bem iluminado, sem sombras duras, sobre um fundo com textura (jornal, toalha estampada).
2. No KIRI, escolha **Photo Scan** e crie um novo projeto.
3. Tire fotos **girando ao redor** do objeto, uma a cada ~15°–20°, mantendo **60–70% de sobreposição** entre fotos vizinhas (o objeto quase todo aparece nas duas). Faça duas alturas: uma na linha do objeto, outra mais de cima.
4. Alvo: 30–60 fotos (o modo Photo Scan aceita até ~150). Cubra o objeto inteiro.

> A regra de sobreposição é a **mesma** das fotos aéreas (recobrimento longitudinal): sem sobreposição, não há como o algoritmo (nem o seu olho) reconstruir o 3D.

### Parte B — Processar (20 min)
5. **Upload** → o processamento roda na nuvem (~2 min). Aguarde a notificação.
6. Abra o modelo 3D. Gire, aproxime. Onde ficou bom? Onde falhou (partes lisas, oclusões, poucas fotos)?

### Parte C — Ligar à fotogrametria aérea (40 min)
7. Responda, por escrito:
   - Que papel a **sobreposição** entre fotos teve? Relacione com o **recobrimento longitudinal** de 60% das fotos aéreas.
   - O KIRI reconstruiu o relevo do objeto. Uma câmara num avião faz o mesmo com o terreno. Qual a diferença de escala e de geometria (projeção cônica, altura de voo)?
   - O que aconteceria com um objeto **liso e brilhante**? Relacione com áreas de água ou telhados espelhados nas fotos aéreas.
8. **Fotos históricas:** abra o GeoSampa, aba de download de imagens, e localize as **fotografias aéreas de 1954** (e 1940/2000) da área de estudo. Baixe **dois quadros consecutivos da mesma faixa** — serão o par estéreo da Aula 11.

## Discussão

- Fotogrametria "de bolso" e aerofotogrametria compartilham qual princípio?
- Por que a ortofoto (produto final) **não** serve para ver relevo, mas as fotos brutas sim?

## Entrega

- [ ] Modelo 3D do objeto (captura de tela ou link do KIRI).
- [ ] As respostas da Parte C.
- [ ] Os dois quadros de 1954 baixados do GeoSampa (para a Aula 11).
