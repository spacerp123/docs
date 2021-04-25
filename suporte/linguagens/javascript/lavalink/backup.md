# Quero fazer backup dos meus arquivos mas é muito pessado download o que eu faço?
Para reduzir o peso do download do backup você pode remover:
- o diretório `java`
- o diretório `node_modules` que se encontra no diretório `bot` (já que a Discloud não consegue controlar esse `node_modules` devido não estar na raiz da Instancia)
- caso não queira receber os no backup dos logs remova tambem o diretório `logs`