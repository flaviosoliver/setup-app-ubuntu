# Insomnia Rest

Check: No
Editado: Jun 7, 2021 6:28 PM
Tag Descrição: Cliente REST API
Tag Método: Arquivo DEB/APT

### Preparação

1. Acesse ao site do Insomnia Rest e faça o download do pacote `DEB`

    [Download](https://insomnia.rest/download)

### Instalação

1. Após ter baixado o arquivo, vá até a pasta onde está armazenado e execute.

    Se o seu sistema tiver suporte a instalação de pacote `DEB` por meio de um gerenciador, basta executar arquivo e mandar o Gerenciador instalar

    ![Insomnia%20Rest%200afabee19e9e48dc99008aec110ac996/Untitled.png](Insomnia%20Rest%200afabee19e9e48dc99008aec110ac996/Untitled.png)

**Ou...**

1. A instalação do `DEB` pode ser feito também pelo terminal

    Com o método `apt`, informando o local onde está salvo

    ```bash
    sudo apt install /home/nome/Downloads/Insomnia.Core-2021.3.0.deb
    ```

    Ou então, abrir a pasta no terminal e executar o comando dentro dela

    ```bash
    sudo apt install ./Insomnia.Core-2021.3.0.deb
    ```

    Ou com o método `dpkg`

    ```bash
    sudo dpkg -i Insomnia.Core-2021.3.0.deb
    ```

- Ou...
    1. Pode fazer a requisição do pacote pelo terminal

        ```bash
        echo "deb [trusted=yes arch=amd64] https://download.konghq.com/insomnia-ubuntu/ default all" \
            | sudo tee -a /etc/apt/sources.list.d/insomnia.list
        ```

    2. Atualize a lista de pacote

        ```bash
        sudo apt-get update
        ```

    3. Instale o Insomnia

        ```bash
        sudo apt-get install insomnia
        ```