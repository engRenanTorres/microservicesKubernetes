# Curso sobre Micro Serviços com Kubernets

## Trata-se de um serviço de votos onde

- O voto é recebido em um app python;

- Guardado em um banco REDIS;

- Um app .Net fica escutando o banco REDIS e redireciona o voto ao BD POSTGRESSQL;

- Por fim, o voto é exibido por um app em Node.js.
