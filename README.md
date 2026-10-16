# monitoramento-sla-suporte
Automação que coleta os chamados e analisa a eficiência do atendimento ao cliente utilizando python, jira e powerbi. O script ira tratar os dados e
classifica-los de acordo com a sua prioridade e complexidade

# Ferramentas utilizadas: 

-> Python 3.12.10: Ira criar o script de automação que irá acessar a API, coletar os dados, tratar os dados e gerar planilhas para análise no powerbi.

-> PowerBI: Ira receber os dados tratados e montar os relatórios de eficiência do atendimento ao cliente.

-> Jira: Gerenciador de chamados que contera as informações utilizadas

-> API Jira: Ira ser a ponte de comunicação entre o python e o jira

-> Link para a documentação da API: https://developer.atlassian.com/cloud/jira/platform/rest/v3/intro/#expansion

# Itens necessários para a conexão com a API Rest do Jira

token: Token ira identificar o projeto que será acessado

senha_api: Senha de acesso para autenticação na API

email: Email do usuário registrado no Jira 

jira_url: url utilizada nas requisições a API.

# O que o python faz:

-> Consome os dados da API Rest do Jira

-> Ira transformar os dados em DataFrames para análise

-> Ira tratar e higienizar os dados retornados pela API

-> Ira gerar um log de erros caso ocorra algum erro na execução

-> Ira criar uma pasta que contera as planilhas de informações de cada
análise

-> Ira gerar as planilhas que irão alimentar o PowerBI

-> Classifica entre "SLA Cumprido", "SLA em Risco" e "SLA Estourado"

# Bibliotecas e Funções Utilizadas:
os: Ira criar diretórios e acessar variáveis de ambientes 

requests: Irá realizar requisições a API do Jira

HTTPBasicAuth: Ira realizar a autenticação do usuário usando as credenciais disponibilizadas
pelo Jira

dotenv: Ira carregar as variáveis de ambiente no código

datetime: Ira coletar a data e a hora do sistema

pandas: Ira tratar e análisar os dados
# O que o PowerBI faz: 

->  Calcula a taxa de resolução no primeiro contato (FCR)

-> Mostra os chamados pendentes por analista

-> Tempo Médio de Espera

-> Mapa de calor de volume de chamados por horário do dia.

-> Mostra a frequência de cada tipo de chamado.