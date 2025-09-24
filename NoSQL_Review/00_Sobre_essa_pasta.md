# 📂 Resumo de Ricardo – Conteúdo e Organização

Esta pasta reúne arquivos e anotações para revisão de **NoSQL e MongoDB**, organizados para estudo rápido e completo.

---

## 1. `pos_nosql`
**Tema principal:** Conceitos gerais de NoSQL  

**Conteúdo:**
- Origem: surgiu da necessidade de manipular Big Data e clusters.
- Significado: **Not Only SQL** → complementa bancos relacionais.
- Benefícios: escalabilidade horizontal, alta disponibilidade, flexibilidade de esquema.
- Desafios: consistência eventual e integridade de dados na aplicação.
- Categorias de NoSQL com exemplos práticos:
  - **Chave-Valor**: Redis, Riak → cache, sessão de usuário.
  - **Documentos**: MongoDB, CouchDB → dados semi-estruturados, APIs.
  - **Colunar**: Cassandra, HBase → Big Data, análises OLAP.
  - **Grafos**: Neo4j → redes sociais, roteamento, recomendações.

**Uso:** Base teórica para entender **tipos de banco, benefícios e desafios**.

---

## 2. `Introducao-aoMongoDB`
**Tema principal:** MongoDB detalhado e comparação com SQL  

**Conteúdo:**
- Estrutura: Database → Coleções → Documentos
- Cada documento possui **_id**, formato **BSON**
- Componentes: 
  - **mongod** → servidor
  - **mongo** → shell cliente
  - **mongos** → roteador para sharding
- Comparativo SQL x MongoDB:
  | SQL        | MongoDB       |
  |------------|---------------|
  | Tabela     | Coleção       |
  | Linha      | Documento     |
  | Coluna     | Campo         |
  | JOIN       | Documentos embutidos / referências |
- CRUD básico: `insert`, `find`, `update`, `remove`
- Operadores importantes: `$gt`, `$lt`, `$in`, `$and`, `$or`, `$regex`, `$exists`
- Dot notation → acesso a subdocumentos/arrays
- Limitações: documento máximo 16 MB, sem JOIN nativo, atomicidade por documento

**Uso:** Compreender **estrutura, CRUD, operadores e limitações** do MongoDB.

---

## 3. `Projeto de Persistência Poliglota com MongoDB - AV1`
**Tema principal:** Integração de múltiplos bancos (SQL + NoSQL)  

**Conteúdo:**
- Conceito de **persistência poliglota**: usar diferentes bancos conforme a natureza dos dados
- Exemplo prático:
  - **SQLite** → dados tabulares (usuários, cidades, estados)
  - **MongoDB** → documentos JSON com coordenadas geoespaciais
  - **Python + Streamlit** → interface interativa
- Ferramentas usadas: PyMongo, Geopy, Folium, Pandas
- Aplicações: calcular distâncias, listar locais próximos, geoprocessamento

**Uso:** Entender **quando usar SQL + NoSQL e integração prática em projetos**.

---

## 4. `revisao_nosql_mongodb`
**Tema principal:** Revisão consolidada para prova  

**Conteúdo:**
- Revisão de conceitos gerais de NoSQL
- Tipos de bancos NoSQL + exemplos
- MongoDB em detalhe: CRUD, operadores, dot notation
- Escalabilidade: **Sharding** e **ReplicaSet**
- GeoJSON e consultas geoespaciais: `$near`, `$geoWithin`, `$geoIntersects`
- Persistência poliglota: integração SQL + NoSQL
- Pontos críticos para prova: integridade sem JOIN, consistência forte vs eventual

**Uso:** Guia final para estudo rápido antes da prova.

---

### 💡 Dicas de estudo
- Relacione **tipo de NoSQL → ferramenta → caso de uso**
- Pratique **CRUD e consultas geoespaciais** no MongoDB
- Revise a **persistência poliglota** e por que SQL + NoSQL juntos
