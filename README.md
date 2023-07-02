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

> Em um determinado sistema para locação de equipamentos em geral que visa facilitar a gestão de locação. Dessa maneira, o sistema precisa controlar os equipamentos através da identificação, tipo ( equipamentos de uso geral), data de fabricação, modelo, marca e valor da locação. O sistema também deve permitir o controle de clientes através do nome, data nescimento, sexo, cpf, endereço, senha e contato(telefone, e-mail, WhatsApp ou Telegram) . Além disso, precisa-se controlar os empréstimos dos equipamentos através da identificação,data da solitação, valor da solicitação, data da validação e status(aprovado ou reprovado). O funcionário possui uma matrícula e gerencia os empréstimos. No ato de locação de um determinado equipamento emprestado, o cliente deve assinar o termo de responsabilidade, onde ele se responsabiliza por quaisquer danos ao equipamento. O sistema deve permite que um cliente pegue mais do que um equipamento.

### 4.PROTOTIPAÇÃO, PERGUNTAS A SEREM RESPONDIDAS E TABELA DE DADOS<br>
#### 4.1 RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>
Segue abaixo o link do prototipo desenvolvido para a empresa <br>

[PROTOTIPO-SITE](https://trabalhobancodedados.github.io/Prototipo-site/)

#### 4.2 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    a) O sistema proposto poderá fornecer quais tipos de relatórios e informaçes? 
    b) Crie uma lista com os 5 principais relatórios que poderão ser obtidos por meio do sistema proposto!

    A Empresa MCMY precisa inicialmente dos seguintes relatórios:
    
> - O sistema podera gerar um relatório sobre a quantidade de equipamentos em estoque, como a status de aprovação de empréstimo sobre um determinado equipamento para um cliete. Um relatório de nossos clientes e Funcionários. 
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
        
