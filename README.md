# TRABALHO 01:  Empresa de Contratação GHHL
Trabalho desenvolvido durante a disciplina de BD1


# Sumário
- [ ] #1 [Componentes preenchidos](#1-componentes)
- [ ] componentes preenchidos
- [ ] componentes preenchidos

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Josué Ramos Souza: josue.rsou@gmail.com<br>
Luiz Sampaio Horta: luizhorta2910@gmail.com<br>
Mateus Lannes Cunha: mateuslannes100@gmail.com<br>
<br>

### 2.INTRODUÇÃO E MOTIVAÇÃO<br>

Este documento contém a especificação do projeto do banco de dados de <GHHL Contratação> 
<br>e motivação da escolha realizada. <br>

 
 > Montar um sistema no estilo de um site online que consiga receber serviços de clientes contratantes da área de Tecnologia da Informação e também exibir vagas para candidatos com base nos modelos oferecidos pela empresa com formas de atuação remota, presencial ou híbrida, monitorar a contratação dos candidatos que se candidatarem às vagas, controlar informações de funcionários e filiais da empresa. Armazenar informações referentes a empresa e suas filiais, funcionarios e candidatos e as vagas oferecidas pela empresa.

### 3.MINI-MUNDO<br>
## Descrição do Minimundo:
<!-- Descrever o mini-mundo! (Não deve ser maior do que 30 linhas, se necessário resumir para justar) <br>
Entrevista com o usuário e identificação dos requisitos.(quando for o caso de sistemas com cliente  real)<br>
Descrição textual das regras de negócio definidas como um  subconjunto do mundo real 
cujos elementos são propriedades que desejamos incluir, processar, armazenar, 
gerenciar, atualizar, e que descrevem a proposta/solução a ser desenvolvida. -->

<!-- O sistema proposto para a "Devcom Projetos conterá as informacões aqui detalhadas. Dos Projetos serão armazenados o número, nome e cidade. Dos Departamentos serão armazenados o número e nome. O cliente destacou que cada projeto pode ter vários departamentos auxiliando no seu desenvolvimento, e cada departamento pode estar envolvido em vários projetos. Os dados relativos aos empregados que serão armazenados são: rg, nome, cpf, salário, data inicial do salario e supervisor de cada empregado. É importante destacar que cada empregado pode ser supervisionado por outro empregado, e obrigatoriamente deve estar alocado a um único departamento, mas pode gerenciar vários departamentos ou não gerenciar nenhum. Um empregado também pode participar de vários projetos, caso seja necessário, mas não precisa obrigatoriamente estar alocado em algum projeto. Com relação aos dependentes serão armazenadas as informações de nome do dependente, data de nascimento, sexo e grau de parentesco. Cada empregado pode ter vários dependentes, mas um dependente esta associado apenas a um único empregado. Com relação ao histórico de salário devemos armazenar as informações de valor do salário, data de início do salário no período e data final do salário no período. É importante lembrar que cada funcionario pode ter diversos eventos de histórico de salário associados a ele visto que este dado pode ser alterado várias vezes. 
-->
> Uma empresa multinacional de tecnologia deseja um sistema para auxiliar na  contratação de novos funcionários, uma vez que, atualmente, o departamento de RH apresenta problemas de lentidão com o levantamento de dados dos candidatos às vagas de emprego e encontrar bons candidatos de acordo com a necessidade de seus contratantes. As principais áreas de busca de vagas são segurança, desenvolvimento de software, banco de dados, marketing e design. As etapas da contratação são divididas em entrevista com RH, entrevista técnica e exame admissional. O sistema a ser desenvolvido deve permitir o cadastro de novos candidatos e seus dados, o que deve ser feito mediante validação de um gestor, o sistema também deve permitir o cadastro de novas filiais, com seus endereços, meios de contato e gestores responsáveis, para que possam selecionar funcionários de acordo com elas. A empresa tem na sua estrutura 3 tipos de gestores, gestor geral, gestor de filial e gestor de contratação, que são responsáveis pelo nível de decisão da empresa. Os gestores precisam cadastrar o nome, a filial que trabalha e e-mail para receber as propostas de vagas. A gerência deve poder emitir relatórios com relação a localidade, idade, nível de escolaridade e certificações de seus candidatos (currículos via PDF), para definir planos de carreiras e outros atributos de gestão.
Para facilitar o trabalho do departamento de RH na seleção de candidatos, as vagas são separadas de acordo com a filial, área de atuação, cargos (CLT, PJ, estágio, trainee ou freelance), carga horária e modelo presencial, híbrido ou remoto. Para um melhor trabalho do time do comercial o sistema deve conseguir emitir um relatório instantâneo com as qualificações dos candidatos para entrar nas licitações que exigem um certo nível profissional dos mesmos. O nível de qualificação dos funcionários seguirá as especificações de mercado, ou seja, júnior, pleno e sênior nas áreas relacionadas a desenvolvimento e análise  e sênior para as demais áreas. O sistema deve fornecer uma página sobre a empresa contendo a história da empresa, clientes, visão, parceiros e certificações, o sistema deve ter um horário pré-determinado para manutenções no horário da madrugada entre 02:00am e 04:00am. O sistema deve permitir que o usuário encontre uma filial próxima pesquisando com base em um CEP inserido e filtrar as vagas pela filial, as filiais pré-existentes a essa documentação são a matriz no Brasil, filial no México e filial em Portugal.


