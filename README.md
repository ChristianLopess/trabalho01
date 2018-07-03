                 
# TRABALHO 01:  Semaforup
Trabalho desenvolvido durante a disciplina de Banco de Dados do Integrado

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Christian Lopes de Souza:christianlopessouza@gmail.com<br>
Gabriel de Souza Klier Conceição:desouzagabriel80@gmail.com<br>
...

### 2.INTRODUÇÃO E MOTIVAÇAO<br>
<br>e motivação da escolha realizada. <br>

> As formas de tirar uma carteira de habilitação nos dias atuais ficaram facilitadas, logo prevendo que a idade mínima é de 18 anos, logo a quantidade de pessoas que possuem veículos acabam por aumentar e assim tende a continuar.
Com a facilidade de comprar um veículo, usado ou novo, seja por meio de longos financiamentos ou não. Existem por volta de 42 milhões de Carteiras de Motoristas ativas no Brasil.
Com o forte avanço e o crescente número de veículos, as ruas devem estar devidademente preparadas para se adaptar a um grande volume de tráfego que varia diariamente dependendo do momento. Para isto, a forma de semáforos com tempo fixo já não vai ser a melhor proposta para conter o atraso no transito em função da demanda. Sendo assim, nosso trabalho visa o desenvolvimento de um semáforo inteligente e totalmente autônomo que conduza o tráfego de uma forma que atenda a demanda de veículos locais.
Em um cruzamento de duas ou mais vias existem movimentos que não podem ser feitos simultaneamente, pois podem se colidir, estabelencendo normas de controle de direito de passagem com o objetivo de melhorar o fluxo do tráfego e reduzir os riscos de acidentes.
 
 

### 3.MINI-MUNDO<br>

Entrevista com o usuário e identificação dos requisitos.<br>
Descrição textual das regras de negócio definidas como um  subconjunto do mundo real 
cujos elementos são dpropriedades que desejamos incluir, processar, armazenar, 
gerenciar, atualizar, e que descrevem a proposta/solução a ser desenvolvida.

> O sistema que foi proposto para o Semaforup, trata-se de um sistema simples que calcula proporcionalmente de 1 para 1 os semáforos cadastrados na base de dados. Os semáforos com essa tecnologia e esse software são chamados de "Semafobots", eles tem uma programação e a utilização de sensores que permitem calcular o tempo que outro semáforo vinculado irá ficar aberto. A informção é captada por um sensor que se localiza no chão paralelo ao semáforo, então, as informações relacionadas a quantidade de carros (fluxo) e velocidade média por minuto. 
>Com essas informações dentro da memória, todos os semáforos que tenham alguma relação ou vinculo, que esteja relacionada à algum cruzamento ou ruas que dependem do fluxo da outra. Logo é feita uma escala de 1 a 100 (percentual) em coparação de dois semafobots e fará um percentual do tempo limite que foi imposto à um semáforo - que é de 60 segundos - e dividirá proporcinalmente equivalente a média do fluxo de carros (por minuto) para cada uma dessas ruas. Em um exemplo para ficar mais claro .: Uma rua chama "AA" e outra rua chamada "BB", dentro de um minuto passaram 54 carros na Rua AA e 33 carros na Rua BB, sendo assim com essas informações, o software soma os valores das quantidade de carros (33+54=87) e dividem cada valor da Rua pelo todo (33/87=~38%), (54/87=~62%).  Agora tendo uma relação de 38(Rua AA) para 62(Rua BB), temos que 38% de 1 minuto ficará destinado para o semáforo referente a Rua AA e 62% destinado a Rua BB, sendo assim 22.8 e  37,2 segundos. 
>Há em caso de cruzamentos, relações específicas que fazem média com várias ruas, tendo uma base de dados maior para armazenar mais informações, um sistema híbrido para evitar acidente e diminuir a demora do transito. Haverá o semáfaro com uma configuração fixa, que será avaliada se será necessário a utilização desse recurso. A "configuaração fixa" é de um tempo fixo, determinada por ruas específicas ou ruas de modo geral, que por padrão são 30 segundos, mas podem ser alteradas ou cadastradas com tempo diferente.