INSERT INTO pessoa (cod, nome, sexo, data_nasc, cpf, senha, endereco) 
VALUES 
(1, 'Alexandre', 'M', '1961/05/06', '76975667020', 'xjbqA', 'av.Jão Carlos 178'),
(2, 'Roberto', 'M', '1954/07/07', '48733649065', 'sNY3S', 'rua Marcos Silva 555'),
(3, 'Claudia', 'F', '1966/09/03', '33039360051', 'oz3hx', 'rua Karla Peixes 478'),
(4, 'Sandra', 'F', '1955/08/09', '013531960-97', 'n10Tr', 'av. Pardos 789'),
(5, 'Arlindo', 'M', '1978/09/11', '100597000-92', 'YF4xh', 'av. Pedras 887'),
(6, 'Ricardo', 'M', '1972/02/12', '347192030-78', 'QGb9y', 'av. Caracol 777'),
(7, 'Fernanda', 'F', '1988/08/10', '654323920-46', 'jKtIx', 'rua Neves 436'),
(8, 'Amanda', 'F', '1957/06/14', '574779440-07', 'JUjxY', 'rua B 123'),
(9, 'João', 'M', '1989/08/17', '112364030-02', 'PfHtH', 'rua numero 424'),
(10, 'Jonas', 'M', '1982/01/30', '524822510-87', 'ogjkz', 'rua Java 493'),
(11, 'Nivaldo Batista Lima', 'M', '1989/03/09', '123654789.23', 'GustavoLima', 'av.Jão Carlos 178'),
(12, 'José Abelardo Barbosa de Medeiros', 'M', '1917/09/30', '321456987.56', 'Chacrinha', 'av.Jão Carlos 18'),
(13, 'José Albertino da Silva', 'M', '1965/05/06', '231546897.89', 'Caju', 'rua Marcos Silva 555'),
(14, 'Mirosmar José de Camargo', 'M', '1962/08/17', '213564879.78', 'ZezeDiCamargo', 'rua Marcos Silva 55'),
(15, 'José Roberto da Silva', 'M', '1967/02/25', '312465978.45', 'Castanha', 'rua Marcos Silva 5'),
(16, 'Maria de Fátima Silva', 'F', '1990/06/14', '154789632.45', 'MariaFatima', 'rua João Paulo 123'),
(17, 'Ana Carolina Santos', 'F', '1985/12/03', '785965321.78', 'AnaCarolina', 'av. das Flores 456'),
(18, 'Pedro Henrique Souza', 'M', '1995/07/22', '987654321.45', 'PedroHenrique', 'rua da Paz 789'),
(19, 'Mariana Oliveira', 'F', '1992/04/18', '654789123.32', 'MarianaOliveira', 'av. São João 456'),
(20, 'Lucas Santos', 'M', '1998/10/29', '564987321.45', 'LucasSantos', 'rua das Acácias 123'),
(21, 'Carolina Fernandes', 'F', '1990/08/06', '789321654.45', 'CarolinaFernandes', 'rua dos Ipês 987'),
(22, 'Rafael Silva', 'M', '1987/03/14', '654987321.12', 'RafaelSilva', 'av. Brasil 456'),
(23, 'Juliana Souza', 'F', '1995/06/27', '987654123.78', 'JulianaSouza', 'rua da Liberdade 789'),
(24, 'Fernando Pereira', 'M', '1985/12/02', '564789321.01', 'FernandoPereira', 'av. Paulista 123'),
(25, 'Andréa Santos', 'F', '1991/09/25', '321789654.45', 'AndreiaSantos', 'rua das Flores 987'),
(26, 'Marcelo Oliveira', 'M', '1982/02/18', '789123564.32', 'MarceloOliveira', 'av. Copacabana 456'),
(27, 'Isabela Lima', 'F', '1997/11/10', '123321789.45', 'IsabelaLima', 'rua das Mangueiras 789'),
(28, 'Eduardo Costa', 'M', '1980/05/03', '789321123.56', 'EduardoCosta', 'av. dos Coqueiros 123'),
(29, 'Vanessa Rodrigues', 'F', '1994/08/07', '564789123.89', 'VanessaRodrigues', 'rua dos Pinheiros 456'),
(30, 'Leonardo Almeida', 'M', '1987/01/21', '789564321.45', 'LeonardoAlmeida', 'av. das Palmeiras 987'),
(31, 'Camila Ferreira', 'F', '1993/07/15', '123789564.56', 'CamilaFerreira', 'rua das Oliveiras 123'),
(32, 'Gustavo Carvalho', 'M', '1984/09/12', '456123789.89', 'GustavoCarvalho', 'av. das Aroeiras 456'),
(33, 'Beatriz Gomes', 'F', '1999/03/28', '789456123.78', 'BeatrizGomes', 'rua das Laranjeiras 987'),
(34, 'Ricardo Fernandes', 'M', '1983/11/09', '789123456.45', 'RicardoFernandes', 'av. dos Girassóis 123'),
(35, 'Patrícia Santos', 'F', '1990/04/24', '456789123.32', 'PatriciaSantos', 'rua dos Cravos 456'),
(36, 'Henrique Lima', 'M', '1988/08/28', '789456321.01', 'HenriqueLima', 'av. das Orquídeas 987'),
(37, 'Larissa Almeida', 'F', '1996/06/13', '123789456.45', 'LarissaAlmeida', 'rua das Begônias 123'),
(38, 'Fernando Rodrigues', 'M', '1981/03/05', '789123564.32', 'FernandoRodrigues', 'av. das Hortênsias 456'),
(39, 'Priscila Costa', 'F', '1992/10/18', '456789123.78', 'PriscilaCosta', 'rua das Violetas 987'),
(40, 'Rafaela Gomes', 'F', '1989/12/29', '789456123.89', 'RafaelaGomes', 'av. das Camélias 123'),
(41, 'Vinicius Carvalho', 'M', '1986/02/07', '123789564.56', 'ViniciusCarvalho', 'rua das Margaridas 456'),
(42, 'Carolina Martins', 'F', '1991/09/10', '789123456.45', 'CarolinaMartins', 'av. das Tulipas 987'),
(43, 'Bruno Ferreira', 'M', '1985/07/02', '456789123.32', 'BrunoFerreira', 'rua das Azaleias 456'),
(44, 'Laura Oliveira', 'F', '1998/04/16', '789456321.01', 'LauraOliveira', 'av. das Petúnias 987'),
(45, 'Gabriel Santos', 'M', '1984/11/20', '123789456.45', 'GabrielSantos', 'rua das Bromélias 123'),
(46, 'Letícia Lima', 'F', '1993/06/07', '789123564.32', 'LeticiaLima', 'av. das Gérberas 456'),
(47, 'Marcelo Costa', 'M', '1981/01/03', '456789123.78', 'MarceloCosta', 'rua das Rosas 987'),
(48, 'Amanda Rodrigues', 'F', '1995/08/26', '789456123.89', 'AmandaRodrigues', 'av. das Begônias 123'),
(49, 'Guilherme Almeida', 'M', '1987/04/11', '123789456.56', 'GuilhermeAlmeida', 'rua das Orquídeas 456'),
(50, 'Carolina Sousa', 'F', '1992/12/14', '789123456.45', 'CarolinaSousa', 'av. das Hortênsias 987')



