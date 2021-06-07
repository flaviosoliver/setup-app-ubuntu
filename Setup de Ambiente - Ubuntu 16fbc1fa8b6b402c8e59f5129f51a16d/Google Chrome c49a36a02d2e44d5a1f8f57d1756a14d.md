# Google Chrome

Check: No
Editado: Jun 7, 2021 6:28 PM
Tag Descrição: Navegador Web
Tag Método: Arquivo DEB

### Preparação

1. Para instalar o Navegador Web Google Chrome, acesse ao site para download

    [Navegador da Web Google Chrome](https://www.google.com/intl/pt-BR/chrome/)

2. Um arquivo `DEB` será baixado com a versão estável mais recente

### Instalação

1. Após o download concluído, acesse a pasta de destino e execute o arquivo, o Gerenciador de Programas será aberto e clique em instalar.

**Ou...**

1. A instalação do `DEB` pode ser feito também pelo terminal

    Com o método `apt`, informando o local onde está salvo

    ```bash
    sudo apt install /home/nome/Downloads/google-chrome-stable_current_amd64.deb
    ```

    Ou então, abrir a pasta no terminal e executar o comando dentro dela

    ```bash
    sudo apt install ./google-chrome-stable_current_amd64.deb
    ```

    Ou com o método `dpkg`

    ```bash
    sudo dpkg -i google-chrome-stable_current_amd64.deb
    ```