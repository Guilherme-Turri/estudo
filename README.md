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
- Dados sao usados para aprender
- aprendizado atraves de um modelo
- apredizado deve ser melhorado e deve ser medido
- - ex : Marketing(qual cliente comprou ) Rh (qual o melhot candidato) Financas (prever vendas)
- Dividido basicamente em 4 tarefas:
- Classificacao
- - SIMPLES (Binária) -> Prever se chove (True False), tipo de animal(dog, cat, rat)
- MultiClasse -> tipo de animal(dog, cat, rat)
  
- Regressao
- - prever numero (quando o mkt vai vender a partir de um investimento)
- AgrupamentoA :grupar por caracteristicas semmelhantes pode ser Difuso = Cada elemento pertence o grupo segundo uma probabilidade. Modelo Hierarquico = permite que um grupo tenha subgrupos
- Associcao
- - Buscar elementos com caracateriscas em comum (carrinho de compra, quem compra a compra b)
 
 Classificao e regressao sao supervisionados (possui classe [resultado])
 Agrupamento e Associcao sao nao supervisionados

 Tarefa é diferente de tipo algoritimo que é diferente de Algoritimo
 ex: Classificacao != Bayes =! Naiive Bayes

 PREVISAO X AVALIACAO
 metodo HoldOut
 dados separa em dois grupos= 70% e 30%. 70% vao para treino -> classficador que gerado modelo. 30% vao pra testes e depos mesmo modelo gerado pelo classificador
 tem a previsao e pode se comprar a avaliacao.
 Classificador deve ser genérico, nao deve ser super ajustado (só funciona bem em treino) ou Subajustado,(Nao consegue boas taxas de previsao)

 Arvore de Devisao
-No Raiz
- No interno
- No terminais
- Algoritimo de particao : grau de pureza

 MAtriz de confusao = Verdadeiro Positivo x Falso Negativo X Falso Positivo x Verdadeiro Negativo

### Regressao Logistica
- Apenas dois estados S ou N. Variavel de resposta é binária.
Ex:
 Gasto em camapanha politica x ser eleito. Achar um Ponto que separa se vai ou nao. Gera PROBABILIDADE e partir dai, a resposta binária.


### Series Temporais
- Dados precisam de um ponto temporal: Deve ser relacionado a um intervalo regular de tempo dd/mm//yyy
- suppoe que exista alguma dependencia entre os intervalor

- proposito:
- - explicacao/compreeeensao de caracteristicas importantes
- - Previsao
  - Controle
ex de uso: Previsao tempo, Ocupacao Hotel, Epdemia
pode ser Estacionaria e nao estacionaria.

Pode ser usado algoritmos como ARIMA e SES, Dados mais prox influenciam mais na previsao

VALORES OBSERVADOS (lembrando que pode conter ou nao):
- Tendencia
- Sazaonalidade
- Aleatoriedade

### Regressao Linear
- Previsao com variavel numérica
- Regressao linear simples
- - 1 variável explanatória (eixo x) exmplica uma variável dependente(eixo y)
- Correlacao:
- - Se uma variavel aumenta (ou diminui), a outra tambem
- Previsao
- - Modelo que usa a 'linha de melhor ajuste'
- Residuo
- - Diferenca entre o valor real da variável e o valor da linha (reta) criada pelo modelo. Essa pode ser medida ( -, 0, +)
 - - Valor ajustado é o valor criado pela linha
- Outliers - Valor 'estourado', fora do padrao.
- - Deve avaliar se este dado deve ou nao fazer parte do modelo. verificar se nao e erro, ou caso atipico.
- Extrapolacao
- - Valor de previsao fora dos dados da variavel explanatória.
- Regressao linear Multipla
- - Duas ou mais variaveis explanatórias para prever a variaável dependente.

### Tecninca ensemble 
- Combina o resultado de muçtiploes modelos em busca de produzir um modelor melhor, sendo:
- 
- - Bagging -> Baseado em 'ensacamento': Separa o um dataset em varios dataset menores, a partir de cada ds menor se cria um modelo (arvore de decisao) que depois vai pro 'Votador'. Se for um problema de classifiacao normalmente se usa a maioria, se for um problema de regressao se usa a Média aritimetica. ex: Randon Forest.

 - Boosting: Baseado em Reforco, aprende com o proprio erro. Modelos sao adicionados sequencialmente até que seja minizado, ou atingir a qtd maxima de modelos
 - 
 - Stacking: Aprende combinar melhor a previsao de varios modelos.
 - -------------------------------------------------------

## CLOUD  AZURE = ANALISE/ML/IA
.....
------------------------------------------------------
## CRISP-DM
Metodologia life-cicle projeto Data Science.
- importante para Organizacao e Planejamento do processo.

### ENTENDIMENTO DO NEGOCIO <--> ENTENDIMENTO DOS DADOS -> PREPARACAO DOS DADOS <--> MODELAGEM --> AVALIACAO +-> IMPLEMENTACAO
<--> Mao dupla (pode ir e voltar fase/processo).
--> Mao unica (só avanca fase/processo). 
+-> Mao unica ou volta pra primeira fase/prcesso.


### Entendimento do Negocio:
- Objetivo do projeto: O que fazer com a base dase de dados? Dashboard? Campanha? Insight
- Critério de Sucesso: Será tralhado com a sua base dados
- Recursos e Contigenciamento: Definir equipe, como resgatar os dados, definir permissao de acesso.
- Objetivo do data Mining: Critérios de sucesso: qual sera a medicao: Acurácia? R², etc.
- Planejamento estrutural do Processo: Definir Prazos
.....

### Entendimento dos Dados:
(Geralmente segunda parte mais loonga)
- Definir variáveis a serem incluidas no projeti
- Definir se a base de dados é boa e resolve o problema levantado na primeira fase.
- Fazer analise exploratória dos dados
- Verificar a qualidade dos dados

### Preparacao dos Dados:
(Geralmente parte mais loonga)
- mao na massa
- transformar o data set original  no data set de modelagem (Selecao, limpeza, normalizacao)
- Criacao de novas variaveis se necessário
- Integracao dos dados/Formatacao: Faciliar acesso, organizacao, etc.

### Modelagem:
fase de escolha de tecnica. Ex: Ckuster? Regressao Linear, Logisita? (depende do que a base de dados oferece e o que se busca)
Após a construcoa do modelo, é feita a base de avaliacao. Ex: Accuracia? R²? (depende da tecnica escolhida) 
É comum voltar ao passo anterior.

### Avaliacao:
Rever criterios de sucesso e verificar se foi atendido. Rever o processo completo. Nessa parte pode voltar para o passo 1.

### Implementacao:
colocar em producao
- Planejamento de implatancao, monitoramento e Manutencao.
- Producao de Relatório final: Conter informacao para futura manutencao ou outro time queira usar.
Revisao Geral do PROCESSO.
--------------------------------------
