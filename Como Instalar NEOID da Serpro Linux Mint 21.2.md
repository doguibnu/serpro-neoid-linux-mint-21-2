## Como Instalar NeoID da Serpro no Linux Mint 21.2

**OBS: Alguns comandos realizados devem requerer permissão de super usuário (sudo), necessitando a senha de adminitrador do sistema.**

Verificando a versão do sistema:
![01-versao-mint-44](https://github.com/doguibnu/serpro-neoid-linux-mint-21-2/assets/38897311/562ef9c8-6ec1-4968-b41e-a2f9c1547fe2)

Abrir um **terminal** para executar o **update** e o **upgrade** do sistema com o comando:
```
sudo apt update -y && sudo apt upgrade -y
```

Ao finalizar o processo, executar um **reboot** do sistema, com o comando:
```
sudo reboot
```

Nesta versão do **Linux Mint (21.2)** é necessário baixar alguns pacotes manualmente para que se possoa instalar o aplicativo **NeoID** de forma correta e com o funcionamento desejado, sem erros.  Abrir um **terminal** do sistema. Com o terminal aberto, utilizar o comando para fazer uma pasta chamada **serpro**. Pasta feita, **entre/mude** para a pasta criada. Siga com os comandos abaixo:

```
mkdir serpro
cd serpro
```

A tela de terminal deve ser parecida como a figura abaixo:

![](/home/prefprudeserpro/.var/app/com.github.marktext.marktext/config/marktext/images/2023-07-19-16-03-20-02-tela-terminal06.png)

Dentro desta pasta criada, vamos iniciar o processo de instalação de alguns pacotes necessários. O primeiro pacote a ser baixado é: `libssl1.0.0_1.0.2g-1ubuntu4.20_amd64.deb`  Utilize o comando abaixo:

```
wget http://nz2.archive.ubuntu.com/ubuntu/pool/main/o/openssl/libssl1.0.0_1.0.2g-1ubuntu4.20_amd64.deb
```

Após o comando, sua tela deve parecer com esta abaixo:

![](/home/prefprudeserpro/.var/app/com.github.marktext.marktext/config/marktext/images/2023-07-19-16-12-59-03-pacote01-libssl04.png)

Vamos instalar o pacote com o comando abaixo. **Atenção:** para este comando, irá pedir a senha de super usuário **(sudo)**:

```
sudo dpkg -i libssl1.0.0_1.0.2g-1ubuntu4.20_amd64.deb
```

Quando executar o comando, sua tela de **terminal** deve parecer como abaixo. Digite a tecla **enter**:

![](/home/prefprudeserpro/.var/app/com.github.marktext.marktext/config/marktext/images/2023-07-19-16-19-52-04-sudo-prim-pacote9.png)



O comando irá solicitar a **senha** de super usuário como mostra a figura abaixo. Digitar a senha de super usuário **(sudo)** e teclar **enter**.

![](/home/prefprudeserpro/.var/app/com.github.marktext.marktext/config/marktext/images/2023-07-19-16-22-12-05-tela-sudo-prim-comando1.png)



O comando irá **instalar o pacote**. A tela deve parecer como a figura abaixo:

![](/home/prefprudeserpro/.var/app/com.github.marktext.marktext/config/marktext/images/2023-07-19-16-30-01-06-instalar-primeiro-comando33.png)

Ainda no mesmo **terminal**, vamos executar a instalação do próximo pacote necessário que é: `libssl1.1_1.1.0g-2ubuntu4_amd64.deb` Utilizar o comando abaixo e digitar a tecla **enter:**

```
wget libssl1.1_1.1.0g-2ubuntu4_amd64.deb
```

A tela do comando deve parecer com esta abaixo:

![](/home/prefprudeserpro/.var/app/com.github.marktext.marktext/config/marktext/images/2023-07-19-16-45-08-07-segundo-pacote7.png)

Quando o comando for executado, a tela deve parecer como esta abaixo:

![](/home/prefprudeserpro/.var/app/com.github.marktext.marktext/config/marktext/images/2023-07-19-16-49-09-08-down-segundo-pacote.png)



Vamos instalar este segundo pacote baixado com o comando indicado. **Atenção:** o comando irá solicitar a senha de super usuário **(sudo)**, digite a tecla **enter** e digite a senha de super usuário.

```
sudo dpkg -i libssl1.1_1.1.0g-2ubuntu4_amd64.deb
```

Ao executar o comando, a tela de **terminal** deve parecer como esta abaixo:

![](/home/prefprudeserpro/.var/app/com.github.marktext.marktext/config/marktext/images/2023-07-19-16-57-49-10-tela-instala-segundo-pacote-17.png)



Próximo passo, vamos baixar e instalar o pacote: **libnss3-tools** através do site da comunidade **Linux Mint.** Abra o navegador Firefox e acesse o endereço:

[Linux Mint - Community](https://community.linuxmint.com/software/view/libnss3-tools) . O navegador deve mostrar a tela como na figura abaixo. Clicar no botão **Install**:

![](/home/prefprudeserpro/.var/app/com.github.marktext.marktext/config/marktext/images/2023-07-20-08-37-10-11-site-libnss0fire.png)

Quando clicar, uma janela irá abrir questionando se permite que o site possa abrir a ligação do aplicativo **apt (instalar pacotes)** com o **AptURl**. Clique em: **Abrir/Permitir Ligação** como mostra a figura abaixo:

![](/home/prefprudeserpro/.var/app/com.github.marktext.marktext/config/marktext/images/2023-07-20-08-56-49-12-clicar-abrir-link-52a.png)

Então, uma janela de instalação de programa irá questionar se deseja instalar o pacote desejado, como mostra a figura abaixo. **Clique** em **Instalar**:

![](/home/prefprudeserpro/.var/app/com.github.marktext.marktext/config/marktext/images/2023-07-20-09-02-37-13-tela-de%20instalar-pacote0libnss3-50.png)

Inserir a senha de **super usuário** e clique em **Autenticar** para executar a instalação do pacote como mostra a figura abaixo. O pacote será instalado no sistema e a tela de instalação irá fechar.

![](/home/prefprudeserpro/.var/app/com.github.marktext.marktext/config/marktext/images/2023-07-20-09-17-47-14-senha-para-instalar-pacote.png)



Com os pacotes necessários instalados no sistema para o funcionamento correto do NeoID, vamos baixar o instalador do NEOID da Serpro, no site de download, acessando o siite:  [NeoID - Seu certificado digital em nuvem - Drivers](https://neoid.estaleiro.serpro.gov.br/downloads/) selecione o sistema operaciona **Linux** e clique em **baixar**. Veja a figura abaixo: 

![](/home/prefprudeserpro/.var/app/com.github.marktext.marktext/config/marktext/images/2023-07-20-09-35-16-15-neo-id-baixiar-site-54aa.png)

Quando o downlaod for concluído, **clique** no arquivo baixado para podermos fazer a instalação do mesmo, como mostra a figura abaixo:

![](/home/prefprudeserpro/.var/app/com.github.marktext.marktext/config/marktext/images/2023-07-20-09-43-47-16-dowload-neo-id-44aa.png)

Aguarde o sistema mostrar a tela de instalação do program e então clique no botão: **Instalar Pacote**. Será requerido a senha de **super usuário (sudo)**.

![](/home/prefprudeserpro/.var/app/com.github.marktext.marktext/config/marktext/images/2023-07-20-09-48-21-16-instalar-Neoid36.png)

Inserir a senha e clicar em **Autenticar**:

![](/home/prefprudeserpro/.var/app/com.github.marktext.marktext/config/marktext/images/2023-07-20-09-54-14-17-senha-instalar-neoidg.png)

Alguns softwares adicionais serão requeridos para a instalação completa do aplicativo. Clique em **Continuar** e aguarde a finalização do processo. Veja a figura abaixo:

![](/home/prefprudeserpro/.var/app/com.github.marktext.marktext/config/marktext/images/2023-07-20-10-02-36-18-pacotes-requeridos-neoid31.png)



Após a instalação do programa, clique no menu do Linux Mint e encontre o programa**NEOID** como motra a figura abaixo e **clique** para iniciar o mesmo:

![](/home/prefprudeserpro/.var/app/com.github.marktext.marktext/config/marktext/images/2023-07-20-10-10-32-21-menu-neoid-mint.png) 

Para aprender a usar o **NeoID**, utilize o manual oficial disponibilizado no site da [Serpro ](https://neoid.estaleiro.serpro.gov.br/downloads/Manual-NeoID.pdf)

## Tutorial Realizado pelo **Setor de TI**

[Prefeitura Muncipal de Prudentópolis - Paraná](https://www.prudentopolis.pr.gov.br/)



**Douglas Giovani Oechsler**

**Selmo Andrei Bobato**








