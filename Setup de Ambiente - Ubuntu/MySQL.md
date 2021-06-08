# MySQL

Check: No
Editado: Jun 7, 2021 6:28 PM
Tag Descrição: Banco de Dados SQL
Tag Método: APT

### Instalação

1. Atualize a lista de pacotes

    ```bash
    sudo apt update
    ```

2. Insira o comando

    ```bash
    sudo apt install mysql-server
    ```

3. Para verificar a instalação e Status do Serviço:

    ```bash
    sudo systemctl status mysql
    ```

    Ou

    ```bash
    sudo service mysql status
    ```

4. Iniciar Serviço

    ```bash
    sudo systemctl start mysql
    ```

    Ou

    ```bash
    sudo service mysql start
    ```

5. Parar Serviço

    ```bash
    sudo systemctl start mysql
    ```

    Ou

    ```bash
    sudo service mysql stop
    ```

6. Para que o MySQL não inicialize junto com o Sistema Operacional (Economiza memória de processamento enquanto o Banco não estiver sendo utilizado)

    ```bash
    sudo systemctl disable mysql
    ```

7. Adicionar a inicialização do MySQL junto com Sistema Operacional

    ```bash
    sudo systemctl enable mysql
    ```

8. Inserir senha no usuário `root`

    Acesse o usuário `root` do MySQL

    ```bash
    sudo mysql -u root -p
    ```

    Agora para definir uma senha, onde está a informação `senha-aqui` escreva a senha que deseja para o usuário. 

    **ATENÇÃO!**

    Guarde essa senha, pois ela é o `root` do Banco de Dados, para realizar conexão ao MySQL, daqui pra frente, você sempre precisará dela

    ```bash
    ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'senha-aqui'; flush privileges;
    ```