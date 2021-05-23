# Comandos que aprendi em linux: :brazil:

Ctrl+alt+T - abre terminal
pwd -  nome do diretório de trabalho atual
ls - lista  

ls <pasta especifica> - lista uma pasta especifica
ls -l - lista com detalhes a mais
man ls - manual 
ls --help - ajuda 
cd - muda o diretorio , avança pasta
cd .. - retorna diretório
cd / - muda diretorio para do linux
cd ~ - muda diretorio para pessoal
mkdir - cria uma pasta
history - exibe histórico
mv <pasta> ~ - move o arquivo para o diretorio pessoal 
mv <nome da pasta> <nome novo> - renomeia o arquivo
touch <nome> - cria um conteudo vazio 
cp <nome do arquivo> </home/leandro> - copia o arquivo 
clear - limpa a tela
rmdir - pra remover um diretorio 
rm -r - remove diretorio
<comando> --help - traz ajuda do comando
man <comando> - traz manual do comando
date - mostra data

alias  trc='traceroute' - substitui o comando vira trc

cal - mostra o calendário

exit - sai do terminal

## Atalhos:

Seta para cima - ultimo comando
!! - executa ultimo comando
CTRL+C - Cancela o comando atual
CTRL+Z - Pausa o comando atual
CTRL+D - Faz o logout
CTRL+W - Apaga uma palavra na linha atual
CTRL+U - apaga a linha toda 
CTRL+R - Busca o comando recente
TAB - Completa o comando

## TOUCH:

nano <nome do arquivo> - editor de texto 
cat - visualiza o conteúdo do nano
tac <nome do arquivo> - ele exibe e inverte as linhas.
head <nome do arquivo> - exibe as 10 primeiras linhas
tail <nome do arquivo> - exibe as 10 últimas linhas
tail <nome do arquivo> > <nome do arquivo> - cria um arquivo novo com as 10 últimas linhas do nano.
head <nome do arquivo>  > <nome do arquivo - cria um arquivo novo com as 10 primeiras linhas
cal > <nome do arquivo> - cria um calendario dentro de um arquivo.
date >> <nome do arquivo> - coloca data dentro do arquivo.
cal 2020 > <nome do arquivo> - vai substituir o que tiver dentro pelo cal
tail <nome do arquivo> | grep <palavra dentro do arquivo> - ele procura e marca a palavra desejada nas ultimas 10 linhas
cat <nome do arquivo> | more - exibe um mais limitando o nano
cat <nome do arquivo> | less - exibe dois pontos e vai aparecendo o resto do texto
cat <nome do arquivo> & cat <nome do arquivo> - junta os nanos
mkdir <nome do arquivo> && cd <nome do arquivo> - cria a pasta e abre ela
file <nome do arquivo> - especifica a pasta
whatis <comando> - exibe o que faz determinado comando
find ~ -name <nome arquivo> - mostra o diretorio do arquivo 

## Diretórios:

cd / - muda diretorio para o raiz
cat /proc/cpuinfo - ve as informações do cpu
cat /proc/meminfo - informações da memória 
lspci - exibe os hardware conectados no pc
lsusb - exibe os dispositovs usb
arch/uname -m - mostra a arquitetura do sistema.
uname - mostra o kernel do sistema
uname -r - mostra a versão do kernel
free - mostra a saida da memoria fisica e a virtual
du -h ~ - mostra o diretório e o espaço q ocupa
cat /etc/passwd - mostra quantos usários tem
reboot - reinicia o sistema
shutdown --help - manual do shutdown.
shutdown -h <tempo q ele vai desligar maquina>
lscpu - mostra as informações do cpu
lshw - mostra a lista de todos os hardware q ele achar
lshw -short - mostra alguns caminhos de hardware e os tipos

## REDE :

sudo apt install net-tools - instala ferramentas de rede

Ifconfig  - exibe configuração de ip

hostname - traz o nome do pc na rede

hostname - I - traz o ip

hostname - i - traz o loopback

