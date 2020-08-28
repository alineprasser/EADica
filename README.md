# TRABALHO 01:  EADica
Trabalho desenvolvido durante a disciplina de BD1

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Aline Bravin Prasser: aline_bravin@hotmail.com<br>
Luara Hombre Sathler: luara.hombres@gmail.com<br>

### 2.INTRODUÇÃO E MOTIVAÇÃO<br>
Este documento contém a especificação do projeto do banco de dados EADica
<br>e motivação da escolha realizada. <br>

> A instituição de ensino online "EADica" visa criar um ambiente onde os usuários podem consumir aulas de forma dinâmica e, ao final de cada curso, sejam recompensados com um certificado que comprove a sua capacitação no assunto que desejar. Tendo em vista as dificuldades geradas por causa da atual pandemia de Covid-19, "EADica" é uma alternativa àqueles que gostariam de aprender ou aprimorar seu conhecimento em cursos que abrangem diversas áreas. Para atender suas demandas, a empresa precisa de um sistema que armazene os dados dos Usuários, Instrutores e Cursos, além de armazenar as informações do aluno e professor em relação a seus respectivos cursos. Ademais, o sistema deverá permitir que o usuário assista as vídeo-aulas, possa ver seu progresso no curso e receba o seu certificado de conclusão e que os instrutores publiquem seus cursos.


### 3.MINI-MUNDO<br>

Descrever o mini-mundo! (Não deve ser maior do que 30 linhas, se necessário resumir para justar) <br>
Entrevista com o usuário e identificação dos requisitos.(quando for o caso de sistemas com cliente  real)<br>
Descrição textual das regras de negócio definidas como um  subconjunto do mundo real 
cujos elementos são propriedades que desejamos incluir, processar, armazenar, 
gerenciar, atualizar, e que descrevem a proposta/solução a ser desenvolvida.

> Uma instituição de ensino a distância deseja um sistema de informação para gerenciar suas atividades e prover cursos online.<br>
Dos alunos serão armazenadas informações como nome, cpf, email, matrícula e senha de acesso ao sistema.<br>
Dos cursos serão armazenados o nome, categoria (tecnologia, biologia, matemática, filosofia...), tempo de duração, descrição e certificado de conclusão.<br>
Cada aluno pode estar inscrito em nenhum ou vários cursos ao mesmo tempo, enquanto um curso precisa ter pelo menos um aluno inscrito.<br>
Os dados armazenados dos instrutores são nome, email, cpf,valor da comissão e senha de acesso ao sistema. <br>
Um instrutor poderá auxiliar em vários cursos, mas não obrigatoriamente precisa estar ativo em algum. E obrigatoriamente, um curso precisa de no mínimo um instrutor ministrando.<br>
Ao final do curso, as horas cumpridas do aluno precisam ser validadas antes de ser emitido o certificado final contendo nome do aluno, nome do curso, nome do instrutor, quantidade de horas total, quantidade de horas cumpridas e data da emissão do certificado.


### 4.PROTOTIPAÇÃO, PERGUNTAS A SEREM RESPONDIDAS E TABELA DE DADOS<br>
#### 4.1 RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>
Neste ponto a codificação não e necessária, somente as ideias de telas devem ser criadas, o princípio aqui é pensar na criação da interface para identificar possíveis informações a serem armazenadas ou descartadas <br>

