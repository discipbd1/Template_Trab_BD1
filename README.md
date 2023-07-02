# TRABALHO 01:  Empresa MCMY
Trabalho desenvolvido durante a disciplina de BD1

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Cleiton Gomes dos Santos: cleitongomes@ucl.br<br>
Marianna Almeida Santos: marianna.almeidasa@gmail.com<br>
Murilo Andrade Carvalho: muriloandradec@gmail.com<br>
Yasmim Da Silva Nunes: yasmimnunes.yn@gmail.com<br>


### 2.INTRODUÇÃO E MOTIVAÇÃO<br>
Este documento contém a especificação do projeto do banco de dados <nome do projeto> 
<br>e motivação da escolha realizada. <br>

> A empresa MCMY visa colaborar com desenvolvimento de projetos para melhora da locação de equipamentos e de ferramentas em geral. Sabendo-se dos desafios para gerenciar um sistema de aluguel dentro de uma empresa e visando unir as informações referentes a clientes, funcionários, equipamentos, contratos, renovação e manutenção em um mesmo local, ficamos motivados com o desenvolvimento deste sistema. O Sistema "MCMY" tem como objetivo gerenciar todas as informações ao desenvolvimento das atividades de empresas (filiais). Para realizar suas operações adequadamente e a empresa necessita que o sistema armazene informações relativas aos dados (contato, endereços, dados dos equipamentos), empregados. Além de também armazenar dados sobre aprovação de aluguel.
 
### 3.MINI-MUNDO<br>

> Num determinado sistema para locação de equipamentos em geral, visa facilitar a gestão de locação. Dessa maneira, o sistema precisa controlar os equipamentos através da identificação, tipo ( equipamentos de construção civil ), data de aquisição, modelo, marca e ano de lançamento. O sistema também deve permitir o controle de clientes através do nome, data nescimento, sexo, cpf, endereço, contato e senha. Também é preciso controlar os empréstimos dos equipamentos através do atual responsável pelo equipamento, a data do empréstimo e a data de renovação.Esse alerta precisa estar integrado com o WhatsApp para enviar mensagens. No ato de locação de um determinado equipamento emprestado, o cliente deve assinar o termo de responsabilidade, onde ele se responsabiliza por quaisquer danos ao equipamento. O sistemadeve permitir que um cliente pegue mais do que um equipamento.

### 4.PROTOTIPAÇÃO, PERGUNTAS A SEREM RESPONDIDAS E TABELA DE DADOS<br>
#### 4.1 RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>
Segue abaixo o link do prototipo desenvolvido para a empresa <br>

[PROTOTIPO-SITE](https://trabalhobancodedados.github.io/Prototipo-site/)

#### 4.2 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    a) O sistema proposto poderá fornecer quais tipos de relatórios e informaçes? 
    b) Crie uma lista com os 5 principais relatórios que poderão ser obtidos por meio do sistema proposto!
    
> O sistema podera gerar um relatório sobre a quantidade de equipamentos em estoque, como a status de aprovação de empréstimo sobre um determinado equipamento para um cliete. Um relatório de nossos clientes e Funcionários. 
A Empresa MCMY precisa inicialmente dos seguintes relatórios:

> - Relatório que mostre os tipos de equipamentos, suas respectivas quantidades, modelo, marca, nome e data de fabricação;
> - Relatório que mostre as informações relacionadas a todos empregados de empresa (sem excluir ninguém) contendo nome, cpf, sexo, data de nascimento, endereço e matricula. 
> - Relatório que mostre os empréstimos dos clientes contendo status (de aprovação ou negação do pedido) data de validação, data de solicitação e valor da solicitação;
> - Relatório que mostre os clientes com as seguintes informações: nome, cpf, sexo, data de nascimento e endereço.
 

 
 
#### 4.3 TABELA DE DADOS DO SISTEMA:
    a) Esta tabela deve conter todos os atributos do sistema e um mínimo de 10 linhas/registros de dados.
    b) Esta tabela tem a intenção de simular um relatório com todos os dados que serão armazenados 
    
![Exemplo de Tabela de dados da Empresa MCMY](https://github.com/TrabalhoBancodeDados/Template_Trab_BD1/blob/master/arquivos/TabelaEmpresaMCMY_sample.xlsx?raw=true "Tabela - Empresa MCMY")
    
    
### 5.MODELO CONCEITUAL<br>
    A) Utilizar a Notação adequada (Preferencialmente utilizar o BR Modelo 3)
    B) O mínimo de entidades do modelo conceitual pare este trabalho será igual a 3 e o Máximo 5.
        * informe quais são as 3 principais entidades do sistema em densenvolvimento<br>(se houverem mais de 3 entidades, pense na importância da entidade para o sistema)       
    C) Principais fluxos de informação/entidades do sistema (mínimo 3). <br>Dica: normalmente estes fluxos estão associados as tabelas que conterão maior quantidade de dados 
    D) Qualidade e Clareza
        Garantir que a semântica dos atributos seja clara no esquema (nomes coerentes com os dados).
        Criar o esquema de forma a garantir a redução de informação redundante, possibilidade de valores null, 
        e tuplas falsas (Aplicar os conceitos de normalização abordados).   
        
