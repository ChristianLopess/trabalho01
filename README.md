# TRABALHO 01:  Semaforup
Trabalho desenvolvido durante a disciplina de Banco de Dados do Integrado

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Christian Lopes de Souza:christianlopessouza@gmail.com<br>

...

### 2.INTRODUÇÃO E MOTIVAÇAO<br>
Este documento contém a especificação do projeto do banco de dados <semaforup> 
<br>e motivação da escolha realizada. <br>

> O projeto Semaforup tem como princípio melhorar o trânsito, deixando-o mais fluido e mais rápido. A sincronização dos semáforos de um percurso para evitar interromper o trânsito em cada esquina. A nova tecnologia também permite que um operador de trânsito opere os sinais por meio de computadores ou mesmo de um celular. A possibilidade é útil, por exemplo, para orientar desvios no trânsito, colocar os sinais no piscar amarelo ou acionar o verde e o vermelho por tempo indeterminado. Sua utilidade não irá só agilisar os motoristas, assim também, como  os pedestres, que em grandes avenidas movimentas não precisarão esperar um grande tempo para atravessar a rua. Os sensores, com sua eficiência captarão, por meio de sensores a movimentação de pedestres e veículos, evitando acidentes e simultaneamente prezando pela rapidez e dinamização.
 

### 3.MINI-MUNDO<br>

Descrever o mini-mundo! (Não deve ser maior do que 30 linhas) <br>
Entrevista com o usuário e identificação dos requisitos.<br>
Descrição textual das regras de negócio definidas como um  subconjunto do mundo real 
cujos elementos são propriedades que desejamos incluir, processar, armazenar, 
gerenciar, atualizar, e que descrevem a proposta/solução a ser desenvolvida.

> O sistema proposto para o semafobot trata-se de um sistema integrado a câmeras próprias capazes de analisar a movimentação de veículos em cada uma das vias de um cruzamento; e, a partir dos dados, tomar automaticamente decisões para melhorar o fluxo na via mais carregada. Na prática cotidiana, ele ajustará o sinal para permanecer aberto por mais tempo onde há maior demanda e fechar mais rapidamente quanto for oportuno, marcadores no asfalto contam a passagem dos veículos e os dados são enviados para um banco de dados, que calcula quanto tempo os sinais devem ficar abertos e fechados. A informação é utilizada por um controlador para fazer o ajuste.Todos os dados e imagens coletadas pelos semafobot's serão enviadas para o nossos bancos de dados, de lá, os técnicos farão o acompanhamento das condições para também realizar intervenções manuais.


### 4.RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br> ✔
Neste ponto a codificação não e necessária, somente as ideias de telas devem ser desenvolvidas. O princípio aqui é pensar na criação da interface para identificar possíveis informações a serem armazenadas e/ou descartadas <br>

Sugestão: https://balsamiq.com/products/mockups/<br>

![Alt text](https://github.com/semaforup/trabalho01/blob/master/imagens/img.png?raw=true "Title")
![Arquivo PDF do Protótipo Balsamiq feito para Empresa Semaforup](https://github.com/semaforup/trabalho01/blob/master/arquivos/NewProject.pdf?raw=true "Empresa Semaforup")


#### 4.1 TABELA DE DADOS DO SISTEMA: ✔  
![Tabela](https://github.com/semaforup/trabalho01/blob/master/arquivos/TabelaSemaforup%20(1).xlsx "Modelo Conceitual")    
    
    
#### 4.2 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO? ✔
1)qual a quantidade de veículos que passam em um determinado semáforo em um ano?
2)em quais locaos houve maior quantidade de veículos em uma semana?
3)quantos usuários acessaram o sistema em 3 dias?
4)quantos semáforos há em um determinado bairro?
5)quantos carros ultrapassaram uma determinada velocidade em determinado logradouro?


### 5.MODELO CONCEITUAL<br> ✔
        
