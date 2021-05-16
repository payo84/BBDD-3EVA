# PROYECTO BASE DE DATOS QUEVEDO

## PORTADA

```

PROYECTO BASE DE DATOS

DESARROLLO DE APLICACIONES WEB CURSO “1” CLASE “B”

TEMA:
PROYECTO QUEVEDO FEST

INTEGRANTES:
GUSTAVO ADOLFO PAYO GANDARIAS

DOCENTE:
CARLOS GONZÁLEZ SÁNCHEZ

IES FRANCISCO DE QUEVEDO (MADRID)











```



## INDICE

```
Resultado:
```
INDICE

1.	INTRODUCCIÓN…………………………………………………………………………   3
2.	MODELO CONCEPTUAL
2.1.	ESPECIFICACIONES………………………………………………………………… 
2.2.	DIAGRAMA ENTIDAD-RELACIÓN…………………………………………… 5
3.	MODELO LÓGICO
3.1.	MODELO RELACIONAL……………………………………………………………6
3.2.	NORMALIZACIÓN/ DESNORMALIZACIÓN………………………………
4.	MODELO FÍSICO
4.1.	DIAGRAMA DE BASE DE DATOS……………………………………………. 7
4.2	. CREACIÓN DE TABLAS Y OTROS OBJETOS…………………………………… 8-9
4.3	. CARGA DE DATOS DE PRUEBA……………………………………………………. 10-11-12
5 
5.1. CONSULTAS MÁS FRECUENTES…………………………………………………… 13
5.2.  CONSULTAS SENCILLAS……………………………………………………………… 14




```

## INTRODUCCIÓN

```
Resultado:
```

INTRODUCCIÓN

Una base de datos es un conjunto de datos que pertenecen al mismo contexto, los tenemos todos almacenados para un posterior uso. 
Lo que en este proyecto vamos a reflejar es una base de datos que tendría una empresa dedicada a los festivales de música y organización de eventos, la mayoría de la base de datos iría en papel o de una manera informatizada, y que con la base de datos que creemos lo unificaríamos.
La base de datos en la que nos vamos a centrar sería la referente al
-	Área administrativa    y dividida a su vez en
•	Área Financiera
                    Ingresos
                    Gastos
•	Área personal
      Administración
      Seguridad
      Técnico
      Voluntariado
•	Área asuntos legales


Con esta base de datos tendremos de una forma organizada, clara, en poco espacio y de manera informatizada toda la información relativa tanto al personal que trabaja en nuestra empresa tanto directa como indirectamente, los asuntos legales que conlleve, así como lo relativo a la parte económica del proyecto, detallando de una manera concisa los gastos e ingresos que tenemos en la empresa, así como los detalles desde donde proceden, hasta las fechas de dichas facturas.
Cualquier dato es modificable, con lo que podemos añadir datos e ir actualizando nuestra base de datos con los eventos que nos vayan surgiendo y aquellos

```

## DIAGRAMA ENTIDAD RELACIÓN

Resultado:

```

```

## MODELO RELACIONAL


Resultado:
```

MODELO RELACIONAL

MODELO RELACIONAL:
•	Área financiera (COD_D, nombre, descripción, planta)
•	Personal ( COD_D, nombre, descripción, planta)
•	Asuntos legales (COD_D, nombre, descripción, planta)
•	Ingresos (COD_I, día, mes, año, COD_D(FK))
•	Gastos (COD_G,, día, mes, año, COD_D(FK))
•	Administración (DNI, nombre, apellido, teléfono,(COD_D(FK))
•	Seguridad (DNI, nombre, apellido, teléfono, num_habilitación seguridad,(COD_D(FK))
•	Técnico (DNI, nombre, apellido, teléfono,(COD_D(FK))
•	Voluntariado (DNI, nombre, apellido, teléfono,(COD_D(FK))
•	Entradas (CODIGO_E, número, precio, fecha,(COD_I(FK))
•	Patrocinadores (COD_P, factura, fecha,(COD_I(FK))
•	Retransmisión (COD_R, factura, fecha,(COD_I(FK))
•	Grabaciones (COD_G, factura, fecha,(COD_I(FK))
•	Artistas (nombre, apellido, fecha,(COD_G(FK))
•	Personal (nombre, apellido, fecha,(COD_G(FK))


```

## DIAGRAMA BASE DE DATOS

