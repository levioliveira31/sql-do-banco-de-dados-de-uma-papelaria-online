# sql-do-banco-de-dados-de-uma-papelaria-online
CREATE database papelaria_online;

use papelaria_online;

CREATE table clientes(
    id int AUTO_INCREMENT primary KEY,
    nome char,
    recado char(80)
);
   
CREATE table produtos(
    id_prod int AUTO_INCREMENT primary KEY,
    nome_prod char,
    tipo char(18)
);

CREATE table entrega(
    id_cliente int(15),
    id_prod int(5),
    endeco char(70),
    FOREIGN key(id_cliente) REFERENCES clientes(id),
    FOREIGN key(id_prod) REFERENCES produtos(id_prod)
);
