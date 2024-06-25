# Curso sobre Micro Serviços com Kubernets

## Trata-se de um serviço de votos onde

- O voto é recebido em um app python;

- Guardado em um banco REDIS;

- Um app .Net fica escutando o banco REDIS e redireciona o voto ao BD POSTGRESSQL;

- Por fim, o voto é exibido por um app em Node.js.

## Como usar

### Resetar o minikube

```bash
minikube delete
minikube start
```

### Ordem de criação

1. namespace
2. deployment
3. service

### Comandos de criacao

```bash
kubectl create -f deployments/ --save-config --record
```

Cria todos os deploys dentro da pasta deployment

### Comandos de busca

```bash
kubectl get all -n vote # vote = nome do namespace
kubectl logs -p *nome do pod*
```

```bash
minikube service result --url -n vote # busca a url do servico result
```
