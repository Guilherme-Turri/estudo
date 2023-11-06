# DATA/AI

## Armazenamento X Processamento

### DataLake x Data Warehouse x Data Base

- Data Lake (Macro) -> Repo que armazena grande qtd de dados variados, brutos nativos (nao refinados). Pode conter dados estruturados (tabelas), Nao Estruturados(audio, video) e semi estruturados (JSON. pode ser usado para fazer consultas, analise preditivas, com grande enfoque em ML.

- Data Warehouse (Macro) -> Repo que armazena a 'fonte da verdade', tb com grande qtd de dados, porem unificados, categorizados e organizados.
Facilita consulta pois possui dados centralzado. -> Modelo Dimensinal, grande enfoque em BI.

- Data Base - (Micro). Esquema para produto, Relacional e Nao relacional (SQL x Nosql). Consulta referente ao produto, nao ao negócio.
 

### Hadoop
- Gestao de grande volume de dados (Big Data), baseado em cluster -> Conjunto de servidores interligados e distribuidos.
- Criado para rodar On Premisse. utilizado em ML, Analise e Mineracao.


### Apache Spark
- Engine para grande processamento de dados de larga escala (Estruturado, !Estruturado, SemiEstruturado E Grafo.)
- Compilacao em cluster, utiliza processamento em memória
- Forte ETL
- Grande vantagem a velocidade, e possui varias cargas de trabalho: Analise em tempo real, Aprendizado de máquina, possui API para JAVA, Py, etc. Pode ser usado com Hadoop, Kubernets, etc

### DataBrics
- Solucao BIG DATA, ferramenta de processamento de dados em Nuvem Publica.
 
- Possibilitas usar Apache Spark/Py/Sql de forma segura e otimizada.

- Automatiza processo de ETL, Governa acesso a dados. Interacao por Notebooks (ipynb)

- Util para Analise BI, Data Science/ML, RealTime Application.

## CLOUD  AZURE = Armazenamento X Processamento

### Azure SQL
- PASS de BD, podennto provisionar as caracteriscas, tamanho., DTU, ETC.
- custo inicial baixo (capex x Opex) 

### Azure CosmosDB
-Solucao NoSQL - > modelagem por "documento, que pode ter documento filho (JSON)
- Cosmo Container - > Particao com chave (id) onde 'dentro' possui os documentos.
- fornece api facilitar consultas ( escrever SQL, Mongo, Gremlim[grafos] dentro do cosmos)
- integracao com outros servicos Azure-> Functions, EKS, IoT.
- baseado em requests (Trhowputs)

### Azure postgres
- Daas (DataBse as a service)
- SGBD com escalabilidade, seguranca e preco. (Relacional), roda tanto com VM, Docker, etc. 

### Azure DataLake
- Serviço DatLake Azure, como vantagem escalabilidade e performance. Pode ser usado em ampla gama de aplicacoes -> Analise, mineracao, big data, ml
- Versatilidade, suporta qualquer tuio de dado. sendo estruturado ou nao

### Azure DataFactory
- Ferramenta ETL Azure, cria facilmente pipelines gerenciaveis.
- Ingestao de dados em Batch (nao suporta real time)
- - Interage com Repo Git, focanado mais 'seguro' caso queira voltar para versao mais antiga.
- Possui data flow que que abstrai ferramentas integradas (Spark, Py, Scala, etc.)

### Azure Sinapse Analitics
- Servico de Analise de Dados Unificada.
- Possui IA integrada: Recursos proprios para auxiliar.
- Versátil para tipos de dados.
- Pode treinar modelos, indentificar padroes (mineracao de dados)
- Necessita DataLake para alimentar.

### Azure DataBrics
- Plataforma analise de dados Microsoft baseado no Apache Spark
- Oferece ID, suporta Py, Scala, R, Etc
- Baseado em Pay to use.
- Muito usado dados para treinamento de ML.

| Ingestao (Kafka, Hub) -------> Armazenamento (Blob, DataLake) ------> Preparacao e Treinanmento (DataBrics/ML )----->Modelo e Dispocicao (DB)

### Azure HDInsights
- Implementacao Hadoop da Microsoft, servico PaaS
- gerencia ciclo de vida dos clusters (provisionamento, config, etc)
- pode ser integrado com outros servicos Azure (Db, DataLake, ML)
- pode escolher o tipo de cluster

### Azure EventHub
- Servico de ingestao de dados em tempo real de qualquer fonte
- dados podem ser processados por outros servicos azure
- elasticidade conforme a quts de dados

### Azure Stream Analitics
- Service Azure que pode analizar em tempo real os dados.
  | Dipositivo IoT ----> Azure Event Hub ---> Azure Stream Analitics.

-----------------------------------------

## ANALISE/ML/IA
### Machine Learning
- Uso de algoritmos para treinar sistemas a identificar padrões e tomar decisões com base nos dados.

### Mineração de Dados (Data Mining)
-Processo de descobrir padrões, relações e informações úteis nos dados, muitas vezes usando algoritmos de aprendizado de máquina.

### Análise de Séries Temporais:
- Trata da análise de dados que variam ao longo do tempo, sendo comum em previsão e modelagem de tendências.

### Análise de Regressão:
- Examina a relação entre variáveis independentes e dependentes para fazer previsões ou entender a influência de uma variável sobre outra.

### Análise de Risco (Risk Analysis):
- Avalia a probabilidade e o impacto de eventos incertos com base em dados históricos.

### Análise de Sentimento (Sentiment Analysis):
- Classifica o sentimento expresso em dados textuais, geralmente em relação a produtos, serviços ou tópicos específicos.

### Aprendizado Supervisionado
- Um tipo de aprendizado de máquina em que os algoritmos são treinados com um conjunto de dados rotulados, ou seja, os exemplos de entrada estão associados a saídas desejadas. O objetivo é fazer previsões ou classificações com base nesses exemplos.

### Aprendizado Não Supervisionado
- Nesse tipo de aprendizado, os algoritmos analisam dados não rotulados para descobrir padrões, estruturas ocultas ou segmentações nos dados. Isso inclui tarefas como clustering e redução de dimensionalidade.

### Redes Neurais Artificiais (Artificial Neural Networks):
- Modelos inspirados na estrutura do cérebro humano, compostos por neurônios artificiais interconectados, usados em tarefas de aprendizado profundo.

### Aprendizado Profundo (Deep Learning):
- Uma subárea do aprendizado de máquina que utiliza redes neurais profundas (com várias camadas) para aprender características e representações complexas dos dados, frequentemente usado em visão computacional, processamento de linguagem natural e muito mais.

### Validação Cruzada (Cross-Validation):
- Técnica usada para avaliar o desempenho do modelo, dividindo os dados em conjuntos de treinamento e teste múltiplas vezes para evitar o viés na avaliação.


## CLOUD  AZURE = ANALISE/ML/IA
.....
