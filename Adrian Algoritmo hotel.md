Algoritmo sin_titulo
	Escribir "HOLA MUY BUEN DIA, USTED USTED ESTA SIENDO ATENDIDO POR EL SERVICIO A CLIENTES DE LOS FAMOSOS HOTELES: LEDESMA MASCAREÑO"
	Escribir  "¿Cuantos dias se hospedará?:";
	Leer dias_de_hospedaje;
	precio <- 0;
	Escribir "Menu de habitaciones disponibles.";
	Escribir "elija una opcion del (1-4)"
	Escribir "    1.- Regular: 1 recamara con desayuno incluido";
	Escribir "    2.- Doble: 1 recamara con desayuno y cena incluido";
	Escribir "    3.- Familiar: 2 recamaras con todo incluido y buffet especial";
	Escribir "    4.- Suite-premium: Acceso a todo incluido, piscina privada, spa incluido sin costo adicional"
	Repetir
		Leer tipo_de_habitacion;
		Si tipo_de_habitacion<1 O tipo_de_habitacion>4 Entonces
			Escribir  "Numero invalido. Favor de ingresarlo nuevamente. ";
			Escribir "Menu de habitaciones disponibles.";
			Escribir "elija una opcion del (1-4)"
			Escribir "    1.- Regular: 1 recamara con desayuno incluido";
			Escribir "    2.- Doble: 1 recamara con desayuno y cena incluido";
			Escribir "    3.- Familiar: 2 recamaras con todo incluido y buffet especial";
			Escribir "    4.- Suite-premium: Acceso a todo incluido, piscina privada, spa incluido sin costo adicional"
		FinSi
	Hasta Que tipo_de_habitacion >= 1 Y tipo_de_habitacion <= 4;
	Si tipo_de_habitacion = 1 Entonces
		precio <- 500;
	FinSi
	Si tipo_de_habitacion = 2 Entonces
		precio <- 1200;
	FinSi
	Si tipo_de_habitacion = 3 Entonces
		precio <- 2000;
	FinSi
	Si tipo_de_habitacion= 4 Entonces
		precio<-5000;
	FinSi
	subtotal <- dias_de_hospedaje*precio;
	Si dias_de_hospedaje >= 3 Y tipo_de_habitacion = 3 Entonces
		Escribir "Usted eligio la habitacion familiar"
		descuento <- subtotal*0.25;
	SiNo
		Si dias_de_hospedaje >= 5 y tipo_de_habitacion = 1 Entonces
			Escribir "Usted eligio la habitacion regular"
			descuento<-subtotal*0.15;
		SiNo
			Si dias_de_hospedaje >= 7 y tipo_de_habitacion = 2 Entonces
				Escribir "Usted eligio la habitacion Doble"
				descuento<-subtotal*0.30;
			SiNo
				Si dias_de_hospedaje>=1 y tipo_de_habitacion=4 Entonces
					Escribir "Usted eligio la habitacion Suite-premium"
					descuento<-subtotal*0.10
				SiNo
					Si dias_de_hospedaje=3 y tipo_de_habitacion=1 Entonces
						Escribir "Usted eligio la habitacion regular"
						descuento<-subtotal*0.05
					SiNo
						descuento <- 0;
					Fin Si
				Fin Si
			Fin Si
		Fin Si
	FinSi
	total <- subtotal-descuento;
	Escribir "Se le descontará: ", "$" descuento;
	Escribir "La habitacion cuesta: ", "$" precio;
	Escribir "Valor de subtotal: ", "$" subtotal;
	Escribir "Usted debe pagar lo siguiente: ", "$" total;
FinAlgoritmo


<!---
AdrianFL04/AdrianFL04 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