(https://github.com/alineprasser/EADica/blob/master/images/Prototipo.PNG?raw=true)

[Arquivo PDF do Protótipo Balsamiq EADica](https://github.com/alineprasser/EADica/blob/master/arquivos/EADica%20-%20Prototipo.pdf)
#### 4.2 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    a) O sistema proposto poderá fornecer quais tipos de relatórios e informaçes? 
    b) Crie uma lista com os 5 principais relatórios que poderão ser obtidos por meio do sistema proposto!
    
> A Empresa DevCom precisa inicialmente dos seguintes relatórios:
* Relatório que mostre o nome de cada supervisor(a) e a quantidade de empregados supervisionados.
* Relatório relativo aos os supervisores e supervisionados. O resultado deve conter o nome do supervisor e nome do supervisionado além da quantidade total de horas que cada supervisionado tem alocada aos projetos existentes na empresa.
* Relatorio que mostre para cada linha obtida o nome do departamento, o valor individual de cada salario existente no  departamento e a média geral de salarios dentre todos os empregados. Os resultados devem ser apresentados ordenados por departamento.
* Relatório que mostre as informações relacionadas a todos empregados de empresa (sem excluir ninguém). As linhas resultantes devem conter informações sobre: rg, nome, salario do empregado, data de início do salario atual, nomes dos projetos que participa, quantidade de horas e localização nos referidos projetos, numero e nome dos departamentos aos quais está alocado, informações do historico de salário como inicio, fim, e valores de salarios antigos que foram inclusos na referida tabela (caso possuam informações na mesma), além de todas informações relativas aos dependentes. 
>> ##### Observações: <br> a) perceba que este relatório pode conter linhas com alguns dados repetidos (mas não todos). <br>  b) para os empregados que não possuirem alguma destas informações o valor no registro deve aparecer sem informação/nulo. 
* Relatório que obtenha a frequencia absoluta e frequencia relativa da quantidade de cpfs únicos no relatório anterior. Apresente os resultados ordenados de forma decrescente pela frequencia relativa.

 
 
#### 4.3 TABELA DE DADOS DO SISTEMA:
    a) Esta tabela deve conter todos os atributos do sistema e um mínimo de 10 linhas/registros de dados.
    b) Esta tabela tem a intenção de simular um relatório com todos os dados que serão armazenados 
    
[Tabela de dados EADica](https://github.com/alineprasser/EADica/blob/master/arquivos/Tabela%20-%20EADica.xlsx?raw=true)
    
    
### 5.MODELO CONCEITUAL<br>
    A) Utilizar a Notação adequada (Preferencialmente utilizar o BR Modelo 3)
    B) O mínimo de entidades do modelo conceitual pare este trabalho será igual a 3 e o Máximo 5.
        * informe quais são as 3 principais entidades do sistema em densenvolvimento<br>(se houverem mais de 3 entidades, pense na importância da entidade para o sistema)       
    C) Principais fluxos de informação/entidades do sistema (mínimo 3). <br>Dica: normalmente estes fluxos estão associados as tabelas que conterão maior quantidade de dados 
    D) Qualidade e Clareza
        Garantir que a semântica dos atributos seja clara no esquema (nomes coerentes com os dados).
        Criar o esquema de forma a garantir a redução de informação redundante, possibilidade de valores null, 
        e tuplas falsas (Aplicar os conceitos de normalização abordados).   
        
![Alt text](https://github.com/alineprasser/EADica/blob/master/images/conceitual.png?raw=true "Modelo Conceitual")
    
    
        
    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: [Nomes dos que participaram na avaliação]
    [Grupo02]: [Nomes dos que participaram na avaliação]

#### 5.2 Descrição dos dados <br>
   * PESSOA: Tabela que armazena as informações que serão herdadas para cada Aluno e Instrutor.
       - id_pessoa: Campo da tabela PESSOA que armazena a identificação da pessoa.
       - email: Campo da tabela PESSOA que armazena o e-mail de acesso para cada pessoa que acessar o EADica.
       - senha: Campo da tabela PESSOA que armazena a senha de acesso para cada pessoa que acessar o EADica.
       - cpf: Campo da tabela PESSOA que armazena o número de Cadastro de Pessoa Fisica para cada pessoa que acessar o EADica.
       - nome: Campo da tabela PESSOA que armazena o nome completo para cada pessoa que acessar o EADica.
       
   * ALUNO: Tabela que armazena as informações específicas de Aluno.
       - matrícula: Campo da tabela ALUNO que armazena o número de matrícula de cada aluno cadastrado no EADica.
       
   * INSTRUTOR: Tabela que armazena as informações específicas de Instrutor.
       - valor_comissão: Campo da tabela INSTRUTOR que armazena o valor em reais recebido pelo intrutor, referente a sua contribuição dando aulas no EADica.
    
   * CURSO: Tabela que armazena as informações referente a cada curso disponível no EADica.
       - id_curso: Campo da tabela CURSO que armazena a identificação do curso.
       - nome: Campo da tabela CURSO que armazena o nome para cada curso.
       - duração: Campo da tabela CURSO que armazena o tempo de duração, em horas, para cada curso.
       - categoria:Campo da tabela CURSO que armazena a categoria para cada curso.
       - descrição: Campo da tabela CURSO que armazena a descrição (mais informações sobre o curso) para cada curso.
       - certificado.
       
   * ASSISTE: Relacionamento entre Aluno e Curso.
       - data:
       - horas_assistidas:
      
   * MINISTRA: Relacionamento entre Istrutor e Curso.
       - horas_ministradas:
    
### 6.	MODELO LÓGICO<br>
![Alt text](https://github.com/alineprasser/EADica/blob/master/images/logico.jpeg?raw=true "Modelo Conceitual")

        a) inclusão do esquema lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)

