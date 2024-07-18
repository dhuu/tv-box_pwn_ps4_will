Este é o instalador online/offline do exploit PPPwn para PS4 com suporte para TV BOX

Dispositivos TV BOX em que este instalador é executado

TV BOX com processador Amlogic roda Armbain OS

CAIXA DE TV com processador Arm64 executa o sistema operacional Armbain

CAIXA DE TV com processador Arm32 executa o sistema operacional Armbain

CAIXA DE TV com processador Armv7 executa o sistema operacional Armbain

TV BOX com processador RockChip roda Armbain OS

NOTA: A TV BOX deve estar enraizada para instalar o sistema operacional Armbian nela

Este instalador também funciona em

Framboesa Pi 5

Framboesa Pi 4 Modelo B

Framboesa Pi 400

Framboesa Pi 3B+

Raspberry Pi 2 Modelo B

Raspberry Pi Zero 2 W com adaptador USB para Ethernet

Raspberry Pi Zero W com adaptador USB para Ethernet

Você precisa gravar Raspberry Pi OS Lite ou Armbian Cli/Minimal em um cartão SD.

Depois de gravar o sistema apropriado no cartão SD, desconecte o cartão SD do computador e conecte-o novamente. Você verá uma partição chamada BOOT. Basta copiar a pasta do firmware que você baixou para a raiz da partição BOOT do cartão SD e inserir o cartão SD. em seu dispositivo, seja um Raspberry Pi ou TV BOX, e conclua o processo de instalação do sistema

Depois que o sistema for inicializado com sucesso, você não precisará instalar todo o sistema

As etapas da instalação

Você será solicitado a inserir nome de usuário e senha. Digite root no campo de nome de usuário e digite 1234 no campo de senha.

Você será solicitado a alterar sua senha. Digite qualquer senha que desejar

Quando for solicitado que você insira o nome do dispositivo, pressione os botões Ctrl + C e o prompt de comando será aberto

No prompt de comando, digite o seguinte comando:

sudo bash /boot/firmware/PPPwn/install.sh

O instalador irá perguntar sobre as configurações de instalação. Após a conclusão da instalação, reinicie o dispositivo e parabéns. Seu dispositivo foi configurado com sucesso. Agora você pode conectá-lo ao PS4 e ativar o Jailbreak.
Para GoldHen você precisa colocar o arquivo goldhen.bin na raiz de uma unidade USB e conectá-lo ao console. Assim que o goldhen for carregado pela primeira vez, ele será copiado para o disco rígido interno do console e o USB não será mais necessário. Para atualizar o goldhen basta repetir o processo acima e a nova versão será copiada para o disco rígido interno

Se quiser como configurar a conexão no PS4, veja a lista abaixo.

Vá para Configurações e depois Rede

Selecione Configurar conexão com a Internet e escolha Usar um cabo LAN

Escolha Configuração personalizada e escolha PPPoE para configurações de endereço IP

Digite ppp para ID de usuário PPPoE e senha PPPoE

Escolha Automático para configurações de DNS e configurações de MTU

Escolha Não usar para servidor proxy

NOTA: se você habilitar o acesso à internet você deve corresponder ao nome de usuário e senha digitados durante a instalação ou usar o ppp padrão

NOTA: que este instalador funciona normalmente no Raspberry Pi, mas esta explicação se concentra mais em dispositivos TV BOX

```sh
apt update
apt install git -y
rm -f -r PI-Pwn
systemctl stop pipwn
git clone https://github.com/dhuu/tv-box_pwn_ps4_will.git
mkdir /boot/firmware/
cd PI-Pwn
cp -r PPPwn /boot/firmware/
cd /boot/firmware/PPPwn
chmod 777 *
bash install.sh
```
