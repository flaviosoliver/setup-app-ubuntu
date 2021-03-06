# Zoom

Check: No
Editado: Jun 7, 2021 6:28 PM
Tag Descrição: Cliente de Reuniões Virtuais
Tag Método: Arquivo DEB

### Preparação

1. Para instalar o Zoom, acesse ao site para download

    [Video Conferencing, Web Conferencing, Webinars, Screen Sharing](https://zoom.us/download)

2. Escolha o seu Sistema Operacional e a arquitetura

    ![Zoom/Untitled.png](Zoom/Untitled.png)

3. Um arquivo `DEB` será baixado com a versão estável mais recente

### Instalação

1. Após o download concluído, acesse a pasta de destino e execute o arquivo, o Gerenciador de Programas será aberto e clique em instalar.

**Ou...**

1. A instalação do `DEB` pode ser feito também pelo terminal

    Com o método `apt`, informando o local onde está salvo

    ```bash
    sudo apt install /home/nome/Downloads/zoom_amd64.deb
    ```

    Ou então, abrir a pasta no terminal e executar o comando dentro dela

    ```bash
    sudo apt install ./zoom_amd64.deb
    ```

    Ou com o método `dpkg`

    ```bash
    sudo dpkg -i zoom_amd64.deb
    ```