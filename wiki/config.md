# Documentação do Código

Este é o código de configuração utilizado para definir os parâmetros de diferentes serviços integrados em nosso projeto de software. 

## Variáveis

```yaml
aimpact_licence: "GFT_LICENCE"
language: pt-br
isAzureOpenAI: true
AzOpenAI:
  endpoint: "AZ_OPENAI_ENDPOINT"
  token: "AZ_OPENAI_TOKEN"
  engine: "AZ_OPENAI_ENGINE"
isFortify: false
Fortify:
  url: ""
  token: ""
  applicationId: ""
isBitBucket: false
BitBucket:
  token: ""
  repository: ""
  basebranch: ""
isGitHub: true
GitHub:
  token: "GITHUB_TOKEN"
  repository: "GITHUB_REPOSITORY"
  basebranch: "GITHUB_BASE_REF"
isSonarCloud: false
SonarCloud:
  url: ""
  token: ""
  componentKey: ""
Responda no Idioma: pt-br
```

## Descrição

- `aimpact_licence`: Esta é a chave de licença utilizada para autenticar o uso de determinado software ou recurso. Aqui, é usada a chave "GFT_LICENCE".

- `language`: Define a linguagem a ser usada. Neste caso, o valor é 'pt-br', indicando que o idioma padrão é o português do Brasil.

- `isAzureOpenAI`: Uma variável booleana que determina se a funcionalidade Azure OpenAI é ativada ou não. Neste caso, está ativada (`true`).

- `AzOpenAI`: Define as configurações para a integração com o Azure OpenAI. Isso inclui o endpoint, o token de acesso e o motor de IA a ser usado.

- `isFortify`: Uma variável booleana que indica se a funcionalidade Fortify está ativada ou não. Neste caso, está desativada (`false`).

- `Fortify`: Define as configurações para a integração com o Fortify, uma ferramenta de análise de segurança de código estático.

- `isBitBucket`: Uma variável booleana que indica se a funcionalidade BitBucket está ativada ou não. Neste caso, está desativada (`false`).

- `BitBucket`: Define as configurações para a integração com o BitBucket, uma ferramenta de controle de versão.

- `isGitHub`: Uma variável booleana que indica se a funcionalidade GitHub está ativada ou não. Neste caso, está ativada (`true`).

- `GitHub`: Define as configurações para a integração com o GitHub, uma plataforma de hospedagem de código-fonte com controle de versão usando git.

- `isSonarCloud`: Uma variável booleana que indica se a funcionalidade SonarCloud está ativada ou não. Neste caso, está desativada (`false`).

- `SonarCloud`: Define as configurações para a integração com o SonarCloud, uma ferramenta de inspeção contínua de qualidade de código.

- `Responda no Idioma`: Define o idioma no qual as respostas devem ser fornecidas. Neste caso, 'pt-br' indica que as respostas devem ser em português do Brasil.

As variáveis que estão com valores vazios ("") representam campos que devem ser preenchidos de acordo com as informações do usuário ou do projeto.