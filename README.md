Este repositório contém um projeto de banco de dados relacional desenvolvido em SQL para simular a operação de uma loja de produtos eletrônicos. O sistema inclui funcionalidades para cadastro e manipulação de dados de clientes, pedidos, produtos, fornecedores e categorias, além de funcionalidades extras como filtros, atualizações e relacionamentos com chaves estrangeiras.

## 📦 Estrutura do Projeto

O banco de dados é composto pelas seguintes tabelas:

| Tabela               | Descrição                                             |
|----------------------|--------------------------------------------------------|
| `tabelafornecedores` | Armazena informações dos fornecedores                  |
| `tabelapedidos`      | Registra os pedidos realizados pelos clientes         |
| `tabelaclientes`     | Armazena dados dos clientes                           |
| `tabelacategorias`   | Define as categorias dos produtos                     |
| `tabelaprodutos`     | Lista todos os produtos disponíveis na loja           |
| `tabelapedidosgold`  | Registra apenas os pedidos com valor acima de R$400   |
| `funcionarios`       | Exemplo didático de criação de tabela de funcionários |

## 🛠️ Funcionalidades Implementadas

- Criação de tabelas com chaves primárias e estrangeiras
- Inserção de dados fictícios em massa (clientes e produtos)
- Filtros e consultas com `WHERE`, `BETWEEN`, `LIKE`, `ORDER BY`, `IN`, `DISTINCT`
- Atualização de dados com `UPDATE`
- Exclusão com `DELETE`
- Relacionamento entre tabelas usando `FOREIGN KEY`
- Tabela extra com pedidos considerados "premium" (`tabelapedidosgold`)

## 📊 Exemplos de Consultas

```sql
-- Buscar todos os produtos com preço entre R$200 e R$600
SELECT * FROM tabelaprodutos
WHERE preco_de_compra BETWEEN 200 AND 600;

-- Filtrar clientes com nome iniciado após a letra 'C'
SELECT * FROM tabelaclientes WHERE nome_cliente > 'C';

-- Atualizar o status de pedidos em processamento
UPDATE tabelapedidos
SET status = 'Enviado'
WHERE status = 'Processando';


🧱 Tecnologias Utilizadas
SQL padrão

Compatível com SQLite, PostgreSQL e MySQL (com pequenas adaptações)

Ideal para uso em SGBDs educacionais ou simuladores como DB Browser for SQLite
