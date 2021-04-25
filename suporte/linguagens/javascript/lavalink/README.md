---
description: Aprenda a hospedar o seu BOT JavaScript com 1 servidor Lavalink na mesma instancia na Discloud
---

# Lavalink


## Como imcomperar o codigo
1. Baixar a codigo pelas [`Releases`](https://github.com/discloud/lavalink-nodejs/releases) ou [Clique Aqui](https://github.com/discloud/lavalink-nodejs/releases/latest/download/lavalink-nodejs.zip)
2. Depois de baixado, basta colocar o codigo do seu bot no diretório `bot`
3. No arquivo `config.json` no `fileRunBot` altere o nome do arquivo principal (no caso está `bot.js` mas se for outro nome (como por exemplo `index.js`) troque para o nome correto)
4. No seu codigo, área onde você conecta o Lavalink por favor coloque este dados:
    ```js
    {
        host: "localhost",
        port: 2333,
        password: "discloud"
    }
    ```

Depois de tudo feito e envie para a Discloud colocando `index.js` como Arquivo Principal