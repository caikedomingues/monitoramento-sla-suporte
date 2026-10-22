# monitoramento-sla-suporte
Automação que coleta os chamados e analisa a eficiência do atendimento ao cliente utilizando python, jira e powerbi. O script ira tratar os dados e
classifica-los de acordo com a sua prioridade e complexidade

# Classificações das prioridades:

-> High(Alta): Exige solução rápida (até 24 horas)

-> Medium (Média): Prazo intermediário (até 72 horas)

-> Low(Baixa): Prazo maior (até 120 horas)

# Classificações do SLA:

-> SLA Cumprido: SLA cumprido dentro do prazo estabelecido (resolvido dentro das horas estabelecidas)

-> SLA em Risco: SLA próximo de estourar o prazo estabelecido (faltando 1 hora para ultrapassar o prazo estabelecido)

-> SLA Estourado: SLA estourado fora do prazo estabelecido (ultrapassou a quantidade de horas necessárias).

-> Em Andamento: O chamado ainda não foi resolvido.

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

-> Irá Classificar as tarefas entre "SLA Cumprido", "SLA em Risco" e "SLA Estourado" com base em seus status, prioridade e tempo de execução.

-> Ira criar uma pasta que contera as planilhas de informações de cada
análise

-> Ira gerar as planilhas que irão alimentar o PowerBI


# Bibliotecas e Funções Utilizadas:
os: Ira criar diretórios e acessar variáveis de ambientes 

requests: Irá realizar requisições a API do Jira

HTTPBasicAuth: Ira realizar a autenticação do usuário usando as credenciais disponibilizadas
pelo Jira

dotenv: Ira carregar as variáveis de ambiente no código

datetime: Ira coletar a data e a hora do sistema

pandas: Ira tratar e análisar os dados

# Tratamentos Realizados:
-> Registramos em logs todos os erros relacionados a conexões com API

-> Substituimos todos os valores nulos por valores padrões. Dessa forma,
não será necessário remove-los da base de dados

-> Convertamos as colunas de data e hora para o formato datetime

-> Criamos a coluna que conterá as classificações de cada tarefa.

# O que o PowerBI faz: 

->  Calcula a taxa de resolução no primeiro contato (FCR)

-> Mostra os chamados pendentes por analista

-> Tempo Médio de Espera

-> Mapa de calor de volume de chamados por horário do dia.

-> Mostra a frequência de cada tipo de chamado.