INSERT INTO contato_tipo(cod, descricao)
VALUES
(1, 'telefone'),
(3, 'e-mail'),
(2, 'telegram'),
(4, 'whatsapp'),
(5, 'Skype'),
(6, 'Facebook'),
(7, 'LinkedIn'),
(8, 'Instagram'),
(9, 'Twitter'),
(10, 'Pinterest'),
(11, 'Snapchat'),
(12, 'TikTok'),
(13, 'YouTube')



INSERT INTO contato(cod, contato, contato_tipo_cod)
VALUES
(1, '1234567890', 1),
(2, 'email@example.com', 3),
(3, '9876543210', 1),
(4, 'anotheremail@example.com', 3),
(5, 'telegram_username', 2),
(6, 'whatsapp_number', 4),
(7, 'skype_username', 5),
(8, 'facebook_username', 6),
(9, 'linkedin_profile', 7),
(10, 'instagram_handle', 8),
(11, 'twitter_handle', 9),
(12, 'pinterest_username', 10),
(13, 'snapchat_username', 11),
(14, 'tiktok_username', 12),
(15, 'youtube_channel', 13),
(16, '0987654321', 1),
(17, 'email2@example.com', 3),
(18, '5678901234', 1),
(19, 'anotheremail2@example.com', 3),
(20, 'telegram_username2', 2),
(21, 'whatsapp_number2', 4),
(22, 'skype_username2', 5),
(23, 'facebook_username2', 6),
(24, 'linkedin_profile2', 7),
(25, 'instagram_handle2', 8),
(26, 'twitter_handle2', 9),
(27, 'pinterest_username2', 10),
(28, 'snapchat_username2', 11),
(29, 'tiktok_username2', 12),
(30, 'youtube_channel2', 13),
(31, '0987654321', 1),
(32, 'email3@example.com', 3),
(33, '5678901234', 1),
(34, 'anotheremail3@example.com', 3),
(35, 'telegram_username3', 2),
(36, 'whatsapp_number3', 4),
(37, 'skype_username3', 5),
(38, 'facebook_username3', 6),
(39, 'linkedin_profile3', 7),
(40, 'instagram_handle3', 8),
(41, 'twitter_handle3', 9),
(42, 'pinterest_username3', 10),
(43, 'snapchat_username3', 11),
(44, 'tiktok_username3', 12),
(45, 'youtube_channel3', 13),
(46, '0987654321', 1),
(47, 'email4@example.com', 3),
(48, '5678901234', 1),
(49, 'anotheremail4@example.com', 3),
(50, 'telegram_username4', 2),
(51, 'whatsapp_number4', 4),
(52, 'skype_username4', 5),
(53, 'facebook_username4', 6),
(54, 'linkedin_profile4', 7),
(55, 'instagram_handle4', 8),
(56, 'twitter_handle4', 9),
(57, 'pinterest_username4', 10),
(58, 'snapchat_username4', 11),
(59, 'tiktok_username4', 12),
(60, 'youtube_channel4', 13)



