# Sobre o projeto
Esse projeto foi desenvolvido utilizando docker. Na configuração do docker-compose existe três imagens no qual iniciará os respectivos containers: elasticsearch, kibana e logstash. O logstash utiliza o Jdbc Input Plugin para ler as informações do banco relacional e salvar no elasticsearch através do pipeline configurado.

<img src="https://assets.digitalocean.com/articles/elastic_1804/logstash_pipeline_updated.png" width="600">


## 1. Configurando Logstash
Abra o arquivo **logstash.conf** e altere conforme suas configurações de banco de dados.

## 2. Executando containers
> docker-compose -f stack-elk.yml up

## 3. Abra o painel do Kibana
> http://localhost:5601

Faça a consulta/search no elasticsearch para validar se sua tabela foi sincronizada com sucesso.
