# Sobre
Essa aplicação utiliza uma imagem de node 14 disponivel no docker hub e está sendo utiliza para aprender os comandos iniciais
Estou usando o livro https://stack.desenvolvedor.expert/appendix/docker para apoiar no estudo.
Outras referências:
* https://docs.docker.com/engine/reference/builder/
* https://docs.docker.com/develop/develop-images/dockerfile_best-practices/

## O que é Docker?

Docker é uma plataforma aberta, criada com o objetivo de facilitar o desenvolvimento, a implantação e a execução de aplicações em ambientes isolados. Foi desenhada especialmente para disponibilizar uma aplicação da forma mais rápida possível.

O Docker utiliza o modelo de container para “empacotar” a aplicação que, após ser transformada em imagem Docker, pode ser reproduzida em plataforma de qualquer porte; ou seja, caso a aplicação funcione sem falhas em seu notebook, funcionará também no servidor ou no mainframe. Construa uma vez, execute onde quiser.

Os containers são isolados a nível de disco, memória, processamento e rede. Essa separação permite grande flexibilidade, onde ambientes distintos podem coexistir no mesmo host, sem causar qualquer problema.

O modelo de isolamento utilizado no Docker é **a virtualização a nível do sistema operacional**, um método de virtualização onde o kernel do sistema operacional permite que múltiplos processos sejam executados isoladamente no mesmo host. Esses processos isolados em execução são denominados no Docker de container.

Para criar o isolamento necessário do processo, o Docker usa a funcionalidade do kernel, denominada de namespaces, que cria ambientes isolados entre containers: os processos de uma aplicação em execução não terão acesso aos recursos de outra. A menos que seja expressamente liberado na configuração de cada ambiente.

Para evitar a exaustão dos recursos da máquina por apenas um ambiente isolado, o Docker usa a funcionalidade cgroups do kernel, responsável por criar limites de uso do hardware a disposição. Com isso é possível coexistir no mesmo host diferentes containers sem que um afete diretamente o outro por uso exagerado dos recursos compartilhados.

## Por que usar Docker?

Abaixo alguns trechos retirados do livro:

### 1 – Ambientes semelhantes
A aplicação pode ser instanciada como container em qualquer ambiente que desejar.

### 2 – Aplicação como pacote completo
Utilizando as imagens Docker é possível empacotar toda sua aplicação e dependências, facilitando a distribuição, pois não será mais necessário enviar uma extensa documentação explicando como configurar a infraestrutura necessária para permitir a execução, basta disponibilizar a imagem em repositório.
As imagens Docker podem utilizar tags e, assim, viabilizar o armazenamento de múltiplas versões da mesma aplicação. Isso significa que em caso de problema na atualização, o plano de retorno será basicamente utilizar a imagem com a tag anterior.

### 3 – Padronização e replicação
Como as imagens Docker são construídas através de arquivos de definição, é possível garantir que determinado padrão seja seguido, aumentando a confiança na replicação. Basta que as imagens sigam as melhores práticas de construção para que seja viável escalarmos a estrutura rapidamente.

## Instalação

O Docker deixou de ser apenas um software para virar um conjunto deles: um ecossistema.

Nesse ecossistema temos os seguintes softwares:

* **Docker Engine**: É o software base de toda solução. É tanto o daemon responsável pelos containers como o cliente usado para enviar comandos para o daemon.
* **Docker Compose**: É a ferramenta responsável pela definição e execução de múltiplos containers com base em arquivo de definição.
* **Docker Machine**: é a ferramenta que possibilita criar e manter ambientes docker em máquinas virtuais, ambientes de nuvem e até mesmo em máquina física.

