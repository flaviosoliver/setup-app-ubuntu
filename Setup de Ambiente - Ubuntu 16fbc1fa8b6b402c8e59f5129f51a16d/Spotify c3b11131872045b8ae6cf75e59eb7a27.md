# Spotify

Check: No
Editado: Jun 7, 2021 6:28 PM
Tag Descrição: Cliente Spotify
Tag Método: Arquivo DEB ou CURL/APT

### Instalação

1. Realize a requisição do pacote de instalação pelo método `CURL`

    ```bash
    curl -sS https://download.spotify.com/debian/pubkey_0D811D58.gpg | sudo apt-key add -
    echo "deb http://repository.spotify.com stable non-free" | sudo tee /etc/apt/sources.list.d/spotify.list
    ```

2. Atualize a lista de pacotes

```bash
sudo apt-get update
```

3. Instale o pacote

```bash
sudo apt-get install spotify-client
```