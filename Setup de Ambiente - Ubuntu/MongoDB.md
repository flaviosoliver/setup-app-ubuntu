# MongoDB

Check: No
Editado: Jun 7, 2021 6:28 PM
Tag Descrição: Banco de Dados NoSQL
Tag Método: WGET/APT

### Instalação

1. Importando a chave pública utilizada pelo gerenciamento de pacotes

    ```bash
    wget -qO - https://www.mongodb.org/static/pgp/server-4.4.asc | sudo apt-key add -
    ```

    Este comando deve retornar um **OK** .

2. Porém, se você receber um erro indicando que `gnupg` não está instalado, faça como abaixo:

    Instalar o `gnupg` e as bibliotecas necessárias através do comando:

    ```bash
    sudo apt-get install gnupg
    ```

3. Após a instalação, tente importar a chave outra vez:

    ```bash
    wget -qO - https://www.mongodb.org/static/pgp/server-4.4.asc | sudo apt-key add -
    ```

4. Criar o arquivo de lista

    ```bash
    echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/4.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.4.list
    ```

5. Atualize a lista de repositórios

    ```bash
    sudo apt-get update
    ```

6. Instalar o MongoDB

    ```bash
    sudo apt-get install -y mongodb-org
    ```

7. Para verificar a instalação e Status do Serviço:

    ```bash
    sudo systemctl status mongod
    ```

    Ou

    ```bash
    sudo service mongod status
    ```

8. Iniciar Serviço

    ```bash
    sudo systemctl start mongod
    ```

    Ou

    ```bash
    sudo service mongod start
    ```

9. Parar Serviço

    ```bash
    sudo systemctl stop mongod
    ```

    Ou

    ```bash
    sudo service mongod stop
    ```

10. Reiniciar MongoDB

    ```bash
    sudo systemctl restart mongod
    ```

    Ou

    ```bash
    sudo service mongod restart
    ```

11. Para que o MySQL não inicialize junto com o Sistema Operacional (Economiza memória de processamento enquanto o Banco não estiver sendo utilizado)

    ```bash
    sudo systemctl disable mongod
    ```

12. Adicionar a inicialização do MySQL junto com Sistema Operacional

    ```bash
    sudo systemctl enable mongod
    ```