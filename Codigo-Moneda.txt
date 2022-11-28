Algoritmo sin_titulo
//opcion de jugar o no
definir opj como entero
//opcion de apostar
definir opa como entero
//dinero inicial,recarga
definir saldo Como Entero
//apuesta
definir apuesta,recarga como entero
//lado de la moneda
definir lado Como entero
//Intuision
definir intuision Como entero
//nombre del jugador
definir nombre Como Caracter
recarga<-0
opj<-0
OPA<-0
Mientras opj<>2
	escribir 'ESCRIBA SU NOMBRE'
	leer nombre
	escribir '(1)DESEA JUGAR (2)SALIR'
	LEER opj
	segun opj
		1:
			Mientras opa<>4
				escribir '(1) RECARGAR SALDO'
				escribir '(2) APOSTAR'
				escribir '(3) VERIFICAR DINERO'
				escribir '(4) SALIR'
				leer opa
				segun opa
				1:
					Escribir 'DIGITE EL MONTO A RECARGAR'
					leer recarga
					escribir 'SALDO ANTERIOR ',saldo
					escribir 'RECARGA ',recarga
					saldo=saldo+recarga
					escribir 'SALDO ACTUAL ',saldo
				2:	
					escribir 'CUANTO DESEA APOSTAR'
					leer apuesta
					si ((saldo >0) & (saldo>=apuesta))
						lado<-Aleatorio(1,2);
					escribir 'ESCOGA (1)CARA (2)SELLO'
					leer intuision
					Para I<-1 Hasta 50 Con Paso 1 Hacer
						lado<-Aleatorio(1,2);
					Fin Para
					segun lado
						1:
							escribir 'GANO'
							saldo<-saldo+(apuesta*2)
						2:
							escribir 'PERDIO'	
							saldo<-saldo-apuesta
					escribir lado
					De Otro Modo:
						Escribir  'OPCION INCORRECTA'
					fin segun	
					sino
						escribir 'RECARGUE PRIMERO SU CUENTA'
					fin si
				3:
					escribir nombre, ' SU DINERO ACTUAL ES ',saldo
				4:
					Escribir  'SALIENDO DEL JUEGO'
				De Otro Modo:
					escribir 'OPCION INVALIDA'
			FinSegun
		fin mientras
			2:				
				Escribir  'SALIENDO DEL JUEGO'
			De Otro Modo:
				escribir 'OPCION INVALIDA'
fin segun	
fin mientras
FinAlgoritmo
