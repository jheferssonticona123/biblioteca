
create database dblibreria;
use dblibreria;
create table tusuario(
nombre_usuario varchar(50),
correo_usuario varchar(50)  primary key,
contraseña_usuario varchar(50)
);
create table tlibro(
nombre_libro varchar(50)  primary key,
autor_libro varchar(50),
categoria_libro varchar(50),
precio_libro varchar(50)
);
create table tpago(
num_operacion int auto_increment primary key,
autor_libro varchar(50),
categoria_libro varchar(50),
precio_libro varchar(50),
correo_usuario varchar(50),
nombre_libro varchar(50),
FOREIGN KEY (correo_usuario) REFERENCES tusuario(correo_usuario),
FOREIGN KEY (nombre_libro) REFERENCES tlibro(nombre_libro)
)