INSERT INTO possui(pessoa_cod, contato_cod)
VALUES
(1, 1),
(2, 2),
(3, 3),
(4, 4),
(5, 5),
(6, 6),
(7, 7),
(8, 8),
(9, 9),
(10, 10),
(11, 11),
(12, 12),
(13, 13),
(14, 14),
(15, 15),
(16, 16),
(17, 17),
(18, 18),
(19, 19),
(20, 20),
(21, 21),
(22, 22),
(23, 23),
(24, 24),
(25, 25),
(26, 26),
(27, 27),
(28, 28),
(29, 29),
(30, 30),
(31, 31),
(32, 32),
(33, 33),
(34, 34),
(35, 35),
(36, 36),
(37, 37),
(38, 38),
(39, 39),
(40, 40),
(41, 41),
(42, 42),
(43, 43),
(44, 44),
(45, 45),
(46, 46),
(47, 47),
(48, 48),
(49, 49),
(50, 50),
(1, 51),
(2, 52),
(3, 53),
(4, 54),
(5, 55),
(6, 56),
(7, 57),
(8, 58),
(9, 59),
(10, 60);




INSERT INTO tipo_equipamento( cod, nome)
values
(1,'TUPIA'),
(2,'ASPIRADOR INDUSTRIAL'),
(3,'MINI-ESCAVADEIRA'),
(4,'ENCERADEIRA INDUSTRIAL'),
(5,'BRITADEIRA A CAMBUSTÃO'),
(6,'SERRA DE BANCADA'),
(7,'SERRA SABRE'),
(8,'EXTRATORA DE ESTOFADO'),
(9,'MOTOR ESMERIL'),
(10,'POLITRIZ')


