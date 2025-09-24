# Conceitos-Chave sobre NoSQL – Versão Visual

## 1. Origem
NoSQL surgiu da necessidade de manipular **Big Data** e dados distribuídos em clusters, onde os bancos relacionais tradicionais enfrentam limitações de escalabilidade e performance.

---

## 2. Significado
**NoSQL = Not Only SQL**  
> Não substitui bancos relacionais, mas os complementa, trazendo flexibilidade e performance para cenários específicos.

---

## 3. Benefícios
| Benefício | Descrição |
|-----------|-----------|
| **Escalabilidade horizontal** | Permite adicionar mais servidores para lidar com crescimento de dados |
| **Alta disponibilidade** | Sistema continua funcionando mesmo com falhas em nós específicos |
| **Flexibilidade de esquema** | Sem necessidade de schema fixo; documentos podem variar em estrutura |

---

## 4. Desafios
- **Consistência eventual:** nem todos os nós refletem a atualização imediatamente  
- **Integridade de dados:** responsabilidade da aplicação, já que não há JOINs nativos ou constraints rígidas

---

## 5. Categorias Principais de NoSQL

| Tipo         | Característica         | Exemplos            | Caso de uso |
|-------------|-----------------------|-------------------|------------|
| **Chave-Valor** | Simples, ultra-performático | Redis, Riak | Cache, sessão de usuário |
| **Documentos** | Flexível, JSON/BSON    | MongoDB, CouchDB  | Dados semi-estruturados, APIs |
| **Colunar**   | Massivo, alta escala    | Cassandra, HBase  | Big Data, análises OLAP |
| **Grafos**    | Relações complexas      | Neo4j             | Redes sociais, roteamento, recomendações |

---

### 💡 Dicas de estudo
- Relacione cada tipo de banco NoSQL com **exemplo de ferramenta** e **caso de uso**.  
- Memorize benefícios vs desafios para explicar claramente na prova.  
- Lembre-se: NoSQL **complementa** SQL, não substitui.
