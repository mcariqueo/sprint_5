# Sprint 5 - Nivell 1
## Exercici 1
A. Importa les dades de la base de dades emprada prèviament. 
B. Després de carregar les dades, mostra el model de la base de dades en Power BI.

Preguntas: ¿debo usar las tablas generadas o solo las que nos dieron?

1. Realizo la conexion con MySQL para obtener la base de datos ***sales***, que fue la que creé en MySQL para el sprint_4.

![](files_sprint_5/S5N1.png)

- En este caso podemos ver las 8 tablas extraidas desde MySQL. ***card_status*** corresponde a aquella que creamos para el sprint_4.


2. Ademas haré la creacion de la tabla ***users*** a partir de las tres tablas disponibles.

Para ello tengo el comando de ***anexar para crear nueva consulta***:

![](files_sprint_5/S5N1b.png)
- Lo primero es que todos los id se llamen igual y que los datos sean anexables. Es decir que el tipo de dato de cada campo sea el mismo. 

3. A las tablas les hago el *custom* de los campos.
![](files_sprint_5/S5N1c.png)

Es importante tambien hacer enfasis en la necesidad de hacer `cast`de las variables. Por ejemplo, la fechas que estan como texto, hacerlas que esten es formato `fecha`

## Exercici 2

La teva empresa està interessada a avaluar la suma total del amount de les transaccions realitzades al llarg dels anys.     

Per a aconseguir això, s'ha sol·licitat la creació d'un indicador clau de rendiment (KPI). El KPI ha de proporcionar una visualització clara de l'objectiu empresarial d'aconseguir una suma total de 25.000 € per cada any.

1. Primero creo la medida de 
   1. `KPI objetivo (euros) = 25.000 €`
    ![](files_sprint_5/S5N1E2a1.png)

1. Creo una matriz en la que tengo como filas los años y como campos el total de ventas.

    ![](files_sprint_5/S5N1E2a.png)

3. Realizo el filtro de aceuerdo a `declined = 1`
   
    ![](files_sprint_5/S5N1E2c.png)
   
4. Obtengo el KPI de acuerdo a la visulaizacion correspondiente: 

    ![](files_sprint_5/S5N1E2b.png)