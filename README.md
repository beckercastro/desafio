## Exame - Bexs

### Linha de raciocínio

- Entendimento do ambiente.
- Rodar a aplicação localmente, para analisar as dependências.
- Criação do Dockerfile.
- Rodar as aplicações em container e configurar comunicação entre elas. 
- Criação do docker-compose.yml

### Requisitos 

- docker
- docker-compose

### Como entregar sua solução?

1) Clone do repositório

2) Realize as alterações necessárias para construção/automação da stack. Considere um ambiente local (máquina do desenvolvedor) ou algum provedor de cloud (AWS ou GCP).

### Iniciando ambiente e aplicação

**Build**

Dentro do diretório das aplicação, existe um arquivo chamado **Dockerfile**, este arquivo é responsável pela criação dos containers do app. 

**Como iniciar**

O arquivo chamado `'docker-compose.yml'` na raiz do repositório, é utilizado para a criação do ambiente contendo:
- Aplicação em Python com Flask expondo na porta 8000.
- Aplicação em Go (Golang) expondo na porta 8080.
- Banco de dados Sqlite.

Execute o comando abaixo no repositório raiz:

```$docker-compose up -d .```

O mesmo iniciará o processo de build e execução da aplicação.

Aguarde alguns momentos até o termino das tarefas a serem executadas.

Após esse período, em seu browser acesse o ambiente utilizando a URL http://127.0.0.1:8000 

### Considerações para os desenvolvedores

```mermaid
graph LR
A[Frontend] -- request -->B((Backend))
B -- response --> A 
B -- request --> C{SQLlite}
C --response --> B
```

- Aplicação Frontend - Aplicação em Python com Flask expondo na porta 8000 um formulário de criação de usuário contendo os campos ID e Name que realiza uma chamada Post com tais dados para a aplicação Backend.
- Aplicação Backend - Aplicação em Go (Golang) expondo na porta 8080 o CRUD de Usuários e armazena em um banco Sqlite3 local.
