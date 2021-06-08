# MongoDB Compass

Check: No
Editado: Jun 7, 2021 6:28 PM
Tag Descrição: Cliente para MongoDB
Tag Método: Arquivo DEB

1. Acessar a página de Download e baixar o arquivo DEB

    [MongoDB Compass Download](https://www.mongodb.com/try/download/compass)

    ![MongoDB%20Compass/Untitled.png](MongoDB%20Compass/Untitled.png)

2. Se o seu sistema tiver suporte a instalação de pacote DEB por meio de um gerenciador, basta executar arquivo e mandar o Gerenciador instalar

    ![MongoDB%20Compass/Untitled%201.png](MongoDB%20Compass/Untitled%201.png)

- **Ou...**
    1. A instalação do `DEB` pode ser feito também pelo terminal

        Com o método `apt`, informando o local onde está salvo

        ```bash
        sudo apt install /home/nome/Downloads/mongodb-compass_1.26.1_amd64.deb
        ```

        Ou então, abrir a pasta no terminal e executar o comando dentro dela

        ```bash
        sudo apt install ./mongodb-compass_1.26.1_amd64.deb
        ```

        Ou com o método `dpkg`

        ```bash
        sudo dpkg -i mongodb-compass_1.26.1_amd64.deb
        ```

- Pode também realizar download do arquivo `DEB` com o método `wget`
    1. Download MongoDB Compass

        ```bash
        wget https://downloads.mongodb.com/compass/mongodb-compass_1.26.1_amd64.deb
        ```