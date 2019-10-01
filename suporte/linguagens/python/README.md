---
description: Aprenda a hospedar seu bot em Python na DisCloud
---

# Python

## Arquivos principais:

* Arquivo a ser executado, é o arquivo principal do seu bot, ou seja, o local onde está o bot.run\(\). GERALMENTE é `main.py`.   
* `requirements.txt`.

  Quaisquer outros arquivos sem ser esses dois podem ser adicionados, e você pode usa-los no código do seu Bot.\(Isso vale para as cogs também\).

### Requirements:

O `requirements.txt` deve conter as bíbliotecas usadas no seu bot, por padrão, deve no mínimo conter a livraria `discord.py`, caso use a livraria `disco-py` basta substituir.

IMPORTANTE!

* As bibliotecas **NÃO SÃO as que você importa**, e sim as que você instala.

  Ex.: `import PIL` mas você instala usando `pip install pillow`, logo deve ser colocado **pillow** e não **PIL**.

Como criar o requirements.txt:

{% page-ref page="exemplo-do-requirements.txt.md" %}

## Preparando seu Bot para enviar para a Discloud

• Faça um **`.zip`** com os arquivos.

![Exemplo no Windows](../../../.gitbook/assets/image%20%2811%29.png)

{% page-ref page="../../../faq/como-compactar-zipar-os-meus-arquivos.md" %}

### Escolha o método para hospedar seu Bot para a Discloud:

{% page-ref page="../../como-hospedar/website.md" %}

{% page-ref page="../../como-hospedar/discord.md" %}

