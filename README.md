# Sobre o projeto
1. Esse projeto tem como objetivo criar um pipeline de dados em regime de batch utilizando as principais ferramentas do mercado.
2. Esses dados devem ser disponibilizados diretamente para ferramentas analíticas, e deve conter tolerância a erros.
# Arquitetura de dados
![](https://github.com/Antonio-Borges-Rufino/ETL-de-dados-usando-GCP.-Airflow-DBT-e-Snowflake/blob/main/LSTM.png)
# Sobre o dataset
1. Os dados aqui utilizados podem ser acessados por [aqui](https://data.cityofnewyork.us/Business/Consumer-Services-Mediated-Complaints/nre2-6m2s).
2. Os dados estão separados nas seguinte colunas:
   - Business Name -> Nome da empresa contra qual foi feita a reclamação -> Tipo: Texto
   - Industry -> Categoria da empresa -> Tipo: Texto
   - Complaint Type -> Tipo de reclamação -> Tipo: Texto
   - Mediation Start Date -> Inicio da mediação -> Tipo: Date & Time
   - Mediation Close Date -> Final da mediação -> Tipo: Date & Time
   - Complaint Result -> Resultado da mediação -> Tipo: Texto
   - Satisfaction -> Se a mediação foi satisfatória para as partes -> Tipo: Texto
   - Restitution -> Total de restituição dada através da mediação -> Tipo: Texto
   - Business Building -> Número do prédio do endereço da empresa -> Tipo: Texto
   - Business Street -> Nome da rua do endereço da empresa -> Tipo: Texto
   - Building Address Unit -> Numero da unidade do endereço (apartamento, suite etc) -> Tipo: Texto
   - Business City -> A cidade onde está localizada a empresa -> Tipo: Texto
   - Business State -> O estado onde está localizada a empresa -> Tipo: Texto
   - Business Zip -> O CEP de onde a empresa está localizada -> Tipo: Texto
   - Complainant Zip -> O CEP de onde o indivíduo está localizado -> Tipo: Texto
   - Longitude	-> -> Tipo: Texto
   - Latitude -> -> Tipo: Texto

# Enviando o arquivo CSV para o cloud storage
1. Primeiro, crie o projeto que vai ser implementado o pipeline.
2. Após isso, crie um novo bucket de armazenamento utilizando o cloud storage, para mais informações clique [aqui](https://github.com/Antonio-Borges-Rufino/Build-an-ETL-Pipeline-for-Financial-Data-Analytics-on-GCP-IaC#criando-armazenamento-do-cloud-storage).
3. Agora é só enviar o arquivo para o bucket, para isso, clique no bucket recem criado e aperte para fazer upload da imagem.
4. ![image](https://github.com/Antonio-Borges-Rufino/ETL-de-dados-usando-GCP.-Airflow-DBT-e-Snowflake/assets/86124443/029b2128-0ab8-4bfb-b67c-f8c785b76cff)
5. Envie o arquivo e pronto.

# Instalando os recursos no compute engine do GCP
1. Clique [aqui](https://github.com/Antonio-Borges-Rufino/Build-an-ETL-Pipeline-for-Financial-Data-Analytics-on-GCP-IaC#configurando-vm-ubunto-no-gpc-fase-compute-engine) caso queira entender como habilitar e criar uma instancia VM no GCP.
2. Com a instância VM criada, podemos nos conectar via SSH pelo navegador, e lá vamos fazer as instalações.
3. Vamos primeiro dar um apt-get update para atualizar o repositório.
```
sudo apt-get update
```
4. Agora vou instalar o airflow, o padrão idela é cosntruir toda aplicação fora do super usuário, mas para facilitar, vou escrever ela toda no super usuário mesmo.
5. Existe algumas configurações interessantes para o airflow, como usar outros bancos de dados para a sua metastore, mas eu vou deixar com o banco de dados normal do airflow.
6. Vamos criar uma pasta no diretório central chamada airflow.
```
mkdir airflow
````
7. Agora vamos criar uma variavel global que aponte para essa pasta.
```
export AIRFLOW_HOME=~/airflow
```
8. Crie um ambiente virtual na pasta airflow e entre nele.
9. Agora instalamos a biblioteca
```
pip install "apache-airflow[celery]==2.8.0" --constraint "https://raw.githubusercontent.com/apache/airflow/constraints-2.8.0/constraints-3.8.txt"
```
10. Podemos executar o airflow usando o comando:
```
airflow standalone
```
11. Esse comando é apenas para ambientes de teste, não sendo considerado para produção.
12. Caso não consiga acessar o nifi, libere todas as portas usando o google cloud shell
```
gcloud compute --project="xxxxx" firewall-rules create "xxxxx" --direction=INGRESS --priority=1000 --network=default --action=ALLOW --rules=all --source-ranges=0.0.0.0/0
```
13. a
