# Desafio

## Como testar

Para executar os testes basta executar os seguintes passos:

   `$ git clone https://github.com/DeyzianeCastelo/Desafio.git` -> Comando para puxar o projeto para a sua máquina.<br>
   `$ cd <sua-pasta>` -> Entrar na pasta do projeto.<br>
   `$ docker-compose --build` -> Contruir imagem. <br>
   `$ docker-compose up -d` -> Ligar servidor.
   
## Dependências

- Docker

## Instalação e Configuração
- Clone ou faça o download deste repositório `$ git clone https://github.com/DeyzianeCastelo/Desafio.git`
- Execute `cp .env` no Mac/Unix ou `COPY .env` no Windows
- Execute `docker-compose up -d` para buildar e criar os containers
- Execute `$ docker-compose up -d` Ligar servidor

### Importante
Sempre fique atento que não exista outro processo rodando nas portas 1106, 8000 e 3306, pois, serão as portas utilizadas ao executar o docker

### Testes
Para rodar os testes, após os containers estarem rodando, execute no seu terminal: vendor/bin/phpunit
   
## Material de Apoio
https://www.linkedin.com/pulse/como-criar-uma-api-restful-com-php-lumen-laravel-e-docker-luann-peixe/?originalSubdomain=pt
   
