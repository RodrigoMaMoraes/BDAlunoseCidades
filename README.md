# BDAlunoseCidades

## Alunos e Cidades (INNER JOIN E ALIASES)

CREATE TABLE Cidades:Esta criando uma tabela chamada "Cidades" com colunas "ID", "NOME" e "POPULACAO".

CREATE TABLE Cidades (
	ID 			INT PRIMARY KEY,
    NOME 		VARCHAR(60) NOT NULL,
    POPULACAO 	INT
    );

CREATE TABLE Alunos: Esta criando uma tabela chamada "Alunos" com colunas "ID", "NOME", "DATA_NASC" e "CIDADE_ID", onde "CIDADE_ID" é uma chave estrangeira referenciando "ID" na tabela "Cidades".    

    CREATE TABLE Alunos (
	ID 			INT PRIMARY KEY,
    NOME 		VARCHAR(60) NOT NULL,
    DATA_NASC	DATE,
    CIDADE_ID 	INT,
    

    FOREIGN KEY (CIDADE_ID) REFERENCES Cidades (ID)
    );
    
INSERT INTO Cidades VALUES ...: Inserindo dados na tabela cidades.
    INSERT INTO Cidades VALUES 
    (1, 'Arraial dos Tucanos', 42632),
    (2, 'Springfield', 13820),
    (3, 'Hill Valley', 27383),
    (4, 'Coruscant', 19138),
    (5, 'Minas Tirith', 31394);

INSERT INTO Alunos VALUES ...: Inserindo dados dos alunos, alguns com informações de cidade e outros sem.

insert into Alunos values (1, 'Immanuel Kant', date'1724-04-22', 4);
insert into Alunos values (2, 'Alan Turing', date'1912-06-23', 3);
insert into Alunos values (3, 'George Boole', date'2002-01-01', 1);
insert into Alunos values (4, 'Lynn Margulis', date'1991-08-12', 3);
insert into Alunos values (5, 'Nicola Tesla', date'2090-01-08', null);
insert into Alunos values (6, 'Ada Lovelace', date'1978-05-28', 4);
insert into Alunos values (7, 'Claude Shannon', date'1982-10-15', 3);
insert into Alunos values (8, 'Charles Darwin', date'2010-02-06', null);
insert into Alunos values (9, 'Marie Curie', date'2007-07-12', 3);
insert into Alunos values (10, 'Carl Sagan', date'2000-11-20', 1);
insert into Alunos values (11, 'Tim Berners-Lee', date'1973-12-05', 4);
insert into Alunos values (12, 'Richard Feynman', date'1982-09-12', 1);

SELECT * FROM Alunos A INNER JOIN Cidades C ON C.ID = A.CIDADE_ID: Realiza uma consulta que combina informações de alunos e cidades com base na correspondência dos IDs, retornando uma lista de alunos com suas cidades.

SELECT * FROM Alunos A 
INNER JOIN Cidades C ON C.ID = A.CIDADE_ID

![BDCIDADESALUNOS](https://github.com/RodrigoMaMoraes/BDAlunoseCidades/blob/main/RelatorioBDcidadesAlunos.png)https://github.com/RodrigoMaMoraes/BDAlunoseCidades/blob/main/RelatorioBDcidadesAlunos.png)
