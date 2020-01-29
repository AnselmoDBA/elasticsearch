# Lab 2 - Ingestão de dadaos via Logstash e Criação de dashboard no Kibana:

## Baixando o conteúdo desse repositório:

```
cd ~
git clone https://github.com/AnselmoDBA/elasticsearch.git
```
## Descompactando o arquivo de dados.
```
cd elasticsearch/
tar zfxv cars.tar.gz
```

## Instalação do Logstash:
Baixando o Logstash e descompactando:
```
wget https://artifacts.elastic.co/downloads/logstash/logstash-7.5.2.tar.gz
tar zfxv logstash-7.5.2.tar.gz
mv logstash-7.5.2 logstash
```

## Editando arquivo de configuração:
Agora vamos editar o arquivo de configuração para ingestão do logstash alterando o host onde serão inseridos os dados. Editar também o caminho onde está disposto o cars.csv
```
vim ~/elasticsearch/logstash-cars.config
```
Editar os seguintes campos:
* path - 
* host - O host da sua maquina virtual que você pega no Strigo.

## Rodando o Logstash e monitorando a entrada dos dados:
```
~/logstash/bin/logstash -f ~/elasticsearch/logstash-cars.config
```
