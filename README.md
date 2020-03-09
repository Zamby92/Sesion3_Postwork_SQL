# Sesion3_Postwork_SQL
Uso de SQL, uso de servidor y consulta de información.
## Se usa la terminal de gitbash para poder trabajar en la carpeta  "Introduccion-a-Base-de-Datos" y  en la subcarpeta  "Sesion-03"
>>pwd
>>ls
>> cd  Introduccion-a-Base-de-Datos
>> cd Sesion-03

##Se crea una carpeta que se nombrara "Postwork-03"
>> mkdir Postwork-03

##El archivo que se descargo con anterioridad se mueve a la dirección asiganda en este momento, el cual previamente ya se habia hecho el unzip
>>cp "/c/Users/ alejandro.zambrano/desktop/Introduccion-a-Base-de-Datos/Sesion-02/Proyecto/Municipal-Delitos-2015-2020_ene2020" "/c/Users/alejandro.zambrano/desktop/Introducciona-a-Base-de-Datos/Sesion-03/Postwork-03"

##Nos edentramos a la carpeta en donde se encuenra el archivo
>> cd Municipal-Delitos-2015-2020_ene2020

##Observamos la información de los archivs
>> head Municipal-Delitos-2015-2020_ene2020.csv  

##Para no batallar con lo largo del archivo, se renombra
>>mv Municipal-Delitos-2015-2020_ene2020.csv Criminalidad-2015-2020.csv

##Nos metemos en la terminal de micly para poder copiar en el servidor el archivo y hacer uso de SQL
>>mycli -u root -h ec2-54-213-51-169-.us-west-2.compute.amazonaws.com

##observamos los dataset
>>show tables;

##Se crea las tablas
>> create table Criminalidad (
    Ano INT,
    Clave_Ent INT,
    Cve_Municipio INT,
    Municipio VARCHAR (50),
    Bien_juridico_afectado VARCHAR (100),
    Tipo_de_delito VARCHAR (100),
    Modalidad VARCHAR (100),
    Enero INT,
    Febrero INT,
    Marzo INT,
    Abril INT,
    Mayo INT,
    Junio INT,
    Julio INT,
    Agosto INT,
    Septiembre INT,
    Octubre INT,
    Noviembre INT,
    Diciembre INT);
 
 ##Se carga la información en el servidor, se hizo con el siguiente comando. Sin embargo no lo pude subir correctamente
 >>LOAD DATA LOCAL INFILE "c:/Users/alejandro.zambrano/Desktop/Introduccion-a-Base-de-Datos/Sesion-03/Postwork-03/Municipal-Delitos-2015-2020_ene2020.csv" into table Criminalidad FIELDS terminated by ",";
 
 
