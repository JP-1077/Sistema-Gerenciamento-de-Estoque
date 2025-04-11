# **📦 Sistema de Gerenciamento de Estoque**

Este projeto tem como objetivo desenvolver um sistema para realizar o controle de estoque de produtos, permitindo gerenciar inventário, registrar pedidos, acompanhar vendas e obter relatórios completos de forma simples e eficiente.

# 

## **🎯 1. Objetivo do Projeto**

Desenvolver uma aplicação que permita:
 * Gerenciar o estoque de produtos de forma eficiente;
 * Registrar pedidos de clientes, atualizando o estoque automaticamente;
 * Acompanhar vendas, lucros e alertas de baixo estoque;
 * Eliminar o uso de planilhas e evitar erros manuais no controle dos produtos;

# 

## **✍🏽 2. System Design**

### Arquitetura do Sistema
O projeto vai seguir um padrão de arquitetura MVT (Model - View - Template) que é nativa do Framework Django. Desta forma, iremos conseguir trazer determinados ganhos para aplicação. São eles:

  * Separação de Responsabilidades
  * Desenvolvimento mais organizado
  * Reutilização de código
  * Nativo do Django

<img src="Arquitetura%20do%20Sistema.png" alt="Arquitetura" width="600"/>

# 

### Funcionalidades do Sistema
O sistema tem como principais funcionalidades:
  * Realizar Cadastro de Produtos.
  * Gerenciar o Estoque do comércio.
  * Registrar os pedidos dos clientes.
  * Gerar Relatórios e Visões sobre o andamento do négocio.

<img src="Funcionalidades%20do%20Sistema.png" alt="Funcionalidades" width="600"/>

#

### Banco de Dados
O banco de dados foi projetado para refletir sobre as principais entidades e operações de um sistema de controle de estoque. Desta forma, ele permite:
  * Cadastrar e categorizar produtos;

  * Registrar pedidos de clientes;

  * Controlar a quantidade de cada item no estoque;

  * Monitorar vendas e gerar relatórios;

  * Ter rastreabilidade de quais produtos foram vendidos em cada pedido.

O modelo possui as respectivas tabelas:
  * **Produto** = Armazena as informações dos produtos cadastrados no sistema.
  * **Categoria** = Agrupa os produtos em categorias.
  * **Pedido** = Registra as informações gerais de uma venda/pedido.
  * **Item Pedido** = Relaciona produtos com pedidos, registrando o que foi vendido e quanto.
    
<img src="Diagrama%20Banco%20de%20Dados.png" alt="Diagrama BD" width="600"/>
