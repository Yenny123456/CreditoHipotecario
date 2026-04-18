# CreditoHipotecario
Algoritmo CreditoHipotecario
		Definir edad, ingresos, historialLimpio, avalDisponible Como Logico
		Definir edadNum, ingresosNum Como Real
		Definir respuesta Como Cadena
		
		Escribir "VALIDACIÓN CRÉDITO HIPOTECARIO "
		
		
		Escribir "Ingrese su edad (18-80 años):"
		Leer edadNum
		
		edad <- (edadNum >= 18 Y edadNum <= 80)
		
		Escribir "Ingrese sus ingresos mensuales ($):"
		Leer ingresosNum
		
		ingresos <- (ingresosNum >= 2000)
		
		
		Escribir "¿Tiene historial crediticio limpio? (s/n):"
		Leer respuesta
		
		historialLimpio <- (respuesta = "s" O respuesta = "S")
		
	
		Si historialLimpio Entonces
			Escribir "Se requiere aval. ¿Dispone de aval? (s/n):"
			Leer respuesta
			avalDisponible <- (respuesta = "s" O respuesta = "S")
		Sino
			avalDisponible <- Verdadero  
		FinSi
		
		
		Si edad Y ingresos Y (historialLimpio O avalDisponible) Entonces
			
			Escribir "CRÉDITO APROBADO"
		Sino
			Escribir " CRÉDITO RECHAZADO"
			
			Si No edad Entonces
				Escribir "Motivo: Edad fuera del rango permitido."
			Sino 
				Si No ingresos Entonces
					Escribir "Motivo: Ingresos insuficientes (mínimo $2000)."
				Sino
					Escribir "Motivo: Historial crediticio no limpio y no dispone de aval."
				FinSi
			FinSi
		finsi	

FinAlgoritmo
