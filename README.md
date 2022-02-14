## Dashboard de Doenças (Flask)
Dashboard simples com informações sobre doenças, pacientes, estado de saúde dividido por Estados do Brasil e data.
Aplicação construída em um projeto da Digital Innovation One.

### Intro

Este app web foi feito utilizando um servidor local MySQL, mas é possível utilizar um banco de sua preferência. [MySQL]()e possuí as seguintes features:

- Cadastro de Usuário
- Cadastro de Pacientes
- Cadastro de Doenças
- Cadastro de Estados de Saúde
- Cadastro de Estados do Brasil
- Consumo de dados via Dashboard

**Principais** bibliotecas utilizadas:

- [Flask]() - Framework Python para desenvolvimento
- [SQLAlchemy]() - Async [MongoDB]() object-document mapper built on [PyDantic]()
- Demais bibliotecas serão encontradas diretamente no requirements.txr

### Setup

Código escrito para Python 3.10 ou inferior. Não esqueça da virtualenv. Os comandos `python` à baixo estão de acordo com Python3.


**Primeiro**, recomendo a instalação e configuração do servidor MySQL.
Após a instalação da ferramenta, basta criar uma conexão local (no geral, é instalada a ferramenta MySQL Workbench que permitirá essa configuração de forma fácil. Utilizaremos logo após)
Depois de criar a conexão local e acessá-la, você deve criar um "Schema" e nomeá-lo conforme achar melhor.

Após este passo, siga até `config.py`, na linha 17 preencha de acordo com o seu banco de dados, seguindo as orientações na linha.

Acesse `admin/Views.py` e comente todas as funções que possuam `inaccessible` em seu nome (isso permitirá acessar a rota [localhost:suaporta/admin/]() para que possa criar um usuário).
Após, basta descomentar a função para retornar tudo ao normal.

Seguindo, é necessário instalar as bibliotecas, utilize o comando à baixo.

```bash
python -m pip install -r requirements.txt
```

Como boa prática em Flask, você pode definir a ENV de desenvolvimento utilizando o seguinte comando:

```bash
$env:FLASK_ENV='development'
```



### Run

Para iniciar a aplicação

```bash
python run.py      
```



[MySQL]: https://www.mysql.com/downloads/ "MySQL downloads Page"
[Flask]: https://flask.palletsprojects.com/en/2.0.x/ "Flask web framework"
[SQLAlchemy]: https://docs.sqlalchemy.org/ "SQLAlchemy "