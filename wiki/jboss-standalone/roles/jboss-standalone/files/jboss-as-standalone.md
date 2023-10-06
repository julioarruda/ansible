# Documentation of JBoss standalone control script

This script is used to control the standalone mode of JBoss application server. The script provides functionality for starting, stopping, restarting and checking the status of the JBoss server.

## Variables

The script uses a number of variables to control its behavior:

- `JBOSS_USER`: The user under which JBoss should run.
- `JBOSS_HOME`: The location of the JBoss installation.
- `JBOSS_PIDFILE`: The location of the file in which the process id of the running JBoss server should be stored.
- `JBOSS_CONSOLE_LOG`: The location of the console log file.
- `STARTUP_WAIT`: The number of seconds the script should wait for JBoss to start before giving up.
- `SHUTDOWN_WAIT`: The number of seconds the script should wait for JBoss to stop before giving up.
- `JBOSS_CONFIG`: The configuration file that should be used when starting JBoss.

## Functions

The script contains a number of functions:

- `start()`: This function is used to start the JBoss server. It first checks if the server is already running, and if not, it starts the server and waits for it to be fully started before returning.
- `stop()`: This function is used to stop the JBoss server. It sends a termination signal to the server and waits for it to stop before returning. If the server does not stop within a specified time, it sends a kill signal.
- `status()`: This function checks and displays the status of the JBoss server. It checks whether the server is running, and if so, it displays the process id. If the server is not running, it indicates this.
- `restart()`: This function stops and then starts the JBoss server.

## Usage

The script is intended to be run from the command line, with one of the following arguments:

- `start`: Starts the JBoss server.
- `stop`: Stops the JBoss server.
- `restart`: Restarts the JBoss server.
- `status`: Checks and displays the status of the JBoss server.