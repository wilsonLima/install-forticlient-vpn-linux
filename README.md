install-forticlient-vpn-linux
=========

Role do Ansible para a instalação do FortiClient VPN em Distribuições Linux


Distribuições Suportadas pela Role
------------
- Fedora 37 ou superior
- Linux Mint 21.1 ou superior
- Ubuntu 22.10 ou superior


Tags da Role 
--------------

- main: Tag a ser utilizada em conjunto com outras tags, se alguma tag for especificada no comando.

- repo: Inclui todos os repositórios da role no Sistema.
- deps: Instala as dependências da role.
- forticlient: Realiza a instalação do FortiClient.


Variáveis da Role 
--------------

- forticlient_version: Versão do FortiClient, valor padrão: "7.2" .


Dependências da Role 
--------------

Debian, Linux Mint e Ubuntu:

- openssh-server. Ex.: sudo apt install openssh-server


Exemplo de Playbook
----------------

Exemplo de uso da Role, com as configurações padrão:

    - hosts: desktop
      roles:
         - install-forticlient-vpn-linux

Exemplo de uso da Role com variáveis:

    - hosts: desktop
      roles:
         - { role: install-forticlient-vpn-linux, forticlient_version: "7.2" }


Exemplo de Comandos
----------------

Comando para executar todas as tasks:

    ansible-playbook -i <caminho_inventario> <caminho_playbook>

Comando para executar a tag "repo" (em caso de uso de tags, a tag "main" é obrigatória):

    ansible-playbook -i <caminho_inventario> <caminho_playbook> --tags "main, repo"


License
-------

MIT License