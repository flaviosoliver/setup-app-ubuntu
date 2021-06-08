# Chave SSH - GitHub

Check: No
Editado: Jun 7, 2021 6:28 PM
Tag Descrição: Chave SSH para Git
Tag Método: Shell Script

### **Criar Chave SSH**

1. Abrir terminal e inserir o comando, informando o seu usuário configurado no Git:

    ```bash
    ssh-keygen-t ed25519 -C "usuario@email.com.br"
    ```

    Caso seu sistema tenha incompatibilidade com o algoritmo **`Ed25519`**, use:

    ```bash
    ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
    ```

    Faça as adaptações das instruções a seguir para o algoritmo **`id_rsa` publico e privado**

2. O comando criará uma nova chave SSH, usando o e-mail fornecido como uma etiqueta.

    `Generating public/private ed25519 key pair.`

3. Quando aparecer a solicitação `Enter a file in which to save the key`, pressione `Enter`.

    O local padrão do arquivo será aceito. Se não quiser alterar, basta confirmar o padrão apertando o `Enter`

    `Enter a file in which to save the key (/home/nome/.ssh/id_ed25519):[Press enter]`

4. Digite a senha desejada. Caso não queira uma senha para essa chave SSH, não digitar nada e apenas teclar `Enter`

    `Enter passphrase (empty for no passphrase): [Type a passphrase]`

    `Enter same passphrase again: [Type passphrase again]`

### **Adicionar sua chave SSH ao ssh-agent**

1. Inicie o ssh-agent em segundo plano.

    ```bash
    eval "$(ssh-agent -s)"
    ```

    Será exibida uma mensagem tipo:

    `> Agent pid 59566`

2. Prossiga com os comandos

    ```bash
    sudo -s -H
    ```

    ```bash
    eval "$(ssh-agent -s)"
    ```

    Será exibida uma mensagem tipo:

    `> Agent pid 59566`

3. Adicione sua chave SSH privada ao ssh-agent. Se você criou sua chave com um nome diferente ou se você estiver adicionando uma chave existente com um nome diferente, substitua *`id_ed25519`* no comando pelo nome do seu arquivo de chave privada.

    ```bash
    ssh-add /home/nome/.ssh/id_ed25519
    ```

    Será exibida uma mensagem tipo:

    `Identity added: /home/nome/.ssh/id_ed25519 (usuario@email.com.br)`

### **Adicionar Chave SSH no GitHub**

1. Copie a chave pública SSH para a sua área de transferência. 
Se o seu arquivo de chave pública SSH tiver um nome diferente do código de exemplo, modifique o nome do arquivo para corresponder à sua configuração atual. Ao copiar sua chave, não adicione novas	linhas nem espaços em branco. **Observe a localização do arquivo da sua chave criado no item 3.**

    ```bash
    clip < /home/you/.ssh/id_ed25519.pub
    ```

    Dica: se `clip` não estiver funcionando, você poderá localizar a pasta `.ssh` oculta, abrir o arquivo no seu editor de texto de preferência e copiá-lo na área de transferência.

2. No canto superior direito de qualquer página, clique na sua foto de perfil e, em seguida, clique em Configurações.

    ![Chave%20SSH%20-%20GitHub/Untitled.png](Chave%20SSH%20-%20GitHub/Untitled.png)

3. Na barra lateral de configurações do usuário, clique em chaves SSH e GPG.

    ![Chave%20SSH%20-%20GitHub/Untitled%201.png](Chave%20SSH%20-%20GitHub/Untitled%201.png)

4. Clique em New SSH key (Nova chave SSH) ou Add SSH key (Adicionar chave SSH).

    ![Chave%20SSH%20-%20GitHub/Untitled%202.png](Chave%20SSH%20-%20GitHub/Untitled%202.png)

5. No campo "Title" (Título), adicione uma etiqueta descritiva para a nova chave. Por exemplo: "Chave Ubuntu".
6. Cole	sua chave no campo "Key" (Chave).

    ![Chave%20SSH%20-%20GitHub/Untitled%203.png](Chave%20SSH%20-%20GitHub/Untitled%203.png)

7. Clique em Add SSH key (Adicionar chave SSH).

    ![Chave%20SSH%20-%20GitHub/Untitled%204.png](Chave%20SSH%20-%20GitHub/Untitled%204.png)

8. Se solicitado, confirme sua senha do GitHub.

    ![Chave%20SSH%20-%20GitHub/Untitled%205.png](Chave%20SSH%20-%20GitHub/Untitled%205.png)