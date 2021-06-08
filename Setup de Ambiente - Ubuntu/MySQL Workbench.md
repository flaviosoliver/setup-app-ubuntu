# MySQL Workbench

Check: No
Editado: Jun 7, 2021 6:28 PM
Tag Descrição: Cliente para MySQL
Tag Método: Arquivo DEB/APT

### Preparação

1. Deve-se entrar no site do MySQL

    [MySQL :: Download MySQL Workbench](https://dev.mysql.com/downloads/workbench/)

2. Realizar o download da versão mais recente conforme seu sistema operacional

    ![MySQL%20Workbench/Untitled.png](MySQL%20Workbench/Untitled.png)

### Instalação

1. Se o seu sistema tiver suporte a instalação de pacote `DEB` por meio de um gerenciador, basta executar arquivo e mandar o Gerenciador instalar

    ![MySQL%20Workbench/Untitled%201.png](MySQL%20Workbench/Untitled%201.png)

- **Ou...**
    1. A instalação do `DEB` pode ser feito também pelo terminal

        Com o método `apt`, informando o local onde está salvo

        ```bash
        sudo apt install /home/nome/Downloads/mysql-workbench-community_8.0.24-1ubuntu21.04_amd64.deb
        ```

        Ou então, abrir a pasta no terminal e executar o comando dentro dela

        ```bash
        sudo apt install ./mysql-workbench-community_8.0.24-1ubuntu21.04_amd64.deb
        ```

        Ou com o método `dpkg`

        ```bash
        sudo dpkg -i mysql-workbench-community_8.0.24-1ubuntu21.04_amd64.deb
        ```

    - Caso apareçam problemas de ausência de dependências e não consiga instalar essas versões desejadas pelo pacote do Workbench

        ![MySQL%20Workbench/Untitled%202.png](MySQL%20Workbench/Untitled%202.png)

        Execute o comando

        ```bash
        sudo apt --fix-broken install
        ```

        **Caso ainda assim não consiga instalar, verifique a compatibilidade do pacote DEB com a versão do seu Ubuntu.**

- Se preferir, pode-se também optar pela versão Snap

    ```bash
    sudo snap install mysql-workbench-community
    ```

    Ao instalar via Snap, pode surgir um problema de permissão de acesso para o serviço do MySQL, que pode ser resolvido dando permissão ao aplicativo para gerenciar senhas e fazer uso de chaves SSH. Entre nas `Configurações do Sistema`, vá em na seção de `Aplicativos` e escolha o `MySQL Workbench`. Nas suas `Permissões & acesso`, autorize essas duas opções:

    ![MySQL%20Workbench/Untitled%203.png](MySQL%20Workbench/Untitled%203.png)

- Sistemas **não-baseados** em **Debian/Ubuntu** podem instalar o MySQL Workbench via `apt`

    ![MySQL%20Workbench/Untitled%204.png](MySQL%20Workbench/Untitled%204.png)

    1. Atualize a lista de repositórios

        ```bash
        sudo apt-get update
        ```

    2. Insira o comando

        ```bash
        sudo apt-get install mysql-workbench-community
        ```

### Personalização do Editor de Query ao estilo Monokay

![MySQL%20Workbench/Untitled%205.png](MySQL%20Workbench/Untitled%205.png)

1. Copie o arquivo `XML` de configuração do editor para um outro local, como exemplo, sua pasta `Documentos`. Seu nome é `code_editor.xml` e fica na pasta

    `/usr/share/mysql-workbench/data`

2. Abra essa cópia com o editor de texto da sua preferência
3. Agora, dentro da tag `<language name="SCLEX_MYSQL">`, localize o código da formatação atual, que pode ser que esteja mais ou menos na linha 50, verifique.

    ![MySQL%20Workbench/Untitled%206.png](MySQL%20Workbench/Untitled%206.png)

4. Selecione todo esse trecho de tags `<style />` de código, apague e em seu lugar insira

    ```xml
    <!-- Guia de cores
    dark-gray:         #282828;
    brown-gray:        #49483E;
    gray:              #888888;
    light-gray:        #CCCCCC;
    ghost-white:       #F8F8F0;
    light-ghost-white: #F8F8F2;
    yellow:            #E6DB74;
    blue:              #66D9EF;
    pink:              #F92672;
    purple:            #AE81FF;
    brown:             #75715E;
    orange:            #FD971F;
    light-orange:      #FFD569;
    green:             #A6E22E;
    sea-green:         #529B2F;
    -->

    <style id="32" fore-color-light="#DDDDDD" back-color-light="#282828" fore-color-dark="#DDDDDD" back-color-dark="#282828" bold="No" />   <!-- STYLE_DEFAULT       !BACKGROUND!   -->
    <style id="33" fore-color-light="#DDDDDD" back-color-light="#282828" fore-color-dark="#DDDDDD" back-color-dark="#282828" bold="No" />   <!-- STYLE_LINENUMBER                   -->
    <style id= "0" fore-color-light="#DDDDDD" back-color-light="#282828" fore-color-dark="#DDDDDD" back-color-dark="#282828" bold="No" />   <!-- SCE_MYSQL_DEFAULT                  -->

    <style id= "1" fore-color-light="#999999" back-color-light="#282828" fore-color-dark="#999999" back-color-dark="#282828" bold="No" />   <!-- SCE_MYSQL_COMMENT                  -->
    <style id= "2" fore-color-light="#999999" back-color-light="#282828" fore-color-dark="#999999" back-color-dark="#282828" bold="No" />   <!-- SCE_MYSQL_COMMENTLINE              -->
    <style id= "3" fore-color-light="#DDDDDD" back-color-light="#282828" fore-color-dark="#DDDDDD" back-color-dark="#282828" bold="No" />   <!-- SCE_MYSQL_VARIABLE                 -->
    <style id= "4" fore-color-light="#66D9EF" back-color-light="#282828" fore-color-dark="#66D9EF" back-color-dark="#282828" bold="No" />   <!-- SCE_MYSQL_SYSTEMVARIABLE           -->
    <style id= "5" fore-color-light="#66D9EF" back-color-light="#282828" fore-color-dark="#66D9EF" back-color-dark="#282828" bold="No" />   <!-- SCE_MYSQL_KNOWNSYSTEMVARIABLE      -->
    <style id= "6" fore-color-light="#AE81FF" back-color-light="#282828" fore-color-dark="#AE81FF" back-color-dark="#282828" bold="No" />   <!-- SCE_MYSQL_NUMBER                   -->
    <style id= "7" fore-color-light="#F92672" back-color-light="#282828" fore-color-dark="#F92672" back-color-dark="#282828" bold="No" />   <!-- SCE_MYSQL_MAJORKEYWORD             -->
    <style id= "8" fore-color-light="#F92672" back-color-light="#282828" fore-color-dark="#F92672" back-color-dark="#282828" bold="No" />   <!-- SCE_MYSQL_KEYWORD                  -->
    <style id= "9" fore-color-light="#9B859D" back-color-light="#282828" fore-color-dark="#9B859D" back-color-dark="#282828" bold="No" />   <!-- SCE_MYSQL_DATABASEOBJECT           -->
    <style id="10" fore-color-light="#DDDDDD" back-color-light="#282828" fore-color-dark="#DDDDDD" back-color-dark="#282828" bold="No" />   <!-- SCE_MYSQL_PROCEDUREKEYWORD         -->
    <style id="11" fore-color-light="#E6DB74" back-color-light="#282828" fore-color-dark="#E6DB74" back-color-dark="#282828" bold="No" />   <!-- SCE_MYSQL_STRING                   -->
    <style id="12" fore-color-light="#E6DB74" back-color-light="#282828" fore-color-dark="#E6DB74" back-color-dark="#282828" bold="No" />   <!-- SCE_MYSQL_SQSTRING                 -->
    <style id="13" fore-color-light="#E6DB74" back-color-light="#282828" fore-color-dark="#E6DB74" back-color-dark="#282828" bold="No" />   <!-- SCE_MYSQL_DQSTRING                 -->
    <style id="14" fore-color-light="#F92672" back-color-light="#282828" fore-color-dark="#F92672" back-color-dark="#282828" bold="No" />   <!-- SCE_MYSQL_OPERATOR                 -->
    <style id="15" fore-color-light="#9B859D" back-color-light="#282828" fore-color-dark="#9B859D" back-color-dark="#282828" bold="No" />   <!-- SCE_MYSQL_FUNCTION                 -->
    <style id="16" fore-color-light="#DDDDDD" back-color-light="#282828" fore-color-dark="#DDDDDD" back-color-dark="#282828" bold="No" />   <!-- SCE_MYSQL_IDENTIFIER               -->
    <style id="17" fore-color-light="#E6DB74" back-color-light="#282828" fore-color-dark="#E6DB74" back-color-dark="#282828" bold="No" />   <!-- SCE_MYSQL_QUOTEDIDENTIFIER         -->
    <style id="18" fore-color-light="#529B2F" back-color-light="#282828" fore-color-dark="#529B2F" back-color-dark="#282828" bold="No" />   <!-- SCE_MYSQL_USER1                    -->
    <style id="19" fore-color-light="#529B2F" back-color-light="#282828" fore-color-dark="#529B2F" back-color-dark="#282828" bold="No" />   <!-- SCE_MYSQL_USER2                    -->
    <style id="20" fore-color-light="#529B2F" back-color-light="#282828" fore-color-dark="#529B2F" back-color-dark="#282828" bold="No" />   <!-- SCE_MYSQL_USER3                    -->
    <style id="21" fore-color-light="#66D9EF" back-color-light="#49483E" fore-color-dark="#66D9EF" back-color-dark="#49483E" bold="No" />   <!-- SCE_MYSQL_HIDDENCOMMAND            -->
    <style id="22" fore-color-light="#909090" back-color-light="#49483E" fore-color-dark="#909090" back-color-dark="#49483E" bold="No" />   <!-- SCE_MYSQL_PLACEHOLDER              -->
    <!-- All styles again in their variant in a hidden command -->
    <style id="65" fore-color-light="#999999" back-color-light="#49483E" fore-color-dark="#999999" back-color-dark="#49483E" bold="No" />   <!-- SCE_MYSQL_COMMENT                  -->
    <style id="66" fore-color-light="#999999" back-color-light="#49483E" fore-color-dark="#999999" back-color-dark="#49483E" bold="No" />   <!-- SCE_MYSQL_COMMENTLINE              -->
    <style id="67" fore-color-light="#DDDDDD" back-color-light="#49483E" fore-color-dark="#DDDDDD" back-color-dark="#49483E" bold="No" />   <!-- SCE_MYSQL_VARIABLE                 -->
    <style id="68" fore-color-light="#66D9EF" back-color-light="#49483E" fore-color-dark="#66D9EF" back-color-dark="#49483E" bold="No" />   <!-- SCE_MYSQL_SYSTEMVARIABLE           -->
    <style id="69" fore-color-light="#66D9EF" back-color-light="#49483E" fore-color-dark="#66D9EF" back-color-dark="#49483E" bold="No" />   <!-- SCE_MYSQL_KNOWNSYSTEMVARIABLE      -->
    <style id="70" fore-color-light="#AE81FF" back-color-light="#49483E" fore-color-dark="#AE81FF" back-color-dark="#49483E" bold="No" />   <!-- SCE_MYSQL_NUMBER                   -->
    <style id="71" fore-color-light="#F92672" back-color-light="#49483E" fore-color-dark="#F92672" back-color-dark="#49483E" bold="No" />   <!-- SCE_MYSQL_MAJORKEYWORD             -->
    <style id="72" fore-color-light="#F92672" back-color-light="#49483E" fore-color-dark="#F92672" back-color-dark="#49483E" bold="No" />   <!-- SCE_MYSQL_KEYWORD                  -->
    <style id="73" fore-color-light="#9B859D" back-color-light="#49483E" fore-color-dark="#9B859D" back-color-dark="#49483E" bold="No" />   <!-- SCE_MYSQL_DATABASEOBJECT           -->
    <style id="74" fore-color-light="#DDDDDD" back-color-light="#49483E" fore-color-dark="#DDDDDD" back-color-dark="#49483E" bold="No" />   <!-- SCE_MYSQL_PROCEDUREKEYWORD         -->
    <style id="75" fore-color-light="#E6DB74" back-color-light="#49483E" fore-color-dark="#E6DB74" back-color-dark="#49483E" bold="No" />   <!-- SCE_MYSQL_STRING                   -->
    <style id="76" fore-color-light="#E6DB74" back-color-light="#49483E" fore-color-dark="#E6DB74" back-color-dark="#49483E" bold="No" />   <!-- SCE_MYSQL_SQSTRING                 -->
    <style id="77" fore-color-light="#E6DB74" back-color-light="#49483E" fore-color-dark="#E6DB74" back-color-dark="#49483E" bold="No" />   <!-- SCE_MYSQL_DQSTRING                 -->
    <style id="78" fore-color-light="#F92672" back-color-light="#49483E" fore-color-dark="#F92672" back-color-dark="#49483E" bold="No" />   <!-- SCE_MYSQL_OPERATOR                 -->
    <style id="79" fore-color-light="#9B859D" back-color-light="#49483E" fore-color-dark="#9B859D" back-color-dark="#49483E" bold="No" />   <!-- SCE_MYSQL_FUNCTION                 -->
    <style id="80" fore-color-light="#DDDDDD" back-color-light="#49483E" fore-color-dark="#DDDDDD" back-color-dark="#49483E" bold="No" />   <!-- SCE_MYSQL_IDENTIFIER               -->
    <style id="81" fore-color-light="#E6DB74" back-color-light="#49483E" fore-color-dark="#E6DB74" back-color-dark="#49483E" bold="No" />   <!-- SCE_MYSQL_QUOTEDIDENTIFIER         -->
    <style id="82" fore-color-light="#529B2F" back-color-light="#49483E" fore-color-dark="#529B2F" back-color-dark="#49483E" bold="No" />   <!-- SCE_MYSQL_USER1                    -->
    <style id="83" fore-color-light="#529B2F" back-color-light="#49483E" fore-color-dark="#529B2F" back-color-dark="#49483E" bold="No" />   <!-- SCE_MYSQL_USER2                    -->
    <style id="84" fore-color-light="#529B2F" back-color-light="#49483E" fore-color-dark="#529B2F" back-color-dark="#49483E" bold="No" />   <!-- SCE_MYSQL_USER3                    -->
    <style id="85" fore-color-light="#66D9EF" back-color-light="#888888" fore-color-dark="#66D9EF" back-color-dark="#888888" bold="No" />   <!-- SCE_MYSQL_HIDDENCOMMAND            -->
    <style id="86" fore-color-light="#AAAAAA" back-color-light="#888888" fore-color-dark="#AAAAAA" back-color-dark="#888888" bold="No" />   <!-- SCE_MYSQL_PLACEHOLDER              --
    ```

5. Salve o arquivo e abra essa pasta no terminal
6. Com o terminal setado para a pasta onde você salvou o arquivo, insira o comando

    ```bash
    sudo mv -b ./code_editor.xml /usr/share/mysql-workbench/data
    ```

    Onde aqui ele moverá o arquivo da pasta onde está para a pasta do MySQL Workbench, criando uma cópia de segurança do arquivo original, ficando assim

    ![MySQL%20Workbench/Untitled%207.png](MySQL%20Workbench/Untitled%207.png)

7. Ao abrir o Workbench no próximo uso, verá que o editor já se encontrará com a nova formatação

    **PS. A instalação via `Snap` não permite esse tipo de edição por configuração do sistema de arquivo, mesmo utilizando o usuário root, a proteção permanece.**