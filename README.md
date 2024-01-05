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