INSERT INTO equipamento(cod, tipo_equipamento_cod, data_fabricacao, modelo, marca, valor_locacao)
VALUES
(1, 1, '2010-05-28', 'Modelo A', 'Marca A', 123.45),
(2, 2, '2011-08-12', 'Modelo B', 'Marca B', 234.56),
(3, 3, '2012-02-03', 'Modelo C', 'Marca C', 345.67),
(4, 4, '2013-09-21', 'Modelo D', 'Marca D', 456.78),
(5, 5, '2014-06-15', 'Modelo E', 'Marca E', 567.89),
(6, 6, '2015-11-30', 'Modelo F', 'Marca F', 678.90),
(7, 7, '2016-03-07', 'Modelo G', 'Marca G', 789.01),
(8, 8, '2017-10-24', 'Modelo H', 'Marca H', 890.12),
(9, 9, '2018-07-17', 'Modelo I', 'Marca I', 901.23),
(10, 10, '2019-12-09', 'Modelo J', 'Marca J', 1012.34),
(11, 1, '2020-01-15', 'Modelo K', 'Marca K', 1112.35),
(12, 2, '2010-11-06', 'Modelo L', 'Marca L', 1212.36),
(13, 3, '2011-04-30', 'Modelo M', 'Marca M', 1312.37),
(14, 4, '2012-09-23', 'Modelo N', 'Marca N', 1412.38),
(15, 5, '2013-06-17', 'Modelo O', 'Marca O', 1512.39),
(16, 6, '2014-12-10', 'Modelo P', 'Marca P', 1612.40),
(17, 7, '2015-02-25', 'Modelo Q', 'Marca Q', 1712.41),
(18, 8, '2016-08-18', 'Modelo R', 'Marca R', 1812.42),
(19, 9, '2017-05-11', 'Modelo S', 'Marca S', 1912.43),
(20, 10, '2018-10-03', 'Modelo T', 'Marca T', 2012.44),
(21, 1, '2019-11-09', 'Modelo U', 'Marca U', 2112.45),
(22, 2, '2020-03-26', 'Modelo V', 'Marca V', 2212.46),
(23, 3, '2010-09-18', 'Modelo W', 'Marca W', 2312.47),
(24, 4, '2011-05-12', 'Modelo X', 'Marca X', 2412.48),
(25, 5, '2012-12-05', 'Modelo Y', 'Marca Y', 2512.49),
(26, 6, '2013-02-19', 'Modelo Z', 'Marca Z', 2612.50),
(27, 7, '2014-08-13', 'Modelo AA', 'Marca AA', 2712.51),
(28, 8, '2015-05-06', 'Modelo BB', 'Marca BB', 2812.52),
(29, 9, '2016-10-29', 'Modelo CC', 'Marca CC', 2912.53),
(30, 10, '2017-07-22', 'Modelo DD', 'Marca DD', 3012.54),
(31, 1, '2018-12-14', 'Modelo EE', 'Marca EE', 3112.55),
(32, 2, '2019-02-28', 'Modelo FF', 'Marca FF', 3212.56),
(33, 3, '2020-08-21', 'Modelo GG', 'Marca GG', 3312.57),
(34, 4, '2010-05-14', 'Modelo HH', 'Marca HH', 3412.58),
(35, 5, '2011-12-07', 'Modelo II', 'Marca II', 3512.59),
(36, 6, '2012-02-21', 'Modelo JJ', 'Marca JJ', 3612.60),
(37, 7, '2013-08-14', 'Modelo KK', 'Marca KK', 3712.61),
(38, 8, '2014-05-07', 'Modelo LL', 'Marca LL', 3812.62),
(39, 9, '2015-10-29', 'Modelo MM', 'Marca MM', 3912.63),
(40, 10, '2016-07-22', 'Modelo NN', 'Marca NN', 4012.64);


INSERT INTO funcionario(matricula, pessoa_cod)
VALUES
(37428, 24),
(95214, 46),
(61073, 6),
(82105, 35),
(49762, 12),
(10983, 44),
(28617, 20),
(41596, 37),
(73942, 32),
(56910, 17),
(82430, 26),
(12034, 11),
(76854, 45),
(62490, 5),
(98245, 28)





