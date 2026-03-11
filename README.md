🛒 Sistema de Caixa para Supermercado

Sistema de caixa desenvolvido para simular o funcionamento de um PDV (Ponto de Venda) de supermercado.
O projeto permite registrar produtos através do código de barras, calcular valores da venda, selecionar forma de pagamento e gerar uma nota fiscal simplificada.

O sistema foi dividido em frontend e backend, seguindo uma arquitetura comum em aplicações modernas.

🚀 Tecnologias Utilizadas
Backend

Java

Spring Boot

Spring Web

Spring Data JPA

MySQL

Maven

Frontend

React.js

JavaScript

HTML

CSS

Axios

Outros recursos

API REST

QR Code para pagamento via Pix

Áudio de leitura de código de barras

Imagens de produtos via Flaticon

🏗 Arquitetura do Sistema

O projeto é dividido em duas partes principais:

frontend (React)
      ↓
API REST
      ↓
backend (Spring Boot)
      ↓
banco de dados MySQL

O frontend faz requisições HTTP para o backend, que busca os dados no banco de dados.

🗄 Estrutura do Banco de Dados

O sistema utiliza quatro tabelas principais:

Produto

Armazena os produtos cadastrados.

Campos principais:

id

nome

preco

codigo_barras

imagem_url

estoque

categoria_id

Categoria

Organiza os produtos por tipo.

Exemplo:

id	nome
1	Alimentos
2	Bebidas

Relacionamento:

1 Categoria → N Produtos
Venda

Representa uma compra realizada no caixa.

Campos:

id

data

Relacionamento:

1 Venda → N Itens de venda
Item_Venda

Registra os produtos que foram vendidos em cada venda.

Campos:

id

venda_id

produto_id

quantidade

Relacionamento:

1 Produto → N Itens de venda
⚙️ Funcionalidades do Sistema

O sistema possui as seguintes funcionalidades:

📦 Registro de Produtos

Busca de produtos por código de barras

Exibição de nome, preço e imagem

🛒 Carrinho de Compra

Adicionar produtos

Definir quantidade

Cancelar último item

Cálculo automático do total

👤 Cadastro de Cliente

Nome

Contato

CPF

💳 Formas de Pagamento

Dinheiro (com cálculo de troco)

Pix (QR Code)

Cartão (crédito ou débito)

🧾 Nota Fiscal

Após finalizar a venda, o sistema gera uma nota fiscal simplificada contendo:

Produtos comprados

Quantidade

Valor unitário

Valor total

Também é possível imprimir a nota diretamente pelo navegador.

💻 Como Executar o Projeto
1️⃣ Clonar o repositório
git clone [https://github.com/seu-usuario/seu-repositorio.git](https://github.com/lucaspires31/system-supermarket)
Backend (Spring Boot)
Entrar na pasta do backend
cd backend
Instalar dependências
mvn clean install
Rodar aplicação
mvn spring-boot:run

O backend ficará disponível em:

http://localhost:8080
Frontend (React)
Entrar na pasta do frontend
cd frontend
Instalar dependências
npm install
Rodar o projeto
npm run dev

O frontend ficará disponível em:

http://localhost:5173
🗃 Configuração do Banco de Dados

O sistema utiliza MySQL.

Exemplo de configuração no application.properties:

spring.datasource.url=jdbc:mysql://localhost:3306/supermercado
spring.datasource.username=root
spring.datasource.password=sua_senha

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
📸 Imagens de Produtos

As imagens utilizadas no sistema são hospedadas publicamente e exibidas através de URLs.

Exemplo:

https://cdn-icons-png.flaticon.com/128/9873/9873609.png
🎯 Objetivo do Projeto

Este projeto foi desenvolvido com fins educacionais, com o objetivo de praticar:

Desenvolvimento Full Stack

Construção de APIs REST

Integração Frontend + Backend

Modelagem de Banco de Dados

Uso do Spring Boot

Desenvolvimento de interfaces com React


👨‍💻 Autor

Lucas Alves

Estudante de Análise e Desenvolvimento de Sistemas e Técnico em Informática, com foco em desenvolvimento Java Backend.
