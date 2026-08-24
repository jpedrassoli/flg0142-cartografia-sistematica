# Imagens de satélite no QGIS (XYZ Tiles)

Para digitalizar sobre imagem recente, usamos **camadas XYZ** (Google Satellite / Esri World Imagery). Elas são servidas por CDN em *tiles* — não saturam com 40 acessos como um WMS, e entram em Web Mercator (EPSG:3857), com reprojeção automática do QGIS.

## Conexão nativa (sem plugin — recomendado)

No painel **Navegador**, botão direito em **XYZ Tiles → Nova conexão**:

| Nome | URL | Zoom máx. |
|------|-----|-----------|
| Esri World Imagery | `https://services.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer/tile/{z}/{y}/{x}` | 19 |
| Google Satellite | `https://mt1.google.com/vt/lyrs=s&x={x}&y={y}&z={z}` | 20 |

Duplo-clique para adicionar ao projeto. A **Esri World Imagery** costuma ser a mais estável em sala.

## Via QuickMapServices (alternativa)

*Complementos → Gerenciar e instalar → QuickMapServices*. Depois **Web → QuickMapServices → Settings → More services → Get contributed pack** (adiciona Google/Bing). Use **Web → QuickMapServices → Google/Bing → Satellite**.

!!! warning "Licença — uma linha para os alunos"
    As imagens do Google/Bing têm **termos de uso** que restringem digitalizar e redistribuir derivados. Para **uso interno de sala**, sem publicar os shapefiles, é aceitável — mas registre que a base tem licença. Se o produto for publicado, troque por **ortofoto de uso aberto**. É, em si, uma boa discussão de ética em dados cartográficos.

!!! tip "Plano B (rede caiu)"
    Tenha a **carta de Campinas georreferenciada salva localmente** (GeoTIFF). Se a internet do laboratório falhar, a digitalização da mancha de 1980 (que é lida da carta) segue sem a imagem recente.
