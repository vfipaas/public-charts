
# Helm Devportal Veecode

Tutorial de instalação do veecode/devportal via helm:

## Adicionando o repositorio helm

Para adicionar o repositorio com devportal execute o comando abaixo:

```bash
helm repo add veecode https://vfipaas.github.io/public-charts/
```
## Atualizando os repositorios helm
```bash
helm repo update
```
## Listando os repositorios
```bash
helm repo list
```
## Values da devportal

#### Gerando o yaml de values do devportal

```bash
  helm show values veecode/devportal > values.yaml
```
## Configurações :

| Parâmetro   | Tipo       | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
| `app.baseURL` | `string` | **Obrigatório**. DNS para frontend do devportal |
| `backend.baseURL`      | `string` | **Obrigatório**. DNS para Backend devportal |
| `auth.okta.clientid`      | `string` | **Obrigatório**. ID da credencial do Okta |
| `auth.okta.clientSecret`      | `string` | **Obrigatório**. Password da credencial do Okta |
| `auth.okta.audience`      | `string` | **Obrigatório**. Audience Okta  |
| `githubtoken`      | `string` | **Obrigatório**. Token para acesso ao projeto no Github |
| `githubSpecHouseURL`      | `string` | **Obrigatório**. URL do repo onde o devportal syncroniza as Specs |

## Instalando o devportal
```bash
helm install devportal veecode/devportal --values ./values.yaml
```
## Removendo o devportal
```bash
helm delete devportal
helm remove repo veecode
```