### 7.	MODELO FÍSICO<br>
        a) inclusão das instruções de criacão das estruturas em SQL/DDL 
        (criação de tabelas, alterações, etc..) 
        
    Criação das Tabelas:
        create table Pessoa (cod_pessoa serial PRIMARY KEY, nome varchar(50), cpf char(11), email varchar(50), senha varchar(20));
        
        create table Aluno (cod_pessoa int, matricula varchar(10), FOREIGN KEY (cod_pessoa) REFERENCES Pessoa (cod_pessoa));
        
        create table Instrutor (cod_pessoa int, qtd_comissao float, FOREIGN KEY (cod_pessoa) REFERENCES Pessoa (cod_pessoa));
        
        create table Curso ( cod_curso serial PRIMARY KEY, nome varchar(50), categoria varchar(255), duracao float, certificado varchar(255), descricao varchar(255));
        
        create table Aluno_Curso (cod_aluno_curso serial PRIMARY KEY, cod_pessoa int, cod_curso int, qtd_horas_assistidas float, data date, FOREIGN KEY (cod_pessoa) REFERENCES            Pessoa (cod_pessoa), FOREIGN KEY (cod_curso) REFERENCES Curso (cod_curso));
        
        create table Instrutor_Curso ( cod_instrutor_curso serial PRIMARY KEY, cod_pessoa int, cod_curso int, qtd_horas_ministradas float, FOREIGN KEY (cod_pessoa) REFERENCES            Pessoa (cod_pessoa), FOREIGN KEY (cod_curso) REFERENCES Curso (cod_curso));

        
       