![Alt text](https://github.com/TrabalhoBancodeDados/Template_Trab_BD1/blob/master/images/modelo_conceitual_final.png?raw=true "Modelo Conceitual")
    
    
        
    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: [Nomes dos que participaram na avaliação]
    [Grupo02]: [Nomes dos que participaram na avaliação]

#### 5.2 Descrição dos dados 
    [objeto]: [descrição do objeto]
    
    - PESSOA: Tabela que armazena as informações relativas ao cliente ou funcionário;
    - nome: campo que armazena o nome da pessoa; 
    - sexo:  campo que armazena o sexo da pessoa;
    - data_nasc: campo que armazena da data de nascimento da pessoa; 
    - CPF: campo que armazena o número de cadastro da pessoa;
    - senha: campo que armazena a senha de login da pessoa;
    - codigo: campo que armazena determinado codigo de uma pessoa;
    - endereco: campo que armazena o endereço da pessoa;
    - fk_PESSOA_codigo: campo que armazena codigo de uma pessoa cadastrada;
    - fk_CONTATO_codigo: campo que armazena o codigo relacionado ao contato de uma pessoa;
    - CONTATO: Tabela que armazena o contato de uma pessoa;
    - contato: campo que armazena o contato de uma pessoa;
    - codigo: campo que armazena o codigo de uma pessoa de uma determinado contato;
    - FK_CONTATO_TIPO_codigo: campo que armazena o tipo de contato de uma derteminada pessoa;
    - CONTATO_TIPO: Tabela que armazena o tipo de contato que a passoa cadastrou;
    - descricao: campo que armazena o tipo de contato (telefone/e-mai/etc);
    - codigo: campo que armazena a pessoa ligada ao contato cadastrado;
    - FUNCIONARIO: tabela que armazena o cadastro do funcionário na empresa;
    - matricula: campo que armazena a matricula do funcionário;
    - FK_PESSOA_codigo: campo que armazena o codigo do funcionário cadastrado;
    - EMPRESTIMO: Tabela que armazena o emprestimo da pessoa;
    - data_solicitacao: campo que armazena a data de soliciação da pessoa para eprestimo;
    - valor_solicitação: campo que armazena o valor da solicitação da pessoa;
    - codigo: campo que armazena o codigo do emprestimo;
    - data_validacao: data em que foi gerada a validação do funcionpario;
    - fk_FUNCIONARIO_matricula: campo que armazrna a matricula do funcionário que gerou a validacao;
    - fk_PESSOA_codigo: campo que armazena o codigo da pessoa que realizou a solicitação;
    - fk_Emprestimo_codigo: campo que armazena o codigo do emprestimo;
    - fk_EQUIPAMENTO_codigo: campo que armazena o codigo do equipameno requisitado;
    - quantidade: campo que armazena a quantidade de equipamento que a pessoa solicitou;
    - EQUIPAMENTO: Tabela que armazena os equipamentos;
    - data_fabricacao: campo que armazena a data de fabricação do equipamento;
    - modelo: campo que armazena o modelo do equipemento:
    - marca: campo que armazena a marca do equipamento.
    - codigo: campo que armazena o codigo do equipamento;
    - valor_locacao: campo que armazena o valor da locaçao do equipamento;
    - FK_TIPO_EQUIPAMENTO_codigo: campo que armazena o campo de um determinado tipo de equipamento;
    - TIPO_EQUIPAMENTO: Tabela que armazena um determinado tipo de equipamento;
    - codigo: campo que armazena um determinado equipamento;
    - nome: campo que armazena o nome do equipamento.
    

### 6	MODELO LÓGICO<br>
        a) inclusão do esquema lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)
![Alt text](https://github.com/TrabalhoBancodeDados/Template_Trab_BD1/blob/master/images/modelo_logico_final2.png?raw=true "Modelo Lógico")

### 7	MODELO FÍSICO<br>
        a) inclusão das instruções de criacão das estruturas em SQL/DDL 
        (criação de tabelas, alterações, etc..) 
        
CREATE TABLE pessoa( cod int, nome varchar(100), sexo varchar(100),data_nasc date, cpf varchar(12),  senha varchar(100), endereco varchar(300),
PRIMARY key (cod)
);

CREATE TABLE contato_tipo( cod int, descricao varchar(300),
PRIMARY key (cod)
);

CREATE TABLE contato( cod int, contato varchar(100), contato_tipo_cod int,
PRIMARY key (cod),
FOREIGN key (contato_tipo_cod) REFERENCES contato_tipo(cod)

);
CREATE TABLE possui( pessoa_cod int, contato_cod int,
FOREIGN key (contato_cod) REFERENCES contato(cod),
FOREIGN key (pessoa_cod) REFERENCES pessoa(cod)
);

CREATE TABLE tipo_equipamento( cod int, nome varchar(100),
PRIMARY key (cod)
);

CREATE TABLE equipamento( cod int, tipo_equipamento_cod int, data_fabricacao date, modelo varchar(100), marca varchar(100), valor_locacao decimal,
PRIMARY key (cod),
FOREIGN key (tipo_equipamento_cod) REFERENCES tipo_equipamento(cod)
);

CREATE TABLE funcionario( matricula int, pessoa_cod int,
PRIMARY key (matricula ),
FOREIGN key (pessoa_cod) REFERENCES pessoa(cod)
);

CREATE TABLE emprestimo( cod int, pessoa_cod int, funcionario_cod int,  data_solicitacao date, valor_solicitacao decimal, status boolean, data_validacao date, 
PRIMARY key (cod),
FOREIGN key (pessoa_cod) REFERENCES pessoa(cod),
FOREIGN key (funcionario_cod) REFERENCES funcionario(matricula)
);

CREATE TABLE destinado( quantidade int, emprestimo_cod int, equipamento_cod int,
FOREIGN key (emprestimo_cod) REFERENCES emprestimo(cod),
FOREIGN key (equipamento_cod) REFERENCES equipamento(cod)
);
       
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