### 4.PROTOTIPAÇÃO, PERGUNTAS A SEREM RESPONDIDAS E TABELA DE DADOS<br>
#### 4.1 RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>
Protótipo navegavel em Figma<br>

Link:[Protótipo Figma](https://www.figma.com/file/dNvctCDrX3DbqgeguQBRIV/Contrata%C3%A7%C3%A3o?node-id=0%3A1)<br>

![Alt text](https://github.com/jramso/Trab_BD1_2022/blob/master/images/Desktop_Enterprise.png?raw=true "Title")

<!--[Protótipo Figma feito para Empresa GHHL Contratação]()-->
#### 4.2 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
<!-- a) O sistema proposto poderá fornecer quais tipos de relatórios e informaçes? -->
>O sistema proposto `GHHL Contratação` fornecera relatórios sobre os usuários do sistema, vagas e filiais.
<!-- b) 5 principais relatório do sistema proposto! -->
 
> A Empresa `GHHL Contratação` precisa inicialmente dos seguintes relatórios: 
- I: Relatório de todos os usuários do sistema.
    - Engloba todos os funcionarios da empresa, só usuários, gestores e candidatos
- II: Relatório de candidatos cadastrados em vagas.
    - Engloba os candidatos, vagas, cargos e areas.
- III: Relatório de gerentes por filial.
    - engloba gestores, tipos de gestores e filiais.
- IV: Relatório de todas as vagas.
    - engloba vagas, cargos e areas.
- V: Relátorio de usuários cujo o endereço mais proximos de cada filial.
    engloba usuários, endereço, logradouro, bairro, cidade, estado, país.
- VI: Relatório geral de todo o sistema:
    engloba todas as relações do sistema, melhor vista em [4.3]().
    
<!-- A Empresa DevCom precisa inicialmente dos seguintes relatórios:
* Relatório que mostre o nome de cada supervisor(a) e a quantidade de empregados supervisionados.
* Relatório relativo aos os supervisores e supervisionados. O resultado deve conter o nome do supervisor e nome do supervisionado além da quantidade total de horas que cada supervisionado tem alocada aos projetos existentes na empresa.
* Relatorio que mostre para cada linha obtida o nome do departamento, o valor individual de cada salario existente no  departamento e a média geral de salarios dentre todos os empregados. Os resultados devem ser apresentados ordenados por departamento.
* Relatório que mostre as informações relacionadas a todos empregados de empresa (sem excluir ninguém). As linhas resultantes devem conter informações sobre: rg, nome, salario do empregado, data de início do salario atual, nomes dos projetos que participa, quantidade de horas e localização nos referidos projetos, numero e nome dos departamentos aos quais está alocado, informações do historico de salário como inicio, fim, e valores de salarios antigos que foram inclusos na referida tabela (caso possuam informações na mesma), além de todas informações relativas aos dependentes. 
>> ##### Observações: <br> a) perceba que este relatório pode conter linhas com alguns dados repetidos (mas não todos). <br>  b) para os empregados que não possuirem alguma destas informações o valor no registro deve aparecer sem informação/nulo. 
* Relatório que obtenha a frequencia absoluta e frequencia relativa da quantidade de cpfs únicos no relatório anterior. Apresente os resultados ordenados de forma decrescente pela frequencia relativa. -->

 
 
#### 4.3 TABELA DE DADOS DO SISTEMA:
    a) Esta tabela deve conter todos os atributos do sistema e um mínimo de 10 linhas/registros de dados.
    b) Esta tabela tem a intenção de simular um relatório com todos os dados que serão armazenados 
    
