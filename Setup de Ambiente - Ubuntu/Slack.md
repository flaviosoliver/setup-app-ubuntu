# Slack

Check: No
Editado: Jun 7, 2021 6:28 PM
Tag Descrição: Ferramenta de Comunicação
Tag Método: Arquivo DEB

### Preparação

1. Para instalar o Slack, acesse ao site para download

    [Linux | Downloads](https://slack.com/intl/pt-br/downloads/linux)

2. Escolha o seu Sistema Operacional e a arquitetura

    ![Slack/Untitled.png](Slack/Untitled.png)

3. Um arquivo `DEB` será baixado com a versão estável mais recente

### Instalação

1. Após o download concluído, acesse a pasta de destino e execute o arquivo, o Gerenciador de Programas será aberto e clique em instalar.

**Ou...**

1. A instalação do `DEB` pode ser feito também pelo terminal

    Com o método `apt`, informando o local onde está salvo

    ```bash
    sudo apt install /home/nome/Downloads/slack-desktop-4.16.0-amd64.deb
    ```

    Ou então, abrir a pasta no terminal e executar o comando dentro dela

    ```bash
    sudo apt install ./slack-desktop-4.16.0-amd64.deb
    ```

    Ou com o método `dpkg`

    ```bash
    sudo dpkg -i slack-desktop-4.16.0-amd64.deb
    ```