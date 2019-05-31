
## Pré-requisitos 

- docker
- docker-compose

## Iniciando ambiente e aplicação

**Build**

Dentro do diretório das aplicação, existe um arquivo chamado **Dockerfile**, este arquivo é responsável pela criação dos containers do app. 

**Execução**

O arquivo chamado `'docker-compose.yml'` na raiz do repositório, é utilizado para a criação do ambiente contendo:
- Aplicação em Python com Flask expondo na porta 8000.
- Aplicação em Go (Golang) expondo na porta 8080.
- Banco de dados Sqlite.

Execute o comando abaixo no repositório raiz:

```$docker-compose up -d .```

O mesmo iniciará o processo de build e execução da aplicação.


---
---
---
---
---
---
---
---
---
---
---


Aguarde alguns momentos até o termino das tarefas a serem executadas.

Após esse período, em seu browser acesse o ambiente utilizando a URL http://127.0.0.1:8000 .

