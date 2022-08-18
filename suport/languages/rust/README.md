# 🦀 Rust

## :file\_folder: Files

You should not send all your application files to `.zip`, there are some exceptions, they are:

```diff
- File Cargo.lock
- File .gitignore
- Folder target
- Folder .git
```

{% content-ref url="cargo.md" %}
[cargo.md](cargo.md)
{% endcontent-ref %}

## :compression: Compressing the Files

For more details on how to **Compress your Files** according to your **Operating System**, you can see below

![](../../../.gitbook/assets/zip-botrs.png)

{% content-ref url="../../faq/zip.md" %}
[zip.md](../../faq/zip.md)
{% endcontent-ref %}

## ✍ Hosting your bot

{% hint style="info" %}
Choose the method for hosting your bot in the Discloud:
{% endhint %}

{% content-ref url="../../host/bots/via-dashboard.md" %}
[via-dashboard.md](../../host/bots/via-dashboard.md)
{% endcontent-ref %}

{% content-ref url="../../host/bots/discord.md" %}
[discord.md](../../host/bots/discord.md)
{% endcontent-ref %}

## :earth\_americas: Hosting Your Site

{% hint style="info" %}
This feature needs some basic requirements to be able to be used, please check the requirements [here](../../host/sites/#requirements) before continuing
{% endhint %}

### Using `Rocket`

**Rocket** is a web framework built in rust, currently it only works in the nightly version of rust

```shell
rustup override set nightly
```

### Installing `Rocket`

Consult the official documentation: [https://rocket.rs/](https://rocket.rs/)

### Configuring `Rocket` for DisCloud

Create an`rust-toolchain.toml` file:

{% code title="rust-toolchain.toml" %}
```toml
[toolchain]
channel = "nightly"
```
{% endcode %}

This will instruct `rustup` to use the `nightly` version, and download that version if necessary.

`discloud.config` example for `Rocket`

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
