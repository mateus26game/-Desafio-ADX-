# Sistema Administrativo de Cadastro e Gerenciamento de Filmes

## 📖 Descrição
Este projeto é um sistema administrativo criado para realizar o **cadastro e gerenciamento de filmes**. Ele foi desenvolvido como parte de um processo seletivo e permite que o usuário gerencie informações de filmes no banco de dados, utilizando operações básicas como:

- **Criar** novos registros de filmes;
- **Visualizar** todos os filmes cadastrados;
- **Atualizar** informações de filmes já existentes;
- **Deletar** filmes do banco de dados.

---

## 🚀 Funcionalidades Principais
1. **Cadastro de Filmes:** Permite inserir filmes com informações como título, gênero, ano, diretor e classificação.
2. **Listagem de Filmes:** Exibe todos os filmes cadastrados em formato organizado.
3. **Atualização de Filmes:** Modifica detalhes de um filme específico.
4. **Remoção de Filmes:** Exclui filmes indesejados do sistema.
5. **Filtros e Pesquisa:** Busca filmes por critérios como gênero, ano de lançamento e mais.

---

## 🛠️ Tecnologias Utilizadas
Este projeto utiliza tecnologias modernas e robustas para garantir a funcionalidade e facilidade de manutenção:

- **Java**: Linguagem principal para a lógica do sistema.
- **Spring Boot**: Framework usado para simplificar o desenvolvimento da aplicação back-end.
- **Banco de Dados**: MySQL (ou outro banco relacional configurável no projeto).
- **Maven**: Gerenciador de dependências e build da aplicação.
- **Postman**: Para testes das rotas (opcional).
- **bootstrap 5**: Para testes web.
---

## 📋 Pré-requisitos
Antes de executar o sistema, você precisará ter as seguintes ferramentas instaladas em seu ambiente:

1. **Java**: Versão 11 ou superior.
2. **MySQL**: Para o banco de dados.
3. **Maven**: Para gerenciar e compilar o projeto.
4. **IDE**: IntelliJ IDEA, Eclipse ou outra de sua preferência.


---
---

## 💻 Projeto em Execução

Projeto rodando com integração ao banco de dados e funcionalidade no site.

---



https://github.com/user-attachments/assets/f5221b62-5576-4c59-86cf-2311296fa705





## ⚙️ Configuração do Ambiente
Siga os passos abaixo para configurar e executar o projeto no seu ambiente local:

### 1. Clone o Repositório
Clone este repositório em sua máquina usando o comando:
```bash
git clone https://github.com/seu-usuario/sistema-filmes.git
```
---


---

## 🛠️ Configurando o pgAdmin

Caso você esteja utilizando o **PostgreSQL** como banco de dados, será necessário configurar o **pgAdmin** para gerenciar e visualizar os dados. Siga os passos abaixo:

### 1. Instale o PostgreSQL e o pgAdmin
- Baixe e instale o **PostgreSQL** (versão 13 ou superior) e o **pgAdmin** no [site oficial do PostgreSQL](https://www.postgresql.org/download/).

### 2. Configure o Banco de Dados no PostgreSQL
- Após a instalação, acesse o **pgAdmin**.
- No menu lateral esquerdo, clique com o botão direito em **Servers** e selecione **Create > Server...**.
- Preencha os campos necessários:
  - **General**:
    - **Name**: Insira um nome para o servidor (exemplo: `ServidorLocal`).
  - **Connection**:
    - **Host name/address**: `localhost`
    - **Port**: `5432` (porta padrão do PostgreSQL)
    - **Maintenance database**: `postgres`
    - **Username**: Seu usuário PostgreSQL (exemplo: `postgres`)
    - **Password**: Sua senha definida na instalação.

Clique em **Save** para finalizar.

### 3. Crie o Banco de Dados para o Sistema
- Dentro do **pgAdmin**, no painel lateral esquerdo, clique com o botão direito em **Databases** e selecione **Create > Database...**.
- No campo **Database Name**, insira o nome do banco de dados que será usado no projeto (exemplo: `sistema_filmes`).
- Em **Owner**, selecione seu usuário PostgreSQL.
- Clique em **Save**.

### 4. Configure o Arquivo `application.properties`
No arquivo de configuração da aplicação (localizado em `src/main/resources/application.properties`), insira as credenciais do banco de dados PostgreSQL. Um exemplo de configuração para PostgreSQL seria:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/sistema_filmes
spring.datasource.username=postgres
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=update
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect
