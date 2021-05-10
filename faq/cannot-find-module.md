## **__Como resolver o seguinte erro?__** `` Error: cannot find module...``
 ### JavaScript
* Geralmente nos logs/terminal informa o arquivo que deu o erro, e as possíveis linhas que o erro pode estar, verifique se nesse arquivo se realmente ele precisa do módulo informado.

* Se não precisar remova o modulo que esta listado no comando.

* Se precisar instale o modulo executando o seguinte comando no VSC/IDE que é ``npm i (nome_do_modulo) --save``.
  * **exemplo:** ``npm i moment --save``.

* Verifique se o módulo se encontra listado no arquivo ``package.json`` antes de hospedar a aplicação na DisCloud. 

* Não coloque nomes com acentuações, letras grandes em seu projeto para não dar conflito no arquivo `package.json`, na parte `"name"`  caso tiver letra maiúscula, caracteres especiais dentre outro, deixa as informações mais simples possível. 
  * **exemplo:** `"name": "meubot",`

* O erro também pode ser por causa que você tenha definido um caminho de leitura errada (`./`, `../` , `../../`, e assim por diante) , quando vai puxar as informações do arquivo caso tiver especificado o caminho de leitura de forma errada, ele não vai conseguir ler.
 
{% hint style="info" %}
 💻 Nota:  Para verificar os logs/terminal, basta ir no canal ``#🔌┃commands`` e executar o comando ``.t`` ou ``.t (ID_DO_BOT)``, alguns módulos pode ter conflito com algumas versões da lib do discord então verifique se tem alguma que não é compatível, Se o erro continuar vá ao canal ``#💻┃javascript`` e peça ajuda.
{% endhint %}