### 4.RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>
Neste ponto a codificação não e necessária, somente as ideias de telas devem ser desenvolvidas. O princípio aqui é pensar na criação da interface para identificar possíveis informações a serem armazenadas e/ou descartadas <br>

Sugestão: https://balsamiq.com/products/mockups/<br>

![Alt text](https://github.com/semaforup/trabalho01/blob/master/imagens/img.png?raw=true "Famoso Mockup do Balq")
![Arquivo PDF do Protótipo Balsamiq feito para Empresa Devcom](https://github.com/semaforup/trabalho01/blob/master/arquivos/NewProject.pdf "Semaforup")


#### 4.1 TABELA DE DADOS DO SISTEMA:
    *feito*    
    
#### 4.2 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    a) Como fazer c om que não haja conflitos de semáforos abertos ao mesmo tempo na mesma tragetória?
    b) Como as informaçõs serão armazenadas para se adaptarem ao fluxo?,
    c) Como os operários do sistema de liberdade para alterarem quais funções?
    d) Como serão obtidas as informações necessárias para que os semáforos funcionem de forma inteligente? 
    e) Como é determinado qual via o semáforo deve permanecer mais tempo aberto? 
    *feito*
    
>## Marco de Entrega 01 em: (24/03/2018)<br>

### 5.MODELO CONCEITUAL<br>
    A) NOTACAO ENTIDADE RELACIONAMENTO 
        * Para nosso prótótipo limitaremos o modelo conceitual nas 5 principais entidades do escopo
        * O protótipo deve possui no mínimo duas relações N para N
        * o mínimo de entidades do modelo conceitual será igual a 5
        
![Alt text](https://raw.githubusercontent.com/semaforup/trabalho01/master/imagens/modelo_conceitual_empresa.png "Modelo Conceitual")
    
    B) NOTACAO UML (Caso esteja fazendo a disciplina de analise)
    C) QUALIDADE 
        Garantir que a semântica dos atributos seja clara no esquema
        Criar o esquema de forma a garantir a redução de informação redundante, possibilidade de valores null, 
        e tuplas falsas
    *feito*    
    
        
    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: [Nomes dos que participaram na avaliação]
    [Grupo02]: [Nomes dos que participaram na avaliação]
    *?*
## Marco de Entrega 01 em: (20/04/2018)<br>
#### 5.2 DECISÕES DE PROJETO
    [atributo]: [descrição da decisão]
    
    Campos de Código (cod_): são multivalorados que são majoritariamente únicos, sendo utilizados como atributos chave para localização e identificação, como são números de série, é importante que tivesse o atributo "int". 
    Campo data: utiliza o atributo "Date", propriamente utilizado para registro de datas, utilizado da forma simples contendo apenas dia,mês e ano [4 digitos]
    Campo minuto e hora: é um multivalorado que recebe um valor único, não utilizado como "hour" pois com esse campo será feito cálculos utilizando outros campos multivalorados "int"
    Campo Quantidade (quant_): são multivalores que servem como contadores, que se atribuem +1 a cada carro identificado em sua passagem pelos sensores do semáforo
    Campo senha e Usuário: são valores compostos, permitido o uso de caracteres e valores numéricos, principamente em senhas para fortalecer a proteção da senha, qualquer invasão poderia acarretar sérios danos ao trânsito
    Campo Nomes (bairro_,cidade_,rua_): São valores atribuidos apenas a caracteres (50), o sistema dos semáforos trabalham com os códigos delas e são passadas ao sistema como um valor simples, não serão utilizados para cálculos
    *feito*


