# Documentation of the Playbook
---

This playbook contains instructions for the deployment of two simple applications to a JBoss server. It consists of two primary components: hosts and roles.

## Structure

```yml
- hosts: all

  roles:
    - java-app
```

## Description

- `hosts: all`: This statement instructs Ansible, the automation tool being used, to execute the tasks on all the hosts mentioned in the inventory file. In this case, it is targeting all hosts.

- `roles:`: This is a way of automatically loading certain vars_files, tasks, and handlers based on a known file structure. Grouping content by roles also allows easy sharing of roles with other users.

    - `- java-app`: This is a role that's most likely responsible for deploying a Java application. The specifics of what this role does can be found in the role's tasks file. Normally, it should be located under the `roles/java-app/tasks/main.yml` file. 

Please note, the role `jboss-standalone` is commented out in the code. If you want to use it, you can uncomment it. This role might be used to (re)deploy JBoss.

---

This is a very basic playbook and it's a good practice to keep things simple. However, depending on the complexity of the tasks, additional roles and tasks can be added to this playbook. Also, it's better to maintain a separate inventory file for hosts for better management.