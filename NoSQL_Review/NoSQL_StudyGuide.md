# 📘 Revisão Completa – Bancos NoSQL e MongoDB  

---

## 1. Conceitos Gerais de NoSQL
- **NoSQL = Not Only SQL**:  
  Bancos de dados que fogem do modelo relacional tradicional.  
- **Motivações:**  
  - Big Data → necessidade de lidar com volumes massivos.  
  - Alta disponibilidade → sistemas que não podem parar.  
  - Escalabilidade → distribuir dados entre muitos servidores.  
  - Flexibilidade → sem esquema fixo, dados podem variar.  
- **Desafios:**  
  - Consistência eventual (trade-off entre disponibilidade e consistência).  
  - Menor suporte a transações complexas.  
  - Integridade de dados depende da aplicação.  

---

## 2. Tipos de Bancos NoSQL e Casos de Uso
1. **Chave-Valor**  
   - Estrutura simples (chave única → valor opaco).  
   - Ex: Redis, Riak.  
   - Uso: cache, sessões, contadores.  

2. **Documentos**  
   - Armazena documentos JSON/BSON.  
   - Ex: MongoDB, CouchDB.  
   - Uso: dados flexíveis, aplicações web/mobile.  

3. **Colunares**  
   - Baseados em famílias de colunas.  
   - Ex: Cassandra, HBase.  
   - Uso: grandes volumes analíticos (Big Data).  

4. **Grafos**  
   - Focados em relações e conexões.  
   - Ex: Neo4j.  
   - Uso: redes sociais, recomendação, análise de conexões.  

---

## 3. MongoDB em Detalhe
- **Modelo:** Documentos BSON.  
- **Comparativo com SQL:**  
  - Tabelas → Coleções  
  - Linhas → Documentos  
  - Colunas → Campos  
- **Componentes principais:**  
  - `mongod` (servidor).  
  - `mongo` (cliente shell).  
  - `mongos` (sharding router).  
- **CRUD:**  
  - Inserir → `db.colecao.insert({...})`.  
  - Consultar → `db.colecao.find({})`.  
  - Atualizar → `db.colecao.update({cond}, {$set:{...}})`.  
  - Remover → `db.colecao.remove({})`.  
- **Operadores importantes:** `$gt`, `$lt`, `$in`, `$and`, `$or`, `$regex`, `$exists`.  
- **Dot notation:** acessar subdocumentos → `{"endereco.cidade":"São Paulo"}`.  

---

## 4. Escalabilidade e Disponibilidade
- **ReplicaSet:**  
  - Múltiplos servidores com os mesmos dados.  
  - Garantia de disponibilidade (failover).  
- **Sharding:**  
  - Particionamento horizontal dos dados (shards).  
  - Permite distribuir coleções grandes em múltiplos nós.  
- **Teorema CAP:**  
  - Não dá pra ter Consistência + Disponibilidade + Particionamento ao mesmo tempo.  
  - MongoDB prioriza Disponibilidade + Particionamento (aceita consistência eventual).  

---

## 5. GeoJSON e Consultas Geoespaciais
- **GeoJSON:** padrão JSON para representar localizações.  
  - Tipos: Point, LineString, Polygon.  
- **Índices geoespaciais:**  
  - `2d` (plano cartesiano).  
  - `2dsphere` (coordenadas na Terra).  
- **Operadores:**  
  - `$near` → pontos próximos.  
  - `$geoWithin` → dentro de uma área.  
  - `$geoIntersects` → cruzando uma área.  
- **Caso de uso:** apps de localização, delivery, mapas.  

---

## 6. Persistência Poliglota
- **Definição:** uso de diferentes bancos ao mesmo tempo, cada um para sua função.  
- **Exemplo prático (projeto):**  
  - SQLite → tabelas de cidades/estados.  
  - MongoDB → documentos JSON com coordenadas e descrições.  
  - Python + Streamlit → interface para visualização no mapa.  
- **Vantagem:** aproveita o melhor de cada tipo de banco.  

---

## 7. Pontos-Chave para Prova
- Diferencie os **4 tipos de NoSQL** e cite exemplos.  
- Explique **por que NoSQL não substitui SQL**.  
- Entenda **consistência eventual** e **atomicidade por documento**.  
- Mostre que sabe o **CRUD no MongoDB** (insert, find, update, remove).  
- Detalhe **ReplicaSet e Sharding**.  
- Explique **GeoJSON + operadores geoespaciais**.  
- Mostre a lógica de **persistência poliglota** e por que ela é usada.  

---

📌 **Resumo final:**  
O segredo é mostrar domínio dos **conceitos teóricos** (CAP, consistência, tipos NoSQL) e **habilidade prática** (MongoDB CRUD, operadores, geoprocessamento).  
