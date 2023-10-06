# JBoss Server Setup

This Ansible playbook sets up JBoss server on a host machine. The following tasks are accomplished:

1. **Install Java 1.7 and some basic dependencies**: This task installs unzip, Java 1.7, libselinux-python, and libsemanage-python using yum package manager.

2. **Download JBoss from jboss.org**: This task downloads the JBoss AS 7.1.1.Final from the official JBoss site and saves it to the `/opt` directory.

3. **Extract archive**: This task extracts the downloaded JBoss archive to the `/usr/share` directory.

4. **Rename install directory**: This task renames the extracted JBoss directory to a version-independent name for easy referencing in the init script.

5. **Copying standalone.xml configuration file**: This task copies the standalone.xml file to the JBoss configuration directory. If the configuration changes, it will trigger a JBoss restart.

6. **Add group "jboss"**: This task creates a new group named "jboss".

7. **Add user "jboss"**: This task creates a new user named "jboss" and adds it to the "jboss" group. The home directory for this user is set as the JBoss installation directory.

8. **Change ownership of JBoss installation**: This task changes the ownership of the JBoss installation directory to the "jboss" user and group.

9. **Copy the init script**: This task copies the JBoss init script to the `/etc/init.d/` directory and sets its permissions to 0755 (rwxr-xr-x).

10. **Workaround for systemd bug**: This task starts the JBoss service and adds it to the system startup. Any errors in this step are ignored.

11. **Enable JBoss to be started at boot**: This task ensures the JBoss service is enabled and started at boot.

12. **Deploy iptables rules**: This task deploys iptables rules if the host's OS major version is not 7.

13. **Ensure that firewalld is installed**: This task installs the firewalld service if the host's OS major version is 7.

14. **Ensure that firewalld is started**: This task starts the firewalld service if the host's OS major version is 7.

15. **Deploy firewalld rules**: This task deploys firewalld rules for the specified HTTP and HTTPS ports if the host's OS major version is 7.

**Note:** The `with_items` directive is used in some tasks to loop over a list of items. The `when` directive is used in some tasks to specify conditions under which the tasks should be executed.