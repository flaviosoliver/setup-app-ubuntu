# ZSH

Check: No
Editado: Jun 7, 2021 6:28 PM
Tag Descrição: Terminal Shell
Tag Método: APT

### Instalação

1. Abrir o terminal

    ```bash
    sudo apt install zsh
    ```

2. Verificar versão instalada

    ```bash
    zsh --version
    ```

3. Tornar o ZSH padrão do shell

    ```bash
    sudo chsh -s $(which zsh)
    ```

4. Para o sistema reconhecer o ZSH como padrão, fazer logoff no usuário do sistema
5. Para verificar o shell padrão configurado:

    ```bash
    echo $SHELL
    ```

    Resultado esperado: `/bin/zsh`

6. Pode verificar também com

    ```bash
    $SHELL --version
    ```

    Resultado esperado: `zsh 5.4.2` ou mais recente