![Exemplo de Tabela de dados da Empresa Devcom](https://github.com/discipbd1/trab01/blob/master/arquivos/TabelaEmpresaDevCom_sample.xlsx?raw=true "Tabela - Empresa Devcom")
    
    
### 5.MODELO CONCEITUAL<br>
    A) Utilizar a Notação adequada (Preferencialmente utilizar o BR Modelo 3)
    B) O mínimo de entidades do modelo conceitual pare este trabalho será igual a 3 e o Máximo 5.
        * informe quais são as 3 principais entidades do sistema em densenvolvimento<br>(se houverem mais de 3 entidades, pense na importância da entidade para o sistema)       
    C) Principais fluxos de informação/entidades do sistema (mínimo 3). <br>Dica: normalmente estes fluxos estão associados as tabelas que conterão maior quantidade de dados 
    D) Qualidade e Clareza
        Garantir que a semântica dos atributos seja clara no esquema (nomes coerentes com os dados).
        Criar o esquema de forma a garantir a redução de informação redundante, possibilidade de valores null, 
        e tuplas falsas (Aplicar os conceitos de normalização abordados).   
        
<!-- ![Alt text](https://github.com/jramso/Trab_BD1_2022/blob/master/ContrataçãoConceitual.png?raw=true "Modelo Conceitual") -->
 
    
![Alt text](https://github.com/jramso/Trab_BD1_2022/blob/master/images/conceitual_2.jpg "Modelo Conceitual 2.0")
    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: [Josué Ramos, Luiz Sampaio, Mateus Lannes]
    [Grupo02]: [Hanna Letícia de Jesus, Higor Campos, Lucas de Souza]

#### 5.2 Descrição dos dados 
    [USUARIO]: [Tabela que armazena usuários que utilizam o sistema]
        [id]: [codigo identificador do usuário][PK]
        [nome]:[nome de um usuário exemplo: Judas de Jesus]
        [data_nasc]:[data de nascimento do usuário de onde se calcula a idade]
    [CANDIDATO]: [Tabela que armazena dados de usuários que são Candidatos as vagas]
        [id_candidato]:[código identificador de candidato]
        [descricao]: [informações de escolaridade do candidato descritas]
    [VAGA]: [Tabela que armazena dados de vagas Cadastradar pelo gestor de Contratação]
        [id]:[codigo identificador da vaga]
        [carga_horaria]:[tempo que será exercido ao contratado na vaga]
    [CARGO]:[Tabela que armazena os cargos de funcionários e os cargos abertos a candidatura]
        [id]: [codigo identificador de cargo]
        [nome_cargo]:[nome do cargo de um usuario do sistema]
    [AREA]:[Tabela que armazena as areas profissionais relacionadas da vaga]
        [id]: [codigo identificador da area]
        [nome_area]: [nome da area profissional exemplo: programação]
    [GESTOR]:[Tabela que armazena gestores]
        [id]: [identificador do `Gestor`] [PK]
        [id_tipo]: [...]
        [email]: [email de contato pelo qual o gestor e responsavel]
    [TIPO_GESTOR]:[Tabela que separa gestores por tipo]
        [id_tipo]: [identificador do tipo de gestor][PK]
        [nome_tipo]: [nome dos tipos de gestores: Geral, Vagas ou Filial]
    [FILIAL]:[Tabela que armazena informações das filiais da empresa]
        [id]:
        [telefone_unico]:
    [ENDERECO]:[Tabela que armazena endereço de usuarios e filiais]
        [id]
        [numero]
        [cep]
    [BAIRRO]:[Tabela que armazena os dados do bairro para o endereço]
        [id]
        [nome_bairro]
    [CIDADE]:[Tabela que armazena os dados da cidade para o endereço]
        [id]
        [nome_cidade]
    [ESTADO]:[Tabela que armazena os dados do estado para o endereço]
        [id]
        [nome_estado]
    [PAIS]:[Tabela que armazena os dados do país para o endereço]
        [id]
        [nome_pais]
    
    EXEMPLO:
    CLIENTE: Tabela que armazena as informações relativas ao cliente<br>
    CPF: campo que armazena o número de Cadastro de Pessoa Física para cada cliente da empresa.<br>


### 6	MODELO LÓGICO<br>
        a) inclusão do esquema lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)
        
![Alt text](https://github.com/jramso/Trab_BD1_2022/blob/master/Contrat_logico.png?raw=true "Modelo Conceitual")

### 7	MODELO FÍSICO<br>
        a) inclusão das instruções de criacão das estruturas em SQL/DDL 
        (criação de tabelas, alterações, etc..) 
        
       
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
        a) inclusão das instruções de inserção dos dados nas tabelas criadas pelo script de modelo físico
        (Drop para exclusão de tabelas + create definição de para tabelas e estruturas de dados + insert para dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL


### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
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


