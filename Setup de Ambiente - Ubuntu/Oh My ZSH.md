# Oh My ZSH

Check: No
Editado: Jun 7, 2021 6:28 PM
Tag Descrição: Plugin para ZSH
Tag Método: Shell Script

### Documentação

[ohmyzsh/ohmyzsh](https://github.com/ohmyzsh/ohmyzsh/wiki)

### Instalação

1. Instalar usando o CURL

    ```bash
    sh -c "$(curl -fsSL [https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh](https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh))"
    ```

2. Para escolher o tema

    [ohmyzsh/ohmyzsh](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes)

3. Para inserir o tema escolhido, abrir o arquivo usando o editor integrado Nano `~/.zshrc`

    ```bash
    sudo nano ~/.zshrc
    ```

4. Colocar o nome do tema na tag `ZSH_THEME`

    Como exemplo: `ZSH_THEME="aussiegeek"`

    ![Oh%20My%20ZSH/Untitled.png](Oh%20My%20ZSH/Untitled.png)

    Salve o arquivo pelo teclado `CRTL O`

    Fechar Nano pelo teclado `CRTL X`

    ![Oh%20My%20ZSH/Untitled%201.png](Oh%20My%20ZSH/Untitled%201.png)

5.  Tem vários outros plugins, podem ser vistos aqui:

    [ohmyzsh/ohmyzsh](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins)

6. Para instalar os plugins deve-se primeiro instalar o ZInit

    ```bash
    sh -c "$(curl -fsSL [https://raw.githubusercontent.com/zdharma/zinit/master/doc/install.sh](https://raw.githubusercontent.com/zdharma/zinit/master/doc/install.sh))"
    ```

7. Após essa instalação, vamos abrir o arquivo `~/.zshrc` novamente ( `sudo nano ~/.zshrc` ) e abaixo da linha `### End of ZInit's installer chunk` que foi adicionada automaticamente no arquivo, adicionamos os seguintes plugins:

    ```
    zinit light zdharma/fast-syntax-highlighting
    zinit light zsh-users/zsh-autosuggestions
    zinit light zsh-users/zsh-completions
    ```

    - Descrição desses plugins:
        - `zdharma/fast-syntax-highlighting`
            - Adiciona syntax highlighting na hora da escrita de comandos que facilita principalmente em reconhecer comandos que foram digitados de forma incorreta;
        - `zsh-users/zsh-autosuggestions`
            - Sugere comandos baseados no histórico de execução conforme você vai digitando;
        - `zsh-users/zsh-completions`
            - Adiciona milhares de completitions para ferramentas comuns como Yarn, Homebrew, NVM, Node, etc, para você precisar apenas apertar TAB para completar comandos;

    Salve o arquivo pelo teclado `CRTL O`

    Fechar Nano pelo teclado `CRTL X`

    ![Oh%20My%20ZSH/Untitled%201.png](Oh%20My%20ZSH/Untitled%201.png)