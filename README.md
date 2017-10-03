# openstack_single_machine_lxd
Implementação fácil e rápida do OpenStack com conjure-up em um único laptop usando contêineres LXD. É ideal para usuários ou desenvolvedores pela primeira vez em contato com a instalação do Openstack. 

Baseado em [https://www.ubuntu.com/download/cloud/try-openstack](https://www.ubuntu.com/download/cloud/try-openstack), com adição de alguns pontos que acredito terem faltado no tutorial básico da Canonical.

```sh
sudo groupadd --system lxd

sudo usermod -G lxd -a ctic

sudo snap install lxd

newgrp lxd

(Fazer logout e logar novamente)

/snap/bin/lxd init --auto

/snap/bin/lxc network create lxdbr0 ipv4.address=auto ipv4.nat=true ipv6.address=none ipv6.nat=false

sudo snap install conjure-up --classic

conjure-up```
