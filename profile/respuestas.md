Cambio las opciones de compilacion para C
profile_me_1_0: Carga tres vectores con valores constantes
Esencialmente tiene dos sumas de array 2D, una por fila y otro por columna 
>gcc -O0 -pg -Wall profile_me_1.c -o profile_me_1_0.e
>time ./profile_me_1_0.e
	real	0m0.887s
	user	0m0.763s
	sys	0m0.124s
>gcc -O1 -pg -Wall profile_me_1.c -o profile_me_1_1.e
>time ./profile_me_1_1.e
	real	0m0.771s
	user	0m0.655s	
	sys	0m0.116s
>gcc -O3 -pg -Wall profile_me_1.c -o profile_me_1_3.e
>time ./profile_me_1_3.e
	real	0m0.002s
	user	0m0.000s
	sys	0m0.002s
Conclusion: la optimizacion 3 cambia mucho. Aumentando size el tiempo de ejecución no cambia
para O3, por lo que de alguna manera saca del doble anidado pues el vector resultado tendrá todos los elementos iguales.

profile_me_2_0: Ingresando por consola un numero carga 3 vectores de esa dimension y realiza operaciones básicas sobre los elementos (pero todos sobre a!!!) y finalmente da la suma de los elementos.
gcc -O0 -pg profile_me_2.c -o profile_me_2_3.e -lm

