# Aula 5 — Projeções cartográficas

**Onde:** sala + laboratório (QGIS) · **Módulo:** I

## Objetivos

- Entender por que toda projeção deforma e o que se escolhe preservar.
- Classificar projeções por propriedade e por superfície.
- Compreender o sistema UTM e situar São Paulo nele.

## Teoria

Não se planifica uma esfera sem deformá-la: a superfície esférica não é **desenvolvível**, ao contrário do cone e do cilindro. Toda projeção é, portanto, uma escolha sobre o que sacrificar. Projeções **conformes** preservam ângulos e formas locais (e distorcem áreas); **equivalentes** preservam áreas (e distorcem formas); **equidistantes** preservam distâncias em direções específicas; **afiláticas** não preservam nenhuma delas (Fitz, 2000, cap. "A representação cartográfica"). Classificam-se ainda pela superfície (plana, cônica, cilíndrica) e por sua posição e situação (tangente/secante; normal/transversa/oblíqua).

O sistema **UTM** resolve o mapeamento sistemático dividindo o mundo em **60 fusos de 6°**, cada um com seu meridiano central e um cilindro transverso secante. Aplica-se ao meridiano central um **fator de escala 0,9996**, e adotam-se falso leste de 500.000 m e, no hemisfério sul, falso norte de 10.000.000 m. São Paulo está no **fuso 23 Sul**, meridiano central **45° W** — número que retorna na Aula 9, na convergência meridiana. No QGIS, exibir uma camada mundial em projeções diferentes e medir a distorção de área (Groenlândia × Brasil) mostra, com números, o preço de cada escolha.

## Roteiro (3h)

| Bloco | Descrição |
|-------|-----------|
| Teoria | Deformação e propriedades; famílias de projeções; o sistema UTM |
| Prática | No QGIS, comparar projeções e medir distorções; determinar o fuso UTM de São Paulo |

## Laboratório

**[Ex. 05 — Projeções e distorção no QGIS](../exercicios/ex-05-projecoes.md)**

## Leituras

- FITZ, P. R. *Cartografia básica*, cap. "A representação cartográfica" (projeções) e "Sistemas de coordenadas" (UTM).
