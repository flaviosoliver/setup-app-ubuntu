# Java

Check: No
Editado: Jun 7, 2021 6:28 PM
Tag Descrição: Plataforma Java
Tag Método: Arquivo TAR.GZ

### **Preparação**

Entre no site e faça o download do pacote `tar.gz`

[Download Java for Linux](https://www.java.com/pt-BR/download/)

![Java/Untitled.png](Java/Untitled.png)

### Instalação

1. Criar um diretório para instalar o JRE

    ```bash
    sudo mkdir /usr/local/java
    ```

2. Mova o pacote baixado para o diretório criado:

    ```bash
    sudo mv jre-8u291-linux-x64.tar.gz /usr/local/java
    ```

3. Entre no diretório:

    ```bash
    cd /usr/local/java
    ```

4. Descompacte o `tarball`:

    ```bash
    sudo tar zxvf jre-8u291-linux-x64.tar.gz
    ```

### Pós instalação

1. Após a instalação, pode apagar o pacote usado no processo para economizar espaço

    ```bash
    sudo rm jre-8u291-linux-x64.tar.gz
    ```

2. Setar para o sistema onde o JRE está instalado:

    ```bash
    sudo update-alternatives --install "/usr/bin/java" "java" "/usr/local/java/jre1.8.0_291/bin/java" 1
    ```

3. Para verificar a versão instalada

    ```bash
    java -version
    ```

    O retorno será semelhante a isso

    ```bash
    java version "1.8.0_291"
    Java(TM) SE Runtime Environment (build 1.8.0_291-b10)
    Java HotSpot(TM) 64-Bit Server VM (build 25.291-b10, mixed mode)
    ```