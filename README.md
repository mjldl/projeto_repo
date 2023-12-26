```markdown
# Instruções

## Criando o namespace 'virtualizacao':

```bash
kubectl create namespace virtualizacao
```

## Instalando charts

Para instalar os charts com base nos arquivos 'mysql-wordpress-values.yaml' e 'wordpress-values.yaml' no namespace 'virtualizacao', siga as instruções abaixo:

### MySQL WordPress

```bash
helm install mysql-wordpress -f wordpress/mysql-wordpress-values.yaml bitnami/mysql --version '9.15.0' --namespace virtualizacao
```

### WordPress

```bash
helm install wordpress -f wordpress/wordpress-values.yaml bitnami/wordpress --version '19.0.4' --namespace virtualizacao
```