who - mostra  como estamos logado na rede

whoami - nome do usuario logado na rede

ping  <site>  - mostra se o site ta ativo

ping --help - manual

dig <site> - traz informações do dns

traceroute <site> - traz informações dos nós que tem no  site

dig <site> + short - ip do site

whois <site> - traz mais informações do site

finger - traz informação do usuário q ta logado no nosso host

## OUTROS COMANDOS :sweat_drops:



wc -l <nomearquivo> - mostra a quantidade de linhas

wc -w <nomearquivo> - mostra a quantidade de palavras

wc --help

ls -a - mostra arquivos ocultos

cmp <arquivo> <arquivo> - compara os arquivo

diff <nome arquivo> <nomearquivo> - mostra a diferença dos arquivo

last reboot - mostra quando reiniciamos

route -n - mostra tabela de roteamento ip do kernel

time <traceroute> - tempo de um processo

uptime - mostra o tempo que o sistema ta rodando

cowsay <"string"> - é uma vaquinha q diz

cowsay -g <"string"> 

cowsay -f dragon <"string"> 

init 0 - desliga maquina

telinit 0 - desliga 

halt - desliga 

seq <numero> <numero> - imprime uma sequencia de numeros no linux

## USUARIO

adduser <nome> - cria um novo usario

sudo <comando> - ganhar privilegio

su <nome do usuario> - troca de usuario

passwd <nome do usuario> - trocar a senha

lastlog - informação de login dos usuários

last - exibe uma lista de usuarios 

id - exibe todos os idetificadores do usuario

cat /etc/passwd - mostra todos os usuarios  

userdel -r <nomedousuario> - remove o usuario

cat /etc/group - exibe todos os grupos do sistema

groups - mostra os grupo do usuario

addgroup <nomedogrupo>- cria um grupo

adduser <usuario> <grupo> - adiciona o usuario ao grupo

gpasswd -a <usuario> <grupo>

gpasswd -d <usuario do grupo> - remove o usuario do grupo

groupdel <nomegrupo> - remove o grupo

ls -lh - verifica a permissao em um diretorio

chmod <numerodaatribuição> -  muda a permissão do grupo de um arquivo ou diretório

## COMPACTAÇÃO E DESCOMPACTAÇÃO

gzip <nome do arquivo>  - compacta o arquivo

gunzip <nome do arquivo> -  descompacta o arquivo

gzip -9 <nome do arquivo> - usa compactação maxima 

zip <nome do arquivo.zip> <nome do arquivo.txt> - compactação

zip <arquivos.zip> <nome do arquivo> <nome do arquivo> - compactou mais de um arquivo

unzip <arquivo.zip> - descompacta

bzip2 <nome do arquivo> - compacta

bzip2 -d <nome do arquivo> - descompacta

rar a  <nome do arquivo.rar> <arquivo que vai ser compactado>

rar x <arquivo.rar> 

tar -cf <nome do arquivo q será gerado> <nome do arquivo>

tar -xvf <nome do arquivo.zip>

tar -xvf <nome do arquivo.zip>  -C  <lugar onde quer descompactar>

## Gerenciamento de pacote

sudo apt install <pacote> - instala o pacote

sudo apt upgrade <pacote> - atualiza o pacote

sudo apt remove <pacote> - desinstala o pacote

apt update && apt upgrade - atualização do sistema

sudo su  - ser o privilegiado

su Leandro

sudo dpkg -i <arquivo> - para instalar o arquivo .deb que está no computador

sudo dpkg -I <pacote.deb> - descrição 

sudo dpkg -r <nome do pacote que está na descrição><package> - desintalação

 ### FEDORA

rpm -ivh <pacote.rpm> - instalação

sudo rpm -ivh --nodeps <pacote.rpm> - caso dê falha na dependencia

rpm -U <pacote.rpm> - atualização do pacote

sudo rpm -e <pacote.rpm> - desintalação

yum install <pacote> - instalação

yum update <pacote> - atualiza

yum remove <pacote> - desintalação 

