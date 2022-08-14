---
description: Aprenda a hospedar o seu bot
---
# :crab: Rust
## Arquivos necessários
```diff
Arquivos Mínimos Necessários
+ Cargo.toml
+ src
+ rust-toolchain.toml ou rust-toolchain (se existir)
+ Outros arquivos usados na aplicação
Arquivos desnecessários:
- Cargo.lock
- target
- .git
```

## ✍ Hospedando o seu bot

{% hint style="info" %}
Escolha o método para hospedar seu Bot na Discloud:
{% endhint %}

{% content-ref url="../../hospedar/bots/via-painel-controle.md" %}
[via-painel-controle.md](../../hospedar/bots/via-painel-controle.md)
{% endcontent-ref %}

{% content-ref url="../../hospedar/bots/discord.md" %}
[discord.md](../../hospedar/bots/discord.md)
{% endcontent-ref %}

## :earth\_americas: Hospedando o Seu Site

{% hint style="info" %}
Esta funcionalidade necessita de alguns requisitos básicos para poder ser utilizada, por favor consulte os requisitos [aqui](../../hospedar/sites/#requisitos) antes de continuar
{% endhint %}
### Utilizando o Rocket
Rocket é um framework web feito em rust, atualmente funciona apenas na versão nightly do rust
```
rustup override set nightly
```
### Instalando o Rocket
Consulte a documentação oficial: https://rocket.rs/
### Configurando Rocket para a discloud
Crie um arquivo rust-toolchain.toml:
```toml
[toolchain]
channel = "nightly"
```
Isso irá instruir o rustup a usar a versão nightly, e baixar essa versão caso seja necessário.
#### Exemplo `discloud.config` para `Rocket`

{% content-ref url="../../faq/discloud.config.md" %}
[discloud.config.md](../../faq/discloud.config.md)
{% endcontent-ref %}

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
