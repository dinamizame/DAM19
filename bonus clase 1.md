#Decision Making
##Task
> Clients complain that the searches for a destinations sometimes fail. Head of product decided to address the issue, and ask development team to work on fix.

> The team committed to work out the solution during August. It was agreed that the team’s bonus payout would depend on effectiveness of the solution.

> The Head of Product ask you to analyze the data and help him to decide whether the team deserve the bonus?
Useful context:
Data for Barcelona destination (18452212) is representative so that any conclusions can be extrapolated for other destinations.

###Step 1
> BBDD : normalize variables August and September.(The point of normalization is to make variables comparable to each other). 

> * Review Data : August have dirty data, I remove the final input because as the time and date show us, that data belongs to September.

> * I include the  week colum in order to comprare the sames days.
> 
> * I took only 27 days of the data, for easily compare the same weeks.
>  FROM sabado 01-09-18  TO  sabado	04-08-18 
UNTIL jueves	27-09-18 TO	jueves	30-08-18


######TABLA TRAFICO - ERROR AGOSTO
| Dia semana 	|  Suma Usuarios Ago| %  U diarios |  Suma Errores Ago 	|% error diario  	|
|---	|---	|---	|---	|---	|
|  Lunes|117.424|16,10|1.614|1,37
	Martes |126.059|17,28|1.651|1,31  	|
|  	Miercoles|122.089  	|16,73  	|1.649  	|1,35  	|
|  	Jueves| 111.275 	|15,25  	| 1.540 	|1,38  	|
|  	Viernes|76.455  	|10,48  	|1.169  	|1,53  
|  	Sabado| 92.455|12,67|3089|3,34
|  Domingo	| 83.800 	|11,49  	|936  	|1,12
|TOTAL| 729.557 |100| 11.648 |1,60
***Saturday 18-08-18 number of users 22.273 number error data 2.352 that specific day the numbers of errors was more than expected (desviacion estandard),  out of the avarge, this could affect the results. ( Avarage erros would be 1,28% instead 1,60%)

######TABLA TRAFICO - ERROR SEPTIEMBRE
| Dia semana 	| Suma Usuarios Sep| %  U diarios | Suma Errores Sep 	|% error diario  	|
|---	|---	|---	|---	|---	|
|  Lunes| 140.797 | 16,25 | 1.510 |1,07
	Martes | 125.288 | 14,46 | 1.283 |1,02 	|
|  	Miercoles| 127.567   	| 14,72  	| 1.683  	|1,32  	|
|  	Jueves|  129.001  	| 14,89   	|  1.336 	|1,04	|
|  	Viernes| 126.151  	| 14,56  	| 1.280 	|1,01 
|  	Sabado|  111.169 | 12,83 | 953 |0,86
|  Domingo	|  106.360  	| 12,28   	| 905  	|0,85
|TOTAL|  866.333  |100|  8.950  |1,03


| MES 	| Suma Usuarios  | Suma Errores 	|% error MES  	|
|---	|---	|---	|---	|---	|
|AGOSTO| 729.557 |11.648 |1,60
SEPTIEMBRE|  866.333  |  8.950  |1,03

######I recommend to give the bonus because the traffic of Septembre increase if you compare with August and the errors went down in Septembrer, even when we had more trafic in the site
######Even though, the incident of the saturday 18 of August 2018 give us a new perspective of the real % of error minimized in the operation of September.  If we keep this day out of our analisys, we change  dramaticly to 1,28% of error in August instead 1,60%. Given this, the real improve was lower than we can apreciate in a firts view. Would be 0,25% instead of 0,57%.
###### I highly recommend to split the bonus in 3 month waiting for more data, that give us accurate information of the effectivity of the strategy




