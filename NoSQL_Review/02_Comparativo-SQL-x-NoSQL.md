# Comparativo Prático: SQL x NoSQL (MongoDB)

| Conceito SQL | Equivalente MongoDB |
|--------------|------------------|
| Tabelas      | Coleções         |
| Linhas       | Documentos BSON  |
| Colunas      | Campos/Atributos |
| JOIN         | Documentos embutidos ou links |
| ACID         | Eventual consistency + atomicidade por documento |
| Schema rígido| Schema flexível (schemaless) |

## Observações
- NoSQL não faz JOINs complexos nativamente → usa **documentos embutidos** ou referências.
- Consistência eventual = nem todos os nós refletem imediatamente a atualização.
