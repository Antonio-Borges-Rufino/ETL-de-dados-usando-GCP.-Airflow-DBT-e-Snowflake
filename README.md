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
   - Complaint Type	-> Tipo de reclamação -> Tipo: Texto
   - Mediation Start Date	-> Inicio da mediação -> Tipo: Date & Time
   - Mediation Close Date	-> ->
Date mediation ended.
Date & Time
   - Complaint Result	-> ->
Outcome of mediation efforts. See Appendix A for further details about complaint results.
Plain Text
   - Satisfaction	-> ->
This section indicates whether the complaint was mediated to the satisfaction of both the business and consumer. See Appendix A for Yes, No, and NA assignments.
Plain Text
   - Restitution	-> ->
Total amount of consumer restitution secured through mediation.
Plain Text
   - Business Building	-> ->
The building number of the business’s address.
Plain Text
   - Business Street	-> ->
The street name of the business’s address.
Plain Text
   - Building Address Unit	-> ->
The unit number of the business’s address (e.g., Apartment/Suite/Other).
Plain Text
   - Business City	-> ->
The city where the business is located.
Plain Text
   - Business State	-> ->
The state where the business is located.
Plain Text
   - Business Zip	-> ->
The zip code where the business is located.
Plain Text
   - Complainant Zip	-> ->
The zip code where the individual who filed the complaint is located.
Plain Text
   - Longitude	-> ->
Plain Text
   - Latitude	-> ->
Plain Text