### 8.	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
        a) inclusão das instruções de inserção dos dados nas tabelas criadas pelo script de modelo físico
        (Drop para exclusão de tabelas + create definição de para tabelas e estruturas de dados + insert para dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL
        
        Inserção de Dados
        insert into Pessoa (nome, cpf, email, senha) values
            ('Sandra Rosa','15348466504', 'sandrarosa@gmail.com', 'randrasosa')
            ,('Alexandre Soares','78533465901','asoares@gmail.com','alesoarestop')
            ,('Pietro Moraes','12344125642','pietro_moraes@gmail.com','orteipmoraes')
            ,('Marcela Gomes','32216401512','marcelagomes@gmail.com','celinha123')
            ,('Paola Guimarães','11211644214','guipaola@gmail.com','p@0l4')
            ,('Arlindo Damasseno','11235481023','damasseno.lindo@gmail.com','lindoardama')
            ,('Pedro Souza','33122633014','p.souza@gmail.com','souzinhapedro')
            ,('Almira Palhares','33466122401','palmirinha@gmail.com', '123145a')
            ,('Samira Alma Alves','14255784612','almasamira@gmail.com','alma!123')
            ,('Carla Tavares','89941225199','tavarescarla@gmail.com','291255!');

        insert into Aluno (cod_pessoa, matricula) values
            (1,20201001)
            ,(2,20201002)
            ,(3,20201003)
            ,(4,20201004)
            ,(5,20201005);

        insert into Instrutor (cod_pessoa,qtd_comissao) values
            (6,50)
            ,(7,50)
            ,(8,55)
            ,(9,55)
            ,(10,55);

        insert into Curso (nome, categoria, duracao, descricao, certificado) values
            ('Lógica de programação para iniciantes','Tecnologia',60, ' Curso focado em ensinar as bases da lógica de programação','Emitido após conclusão')
            ,('Web design','Design',95,'Curso focado em aprimorar conhecimentos já existentes de Design','Emitido após conclusão')
            ,('Banco de dados','Tecnologia',100,'Curso básico de banco de dados','Emitido após conclusão')
            ,('Matemática básica','Matemática',30,'Curso com enfoque básico em matemática para alunos do ensino médio','Emitido ao meio e após a conclusão do curso')
            ,('Gourmetização dos doces','Culinária',150,'Aprenda a fazer doces deliciosos','Emitido após conclusão')
            ,('Gourmetização dos salgados','Culinária',100,'Aprenda a fazer salgadinhos para sua festa','Emitido após conclusão')
            ,('Fundamentos de SQL','Tecnologia',80,'Saiba mais sobre SQL','Emitido após conclusão');

        insert into Aluno_Curso (cod_pessoa, cod_curso, data, qtd_horas_assistidas) values
            (1,4, '2020-06-29', 9)
            ,(2,3,'2020-06-15',24)
            ,(3,2,'2020-06-18',50)
            ,(4,5,'2020-06-16',3)
            ,(5,1,'2020-06-20',4)
            ,(5,3,'2020-06-20',3)
            ,(4,6,'2020-07-01',70);

        insert into Instrutor_Curso (cod_pessoa, cod_curso, qtd_horas_ministradas) values
            (6,3,95)
            ,(7,2,45)
            ,(8,5,130)
            ,(9,1,41)
            ,(10,4,22)
            ,(8,6,90)
            ,(6,7,40);

### 9.	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Incluir para cada tópico as instruções SQL + imagens (print da tela) mostrando os resultados.<br>
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>

># Marco de Entrega 01: Do item 1 até o item 9.1<br>

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    b) Criar no mínimo 3 consultas com operadores aritméticos 
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.

#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>
    a) Criar minimo 3 de exclusão
    b) Criar minimo 3 de atualização

#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>
    a) Uma junção que envolva todas as tabelas possuindo no mínimo 2 registros no resultado
    b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
    a) Criar minimo 2 envolvendo algum tipo de junção

#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)<br>
    a) Criar minimo 1 de cada tipo

#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join (caso não ocorra na base justificar e substituir por uma view)
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho

#### 9.10	SUBCONSULTAS (Mínimo 4)<br>
     a) Criar minimo 1 envolvendo GROUP BY
     b) Criar minimo 1 envolvendo algum tipo de junção

># Marco de Entrega 02: Do item 9.2 até o ítem 9.10<br>

### 10 RELATÓRIOS E GRÁFICOS

#### a) análises e resultados provenientes do banco de dados desenvolvido (usar modelo disponível)
#### b) link com exemplo de relatórios será disponiblizado pelo professor no AVA
#### OBS: Esta é uma atividade de grande relevância no contexto do trabalho. Mantenha o foco nos 5 principais relatórios/resultados visando obter o melhor resultado possível.

    

### 11	AJUSTES DA DOCUMENTAÇÃO, CRIAÇÃO DOS SLIDES E VÍDEO PARA APRESENTAÇAO FINAL <br>

#### a) Modelo (pecha kucha)<br>
#### b) Tempo de apresentação 6:40 

># Marco de Entrega 03: Itens 10 e 11<br>
<br>
<br>
<br> 



### 12 FORMATACAO NO GIT:<br> 
https://help.github.com/articles/basic-writing-and-formatting-syntax/
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
1. <strong>Caso existam arquivos com conteúdos sigilosos<strong>, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário do git "profmoisesomena", para acompanhamento do trabalho.

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://www.sis4.com/brModelo/download.html
<br>


Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")


