# Instalar o QGIS

O **QGIS** é um Sistema de Informações Geográficas livre e gratuito. É o ambiente principal das práticas do curso.

## Instalação

1. Acesse **qgis.org** → *Download*.
2. Escolha a versão **LTR** (*Long Term Release*) — é a mais estável para uso em aula.
3. Windows: baixe o instalador *Standalone* e execute. macOS: baixe o `.dmg`. Linux: siga as instruções da distribuição.
4. Abra o QGIS e confirme o idioma em **Configurações → Opções → Geral → Idioma** (Português do Brasil).

## Ajustes recomendados para o curso

- **SRC do projeto:** ao criar um projeto, defina o Sistema de Referência de Coordenadas como **SIRGAS 2000 / UTM zona 23S** (EPSG:31983), que é o de São Paulo. Barra inferior direita → clique no SRC → busque `31983`.
- **Reprojeção automática:** deixe ativada (*on-the-fly*), padrão do QGIS, para sobrepor camadas em SRC diferentes.
- **Complementos úteis:** menu **Complementos → Gerenciar e instalar complementos**. Instale, quando um exercício pedir: *Terrain Profile* (perfil topográfico), *QuickMapServices* (bases de fundo).

## Conceitos que usaremos

- **Camada raster:** imagem em grade (ortofoto, MDT, folha digitalizada).
- **Camada vetorial:** pontos, linhas e polígonos (curvas, pontos de GPS).
- **SRC / EPSG:** o código do sistema de referência. SIRGAS 2000 geográfico = EPSG:4674; SIRGAS 2000 / UTM 23S = EPSG:31983; Córrego Alegre / UTM 23S ≈ EPSG:22523.
- **Georreferenciar:** atribuir coordenadas a um raster que não as tem (Aula 2).
