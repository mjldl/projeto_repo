## Criando Namespace
```bash

kubectl create namespace virtualizacao
```

## Instalando Helm Charts

Para instalar os charts com base nos arquivos 'mysql-wordpress-values.yaml' e 'wordpress-values.yaml' no namespace 'virtualizacao', execute:

### MySQL WordPress

```bash
helm install mysql-wordpress -f wordpress/mysql-wordpress-values.yaml bitnami/mysql --version '9.15.0' --namespace virtualizacao
```

### WordPress

```bash
helm install wordpress -f wordpress/wordpress-values.yaml bitnami/wordpress --version '19.0.4' --namespace virtualizacao
```

Obs: Ressalta-se que não foi criado portforward, de modo que o acesso foi através do CLI Browser Links: links http://[endereço ipv4 do wordpress svc]/ ; Executado no minikube (dentro do cluster).
