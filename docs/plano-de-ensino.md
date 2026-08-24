# FLG0142 — Elementos de Cartografia Sistemática
## Plano de Ensino

**Departamento de Geografia · FFLCH-USP** · Bacharelado · 4 créditos-aula + 2 créditos-trabalho · 120h · **20h de PCC** · 15 encontros.

---

## 1. Apresentação

O curso trata os elementos que tornam uma **carta topográfica** um documento utilizável: escala, referenciais, projeções, coordenadas, os três nortes, curvas de nível, perfil, e a leitura integrada de planimetria e altimetria. A ementa pede, além disso, que se estabeleça a relação da Cartografia com as áreas vinculadas — **Cartografia Temática, Sensoriamento Remoto, Sistemas de Informações Geográficas e GPS** — e que se discuta a incorporação desses conteúdos no ensino e na formação de professores.

O fio condutor é um **estudo de caso de Campinas**: georreferenciar a carta topográfica do IBGE (1:50.000, anos 1980), descobrir a sua **desatualização** ao sobrepô-la à imagem de satélite atual, e **atualizar** a cartografia de uma sub-região — digitalizando a mancha urbana de 1980 e a atual, as vias novas e marcadores, e medindo a **expansão urbana em quatro décadas**. O relevo (curvas, hipsometria, declividade) explica *onde* e *como* a cidade cresceu. O aluno **lê** a carta e **produz** a atualização, nos formatos **analógico e digital**.

As práticas usam **QGIS** como ambiente principal, com a imagem de satélite atual (**Google/Esri via XYZ Tiles**) como base de digitalização; **Google Earth** para SIG, série histórica e uso didático; o **KIRI Engine** (fotogrametria com o celular); e um **app de GPS**. Não há drone nem campo noturno. A sequência é encadeada, mas com **produto de referência pronto a cada etapa**, para ninguém travar.

**Divisão do tempo:** cada encontro de conteúdo combina uma parte **teórica** (~1h–1h15) e uma parte **prática** (~1h45–2h), em torno de 3h por aula.

---

## 2. Objetivos

Ao final da disciplina, o estudante deve ser capaz de:

1. Conceituar a Cartografia e situá-la em relação a Cartografia Temática, Sensoriamento Remoto, SIG e GPS.
2. Operar seus principais atributos: coordenadas, escala, curva de nível, perfil topográfico, norte e projeções.
3. Ler e usar cartas topográficas nos formatos **analógico e digital**.
4. Discutir a incorporação da Cartografia nas atividades de ensino e na formação de professores (PCC).

---

## 3. Estrutura das 15 aulas

| # | Aula | Ementa/Objetivo |
|---|------|-----------------|
| **Módulo I — A carta e seu sistema de referência** ||
| 1 | Escala e generalização cartográfica *(engajamento — já ministrada)* | esc. / obj. 2 |
| 2 | Cartografia sistemática: conceito e anatomia da folha topográfica | 1 / obj. 1 |
| 3 | Áreas vinculadas: Cartografia Temática, SR, SIG e GPS | 1 / obj. 1 |
| 4 | Referenciais cartográficos: geoide, elipsoide, datum | 2 / obj. 2 |
| 5 | Projeções cartográficas | 3, 8 / obj. 2 |
| 6 | Coordenadas geográficas e UTM; introdução ao GPS | 4 / obj. 1, 2 |
| 7 | Escala: numérica, gráfica, generalização e escala da foto | 3 / obj. 2 |
| **8** | **PROVA** (teórico-prática) | — |
| **Módulo II — Da imagem ao relevo** ||
| 9 | Norte, azimute e medidas angulares | 4 / obj. 2 |
| 10 | Fotogrametria e Sensoriamento Remoto: da imagem à carta | 1, 9 / obj. 1 |
| 11 | Estereoscopia e paralaxe | 5 / obj. 2 |
| **Módulo III — A carta e suas leituras** ||
| 12 | Curvas de nível e perfil topográfico | 5 / obj. 2, 3 |
| 13 | Leitura de cartas: planimetria, altimetria, hipsometria e clinografia | 5, 6, 7 / obj. 2, 3 |
| 14 | SIG e Google Earth na sala de aula; formato digital e ensino | 6, 9, 10 / obj. 1, 3, 4 |
| **15** | **2ª AVALIAÇÃO:** carta topográfica final + produto de PCC | — |

---

## 4. Avaliação

| Componente | Peso |
|-----------|------|
| Exercícios práticos (QGIS, GPS, KIRI, estereoscopia) | 30% |
| **Prova** (Aula 8) | 25% |
| **Carta topográfica final** (analógica + digital, Aula 15) | 25% |
| Produto de PCC (maquete de curvas + sequência didática, Aula 15) | 20% |

Recuperação conforme a norma da unidade.

---

## 5. PCC — 20h

O componente de Práticas como Componente Curricular desenvolve situações didáticas que evidenciem as **transformações curriculares entre o contexto escolar e o universitário**.

**Produto:** maquete de curvas de nível (a partir das próprias curvas geradas na Aula 12) + sequência didática para a Educação Básica, apoiada em um recurso digital (KML no Google Earth, a partir da Aula 14). Momentos de PCC em aula: 2, 12, 13 e 14; consolidação e apresentação na Aula 15.

---

## 6. Ferramentas e dados

- **QGIS** (versão LTR) — ambiente principal. Ver [Instalar o QGIS](ambiente/setup-qgis.md) e [Imagens de satélite (XYZ)](ambiente/setup-xyz-tiles.md).
- **Google Earth Pro** (desktop) — SIG e uso didático. Ver [Instalar o Google Earth](ambiente/setup-google-earth.md).
- **KIRI Engine** (celular/web) e **app de GPS** — ver [Apps no celular](ambiente/setup-apps-celular.md).
- **Dados abertos** (GeoSampa, IBGE) — ver [Fontes de dados](dados/fontes-de-dados.md).

---

## 7. Bibliografia

**Básica**
- FITZ, P. R. *Cartografia básica*. Canoas: La Salle, 2000. *(referência teórica principal do curso)*
- IBGE. *Noções básicas de cartografia*. Rio de Janeiro: IBGE, 1999. *(acesso aberto)*
- OLIVEIRA, C. de. *Curso de cartografia moderna*. Rio de Janeiro: IBGE, 1993.
- MENEZES, P. M. L.; FERNANDES, M. C. *Roteiro de cartografia*. São Paulo: Oficina de Textos, 2013.

**Complementar**
- FITZ, P. R. *Geoprocessamento sem complicação*. São Paulo: Oficina de Textos, 2008.
- DUARTE, P. A. *Fundamentos de cartografia*. Florianópolis: UFSC, 2002.
- LOCH, C.; LAPOLLI, E. M. *Elementos básicos da fotogrametria e sua utilização prática*. Florianópolis: UFSC, 1994.
- DE BIASI, M. Carta clinográfica: os métodos de representação e sua confecção. *Revista do Departamento de Geografia*, USP, n. 6, 1992. *(acesso aberto)*
- QGIS. *QGIS Training Manual / Documentation*. *(acesso aberto)*
