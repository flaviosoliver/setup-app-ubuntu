# Node.JS

Check: No
Editado: Jun 7, 2021 6:27 PM
Tag Descrição: Desenvolvimento JavaScript
Tag Método: APT

### Instalar Node.js v16.x:

1. Instalar Node no Ubuntu:

    ```bash
    curl -fsSL [https://deb.nodesource.com/setup_16.x](https://deb.nodesource.com/setup_16.x) | sudo -E bash -
    sudo apt-get install -y nodejs
    ```

2. Caso o comando CURL ainda não esteja instalado no sistema. 

    ```bash
    sudo apt-get install curl
    ```

    Após instalar o CURL, repita o primeiro comando para enfim instalar o Node.JS

3. Verificar versão instalada:

    ```bash
    node -v
    ```

[nodesource/distributions](https://github.com/nodesource/distributions/blob/master/README.md)