INSERT INTO emprestimo (cod, pessoa_cod, funcionario_cod, data_solicitacao, valor_solicitacao, status, data_validacao)
VALUES
(1, 2, 98245, '2021-01-15', 500.00, true, '2021-02-01'),
(2, 3, 49762, '2021-02-20', 750.00, true, '2021-03-10'),
(3, 4, 62490, '2021-03-10', 1000.00, true, '2021-04-01'),
(4, 7, 82105, '2021-04-05', 200.00, true, '2021-05-01'),
(5, 8, 41596, '2021-05-12', 800.00, true, '2021-06-01'),
(6, 9, 12034, '2021-06-01', 600.00, true, '2021-07-01'),
(7, 10, 76854, '2021-07-20', 350.00, true, '2021-08-01'),
(8, 13, 10983, '2021-08-25', 900.00, true, '2021-09-01'),
(9, 14, 49762, '2021-09-10', 250.00, true, '2021-10-01'),
(10, 15, 82430, '2021-10-05', 400.00, true, '2021-11-01'),
(11, 16, 61073, '2021-11-12', 150.00, true, '2021-12-01'),
(12, 18, 98245, '2021-12-01', 700.00, true, '2022-01-01'),
(13, 19, 28617, '2022-01-20', 300.00, true, '2022-02-01'),
(14, 21, 73942, '2022-02-25', 450.00, true, '2022-03-01'),
(15, 22, 95214, '2022-03-10', 550.00, true, '2022-04-01'),
(16, 23, 76854, '2022-04-15', 950.00, true, '2022-05-01'),
(17, 25, 82430, '2022-05-01', 700.00, true, '2022-06-01'),
(18, 27, 41596, '2022-06-20', 250.00, true, '2022-07-01'),
(19, 29, 12034, '2022-07-05', 400.00, true, '2022-08-01'),
(20, 30, 61073, '2022-08-12', 150.00, true, '2022-09-01'),
(21, 31, 98245, '2022-09-01', 700.00, true, '2022-10-01'),
(22, 33, 62490, '2022-10-20', 300.00, true, '2022-11-01'),
(23, 34, 28617, '2022-11-25', 450.00, true, '2022-12-01'),
(24, 36, 95214, '2022-12-10', 550.00, true, '2022-12-15'),
(25, 38, 98245, '2022-12-15', 950.00, true, '2023-01-01'),
(26, 39, 82430, '2023-01-01', 700.00, true, '2023-02-01'),
(27, 41, 28617, '2023-02-20', 250.00, true, '2023-03-01'),
(28, 43, 61073, '2023-03-05', 400.00, true, '2023-04-01'),
(29, 47, 98245, '2023-04-12', 150.00, true, '2023-05-01'),
(30, 48, 41596, '2023-05-01', 700.00, true, '2023-06-01'),
(31, 50, 95214, '2023-06-20', 300.00, true, '2023-07-01'),
(32, 2, 82430, '2021-01-15', 2500.00, true, '2021-02-01'),
(33, 3, 28617, '2021-02-20', 3000.00, true, '2021-03-10'),
(34, 4, 61073, '2021-03-10', 3500.00, true, '2021-04-01'),
(35, 7, 98245, '2021-04-05', 4000.00, true, '2021-05-01'),
(36, 8, 76854, '2021-05-12', 4500.00, true, '2021-06-01'),
(37, 9, 41596, '2021-06-01', 5000.00, true, '2021-07-01'),
(38, 10, 98245, '2021-07-20', 5500.00, true, '2021-08-01'),
(39, 13, 28617, '2021-08-25', 6000.00, true, '2021-09-01'),
(40, 14, 61073, '2021-09-10', 6500.00, true, '2021-10-01'),
(41, 15, 98245, '2021-10-05', 7000.00, true, '2021-11-01'),
(42, 16, 82430, '2021-11-12', 7500.00, true, '2021-12-01'),
(43, 18, 95214, '2021-12-01', 8000.00, true, '2022-01-01'),
(44, 19, 49762, '2022-01-20', 8500.00, true, '2022-02-01'),
(45, 21, 10983, '2022-02-25', 9000.00, true, '2022-03-01'),
(46, 22, 56910, '2022-03-10', 9500.00, true, '2022-04-01'),
(47, 23, 82430, '2022-04-01', 10000.00, true, '2022-05-01'),
(48, 25, 98245, '2022-05-12', 10500.00, true, '2022-06-01'),
(49, 27, 61073, '2022-06-01', 11000.00, true, '2022-07-01'),
(50, 29, 62490, '2022-07-20', 11500.00, true, '2022-08-01'),
(51, 30, 82105, '2022-08-25', 12000.00, true, '2022-09-01'),
(52, 31, 28617, '2022-09-10', 12500.00, true, '2022-10-01'),
(53, 33, 82430, '2022-10-05', 13000.00, true, '2022-11-01'),
(54, 34, 49762, '2022-11-12', 13500.00, true, '2022-12-01'),
(55, 36, 61073, '2022-12-01', 14000.00, true, '2022-12-15'),
(56, 38, 49762, '2022-12-15', 14500.00, true, '2023-01-01'),
(57, 39, 82105, '2023-01-01', 15000.00, true, '2023-02-01'),
(58, 41, 49762, '2023-02-20', 15500.00, true, '2023-03-01'),
(59, 43, 62490, '2023-03-05', 16000.00, true, '2023-04-01'),
(60, 47, 82105, '2023-04-12', 16500.00, true, '2023-05-01'),
(61, 48, 28617, '2023-05-01', 17000.00, true, '2023-06-01'),
(62, 50, 62490, '2023-06-20', 17500.00, true, '2023-07-01')


