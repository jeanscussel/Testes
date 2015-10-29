#Tutorial git e o github

###by Jean - 28/10/2015


Como ja sabemos o git serve para versionamento e você pode compartilhar com serviços online. 

Usarei o github como exemplo.

####Primeiramente vamos instalar o git

No terminal digite:
$ sudo apt-get install git-core

É necessário gerar uma chave ssh e ter um cadastro em algum repositório git.

Para conferir se você ja tem uma chave digite o comando:

$ ls ~/.ssh/

se já existir uma você pode utilizá-la ou gerar uma nova:

Este comando gera a chave: 

$ sudo ssh-keygen

Este comando entra no diretório onde as chaves estão:

$ cd ~/.ssh 

Este comando abre o arquivo para vera chave:

$ sudo cat ~/.ssh/id_rsa.pub

Agora só copiar TODO o conteúdo da chave e ir para o github adiciona-la. Vá para https://github.com/account e clique em SSH Public Keys depois add another public key. Cole a chave e salve.

#### Novamente no terminal...

Insira os comandos:

$ git config --global user.name Your Name
$ git config --global user.email user@gmail.com

####Pronto...

Agora crie um novo repositório no github e um novo diretório na sua máquina. 

Acesse o diretório criado. Vamos começar iniciando um git neste diretório:

$ git init

Vamos adicionar o repositório do github...

$ git remote add origin git@github.com:username/Testes.git

Agora adicionamos as alterações nos arquivos individualmente ou vários de uma vez.

Um arquivo: 

$ git add teste.txt

Todas as alterações:

$ git add .

Agora vamos comitar:

$ git commit -m mensagem obrigatória

Ultimo passo é enviar as alterações:

$ git push origin master

###Pronto...