Resultado:
```

```

## CREACIÓN DE TABLAS Y OTROS OBJETOS


Resultado:
```
•	Create table ÁREA FINANCIERA (cod_d number(3) primary key, nombre varchar (15) not null, descripción varchar(15), planta number(1) not null);

•	Create table PERSONAL (cod_d number(3) primary key, nombre varchar (15) not null, descripción varchar(15), planta number(1) not null);


•	Create table ASUNTOS LEGALES (cod_d number(3), primary key, nombre varchar (15) not null, descripción varchar(15), planta number(1) not null);

•	Create table INGRESOS (cod_i number(5) primary key, dia number(2) not null, mes number(2) not null, año number (4) not null);


•	Create table GASTOS (cod_g number(5) primary key, dia number(2) not null, mes number(2) not null, año number (4) not null);


•	Create table ADMINISTRACIÓN (dni varchar(9) primary key, nombre varchar(15), apellido varchar(15), teléfono number(9)not null);


•	Create table SEGURIDAD (dni varchar(9) primary key, nombre varchar(15), apellido varchar(15), teléfono number(9)not null, num_habilitación_seguridad number(10) not null);


•	Create table TÉCNICO (dni varchar(9) primary key, nombre varchar(15), apellido varchar(15), teléfono number(9)not null);


•	Create table VOLUNTARIADO (dni varchar(9) primary key, nombre varchar(15), apellido varchar(15), teléfono number(9)not null);

•	Create table ENTRADAS (cod_e number(5) primary key, numero number(5) not null, precio number(3) , fecha date (8) not null);

•	Create table PATROCINADORES (cod_p number(4) primary key, factura number(7) not null, fecha date (8) not null; 

•	Create table RETRANSMISION (cod_p number(4) primary key, factura number(7) not null, fecha date (8) not null;


•	Create table GRABACIONES (cod_p number(4) primary key, factura number(7) not null, fecha date (8) not null;

•	Create table ARTISTAS (nombre varchar (15) not null, apellido varchar(15) not null, fecha date (8) not null;

•	Create table PERSONAL (nombre varchar (15) not null, apellido varchar(15) not null, fecha date (8) not null;






```

## INSERCCION DE DATOS

```
Resultado:
```
1.	Tabla AREA FINANCIERA:
Insert into AREA FINANCIERA values(001,´compras´,´dedicado a compra de material´,1);
Insert into AREA FINANCIERA values(002,´ventas´,´dedicado a ventas de material´,1);
Insert into AREA FINANCIERA values(003,´cuentas´,´dedicado a gestionar los gastos y  los ingresos´,1);

2.	Tabla PERSONAL:
Insert into PERSONAL values(001,´selección´,´dedicado a la selección de personal´,2);
Insert into PERSONAL values(002,´vacaciones´,´dedicado a los cuadrantes de vacaciones´,2);
Insert into PERSONAL values(003,´contratación´,´dedicado a la contratación del personal´,2);

