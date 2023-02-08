# Roteiro para instalação Linux

Execute o comando abaixo:

``` 
wget -qO- https://get.docker.com/ | sh 
```

Acessar o script: https://get.docker.com/

Após terminar o teste, execute o comando abaixo. 

```
docker container run hello-world
```
Este comando roda um containr de hello-word.

Tratamento de possíveis problemas
Se o acesso a internet da máquina passar por controle de tráfego (aquele que bloqueia o acesso a determinadas páginas) você poderá encontrar problemas no passo do apt-key. Caso enfrente esse problema, execute o comando abaixo:

```
wget -qO- https://get.docker.com/gpg | sudo apt-key add -
```