![Alt text](https://github.com/semaforup/trabalho01/blob/master/imagens/Conceitual.png?raw=true "Modelo Conceitual")   
        
    
#### 5.1 Validação do Modelo Conceitual ✔
[Grupo 01] : [Júlia Ferreira, Kézia Souza, Mariana Poli]
[Grupo 02] : [Rafael Rodriguez, Leonardo Fafá]


#### 5.2 DECISÕES DE PROJETO ✔
    esta_em: A opção de usar uma tabela que guarde as informações separadas das localidades pois podem haver locais  com os mesmo nomes
    SENSOR: A opção de usar uma tabela que guarde todas as informações de carros captados pois as informações altera
    CAPTURA: A opção de captura acontece a cada vez que um carro passa no sensor 
    SEMAFORO: A opção de ter a tabela semáforo pois ela é a principal onde as ideias circulam
    USUARIO: A opção de usar uma tabela que guarde as informações dos usuarios 

#### 5.3 DESCRIÇÃO DOS DADOS ✔
    comum: Campo que identifica o tipo de usuario como comum
    operario: Campo que identifica o tipo de usuario como operario
    cod_usuario: Campo único de identificação de um usuario
    nome_usuario: Campo que que armazena os nomes dos usuarios
    senha_usuario: Campo que armazena as senhas de determinado usuario
    email: Campo que armazena os emails de determinado usuario
    telefone: Campo que armazena os telefones de determinado usuario
    sexo: Campo que armazena o tipo de gêneros
    cod_cidade: Campo que armazena o código de identificação referente ao cidade em que o semáforo foi localizado
    cod_bairro: Campo que armazena o código de identificação referente ao bairro em que o semáforo foi localizado
    cod_logradouro: Campo que armazena o código de identificação referente ao logradouro em que o semáforo foi localizado
    velocidade: Campo que guarda a velocidade média dos veículos
    tempo_fechado: Campo que armazena o tempo, baseado nos cálculos , que o semáforo ficará fechado
    latitude: Campo que armazena posição Y de localização
    longitude: Campo que armazena posição X de localização
    dia: Campo que guarda a informação do dia que o carro passou na captura
    mes: Campo que guarda a informação do mês que o carro passou na captura
    ano: Campo que guarda a informação do ano que o carro passou na captura
    hora: Campo que guarda a informação da hora que o carro passou na captura
    minuto: Campo que guarda a informação do minuto que o carro passou na captura
    data_captura: Campo que guarda a informação de data e hora que o carro passou na captura
    cod_sensor: Campo que armazena o código dos sensores relacionados ao semáforo
    modelo: Campo que armazena o modelo dos sensores
    tempo_aberto:Campo que armazena o tempo, baseado nos cálculos , que o semáforo ficará aberto
    

### 6	MODELO LÓGICO<br>✔
![Alt text](https://github.com/semaforup/trabalho01/blob/master/imagens/L%C3%B3gico.PNG?raw=true "Modelo Lógico")

### 7	MODELO FÍSICO<br>✔
    CREATE TABLE USUARIO(
        tipo char(1),
        cod_usuario int PRIMARY KEY,
     nome_usuario varchar(40),
        senha_usuario varchar(40),
        email varchar(60),
        telefone char(9),
        sexo char(1)
    )

    CREATE TABLE SEMAFORO(
        tempo_aberto int,
        tempo_fechado int,
        latitude int,
        longitude int,
        cod_semaforo int PRIMARY KEY,
        cidade int,
        bairro int,
        logra int 
    )

    CREATE TABLE CAPTURA(
        data_captura timestamp PRIMARY KEY,
        dia int,
        mes int,
        ano int,
        hora int,
        minuto int,
        velocidade int,
        cod_semaforo int,
        cod_sensor int
    )

    CREATE TABLE mapa(
        cidade int,
        desc_cidade varchar(40),
        bairro int,
        desc_bairro varchar(40), 
        logra int,
        desc_logra varchar(40),
        cep int PRIMARY KEY,
     cod_semaforo int
    )

    CREATE TABLE SENSOR(
     latitude int,
     longitude int,
     cod_sensor int,
     modelo varchar(20))        
        
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
#### 8.1 DETALHAMENTO DAS INFORMAÇÕES
    insert into usuario values
    ('c',1010,'Renato','re12345','renat@email.com',999043437,'M'),
    ('c',2020,'Cláudio','clsa3232','claudio@email.com',994387292,'M'),
    ('c',3030,'Erick','hehehe','erick@email.com',999982493,'M'),
    ('c',4040,'Flávia','flavinha332','flavia@email.com',869979054,'F'),
    ('o',5050,'Geoavana','88776','geova@email.com',987765543,'F'),
    ('c',6060,'Brenner','cabecademelao','brenner@email.com',977698985,'M'),
    ('o',7070,'Nenê','ostempos','nena@email.com',999043437,'M'),
    ('c',8080,'Aguirre','2001','guirre@email.com',999043437,'M'),
    ('o',9090,'Adriana','33412333','adrinaa@email.com',999043437,'F'),
    ('c',2220,'Fabíola','291201','fabii@email.com',99869953,'F'),
    ('o',2300,'Iana','Ch923','iana@email.com',898908964,'F'),
    ('c',3320,'Felipe','0337','felipe@email.com',999999778,'M'),
    ('c',3220,'Jandira','12222227','jandira@email.com',978747868,'F'),
    ('c',3430,'Reinaldo','bananananica','reinld@email.com',998775945,'M'),
    ('c',3310,'Marta','polentafrita','mart@email.com',988765435,'M')
    
    insert into mapa values 
    (01,'N.Venécia',001,'Mizacity',0015,'Rua da Madeira',010010015,010),
    (02,'Cariacica',002,'Campo Grande',0001,'Rua Dois',010020001,020),
    (02,'Cariacica',002,'Campo Grande',0002,'Rua Barracada',010020002,030),
    (02,'Cariacica',004,'Cobilândia',0003,'Rua Rei',020040003,040),
    (02,'Cariacica',005,'Duandra',0004,'Rua Catupiry',020050004,050),
    (03,'Vitória',006,'Vitorinha',0005,'Av da Penha',030060005,060),
    (03,'Vitória',007,'Mouchoara',0006,'Rua Taquara',030070006,070),
    (03,'Vitória',008,'Centro',0007,'Rua Santo Antonio',030080007,080),
    (03,'Vitória',009,'Penha',0008,'Nossa Senhora',030090008,090),
    (03,'Vitória',010,'Marataises',0009,'Rua Moreira',030100009,100),
    (04,'Serra',011,'Porto Canoa',0010,'Av Mata da Serra',040110010,110),
    (04,'Serra',012,'Serra Dourada',0011,'Rua Trombeta',040120011,120),
    (04,'Serra',013,'Serra Dourada 2',0012,'Rua Japurá',040130012,130),
    (04,'Serra',014,'Porto Dourado',0013,'Rua Centopeia',040140013,140),
    (05,'Vila Velha',015,'Bicanga',0014,'Bairro da Paz',050150014,150) 

    insert into semaforo values
    (30,30,3213,4234,010,'01','001','0015'),
    (15,45,7341,8743,020,'02','002','0001'),
    (12,48,1239,0976,030,'02','002','0002'),
    (50,10,4543,1280,040,'02','004','0003'),
    (32,28,1321,4313,050,'02','005','0004'),
    (45,5,5433,1233,060,'03','006','0005'),
    (30,30,4640,7688,070,'03','007','0006'),
    (30,30,5775,4986,080,'03','008','0007'),
    (31,39,8676,6877,090,'03','009','0008'),
    (20,40,3213,0746,100,'04','010','0009'),
    (37,23,9870,1988,110,'04','011','0010'),
    (33,27,6885,3223,120,'04','012','0011'),
    (16,44,5689,7654,130,'04','013','0012'),
    (30,30,1232,9862,140,'04','014','0013'),
    (28,32,8370,3214,150,'05','015','0014')

    insert into sensor values
    (3213,3125,00001,'KJH98'),
    (4314,1223,00002,'BCG62'),
    (4513,7659,00003,'ASF53'),
    (8743,8980,00004,'KGB12'),
    (1243,3233,00005,'NMJ89'),
    (5478,7565,00006,'PIO09'),
    (8945,2456,00007,'LKI90'),
    (3323,7657,00008,'VCF52'),
    (4432,8998,00009,'AYW12'),
    (7776,4323,00010,'AQW22'),
    (3323,2345,00011,'TYY21'),
    (3213,8772,00012,'NHG90'),
    (4344,9089,00013,'BGT51'),
    (3112,1235,00014,'ZAW89'),
    (6576,5466,00015,'LLM23')

    insert into captura values
     (timestamp '2014-07-02 06:14:25'),02,07,2014,06,14,50,1010),	
     ((timestamp '2016-12-10 22:55:25'),12,10,2016,22,55,35,2020),
     ((timestamp '2017-02-28 12:01:25'),28,02,2017,12,01,58,2020)


#### 8.2 INCLUSÃO DO SCRIPT PARA CRIAÇÃO DE TABELA E INSERÇÃO DOS DADOS✔
       (https://github.com/semaforup/trabalho01/blob/master/arquivos/1 "Insert+Modfis")
       
#### 8.3 INCLUSÃO DO SCRIPT PARA EXCLUSÃO DE TABELAS EXISTENTES, CRIAÇÃO DE TABELA NOVAS E INSERÇÃO DOS DADOS✔
       (https://github.com/semaforup/trabalho01/blob/master/arquivos/2 "Insert+Modfis")



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

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://sis4.com/brModelo/brModelo/download.html
<br>


Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")
