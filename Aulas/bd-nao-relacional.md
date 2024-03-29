# Introdução a Banco de Dados Não Relacionais

- Termo correto: NOT Only SQL
- Não seguem modelo de tabelas e relacionamentos
- Projetados para lidar com **alto volume de dados**, alta escalabilidade, alta **flexibilidade** na estrutura de dados
- Eles são amplamente utilizados onde a consistência imedida dos dados não é crítica

## Diferenças
| SQL  | NoSQL|
| :-------------: | :-------------: |
| Modelo de dados fixo  | Modelo de dados flexível  |
| Escalabilidade vertical (Hardware)  | Escalabilidade horizontal  |
| Transações ACID 100%  | Transações ACID ausentes total ou parcial |
| Linguagem de consulta SQL  | Cada SGBD tem sua própria |

## Vantagens
- Flexibilidade na modelagem
- Alta escalabilidade
- Melhor desempenho em cenário de consulta intensiva
- Tolerância a falhas

## Desvantagens
- Menor consistência de dados imediata
- Menor suporte a consulta complexas ** depente do SGBD

## Tipos
### Key-Value
Armazena dados como pares de chave e valor, onde cada chave é um indentificador único par acessar o valor correspondente
**Ex.:** Redis, Riak, Amazon DynamoDB
**Uso:** Um site pode usar um bd Redis par armazenar informações de sesão de usuário.

### Document
Armazena dados em documentos semiestruturados, geralmente em formato JSON ou BSON.
**Ex.:** MongoDB, Couchbase, Apache CouchDB
**Uso:** Um catálogo de e-commerce pode usar o MongoDB para armazenar informações de produtos.

### Coluna
Armazenam dados em formato de colunas, o que permite alta escalabilidade e eficiência em determinados tipois de consultas.
**Ex.:** Apache Cassandra, ScyllaDB, HBase
**Uso:** Um sistema de registro de aplicativos pode usar o Apache Cassandra para armazenar registros de log.

### Grafos
Armazenar e consultar dados interconectados , onde os relacionamentos entre os dados são tão importantes quanto os próprios dados.
**Ex.:** Neo4j, Amazon Neptune, JanusGraph
**Uso:** Uma rede social pode usar o Neo4j para armazenar os perfis de usuário e suas conexões, permitindo consultas eficientes para encontrar amigos em comum.

# Introdução ao MongoDB
- Bando de dados NoSQL orientado a documentos
- Grande volume de dados, escalabilidade horizontal e modelagem flexível
- Não exige um esquema
- Permite que os documentos sejam armazenados em formato BSON (Binary JSON), proporcionando uma estrutura semiestruturada

## Vantagens
- Flexibilidade na modelagem de dados
- Escalabilidade horizontal para lidar com grande volumes de dados
- Consultas ricas e suporte a consultas complexas
- Alta disponibilidade e tolerância a falhas

## Desvantagens
- Menor consistência imediata em comparação com banco de dados relacionais
- Consultas complexas podem exigir um maior conhecimento e planejamento adequado
- Maior consumo de espaço de armazenamento em comparação com bancos de dados relacionais devido à flexibilidade dos documentos

## Utilização
- Aplicações web
- Análise de big data
- Armazenamento de dados semiestruturados
- Casos de uso de geolocalização

## Estrutura
![Estrutura](https://lh6.googleusercontent.com/ZqnDvueKcgc3M7dxbqYokJ7nKyaKnCNDL0_Khz4ohCwtRzv_bA7GjqCOWO5df-3HcZO54bXS8Q5Vi_kuDjk5m_tJJb4d_lqgOUcrt1pr0Mpwgc6wIoI5y1j1DXDt4qNcN0YmKP0f)
  
### Características
- Devem começar com uma letra ou um underscore
- Podem conter letras, números ou underscores
- Não podem ser vazios
- Não podem ter mais de 64 bytes de comprimento

### Coleções
- agrupamento lógico de documentos
- Não exige esquema ou que os documentos tenham a mesma estrutura

### Documentos
- São armazenados em documentos BSON
- Cada documento possui um identificado único chamado "_id"
- É composto por pares de chaves e valores

```mongodb
{
    _id: Objectld(""),
    "nome_campo":"valor_campo", ...
}
```
### Tipos de dados simples
- String
- Number
- Boolean
- Data
- Null
- Objectld

### Tipos de dados complexos
- Array
- Embedded Document
- Reference
- GeoJSON

# Introdução ao Redis
  É um sistema de armazenamento de dados em memória de alto desempenho

## Características
- Armazenamento em memória
- Estrutura de dados versáril
- Operações atômicas
- Cache de alto desempenho
- Pub/Sub (Publicação/Assinatura)

## Utilização
- Cache de dados
- Filas de mensagens
- Contagem de acessos e estatísticas em tempo real
- Gerenciamento de sessões
- Cache de resultados de consultas

## Principais comandos
- SET
- GET
- DEL
- EXISTS
- KEYS
- INCR
- DECR
