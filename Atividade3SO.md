
# Instalação do Docker e configurações


Antes de intalar o Docker certifique-se de estar usando uma kernel do linux 3.8 ou +, para conferir, basta digirar a seguinte linha de comando no terminal:
> uname -r 

Faça atualização dos pacotes do linux utilizando esse comando abaixo;
 
> #apt-get update


Terminando a atualização dos pacotes, vamos inicir o script de instalação do Docker, adicionando um respositorio docker na sua maquina 

> curl -sSL https://get.docker.com | sh


Para inciar o docker digite o seguinte comando

```sh
/etc/init.d/docker start
```

Para criar uma imagem no docker, basta digitar o seguinte codigo substituindo o nome do sistema desejado, a sua versão e o processo que seja iniciado, no caso o /bin/bash que é o shell

```sh
docker run -i -t ubuntu:14.10 /bin/bash
```
Apos ser baixado a imagem, perceba que automaticamente ira entrar no container, voce percebera pela alteração do nome da maquina no Shell.

E para conferir se o docker esta realmente ativo, digite o seguinte

```sh
ps -ef | grep docker
```

Para ver as imagens que estão rodando no docker, digite o seguinte

```sh
docker ps 
```




## Instalação do Apache


Depos da instalação acima você estara dentro de um container Docker :-), agora instale o Apache:

>apt-get update && apt-get install apache2

Ative o serviço do apache no seu Ubuntu:

>service apache2 start

Verifique o IP da sua máquina Ubuntu:

>ifconfig

No meu caso era: > 127.17.0.3, Coloque este IP no seu navegador e seja feliz. Isto é uma ótima opção para quem está aprendendo PHP, assim você pode ter um servidor sempre que precisar sem afetar em nada seu sistema principal.

Observação:

Se você fechar a máquina (docker – ubuntu) as configurações vão se perder, neste caso, em sua máquina (servidor) abra um terminal e digite o comando :

>docker commit IDdoDocker nomedaimagem

O “IDdoDocker” é o código que está após o root@, exemplo:

>root@8a433ff8df3

Coloque este número no comando e em “nomedaimagem” coloque um novo nome para a imagem ubuntu, exemplo:
docker commit 8a433ff8df3  ubuntuapache
