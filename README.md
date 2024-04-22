# Polls App
Este é um aplicativo de enquetes que utiliza Docker Compose para orquestração de contêineres PostgreSQL e Redis.

## Pré requisitos:
* Docker
* Docker Compose

## Instalação e Execução
1. Clone o repositório para sua máquina local:
```bash
git clone https://github.com/seu-usuario/polls.git
```

2. Navegue até o diretório do projeto:
```bash
cd polls
```

3. Execute o Docker Compose para iniciar os serviços:
```bash
docker-compose up
```
4. Os serviços PostgreSQL e Redis estarão disponíveis nos seguintes endereços:
* PostgreSQL: **`postgresql://docker:docker@localhost:5432/polls`**
* Redis: **`redis://localhost:6379`**

## Rotas

* **GET /polls/:pollId:** Retorna os detalhes de uma enquete específica, incluindo suas opções e contagem de votos.
* **POST /polls:** Cria uma nova enquete com título e opções especificados no corpo da requisição.
* **POST /polls/:pollId/votes:** Registra um voto em uma opção de enquete específica.
* **GET /polls/:pollId/results:** Estabelece uma conexão WebSocket para receber atualizações em tempo real sobre os resultados de uma enquete específica.
