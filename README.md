# 📊 Data Warehouse de Vendas

Este projeto consiste na implementação de um **Data Warehouse (DW)** modelado no **Esquema Estrela (Star Schema)**, com foco em **análise de vendas, clientes, produtos, tempo, geografia e moedas**. O objetivo principal é permitir **consultas analíticas eficientes**, geração de **relatórios gerenciais** e suporte à **tomada de decisão estratégica**.

---

## 🎯 Objetivo do Projeto

O banco foi desenvolvido para:

* Analisar o desempenho de vendas ao longo do tempo
* Avaliar faturamento por produto, categoria e cliente
* Identificar padrões de compra dos clientes
* Apoiar dashboards em ferramentas de BI (Power BI, Tableau, etc.)
* Servir como base de estudo em **Business Intelligence, Data Analytics e Data Science**

Este banco **não é transacional (OLTP)**, mas sim **analítico (OLAP)**.

---

## 🧱 Modelagem do Banco

O Data Warehouse é composto por **Tabelas Dimensão (DIM)** e **Tabelas Fato (FATO)**.

### ⭐ Tabelas Dimensão

As dimensões descrevem o contexto dos dados de negócio.

#### 🧑 DIM_CLIENTE

Armazena informações detalhadas dos clientes:

* Dados pessoais (nome, gênero, estado civil)
* Informações socioeconômicas (renda, educação, ocupação)
* Endereço e contato
* Data da primeira compra

---

#### 📦 DIM_PRODUTO

Contém os atributos dos produtos:

* Nome, cor, tamanho e peso
* Custos, preços e status
* Linha e modelo do produto

---

#### 🗂 DIM_PRODUTO_CATEGORIA

Define as categorias dos produtos.

---

#### 🗂 DIM_PRODUTO_SUBCATEGORIA

Relaciona os produtos às suas subcategorias e categorias.

---

#### 🌍 DIM_GEOGRAFIA

Representa a localização geográfica:

* Cidade, estado e país
* Código postal

---

#### 📅 DIM_DATA

Dimensão de tempo essencial para análises históricas:

* Dia, mês e ano
* Trimestre e semestre
* Calendário fiscal

---

#### 💱 DIM_MOEDA

Armazena os tipos de moedas utilizadas nas vendas.

---

#### 🏪 DIM_REVENDEDOR

Informações sobre empresas revendedoras:

* Tipo de negócio
* Faturamento anual
* Localização

---

## 🔥 Tabelas Fato

As tabelas fato armazenam os **eventos mensuráveis** do negócio.

### 💰 FATO_VENDAS

Tabela central do Data Warehouse, responsável por registrar cada venda realizada:

* Produto vendido
* Cliente
* Datas (pedido, envio e entrega)
* Quantidade
* Valores financeiros (preço, desconto, imposto, frete, custo e valor final)

Essa tabela permite análises como:

* Total de vendas por período
* Ticket médio
* Receita por cliente ou produto

---

### 📦 FATO_PRODUTO_INVENTARIO

Controla o estoque dos produtos:

* Entradas e saídas
* Saldo disponível por data

---

### 💱 FATO_TAXAS

Armazena taxas de câmbio por data:

* Taxa média
* Taxa do fim do dia

---

## 👁️ Views Criadas

### 📊 vw_MediaUnitPricePorProduto

Exibe o **preço médio unitário dos produtos por categoria**, facilitando análises comparativas.

---

### 👥 vw_ClientesCompraramMaisDe2Unidades

Lista clientes que compraram **mais de 2 unidades** de um produto.

---

### 🛒 vw_ClientesProdutosCompraramMaisDe2Unidades

Relaciona clientes e produtos com volume de compra elevado, incluindo:

* Nome do produto
* Linha do produto
* Quantidade total comprada

---

## 🧠 Tecnologias Utilizadas

* SQL (DDL e DML)
* Modelagem Dimensional
* Conceitos de Data Warehouse
* Pronto para integração com Power BI e outras ferramentas de BI

---

## 🚀 Possíveis Aplicações

* Dashboards gerenciais
* Relatórios de desempenho de vendas
* Análises de comportamento do cliente
* Estudos acadêmicos em BI e Data Science
* Projetos de portfólio

---

## 📌 Observação

Este projeto é ideal para fins educacionais e profissionais, demonstrando domínio em:

* SQL Avançado
* Modelagem de Dados
* Business Intelligence
* Análise de Dados

---

📈 **Projeto desenvolvido com foco em análise de dados e inteligência de negócios.**
