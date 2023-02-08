#Sobre
Essa aplicação utiliza uma imagem de node 14 disponivel no docker hub e está sendo utiliza para aprender os comandos iniciais
Estou usando o livro https://stack.desenvolvedor.expert/appendix/docker para apoiar no estudo.

##Por que usar Docker?

Abaixo alguns trechos retirados do livro:

###1 – Ambientes semelhantes
A aplicação pode ser instanciada como container em qualquer ambiente que desejar.

## 2 – Aplicação como pacote completo
Utilizando as imagens Docker é possível empacotar toda sua aplicação e dependências, facilitando a distribuição, pois não será mais necessário enviar uma extensa documentação explicando como configurar a infraestrutura necessária para permitir a execução, basta disponibilizar a imagem em repositório.
As imagens Docker podem utilizar tags e, assim, viabilizar o armazenamento de múltiplas versões da mesma aplicação. Isso significa que em caso de problema na atualização, o plano de retorno será basicamente utilizar a imagem com a tag anterior.

##3 – Padronização e replicação
Como as imagens Docker são construídas através de arquivos de definição, é possível garantir que determinado padrão seja seguido, aumentando a confiança na replicação. Basta que as imagens sigam as melhores práticas de construção para que seja viável escalarmos a estrutura rapidamente.
