# FLG0142 — Elementos de Cartografia Sistemática

Material didático completo da disciplina **Elementos de Cartografia Sistemática** (Departamento de Geografia, FFLCH-USP): 15 encontros (13 de conteúdo + prova + 2ª avaliação), cada um com parte teórica e prática.

**Fio condutor:** leitura e produção de cartas topográficas de um setor de **São Paulo em série temporal**, com dados abertos do **GeoSampa** (fotos aéreas 1940/1954/2000, LiDAR 2017, ortofoto 2020) e do **IBGE**. Formatos **analógico e digital**.

**Ferramentas:** QGIS (principal), Google Earth Pro, KIRI Engine (fotogrametria de celular) e um app de GPS. Base teórica: **Fitz, *Cartografia Básica* (2000)**.

📄 **Site:** https://SEU_USUARIO.github.io/flg0142-cartografia-sistematica/

## Estrutura

```
docs/
├── index.md · plano-de-ensino.md · referencias.md
├── ambiente/    setup-qgis · setup-google-earth · setup-apps-celular
├── dados/       fontes-de-dados
├── aulas/       aula-01..15
├── exercicios/  ex-02..14 (passo a passo)
└── figuras/     7 SVG
```

## Rodar localmente

```bash
pip install mkdocs-material
mkdocs serve   # http://127.0.0.1:8000
```

