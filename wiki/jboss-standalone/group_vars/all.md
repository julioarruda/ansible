# Documentação do Código

Este código define uma série de variáveis utilizadas para a instalação standalone do JBoss e para a configuração específica da AWS (Amazon Web Services).

## Variáveis de Instalação do JBoss

```yaml
http_port: 8080
https_port: 8443
```
As variáveis `http_port` e `https_port` estão configuradas para as portas padrão de HTTP (8080) e HTTPS (8443), respectivamente.

## Variáveis Específicas da AWS

```yaml
ec2_access_key:
ec2_secret_key:
ec2_region: us-east-1
ec2_zone:
ec2_image: ami-6c1e8f04
ec2_instance_type: m1.small
ec2_keypair: djohnson
ec2_security_group: default
ec2_instance_count: 3
ec2_tag: demo
ec2_tag_name_prefix: dj
ec2_hosts: all
wait_for_port: 22
```
Essas variáveis são usadas para configurar uma instância EC2 na AWS. 

- `ec2_access_key` e `ec2_secret_key` são as chaves para acessar a AWS.
- `ec2_region` define a região da AWS em que a instância será criada. Atualmente, está definida como "us-east-1".
- `ec2_zone` é a zona específica dentro da região.
- `ec2_image` é o ID da AMI (Amazon Machine Image) que será usada para criar a instância.
- `ec2_instance_type` é o tipo de instância que será criada. Nesse caso, será uma instância do tipo "m1.small".
- `ec2_keypair` é o nome do par de chaves que será usado para a instância.
- `ec2_security_group` é o grupo de segurança que será aplicado à instância.
- `ec2_instance_count` é o número de instâncias que serão criadas. Atualmente, está definido para criar 3 instâncias.
- `ec2_tag` é a tag que será associada às instâncias.
- `ec2_tag_name_prefix` é o prefixo que será usado no nome das tags.
- `ec2_hosts` define para quais hosts a configuração se aplica. Nesse caso, está definido para se aplicar a todos os hosts.
- `wait_for_port` é a porta que o sistema aguardará ficar disponível.

## Variáveis do Tower

```yaml
tower_user_name: admin
```

A variável `tower_user_name` define o nome do usuário que será definido pelo Tower quando o script for executado através dele. Atualmente, está definido como "admin".