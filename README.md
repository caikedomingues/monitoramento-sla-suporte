# monitoramento-sla-suporte
Automação que coleta os chamados e analisa a eficiência do atendimento ao cliente utilizando python, jira e powerbi.

# Ferramentas utilizadas: 

-> Python 3.12.10: Ira criar o script de automação que irá acessar a API, coletar os dados, tratar os dados e gerar planilhas para análise no powerbi.

-> PowerBI: Ira receber os dados tratados e montar os relatórios de eficiência do atendimento ao cliente.

-> Jira: Gerenciador de chamados que contera as informações utilizadas

-> API Jira: Ira ser a ponte de comunicação entre o python e o jira

# O que o python faz:

-> Consome os dados da API Rest do Jira

-> Ira transformar os dados em DataFrames para análise

-> Ira tratar e higienizar os dados retornados pela API

-> Ira criar uma pasta que contera as planilhas de informações de cada
análise

-> Ira gerar as planilhas que irão alimentar o PowerBI

-> Classifica entre "SLA Cumprido", "SLA em Risco" e "SLA Estourado"


# O que o PowerBI faz: 

->  Calcula a taxa de resolução no primeiro contato (FCR)

-> Mostra os chamados pendentes por analista

-> Tempo Médio de Espera

-> Mapa de calor de volume de chamados por horário do dia.

-> Mostra a frequência de cada tipo de chamado.