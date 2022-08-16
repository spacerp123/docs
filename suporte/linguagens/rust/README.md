# 🦀 Rust

## :file\_folder: Arquivos

```diff
Arquivos Mínimos Necessários
+ Arquivo Cargo.toml
+ Pasta src
+ Arquivo rust-toolchain.toml ou rust-toolchain (se existir)
+ Outros (Se o seu projeto depender de outros arquivos ou pastas deve incluir)
Arquivos desnecessários:
- Arquivo Cargo.lock
- Pasta target
- Pasta .git
```

{% content-ref url="criar-package.json.md" %}
[criar-package.json.md](criar-package.json.md)
{% endcontent-ref %}

## :compression: Compactando os arquivos

![](../../../.gitbook/assets/zip-botrs.png)

Para mais detalhes sobre como **Compactar os seus Arquivos** de acordo com o seu **Sistema Operativo**, pode consultar em baixo:

{% content-ref url="../../faq/zip.md" %}
[zip.md](../../faq/zip.md)
{% endcontent-ref %}

## ✍ Hospedando o seu bot

{% hint style="info" %}
Escolha o método para hospedar seu Bot na Discloud:
{% endhint %}

{% content-ref url="../../hospedar/sites/via-painel-controle.md" %}
[via-painel-controle.md](../../hospedar/sites/via-painel-controle.md)
{% endcontent-ref %}

{% content-ref url="../../hospedar/bots/discord.md" %}
[discord.md](../../hospedar/bots/discord.md)
{% endcontent-ref %}

## :earth\_americas: Hospedando o Seu Site

{% hint style="info" %}
Esta funcionalidade necessita de alguns requisitos básicos para poder ser utilizada, por favor consulte os requisitos [aqui](../../hospedar/sites/#requisitos) antes de continuar
{% endhint %}

### Utilizando o `Rocket`

**Rocket** é um framework web feito em rust, atualmente funciona apenas na versão nightly do rust

```shell
rustup override set nightly
```

### Instalando o `Rocket`

Consulte a documentação oficial: [https://rocket.rs/](https://rocket.rs/)

### Configurando `Rocket` para a DisCloud

Crie um arquivo `rust-toolchain.toml`:

{% code title="rust-toolchain.toml" %}
```toml
[toolchain]
channel = "nightly"
```
{% endcode %}

Isso irá instruir o `rustup` a usar a versão `nightly`, e baixar essa versão caso seja necessário.

#### Exemplo `discloud.config` para `Rocket`

{% code title="discloud.config" %}
```typescript
ID=subdomino
TYPE=site
MAIN=src/main.rs
RAM=512
AUTORESTART=false
VERSION=latest
APT=tools
```
{% endcode %}