INSERT INTO destinado(quantidade, emprestimo_cod, equipamento_cod)
VALUES
(1, 1, 1),
(2, 2, 2),
(3, 3, 3),
(4, 4, 4),
(5, 5, 5),
(6, 6, 6),
(1, 7, 7),
(2, 8, 8),
(3, 9, 9),
(4, 10, 10),
(5, 11, 11),
(6, 12, 12),
(1, 13, 13),
(2, 14, 14),
(3, 15, 15),
(4, 16, 16),
(5, 17, 17),
(6, 18, 18),
(1, 19, 19),
(2, 20, 20),
(3, 21, 21),
(4, 22, 22),
(5, 23, 23),
(6, 24, 24),
(1, 25, 25),
(2, 26, 26),
(3, 27, 27),
(4, 28, 28),
(5, 29, 29),
(6, 30, 30),
(1, 31, 31),
(2, 32, 32),
(3, 33, 33),
(4, 34, 34),
(5, 35, 35),
(6, 36, 36),
(1, 37, 37),
(2, 38, 38),
(3, 39, 39),
(4, 40, 40),
(5, 41, 1),
(6, 42, 2),
(1, 43, 3),
(2, 44, 4),
(3, 45, 5),
(4, 46, 6),
(5, 47, 7),
(6, 48, 8),
(1, 49, 9),
(2, 50, 10),
(3, 51, 11),
(4, 52, 12),
(5, 53, 13),
(6, 54, 14),
(1, 55, 15),
(2, 56, 16),
(3, 57, 17),
(4, 58, 18),
(5, 59, 19),
(6, 60, 20),
(1, 61, 21),
(2, 62, 22);

### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Incluir para cada tópico as instruções SQL + imagens (print da tela) mostrando os resultados.<br>

># Marco de Entrega 01: Do item 1 até o item 9.1<br>


#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>

--------------------------------------------------------------------------------------------
____________________________________________________________________________________________
- 9.1.1 **__*Imagem*__**

![UMA IMAGEM](./images/9.1-tabelas-e-principais-consultas/9.1-teste.PNG)

--------------------------------------------------------------------------------------------
____________________________________________________________________________________________

- 9.1.2 **__*Imagem*__**

![UMA IMAGEM](./images/9.1-tabelas-e-principais-consultas/9.1-teste.PNG)

- 9.1.1 **__*Imagem*__**

![UMA IMAGEM](./images/9.1-tabelas-e-principais-consultas/9.1-teste.PNG)

- 9.1.1 **__*Imagem*__**

![UMA IMAGEM](./images/9.1-tabelas-e-principais-consultas/9.1-teste.PNG)

- 9.1.1 **__*Imagem*__**

![UMA IMAGEM](./images/9.1-tabelas-e-principais-consultas/9.1-teste.PNG)

- 9.1.1 **__*Imagem*__**

![UMA IMAGEM](./images/9.1-tabelas-e-principais-consultas/9.1-teste.PNG)

- 9.1.1 **__*Imagem*__**

![UMA IMAGEM](./images/9.1-tabelas-e-principais-consultas/9.1-teste.PNG)

- 9.1.1 **__*Imagem*__**

![UMA IMAGEM](./images/9.1-tabelas-e-principais-consultas/9.1-teste.PNG)

- 9.1.1 **__*Imagem*__**

![UMA IMAGEM](./images/9.1-tabelas-e-principais-consultas/9.1-teste.PNG)




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