#### 5.3 DESCRIÇÃO DOS DADOS 

    numero_semaforo: campo que armazena numero de localização do Semáforo<br>
    rua_semaforo: campo que armazena o nome da rua onde o semaforo se localiza.<br>
    bairro_semaforo: campo que armazena o nome do bairro onde o semaforo se localiza.<br>
    cidade_semaforo: campo que armazena o nome da cidade onde o semaforo se localiza.<br>
    cod_rua: código referente a uma determinada rua
    cod_bairro: código referente a um determinado bairro
    cod_cidade: código referente a uma determinada cidade
    cod_geral: código de localização que junta os códigos cidade,bairro e rua
    minuto: armazena o minuto em que a analise dos dados de contagem de carros e cálculos que foram feitos, usado para media por minuto,
    hora: armazena a hora em que a analise dos dados de contagem de carros e cálculos que foram feitos,usado para media por hora
    quant_semaforo_vinc: quantidade de semáforos que estão vinculados a esse semáforo, no caso, para estabelecerem conexão entre si e não haver incompatibilidade no tráfego, trocam informações entre si.
    quant_carro_rua_min: armazena a quantidade de carros que passam em determinada rua por minuto
    quant_carro_hr_med: armazena a quantidade de carros que passam em determinada rua por hora, já fazendo a média geral
    med_quant_carros_dia: armazena a quantidade de carros que passaram em um determinado dia a partir de 00:00, baseado nas médias por hora
    data_analise: armazena o dia,mês e ano em que a verificação/análise faz, no caso a cada minuto
    tempo_fechado: baseado nas informações captadas e nos cálculos efetuados, o tempo que determinado semáforo ficará fechado
    nome_usuario_comum: armazena nome de usuario de um usuário comum, que utiliza o sistema apeenas para visualizar
    senha_usuario_comum: armazena senha referente ao usuario comum registrado
    cod_usuario: codigo de identificação referente ao usuário comum registrado
    nome_operario: armazena nome de usuário de um operário do sistema que tem permissões para alterar dados no sistema, como tempo do semáforo, limite do tráfego,etc.
    senha_operario: armazena senha referent ao operário cadastrado
    cod_operario: codigo de identificação referente ao operario comum cadastrado
    *feito*
    
    
    
    
>## Marco de Entrega 01 em: (12/05/2018)<br>
### 6	MODELO LÓGICO<br>
        a) inclusão do modelo lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)

### 7	MODELO FÍSICO<br>
        a) inclusão das instruções de criacão das estruturas DDL 
        (criação de tabelas, alterações, etc..)          
        
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
#### 8.1 DETALHAMENTO DAS INFORMAÇÕES
        a) inclusão das instruções de inserção dos dados nas tabelas criadas pelo script de modelo físic
        b) formato .SQL

#### 8.2 INCLUSÃO DO SCRIPT PARA CRIAÇÃO DE TABELA E INSERÇÃO DOS DADOS
        a) Junção dos scripts anteriores em um único script 
        (create para tabelas e estruturas de dados + dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL
#### 8.3 INCLUSÃO DO SCRIPT PARA EXCLUSÃO DE TABELAS EXISTENTES, CRIAÇÃO DE TABELA NOVAS E INSERÇÃO DOS DADOS
        a) Junção dos scripts anteriores em um único script 
        (Drop table + Create de tabelas e estruturas de dados + dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL


### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Incluir para cada tópico as instruções SQL + imagens (print da tela) mostrando os resultados.<br>
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>
#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    b) Criar no mínimo 3 consultas com operadores aritméticos 
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas
#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.


    
#### 9.5	ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>


#### 9.6	CONSULTAS COM JUNÇÃO E ORDENAÇÃO (Mínimo 6)<br>
        a) Uma junção que envolva todas as tabelas possuindo no mínimo 3 registros no resultado
        b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho
        

## Marco de Entrega 02 em: (16/06/2018)<br>
### ATUALIZAÇÃO DA DOCUMENTAÇÃO DOS SLIDES PARA APRESENTAÇAO SEMESTRAL (Mínimo 6 e Máximo 10)<br>
<br>
    Data de Entrega: (30/06/2018)
<br>

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>

#### 9.8	CONSULTAS COM LEFT E RIGHT JOIN (Mínimo 4)<br>
#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho
#### 9.10	SUBCONSULTAS (Mínimo 3)<br>

#### 9.11	LISTA DE CODIGOS DAS FUNÇÕES E TRIGGERS<br>
        Detalhamento sobre funcionalidade de cada código.
        a) Objetivo
        b) Código do objeto (função/trigger)
        c) exemplo de dados para aplicação
        d) resultados em forma de tabela/imagem
<br>