3.	Tabla ASUNTOS LEGALES:
Insert into ASUNTOS LEGALES values(001,´contratos´,´dedicado a la redacción de contratos´,3);
Insert into ASUNTOS LEGALES values(002,´abogados´,´dedicado a soluciones juridicas´,3
Insert into ASUNTOS LEGALES values(003,´asesores´,´dedicado a asesoría juridica´,3);

4.	Tabla INGRESOS:
             Insert into INGRESOS values(1000,01,04,2020);
             Insert into INGRESOS values(2000,02,05,2020);
             Insert into INGRESOS values(3000,02,07,2020);
             Insert into INGRESOS values(4000,05,07,2020);
             Insert into INGRESOS values(5000,03,09,2020);

5.	Tabla GASTOS:
Insert into GASTOS values(1500,02,04,2020);
Insert into GASTOS values(1600,03,05,2020);
Insert into GASTOS values(1700,04,06,2020);
Insert into GASTOS values(1800,20,06,2020);
Insert into GASTOS values(1900,14,07,2020);

6.	Tabla ADMINISTRACION:
Insert into ADMINISTRACION values(´02088876M´,´Arturo´,´Fernandez´, 653240369);
Insert into ADMINISTRACION values(´01089823K´,´Javier´,´Marcillo´, 672340810);
Insert into ADMINISTRACION values(´21864310L´,´Maria´,´Del Olmo´, 614352120);
Insert into ADMINISTRACION values(´14537834T´,´Abigail´,´Castro´, 678564298);
Insert into ADMINISTRACION values(´96542984Y´,´Bonifacio´,´Herrera´, 614352120);

7.	Tabla SEGURIDAD:
Insert into SEGURIDAD values(´10124563R´,´Estefania´,´Suñe´, 627891007,1178945321);
Insert into SEGURIDAD values(´45290123L´,´Nabila´,´Abdelazid´, 633426547,0234178452);
Insert into SEGURIDAD values(´21320091U´,´David´,´Sabugo´, 678920031,9982634501);
Insert into SEGURIDAD values(´88923762E´,´Francisco´,´García´, 600754904,0978495720);
Insert into SEGURIDAD values(´47238461V´,´Manuel´,´Del Viso´, 671756917,7749814114);
Insert into SEGURIDAD values(´00342351T´,´Alfonso´,´García´, 670200810,9024567030);

8.	Tabla TECNICO:
Insert into TECNICO values(´87345294J´,´Francisco´,´Varela´, 688712300);
Insert into TECNICO values(´09307778T´,´Danilo´,´Armenteros´, 677123456);
Insert into TECNICO values(´13808865V´,´Valeria´,´Betancourt´, 600021642);
Insert into TECNICO values(´45624890B´,´Francisco´,´Martin´, 621026124);
Insert into TECNICO values(´34357456W´,´Valeria´,´Betancourt´, 699066650);

9.	Tabla VOLUNTARIADO:
Insert into VOLUNTARIADO values(´98346284A´,´Francisco´,´Del Olmo´, 698352000);
Insert into VOLUNTARIADO values(´21834039L´,´Enmanuel´,´Peña´, 641531220);
Insert into VOLUNTARIADO values(´21864310L´,´Maria´,´Del Olmo´, 620235012);

10.	 Tabla ENTRADAS:
Insert into ENTRADAS values(07673,5000,32, ´10-09-2020´);
Insert into ENTRADAS values(07674,4000,30, ´15-07-2020´);
Insert into ENTRADAS values(07675,5650,32, ´03-06-2020´);
Insert into ENTRADAS values(07676,5257,40, ´11-07-2020´);
Insert into ENTRADAS values(07677,4001,30, ´01-08-2020´);
Insert into ENTRADAS values(07678,5020,30, ´10-08-2020´);
Insert into ENTRADAS values(07679,5750,55, ´30-07-2020´);

11.	 Tabla PATROCINADORES:
Insert into PATROCINADORES values(2045,0200 ´01-03-2020´);
Insert into PATROCINADORES values(2047,0300, ´06-04-2020´);
Insert into PATROCINADORES values(2049,0400, ´20-04-2020´);

12.	 Tabla RETRANSMISION:
Insert into RETRANSMISION values(5987,0760,´10-09-2020´);
Insert into RETRANSMISION values(5732,0763,´15-07-2020´);
Insert into RETRANSMISION values(5100,0775,´03-06-2020´);

13.	 Tabla GRABACIONES:
Insert into GRABACIONES values(0800,1990,´03-06-2020´);
Insert into GRABACIONES values(0850,1998,´03-08-2020´);
Insert into GRABACIONES values(0890,1999,´13-06-2020´);

14.	 Tabla ARTISTAS:
Insert into ARTISTAS values(´Sergio´,´Dalma´, ´10-09-2020´);
Insert into ARTISTAS values(´Marta´,´Sanchez´, ´15-07-2020´);
Insert into ARTISTAS values(´Dani´,´Martin´, ´03-06-2020´);
Insert into ARTISTAS values(´David´,´Bisbal´, ´11-07-2020´);
Insert into ARTISTAS values(´Alejandro´,´Sanz´, ´01-08-2020´);
Insert into ARTISTAS values(´Aitana´,´Ocaña´, ´10-08-2020´);
Insert into ARTISTAS values(´Lola´,´Indigo´, 30-07-2020´´);

15.	 Tabla PERSONAL:
Insert into PERSONAL values(´Lydia´,´Alvarez´, ´03-06-2020´);
Insert into PERSONAL values(´Hector´,´Bermejo´, ´03-08-2020´);
Insert into PERSONAL values(´Raul´,´González´, ´13-06-2020´);













```

## CONSULTAS MAS FRECUENTES

```
Resultado:
```
 1.	Tabla AREA FINANCIERA:
 Insert into AREA FINANCIERA values(001,´compras´,´dedicado a compra de material´,1);
 Insert into AREA FINANCIERA values(002,´ventas´,´dedicado a ventas de material´,1);
 Insert into AREA FINANCIERA values(003,´cuentas´,´dedicado a gestionar los gastos y  los ingresos´,1);
 
 2.	Tabla PERSONAL:
 Insert into PERSONAL values(001,´selección´,´dedicado a la selección de personal´,2);
 Insert into PERSONAL values(002,´vacaciones´,´dedicado a los cuadrantes de vacaciones´,2);
 Insert into PERSONAL values(003,´contratación´,´dedicado a la contratación del personal´,2);
 
 3.	Tabla ASUNTOS LEGALES:
 Insert into ASUNTOS LEGALES values(001,´contratos´,´dedicado a la redacción de contratos´,3);
 Insert into ASUNTOS LEGALES values(002,´abogados´,´dedicado a soluciones juridicas´,3
 Insert into ASUNTOS LEGALES values(003,´asesores´,´dedicado a asesoría juridica´,3);
 
 4.	Tabla INGRESOS:
              Insert into INGRESOS values(1000,01,04,2020);
              Insert into INGRESOS values(2000,02,05,2020);
              Insert into INGRESOS values(3000,02,07,2020);
              Insert into INGRESOS values(4000,05,07,2020);
              Insert into INGRESOS values(5000,03,09,2020);
 
 5.	Tabla GASTOS:
 Insert into GASTOS values(1500,02,04,2020);
 Insert into GASTOS values(1600,03,05,2020);
 Insert into GASTOS values(1700,04,06,2020);
 Insert into GASTOS values(1800,20,06,2020);
 Insert into GASTOS values(1900,14,07,2020);
 
 6.	Tabla ADMINISTRACION:
 Insert into ADMINISTRACION values(´02088876M´,´Arturo´,´Fernandez´, 653240369);
 Insert into ADMINISTRACION values(´01089823K´,´Javier´,´Marcillo´, 672340810);
 Insert into ADMINISTRACION values(´21864310L´,´Maria´,´Del Olmo´, 614352120);
 Insert into ADMINISTRACION values(´14537834T´,´Abigail´,´Castro´, 678564298);
 Insert into ADMINISTRACION values(´96542984Y´,´Bonifacio´,´Herrera´, 614352120);
 
 7.	Tabla SEGURIDAD:
 Insert into SEGURIDAD values(´10124563R´,´Estefania´,´Suñe´, 627891007,1178945321);
 Insert into SEGURIDAD values(´45290123L´,´Nabila´,´Abdelazid´, 633426547,0234178452);
 Insert into SEGURIDAD values(´21320091U´,´David´,´Sabugo´, 678920031,9982634501);
 Insert into SEGURIDAD values(´88923762E´,´Francisco´,´García´, 600754904,0978495720);
 Insert into SEGURIDAD values(´47238461V´,´Manuel´,´Del Viso´, 671756917,7749814114);
 Insert into SEGURIDAD values(´00342351T´,´Alfonso´,´García´, 670200810,9024567030);
 
 8.	Tabla TECNICO:
 Insert into TECNICO values(´87345294J´,´Francisco´,´Varela´, 688712300);
 Insert into TECNICO values(´09307778T´,´Danilo´,´Armenteros´, 677123456);
 Insert into TECNICO values(´13808865V´,´Valeria´,´Betancourt´, 600021642);
 Insert into TECNICO values(´45624890B´,´Francisco´,´Martin´, 621026124);
 Insert into TECNICO values(´34357456W´,´Valeria´,´Betancourt´, 699066650);
 
 9.	Tabla VOLUNTARIADO:
 Insert into VOLUNTARIADO values(´98346284A´,´Francisco´,´Del Olmo´, 698352000);
 Insert into VOLUNTARIADO values(´21834039L´,´Enmanuel´,´Peña´, 641531220);
 Insert into VOLUNTARIADO values(´21864310L´,´Maria´,´Del Olmo´, 620235012);
 
 10.	 Tabla ENTRADAS:
 Insert into ENTRADAS values(07673,5000,32, ´10-09-2020´);
 Insert into ENTRADAS values(07674,4000,30, ´15-07-2020´);
 Insert into ENTRADAS values(07675,5650,32, ´03-06-2020´);
 Insert into ENTRADAS values(07676,5257,40, ´11-07-2020´);
 Insert into ENTRADAS values(07677,4001,30, ´01-08-2020´);
 Insert into ENTRADAS values(07678,5020,30, ´10-08-2020´);
 Insert into ENTRADAS values(07679,5750,55, ´30-07-2020´);
 
 11.	 Tabla PATROCINADORES:
 Insert into PATROCINADORES values(2045,0200 ´01-03-2020´);
 Insert into PATROCINADORES values(2047,0300, ´06-04-2020´);
 Insert into PATROCINADORES values(2049,0400, ´20-04-2020´);
 
 12.	 Tabla RETRANSMISION:
 Insert into RETRANSMISION values(5987,0760,´10-09-2020´);
 Insert into RETRANSMISION values(5732,0763,´15-07-2020´);
 Insert into RETRANSMISION values(5100,0775,´03-06-2020´);
 
 13.	 Tabla GRABACIONES:
 Insert into GRABACIONES values(0800,1990,´03-06-2020´);
 Insert into GRABACIONES values(0850,1998,´03-08-2020´);
 Insert into GRABACIONES values(0890,1999,´13-06-2020´);
 
 14.	 Tabla ARTISTAS:
 Insert into ARTISTAS values(´Sergio´,´Dalma´, ´10-09-2020´);
 Insert into ARTISTAS values(´Marta´,´Sanchez´, ´15-07-2020´);
 Insert into ARTISTAS values(´Dani´,´Martin´, ´03-06-2020´);
 Insert into ARTISTAS values(´David´,´Bisbal´, ´11-07-2020´);
 Insert into ARTISTAS values(´Alejandro´,´Sanz´, ´01-08-2020´);
 Insert into ARTISTAS values(´Aitana´,´Ocaña´, ´10-08-2020´);
 Insert into ARTISTAS values(´Lola´,´Indigo´, 30-07-2020´´);
 
 15.	 Tabla PERSONAL:
 Insert into PERSONAL values(´Lydia´,´Alvarez´, ´03-06-2020´);
 Insert into PERSONAL values(´Hector´,´Bermejo´, ´03-08-2020´);
 Insert into PERSONAL values(´Raul´,´González´, ´13-06-2020´);
 
 
 
 
 
 
 
 
 
 
 
 

```

## CONSULTAS MAS FRECUENTES
ENUMERAR LOS NOMBRES DE LOS ARTISTAS EN ORDEN ASCENDENTE
```sql
SELECT nombre, apellidos FROM artistas ORDER BY fecha ASC;
```
Resultado:
```
 
 
        Nombre        | apellidos
 ---------------------+-----------
  Dani                |  Martin
  David               |  Bisbal
  Marta               |  Sanchez
  Lola                |  Indigo
  Alejandro           |  Sanz
  Aitana              |  Ocaña 
  Sergio              |  Dalma
 
 
 (7 rows)
 
 

```

## CONSULTAS MAS FRECUENTES
ENUMERAR LAS GRABACIONES QUE SE HICIERON EN AGOSTO
```sql
SELECT cod_g, fecha FROM grabaciones WHERE date_part(´month´, fecha)=8;
```
Resultado:
```
         Cod_g    | fecha 
 -----------------+------------------------
          0850    | 03-09-2020
 
 (1 rows)

```

## CONSULTAS SENCILLAS
PERSONAL DE SEGURIDAD CUYA TERCERA LETRA DEL APELLIDO ES UNA R
```sql
SELECT nombre FROM Seguridad WHERE apellido LIKE '__R%';
```
Resultado:
```
 nombre 
 -----------------
  Francisco
  Alfonso
 
 (2 rows)

```

## CONSULTAS SENCILLAS
MOSTRAR TODA LA INFORMACION DE LA TABLA PERSONAL
```sql
SELECT * FROM personal;
```
Resultado:
```
  codigo_d | nombre      | descripción                            | planta
  ---------+-------------+----------------------------------------+-------
  001      |selección    | dedicado a la selección de personal    | 2                  
  002      |vacaciones   | dedicado a los cuadrantes de vacaciones| 2
  003      |contratación | dedicado a la contratación del personal| 2
  
  (3 rows)                                                  
    

```

```