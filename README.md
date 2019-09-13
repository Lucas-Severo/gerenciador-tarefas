# Gerenciador de Tarefas
Um gerenciador de tarefas feito utilizando a linguagem de programação Python e o framework Django

## Getting Started

### Requisitos

```
python3
Instalação das bibliotecas presentes no requirements.txt
MySql Server
```
### Instalando

 - Instalação do python3 pode ser feita através do download do executável no site:https://www.python.org/downloads/
 - As bibliotecas devem ser instaladas para permitir que a aplicação funcione com as bibliotecas necessárias, para isso execute o comando abaixo em seu ambiente:
     ```
    pip install -r requirements.txt ou
    pip3 install -r requirements.txt
    ```
1. O servidor Mysql pode ser instalado de duas formas:
    - Baixando o MySql Server https://dev.mysql.com/downloads/mysql/
    - Baixando uma ferramenta que possua o MySql como o Xampp, assim toda vez que for utiliza-lo deverá iniciar novamente o servidor
2. Após obtê-lo é necessário configurar o django, para que ele reconheça o servidor disponível:
    - Para isso abra o arquivo settings.py que fica dentro do projeto gerenciador_tarefas
    - Encontre a parte de configuração de database, e informe o usuário e senha, o host e a porta que o servidor está em execução
   ```python
    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.mysql',
            'NAME': 'nome da tabela',
            'USER': 'usuário',
            'PASSWORD': 'senha',
            'HOST': 'localhost',
            'PORT': '3306',
        }
    }
    ```
3. Com seu projeto configurado, agora é necessário criar as tabelas necessárias para o funcionamento do código, para isso o Django possui dois comandos que ajudam a migrar seu código presente no arquivo models.py, que irá fazer toda a configuração necessária para a criação da tabela do banco de dados
    ```
    python manage.py makemigrations
    python manage.py migrate
    ```

# Execução
Para executar o programa é necessário estar dentro do diretório gerenciador_tarefas e executar o comando no Terminal:

```bat
python manage.py runserver
```
Com isso, o servidor irá iniciar na rota padrão
```sh
http://127.0.0.1:8000/
```
