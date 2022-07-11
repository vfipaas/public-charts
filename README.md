
# Helm Devportal Veecode

Tutorial de instalação do veecode/devportal via helm:

## Adicionando o repositorio helm

Para adicionar o repositorio com devportal execute o comando abaixo:

```bash
helm repo add veecode https://vfipaas.github.io/public-charts/
```
## Atualizando os repositorios helm:
```bash
helm repo update
```
## Listando os repositorios:
```bash
helm repo list
```
## Instalando o devportal:
```bash
helm install devportal veecode/devportal
```
## Removendo o devportal:
```bash
helm delete devportal
helm remove repo veecode
```