#### 9.12	GERACAO DE DADOS (MÍNIMO DE 100 MIL REGISTROS PARA PRINCIPAL RELAÇAO)<br>
        a) principal tabela do sistema deve ter no mínimo 100 mil registros
        b) tabelas diretamente relacionadas a tabela principal 10 mil registros
        c) tabelas auxiliares de relacao multivalorada mínimo de 10 registros
        d) registrar o tempo de inserção em cada uma das tabelas do banco de dados
        e) especificar a quantidade de registros inseridos em cada tabela
        Para melhor compreensão verifiquem o exemplo na base de testes:<br>
        https://github.com/discipbd2/base-de-testes-locadora
        

#### 9.13	Backup do Banco de Dados<br>
        Detalhamento do backup.
        a) Tempo
        b) Tamanho
        c) Teste de restauração (backup)
        d) Tempo para restauração
        e) Teste de restauração (script sql)
        f) Tempo para restauração (script sql)
<br>

Data de Entrega: (Data a ser definida)
<br>

#### 9.14	APLICAÇAO DE ÍNDICES E TESTES DE PERFORMANCE<br>
    a) Lista de índices, tipos de índices com explicação de porque foram implementados nas consultas 
    b) Performance esperada VS Resultados obtidos
    c) Tabela de resultados comparando velocidades antes e depois da aplicação dos índices (constando velocidade esperada com planejamento, sem indice e com índice Vs velocidade de execucao real com índice e sem índice).
    d) Escolher as consultas mais complexas para serem analisadas (consultas com menos de 2 joins não serão aceitas)
    e) As imagens do Explain devem ser inclusas no trabalho, bem como explicações sobre os resultados obtidos.
    f) Inclusão de tabela mostrando as 10 execuções, excluindo-se o maior e menor tempos para cada consulta e 
    obtendo-se a media dos outros valores como resultado médio final.
<br>
    Data de Entrega: (Data a ser definida)
<br>   

### 10	ATUALIZAÇÃO DA DOCUMENTAÇÃO DOS SLIDES PARA APRESENTAÇAO FINAL (Mínimo 6 e Máximo 10)<br>
<br>
    Data de Entrega: (Data a ser definida)
<br>

### 11 Backup completo do banco de dados postgres 
    a) deve ser realizado no formato "backup" 
        (Em Dump Options #1 Habilitar opções Don't Save Owner e Privilege)
    b) antes de postar o arquivo no git o mesmo deve ser testado/restaurado por outro grupo de alunos/dupla
    c) informar aqui o grupo de alunos/dupla que realizou o teste.

    
### 12	TUTORIAL COMPLETO DE PASSOS PARA RESTAURACAO DO BANCO E EXECUCAO DE PROCEDIMENTOS ENVOLVIDOS NO TRABALHO PARA OBTENÇÃO DOS RESULTADOS<br>
        a) Outros grupos deverão ser capazes de restaurar o banco 
        b) executar todas as consultas presentes no trabalho
        c) executar códigos que tenham sido construídos para o trabalho 
        d) realizar qualquer procedimento executado pelo grupo que desenvolveu o trabalho

### 13	DIFICULDADES ENCONTRADAS PELO GRUPO<br>  

    
>## Marco de Entrega 04/Entrega Final em: (Data definida no cronograma)<br>

       
### 14  FORMATACAO NO GIT: https://help.github.com/articles/basic-writing-and-formatting-syntax/
<comentario no git>
    
##### About Formatting
    https://help.github.com/articles/about-writing-and-formatting-on-github/
    
##### Basic Formatting in Git
    
    https://help.github.com/articles/basic-writing-and-formatting-syntax/#referencing-issues-and-pull-requests
   
    
##### Working with advanced formatting
    https://help.github.com/articles/working-with-advanced-formatting/

#### Mastering Markdown
    https://guides.github.com/features/mastering-markdown/

### OBSERVAÇÕES IMPORTANTES

#### Todos os arquivos que fazem parte do projeto (Imagens, pdfs, arquivos fonte, etc..), devem estar presentes no GIT. Os arquivos do projeto vigente não devem ser armazenados em quaisquer outras plataformas.
1. Caso existam arquivos com conteúdos sigilosos, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário deste GIT, para acompanhamento do trabalho.

#### Os usuários criado GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://sis4.com/brModelo/brModelo/download.html
<br>


Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?r
