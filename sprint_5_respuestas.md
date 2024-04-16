<center><h1>Sprint 5 - Nivell 1</h1></center>

## Exercici 1

I) Realizo la conexion con MySQL para obtener la base de datos ***sales***, que fue la que creé en MySQL para el sprint_4.

<center>        

![](files_sprint_5/S5N1.png)        

</center>     


<center>
    <p style="line-height: 0.25;">En este caso podemos ver las 8 tablas extraídas desde MySQL.</p> 
    <p style="line-height: 0.25;">Card_status corresponde a aquella que creamos para el sprint_4.</p>
</center>

II) Ademas haré la creacion de la tabla ***users*** a partir de las tblas de users de los distintos paises.

Para ello tengo el comando de ***anexar para crear nueva consulta***:
<center>  

![](files_sprint_5/S5N1b.png)

</center> 

- Inicialmente realizo dejo todos los ID con este nombre, para poder anexar las tablas y crear una tabla de users. A las tablas les hago el *custom* de los campos.
  
- El modelo final es el siguiente: 
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

3. Realizo el filtro de aceuerdo a `declined = 0 `
   
    ![](files_sprint_5/S5N1E2c.png)
   
4. Obtengo el KPI de acuerdo a la visulaizacion correspondiente: 

    ![](files_sprint_5/S5N1E2b.png)


## Exercici 3

Des de màrqueting et sol·liciten crear una nova mesura DAX que calculi la mitjana de transaccions realitzades durant l'any 2021. 

Mesura DAX  y resultado en etiqueta: 
    ![](files_sprint_5/S5N1E3a.png)


És important recordar que l'empresa té un objectiu de vendes establert en 250 transaccions.  

Lo primero es crear la nueva medida de KPI 250 transacciones:

![](files_sprint_5/S5N1E3b.png)

Finalmente, realizo una visualización de Finalmente tenemos: 

![](files_sprint_5/S5N1E3c.png)


## Exercici 4
Realitza el mateix procediment que vas realitzar en l'exercici 3 per a l'any 2022.

![](files_sprint_5/S5N1E4a.png)


## Exercici 5

L'objectiu d'aquest exercici és crear una KPI que visualitzi la quantitat d'empreses per país que participen en les transaccions.       

La meta empresarial és garantir que hi hagi almenys 3 empreses participants per país.    

`KPI = 3`

Per a aconseguir això, serà necessari utilitzar DAX per a calcular i representar aquesta informació de manera clara i concisa: 

![](files_sprint_5/S5N1E5a.png)


## Exercici 6


Genero un filtro para mostrar solo los meses con datos:

![](files_sprint_5/S5N1E6a.png)


![](files_sprint_5/S5N1E6b.png)


## Exercici 7

Crea un gràfic de columnes agrupades que reflecteixi la sumatòria de les vendes per mes.        

L'objectiu de l'empresa és tenir almenys 10.000 transaccions per mes.

![](files_sprint_5/S5N1E7a.png)


## Exercici 8

En aquest exercici, es vol aprofundir en les transaccions realitzades per cada usuari/ària i presentar la informació de manera clara i comprensible. 

Lo primero será crear aquellas columnas que solicitan como:

| N | Campo            | Descripción                                             |
|---|------------------|---------------------------------------------------------|
| 1 | Nom i cognom     | Nombre y Apellido                                       |
| 2 | Edat             | A partir de birth_date obtengo la edad                  |
| 3 | Mitjana euros    | Media en Euros                                          |
| 4 | Mitjana dòlars   | Media en Dólares a traves de la equivalencia entregada. |
| 5 | Condición        | Cumple/No Cumple                                        |


1. Nom i cognom

![](files_sprint_5/S5N1E8a.png)

2. Mitjana euros: Sumatoria de amount
   
3. Mitjana dòlars: Creo una nueva medida:
   
   ![](files_sprint_5/S5N1E8b.png)

4.  La condicion queda reflejada en:
   ![](files_sprint_5/S5N1E8c.png)

   Finalmente la tabla es:

   ![](files_sprint_5/S5N1E8d.png)


## Exercici 9
Redacta un paràgraf breu, de màxim 50 paraules, explicant el significat de les xifres presentades en les visualitzacions de Power BI. Pots interpretar les dades en general o centrar-te en algun país específic. Acompanya les interpretacions realitzades amb la captura de pantalla de les visualitzacions que analitzaràs:

---
**Análisis de KPIs de Ventas**

Los KPIs proporcionan una visión del rendimiento durante el 2021, mientras que del 2022 se dispone de poca información. El año 2021, las ventas superaron ampliamente el objetivo anual, se superó la meta anual de transacciones. China y España tienen menos de 3 empresas, esto permite una oportunidad de mejora en estos mercados.


<center><h1>Sprint 5 - Nivell 2</h1></center>

## Exercici 1



## Exercici 2

Creo el DAX de ventas totales de alemania: 

![](files_sprint_5/S5N2E2a.png)

   
```SUM('sales transactions'[amount])```: Esto suma el monto de las ventas de la tabla 'sales transactions'.

```FILTER('sales companies', 'sales companies'[country] = "germany")```: Esto filtra la tabla 'sales companies' para que solo incluya las filas donde el país es "germany".

En resumen: La expresión DAX que he utilizado, calcula la suma de las ventas ('amount') en la tabla 'sales transactions', considerando solo las ventas realizadas por empresas con sede en ```germany```, según lo especificado en la tabla '''sales companies'''.

## Exercici 3
Escriu un breu paràgraf, màxim de 25 paraules, indica en quin mes no es va arribar a complir amb l'objectiu proposat de l'exercici 1.

#### Respuesta:
Hubo 5 meses que no alcanzaron la meta. Será necesario analizar las causas (temporada baja, falta de campañas, etc.) para proponer estrategias de mejora y aumentar las ventas.



# Sprint 5 - Nivell 3
## Exercici 1

Les mesures estadístiques claus de les variables que consideris rellevants per a comprendre les transaccions realitzades pels usuaris/es: 
- Quantitat de productes comprats per cada usuari/ària.       
- Mitjana de vendes realitzades per usuari/ària, visualitza quins usuaris/es tenen una mitjana de vendes superior a 150 i quins no.
- Comptabilitzar el preu del producte més car consumit per cada usuari/ària.
- Visualitza la distribució geogràfica dels usuaris/es.


Creo en MySQL una tabla que relacione los productos y los usuarios:

[](files)
