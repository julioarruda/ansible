# Documentação do Código de Configuração

Este documento descreve as configurações do projeto de software. As configurações são listadas abaixo:

## Configuração de Licença (licence)
`aImpact_licence: "GFT_LICENCE"` - Esta configuração define a licença do projeto, neste caso, a licença é GFT.

## Configuração de Idioma (language)
`language: en` - Esta configuração especifica o idioma padrão do projeto. O valor 'en' especifica que o idioma padrão é inglês.

## Configuração Azure OpenAI
`isAzureOpenAI: true` - Esta configuração habilita a utilização do serviço Azure OpenAI.

`AzOpenAI:` - Este objeto contém as configurações específicas para a Azure OpenAI, incluindo:
- `endpoint: "AZ_OPENAI_ENDPOINT"` - Define o endpoint da API da Azure OpenAI.
- `token: "AZ_OPENAI_TOKEN"` - Define o token de autenticação para a API da Azure OpenAI.
- `engine: "AZ_OPENAI_ENGINE"` - Define o mecanismo da Azure OpenAI a ser usado.

## Configuração Fortify
`isFortify: false` - Esta configuração define se o serviço Fortify está habilitado ou não.

`Fortify:` - Este objeto contém as configurações específicas para o Fortify, incluindo:
- `url: ""` - Define a URL do servidor Fortify.
- `token: ""` - Define o token de autenticação para o servidor Fortify.
- `applicationId: ""` - Define o ID da aplicação no servidor Fortify.

## Configuração BitBucket
`isBitBucket: false` - Esta configuração define se o serviço BitBucket está habilitado ou não.

`BitBucket:` - Este objeto contém as configurações específicas para o BitBucket, incluindo:
- `token: ""` - Define o token de autenticação para o BitBucket.
- `repository: ""` - Define o repositório BitBucket associado.
- `basebranch: ""` - Define o branch base para o repositório BitBucket.

## Configuração GitHub
`isGitHub: true` - Esta configuração define se o serviço GitHub está habilitado ou não.

`GitHub:` - Este objeto contém as configurações específicas para o GitHub, incluindo:
- `token: "GITHUB_TOKEN"` - Define o token de autenticação para o GitHub.
- `repository: "GITHUB_REPOSITORY"` - Define o repositório GitHub associado.
- `basebranch: "GITHUB_BASE_REF"` - Define o branch base para o repositório GitHub.

## Configuração SonarCloud
`isSonarCloud: false` - Esta configuração define se o serviço SonarCloud está habilitado ou não.

`SonarCloud:` - Este objeto contém as configurações específicas para o SonarCloud, incluindo:
- `url: ""` - Define a URL do servidor SonarCloud.
- `token: ""` - Define o token de autenticação para o servidor SonarCloud.
- `componentKey: ""` - Define a chave do componente no servidor SonarCloud.

## Configuração de Resposta no Idioma
`Responda no Idioma: en` - Esta configuração define o idioma em que as respostas devem ser fornecidas, neste caso, inglês.