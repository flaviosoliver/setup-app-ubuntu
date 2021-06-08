# LibreOffice

Check: No
Editado: Jun 7, 2021 6:28 PM
Tag Descrição: Pacote de Escritório
Tag Método: APT

**Antes da instalação, verificar se existe a versão que é instalada junto com o sistema operacional. Caso exista e prefira essa versão que não é via Snap, remova antes de prosseguir para instalação.**

### Instalação

1. Se ainda não tiver, adicione o repositório do programa com este comando:

    ```bash
    sudo add-apt-repository -y ppa:libreoffice/ppa
    ```

2. Atualize o gerenciador de pacotes com o comando:

    ```bash
    sudo apt update
    ```

3. Agora use o comando abaixo para instalar o programa

    ```bash
    sudo apt-get install libreoffice
    ```

4. Melhorias na parte visual

    ```bash
    sudo apt install libreoffice-gtk2 libreoffice-gtk3
    ```

- Caso seja necessário, desinstale o programa, usando os comandos abaixo

    ```bash
    sudo add-apt-repository ppa:libreoffice/ppa -r -y
    ```

    ```bash
    sudo apt-get remove libreoffice
    ```

    ```bash
    sudo apt-get autoremove
    ```