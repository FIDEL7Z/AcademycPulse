# GeoJSON e Consultas Geoespaciais no MongoDB – Versão Visual

## 1. O que é GeoJSON
Formato JSON padrão para representar **dados espaciais**. Tipos mais comuns:

| Tipo     | Exemplo | Descrição |
|----------|---------|-----------|
| **Ponto** | `{ "type": "Point", "coordinates": [lng, lat] }` | Localização específica |
| **Linha** | `{ "type": "LineString", "coordinates": [[lng1, lat1], [lng2, lat2]] }` | Caminhos ou trajetos |
| **Polígono** | `{ "type": "Polygon", "coordinates": [[[lng1, lat1], [lng2, lat2], [lng3, lat3], [lng1, lat1]]] }` | Áreas fechadas |

---

## 2. Índices Espaciais

| Índice  | Uso |
|---------|-----|
| `2d`    | Plano cartesiano (bidimensional) |
| `2dsphere` | Superfície esférica (Terra), recomendado para GPS/geo apps |

> **Dica:** Sempre use `2dsphere` para dados de localização real (latitude/longitude).

---

## 3. Operadores Geoespaciais

| Operador      | Função | Exemplo MongoDB |
|---------------|--------|----------------|
| `$near`       | Objetos próximos a um ponto | `db.lugares.find({location:{$near:{$geometry:{type:"Point",coordinates:[lng,lat]}}}})` |
| `$geoWithin`  | Objetos dentro de uma área | `db.lugares.find({location:{$geoWithin:{$geometry:{type:"Polygon",coordinates:[...]}}}})` |
| `$geoIntersects` | Objetos que cruzam uma área | `db.lugares.find({location:{$geoIntersects:{$geometry:{type:"Polygon",coordinates:[...]}}}})` |

---

## 4. Casos de Uso
- **Apps de localização:** encontrar usuários ou pontos de interesse próximos  
- **Delivery / logística:** rotas, proximidade de clientes  
- **Mapas interativos:** exibir áreas, trajetos ou regiões de interesse  

---

## 5. MongoDB Atlas (Multicloud)
- MongoDB gerenciado em nuvem  
- **Escalabilidade automática** → adiciona recursos conforme demanda  
- **Alta disponibilidade** → replica dados em múltiplas regiões  
- **Segurança e disaster recovery** → backups automáticos e criptografia

---

### 💡 Dicas de Estudo
- Pratique criar **pontos, linhas e polígonos** em coleções de teste.  
- Experimente consultas com `$near`, `$geoWithin` e `$geoIntersects`.  
- Entenda quando usar **2d vs 2dsphere** → prova pode perguntar a diferença.  
