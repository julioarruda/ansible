---
# Este playbook implementa um servidor JBoss autônomo simples.

- hosts: all

  roles:
    - jboss-standalone

---

## Documentação

Este playbook Ansible é usado para implementar um servidor JBoss autônomo simples. A seguir, detalhamos o que cada linha faz:

- `hosts: all` : Esta linha define que o playbook será executado em todos os hosts no inventário do Ansible. O termo "all" pode ser substituído pelo nome do grupo de hosts que você definiu no arquivo de inventário do Ansible.

- `roles:` : Este termo é usado para definir as roles (papéis) que serão aplicadas aos hosts. As roles são maneiras de agrupar tarefas relacionadas e podem ser reutilizadas em diferentes playbooks.

  - `jboss-standalone`: Esta é a role que será aplicada. Ele deve estar presente no diretório de roles do seu projeto Ansible. Essa role deve conter todas as tarefas necessárias para instalar e configurar um servidor JBoss autônomo.

Lembre-se que um playbook do Ansible é uma lista de tarefas que o Ansible executará em sequência nos hosts especificados. É uma boa prática documentar cada playbook para facilitar o entendimento de quem for usar ou modificar o código no futuro.

Cada role deve ter sua própria documentação explicando o que ela faz, quais variáveis ela espera e quais tarefas ela executa. 

Para executar este playbook, você deve ter o Ansible instalado e configurado corretamente na sua máquina, além de ter acesso SSH aos hosts onde o playbook será executado. Além disso, você deve ter a role `jboss-standalone` disponível no seu projeto.