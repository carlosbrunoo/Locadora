# APS
APS- DESENVOLVIMENTO WEB
# Configurações
Nesse projeto estou usando
JSF, MAVEN, PrimeFace, MYSQL
# Modelo do Banco de dados.

CRIANDO UM BANCO PARA UMA LOCADORA DE CARROS 

CRIANDO BANCO

CREATE DATABASE LOCADORA;

CREATE TABLE CLIENTE(
	IDCLIENTE INT PRIMARY KEY AUTO_INCREMENT,
	NOME VARCHAR(30) NOT NULL,
	SEXO ENUM('M','F') NOT NULL,
	EMAIL VARCHAR(50),
	CPF VARCHAR(15) UNIQUE	
);

CREATE TABLE CARRO(
	IDCARRO INT PRIMARY KEY AUTO_INCREMENT,
	FABRICANTE VARCHAR(100) NOT NULL,
	MODELO VARCHAR(50) NOT NULL,
	COR VARCHAR(30) NOT NULL,
	PORTAS VARCHAR(4) NOT NULL,
	COMBUSTIVEL ENUM('G','E','D') NOT NULL,
	ANO VARCHAR(4) NOT NULL,
	ID_CLIENTE INT,
	FOREIGN KEY(ID_CLIENTE)
	REFERENCES CLIENTE(IDCLIENTE)
);

# INSERINDO DADOS NA TABELA CLIENTE

INSERT INTO CLIENTE VALUES(NULL,'LADY SHIVA','F','LADY2@GMAIL.COM','023453890-10');
INSERT INTO CLIENTE VALUES(NULL,'HILLS MERCER','M','HILLS2@HOTMAIL.COM','014723666-15');
INSERT INTO CLIENTE VALUES(NULL,'BOB ESPONJA','M','ESPONJA2@HOTMAIL.COM','122713463-20');
INSERT INTO CLIENTE VALUES(NULL,'GUSTAVO ARLO','F','GUSTAV@HOTMAIL.COM','024890433-90');
INSERT INTO CLIENTE VALUES(NULL,'FATE NIGHT','F','FATE@GMAIL.COM','123723756-29');
INSERT INTO CLIENTE VALUES(NULL,'MARRONE GAROTAO','M','MARRONE@GMAIL.COM','011723453-25');

# INSERINDO DADOS NA TABELA CARRO

INSERT INTO CARRO VALUES(NULL,'FERRARI','F40','LARANJA','2','G','2019',7);
INSERT INTO CARRO VALUES(NULL,'CHEVROLET','CELTA','VERDE','2','G','2015',2);
INSERT INTO CARRO VALUES(NULL,'HYUNDAI','HB20','BRANCO','4','G','2017',3);
INSERT INTO CARRO VALUES(NULL,'VOLKSWAGEN','VOYAGE','BRANCO','4','G','2017',4);
INSERT INTO CARRO VALUES(NULL,'VOLKSWAGEN','GOL 6','VERDE','4','G','2019',5);
INSERT INTO CARRO VALUES(NULL,'VOLKSWAGEN','AMAROCK','VERDE','4','D','2019',1);

# OPS:
# Não consegui fazer a compra dos veiculos, mas o CRUD padrão está funcional
