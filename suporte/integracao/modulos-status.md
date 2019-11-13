---
description: Módulo para ler métricas do cgroup de contêineres modernos Linux
---

# Módulos Status

![](../../.gitbook/assets/image%20%2825%29.png)

## Informações

O limite de memória definidos nos contêiners é imposto via cgroups, e a maioria das ferramentas Linux que fornecem métricas de recursos do sistema foram criadas antes mesmo da existência de cgroups \(por exemplo: free ou top\).

Eles costumam ler métricas de memória do procsistema de arquivos: `/proc/meminfo`, `/proc/vmstat`, `/proc/PID/smaps` e outros. Isso significa que eles não têm consciência de cgroup . Eles sempre exibirão os números de memória do sistema host \(máquina física ou virtual\) como um todo, que é inútil para os contêineres modernos do Linux.

Esse módulo Nodejs funciona apenas no linux, e foi criado exclusivamente para atender os usuários da [discloudbot.com](https://discloudbot.com/)

As informações fornecidas pelo modulo são geradas pelo [cgroups](https://www.kernel.org/doc/Documentation/cgroup-v1/) no caminho `/sys/fs/cgroup/`

{% tabs %}
{% tab title="📦Javascript" %}
### Instalação do módulo

```bash
$ npm install discloud-status
```

### Forma de uso no JS

```javascript
const discloud = require("discloud-status");

// retorna o uso/total de RAM
let r = discloud.ram();
console.log(r) // 100/1024MB

// dados do uso de RAM
let ur = discloud.usoRam();
console.log(ur) // 100MB

// dados do total de RAM disponível
let tr = discloud.totalRam();
console.log(tr) //1GB
```

[https://www.npmjs.com/package/discloud-status](https://www.npmjs.com/package/discloud-status)
{% endtab %}

{% tab title="🐍Python" %}
### Instalação do módulo 

```bash
$ pip install discloud
```

## Forma de uso no Python

```python
import discloud

# retorna o uso/total de RAM
r = discloud.ram()
print(r) # 100/1024MB

# dados do uso de RAM
ur = discloud.using_ram()
print(ur) # 100MB

# dados do total de RAM disponível
tr = discloud.total_ram()
print(tr) # 1GB
```

[https://pypi.org/project/discloud/](https://pypi.org/project/discloud/)
{% endtab %}
{% endtabs %}



