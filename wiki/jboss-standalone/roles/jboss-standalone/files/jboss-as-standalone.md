# Documentação do Código

Este script é utilizado para controlar a execução do JBoss AS (Application Server) em um modo autônomo. Ele permite iniciar, parar, reiniciar e verificar o status do servidor JBoss.

## Variáveis de Configuração

- `JBOSS_USER`: Define o usuário do JBoss.
- `JBOSS_CONF`: Define o arquivo de configuração do JBoss AS.
- `JBOSS_HOME`: Define o diretório de instalação do JBoss AS.
- `JBOSS_PIDFILE`: Define o arquivo que irá armazenar o PID (Process ID) do JBoss AS.
- `JBOSS_CONSOLE_LOG`: Define o arquivo que irá armazenar os logs de console do JBoss AS.
- `STARTUP_WAIT`: Define o tempo de espera para inicialização do JBoss AS.
- `SHUTDOWN_WAIT`: Define o tempo de espera para finalização do JBoss AS.
- `JBOSS_CONFIG`: Define o arquivo de configuração XML do JBoss AS a ser utilizado.
- `JBOSS_SCRIPT`: Define o script de inicialização do JBoss AS.

## Funções

- `start`: Inicia o servidor JBoss AS. Se o servidor já estiver em execução, a função retorna uma mensagem de falha. Caso contrário, inicia o servidor e aguarda até que o servidor seja iniciado ou até que o tempo de espera definido na variável `STARTUP_WAIT` seja atingido.
- `stop`: Interrompe a execução do servidor JBoss AS. Se o servidor não estiver em execução, a função retorna uma mensagem de sucesso. Caso contrário, tenta interromper a execução do servidor. Se o servidor não for interrompido após o tempo definido na variável `SHUTDOWN_WAIT`, a função força a interrupção da execução.
- `status`: Verifica o status do servidor JBoss AS. Retorna se o servidor está em execução, se está parado mas o arquivo PID existe, ou se está parado.

## Uso

O script aceita os seguintes comandos:

- `start`: Inicia o servidor JBoss AS.
- `stop`: Interrompe a execução do servidor JBoss AS.
- `restart`: Reinicia o servidor JBoss AS.
- `status`: Verifica o status do servidor JBoss AS.
- `reload`: Recarrega a configuração do servidor JBoss AS. Caso nenhum parâmetro seja passado, o script informa quais comandos estão disponíveis.