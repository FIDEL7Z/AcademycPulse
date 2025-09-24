# MongoDB em Profundidade – Versão Visual

## 1. Estrutura
| Conceito      | Descrição                                |
|---------------|------------------------------------------|
| Database      | Contêiner de coleções                     |
| Coleção       | Agrupamento de documentos                 |
| Documento     | Registro individual, em **BSON**         |
| _id           | Identificador único de cada documento    |

---

## 2. Componentes do MongoDB
| Componente | Função |
|------------|--------|
| **mongod** | Servidor MongoDB que armazena os dados |
| **mongo**  | Cliente shell para interagir com o banco |
| **mongos** | Roteador usado em **sharding** para distribuir dados |

---

## 3. Escalabilidade
| Recurso       | Função |
|---------------|--------|
| **Sharding**  | Divide dados em múltiplos shards → escalabilidade horizontal |
| **ReplicaSet**| Mantém cópias redundantes → alta disponibilidade |

---

## 4. CRUD no MongoDB

| Operação | Comando | Exemplo |
|----------|---------|---------|
| **Create** | `insert` | `db.colecao.insert({nome:"Fidelis", idade:25})` |
| **Read**   | `find` | `db.colecao.find({idade:{$gt:20}})` |
| **Update** | `update` | `db.colecao.update({nome:"Fidelis"}, {$set:{idade:26}})` |
| **Delete** | `remove` | `db.colecao.remove({nome:"Fidelis"})` |

---

## 5. Operadores Importantes

| Tipo        | Operadores | Exemplo |
|------------|------------|---------|
| Comparação | `$gt`, `$lt`, `$in` | `{idade:{$gt:20}}` |
| Lógicos    | `$and`, `$or` | `{$or:[{idade:25},{idade:30}]}` |
| Strings/Regex | `$regex` | `{nome:{$regex:"^F"}}` |
| Existência | `$exists` | `{email:{$exists:true}}` |
| Dot Notation | Acessar subdocumentos/arrays | `{"notas.math":10}` |

---

## 6. Limitações
- Documento máximo: **16 MB**
- **Sem JOIN nativo** → relações complexas exigem desnormalização
- Atomicidade garantida apenas **por documento**, não por coleções

---

## 7. Dicas Visuais para Estudo
- Memorize CRUD com a tabela → mais rápido que decorar comandos soltos.
- Visualize operadores por tipo → ajuda na prova de consulta.
- Imagine o sharding como “dividir dados em caixas” e o ReplicaSet como “cópias de segurança automáticas”.
