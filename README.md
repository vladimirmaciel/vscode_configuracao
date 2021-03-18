### Gerenciar dependências em ambientes python com pipenv

- para criar o amabiente virutal foi utilizado o Pipenv;

- Verificar se tem o pip instalado ;

  ```python
  $ pip -v
  ```

- Caso ainda não tenha, realizar o download do script com wget:

  ```python
  $ wget https://bootstrap.pypa.io/get-pip.py
  ```

- e por fim execute-o com através do python:

  ```python
   $ sudo python get-pip.py
  ```

- Verifique novamente se tudo deu certo:

  ```python
  $ pip -v
  ```

- Com o pip devidamente instalado em sua máquina, para instalar o pipenv basta executar:

  ```python
  $ pip install pipenv		
  ```

#### Criando o ambiente 

- O comando abaixo vai criar nosso Pipfile que é o arquivo responsável pelo gerenciamento dos pacotes e uma pasta oculta .env que será responsável por armazenar nosso ambiente do python na versão 3 que foi criado graças a flag --three, 

  ```python
  $ pipenv --three
  ```

#### Ativando nosso ambiente

- Antes de tudo, você precisa saber que para se trabalhar dentro do nosso virtualenv você não precisa necessáriamente ativá-lo. O pipenv disponibiliza um comando para se trabalhar com o virtualenv mesmo que não o tenha ativado, para isso esamos o run, sua sintaxe é a seguinte:

  ```python
  $ pipenv run <command>
  ```

- Se quisessemos listar as bibliotecas instaladas em nosso virtualenv antes mesmo de ativá-lo por exemplo:

  ```
  $ pipenv run pip freeze
  ```

- Teriamos uma saída parecida com essa:

  ```python
  flake8==3.9.0
  py==1.10.0
  pycodestyle==2.7.0
  pyflakes==2.3.0
  pylint==2.7.2
  pyparsing==2.4.7
  pytest==6.2.2
  ```

- Com as dependências devidamente instaladas e nosso ambiente criado, agora é hora de ativa-lo, para isso execute:

  ```python
  $ pipenv shell
  ```

- Por padrão o ambiente é nomeado com o nome da pasta onde o mesmo foi criado. Se tudo deu certo, ao executar o comando abaixo, será retornado alguma versão do python 3:

  ```
  (myproject)$ python --version
  ```

> Tutorial baseado no site https://medium.com/code-rocket-blog/gerenciando-suas-depend%C3%AAncias-e-ambientes-python-com-pipenv-9e5413513fa6