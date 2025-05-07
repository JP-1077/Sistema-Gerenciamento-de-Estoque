# 📋 Diário de Desenvolvimento 

## 1. Preparação do Ambiente ⛏️

**Objetivo:**  
Configurar o ambiente de desenvolvimento com todas as ferramentas necessárias para iniciar o projeto de forma estruturada, garantindo produtividade e organização desde o início.

**Ações Realizadas:**
- Instalação do Python e criação de um ambiente virtual com `venv` para isolar dependências do projeto.
- Instalação do framework Django, principal tecnologia utilizada no back-end.
- Inicialização de repositório Git para controle de versão e versionamento contínuo.
- Escolha do editor de código VS Code com plugins úteis para Python e Django.
- Definição do banco de dados SQLite, por ser leve e ideal para desenvolvimento local.
- Execução do comando `django-admin startproject` para criar a estrutura básica da aplicação.

**Resultado:**  
Ambiente de desenvolvimento funcional e preparado, com dependências instaladas, repositório criado e estrutura inicial do projeto pronta para o desenvolvimento das funcionalidades.

---

## 2. Estrutura Inicial e Configuração ⚙️

**Objetivo:**  
Construir a estrutura inicial da aplicação Django, definindo configurações essenciais, rotas e componentes visuais para facilitar a evolução do sistema.

**Ações Realizadas:**
- Criação do aplicativo principal com `python manage.py startapp sistema`.
- Configuração do `settings.py` com idioma (`pt-br`), timezone (`America/Sao_Paulo`), templates e arquivos estáticos.
- Definição das rotas principais no `urls.py` para controle das páginas da aplicação.
- Integração do Bootstrap 5 via CDN.
- Criação do primeiro template base (`base.html`) com estrutura modular reutilizável.

**Resultado:**  
Sistema inicial com layout estruturado, rotas configuradas e base sólida para implementação das funcionalidades. A aplicação já podia ser acessada localmente com uma interface inicial e organização modular de arquivos.

---

## 3. Modelagem de Dados 📐

**Objetivo:**  
Desenhar a estrutura de dados da aplicação com foco em refletir as entidades do mundo real e permitir operações eficientes de controle de pedidos e estoque.

**Ações Realizadas:**
- Criação dos modelos `Produto`, `Cliente`, `Pedido` e `ItemPedido` no `models.py`, com os campos e relações adequados.
- Definição de chaves estrangeiras (`ForeignKey`) para garantir integridade entre tabelas.
- Implementação de campos específicos como `DecimalField` para valores monetários e `IntegerField` para quantidades.
- Execução dos comandos `makemigrations` e `migrate`.
- Registro dos modelos no Django Admin.

**Resultado:**  
Estrutura de dados robusta e funcional, permitindo registrar clientes, produtos, pedidos e seus itens com consistência e eficiência. A modelagem serviu de base para os relacionamentos e funcionalidades futuras do sistema.

---

## 4. Criando as Views ✍🏽

**Objetivo:**  
Implementar a camada de controle da aplicação, responsável por processar as requisições do usuário, aplicar regras de negócio e repassar as informações corretas para os templates.

**Ações Realizadas:**  
Foram criadas diversas *Function-Based Views* (FBV), permitindo controle direto e estruturado sobre cada fluxo de navegação do sistema.

### Principais Views:

- **`home_view`**
  - Tela inicial do sistema com visão geral e links rápidos.

- **`dashboard_view`**
  - Exibe métricas e indicadores como:
    - Produtos com estoque baixo
    - Produtos mais vendidos
    - Principais clientes
    - Produtos em estoque
  - Utiliza `Sum()` e `F()` com o ORM para gerar dados em tempo real.

- **`produtos_view` (CRUD de produtos)**
  - Visualizar, adicionar, editar e remover produtos.
  - Valida campos obrigatórios e controla estoque mínimo.

- **`pedidos_view` (CRUD de pedidos)**
  - Cadastra e lista pedidos.
  - Atualiza o estoque automaticamente.
  - Integra dados de clientes e produtos.

**Resultado:**  
Sistema dinâmico com experiência fluida. O uso do ORM e boas práticas de separação de responsabilidades garantiram clareza e base sólida para futuras evoluções.

---

## 5. Dashboard 📊

**Objetivo:**  
Oferecer ao usuário uma visão clara e objetiva sobre os dados do sistema, facilitando o monitoramento e a tomada de decisões.

### Visões Apresentadas:
- Produtos com estoque abaixo do mínimo.
- Produtos mais vendidos.
- Principais clientes por valor gasto.
- Produtos armazenados no estoque.

### Etapas do Desenvolvimento:
- Criação da `dashboard_view` utilizando ORM.
- Consultas desenvolvidas para:
  - Estoque baixo
  - Produtos mais vendidos
  - Principais clientes
  - Produtos armazenados
- Criação do template `dashboard.html` com HTML, CSS e Bootstrap.

**Resultado:**  
Dashboard funcional e intuitivo, com informações visuais claras e acessíveis sobre o desempenho e status do estoque e vendas.

---

## 6. Front-End 💻

**Objetivo:**  
Construir a interface visual do sistema com foco em usabilidade, responsividade e acessibilidade.

### Atividades Realizadas:
- **Prototipagem no Figma**:
  - Tela inicial, Produtos, Pedidos e Dashboard.

- **Implementação com HTML, CSS e Bootstrap**:
  - HTML5 para estrutura semântica.
  - CSS3 personalizado para estilos únicos.
  - Bootstrap para responsividade e componentes prontos.

**Resultado:**  
Sistema com identidade visual clara e funcional. Navegação simples, agradável e focada no usuário final.

---

## 7. Testes 🧐

**Objetivo:**  
Garantir que todas as funcionalidades do sistema funcionem corretamente de forma integrada.

### Tipos de Testes Aplicados:

- 🧩 **Testes de Integração**
  - Verificam interações entre módulos (ex: atualização de estoque ao registrar pedido).

- 🧪 **Testes de Sistema (End-to-End)**
  - Simulam o uso completo por um usuário.
  - Ex: adicionar produto → fazer pedido → consultar no dashboard.

- 🔁 **Testes de Regressão**
  - Garantem que funcionalidades antigas não foram afetadas por mudanças recentes.

### Metodologia:
- Comparação entre comportamentos esperados e reais.
- Correção ágil de bugs.
- Ciclos curtos de testes e validação.

**Resultado:**  
Todos os fluxos principais validados com sucesso. Inconsistências corrigidas rapidamente, garantindo estabilidade e confiabilidade da aplicação.

---
