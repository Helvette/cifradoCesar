## Cifrado César. 

#### *Crea una web que pida, por medio de un prompt(), una frase al usuario y devuelva el mismo mensaje encriptado según el algoritmo de Cifrado César con el parámetro de desplazamiento de 33 espacios hacia la derecha.*

## Diagrama de flujo de cifradoCesar.
![http://i.picasion.com/resize86/b5d238d854dc7a8a589cd4fa437657cb.png]

## Pseudocódigo de cifradoCesar.

```
Crea una función que almacene nuestro código de bienvenida al usuario{
	Crea un bucle que contenga una petición al usuario y se ejecute una vez antes de analizar las condiciones{
		Crea una variable que contenga una petición al usuario;
		Si la respuesta ingresada por el usuario es 1{
			Crear una variable que contenga otra petición al usuario, en este caso se solicita un texto para cifrar;
			Invocar a la función cipher con el texto ingresado por el usuario como argumento;
		}
		Si la respuesta ingresada por el usuario es 2{
			Crear una variable que contenga otra petición al usuario, en este caso se solicita un texto para descifrar;
			Invocar a la función decipher con el texto ingresado por el usuario como argumento;
		}De otra forma{
			Solicitar que se ingrese un número válido a través de un alert.
		}
	}Repetir el bucle siempre que el usuario ingrese algo diferente a 1 o 2;
}
Invocar a la función para que se ejecute lo que contiene;


Crea una función que cifre un string determinado{
	Crea una variable newString que almacene un string vacío para almacenar el texto ya cifrado allí;
	Iterar en cada índice del string{
		Si el valor en el índice actual es un espacio (" "){
			Sumarle a nuestra var newString un espacio;
		}
		Si el valor en el índice actual es una minúscula{
			Crear una variable character que almacene el valor del índice actual transformado a su número equivalente en ASCII;
			Cifrar el número ASCII con la fórmula del Cifrado César (((character - 97) + 33) % 26) + 97;
			Converstir a string el número ASCII;
			Concatenarle a var newString el string obtenido;
		}De otra forma{
			Crear una variable character que almacene el valor del índice actual transformado a su número equivalente en ASCII;
			Cifrar el número ASCII con la fórmula del Cifrado César (((character - 65) + 33) % 26) + 65;
			Converstir a string el número ASCII;
			Concatenarle a var newString el string obtenido;
		}
	}
	document.write del string ya cifrado.
	Retornar un alert con el string ya cifrado.
}

Crear una función que descifre un código determinado{
		Crea una variable newString que almacene un string vacío para almacenar el texto ya cifrado allí;
	Iterar en cada índice del string{
		Si el valor en el índice actual es un espacio (" "){
			Sumarle a nuestra var newString un espacio;
		}
		Si el valor en el índice actual es una minúscula{
			Crear una variable character que almacene el valor del índice actual transformado a su número equivalente en ASCII;
			Descifrar el número ASCII con la fórmula del Cifrado César modificada ((((character - 97) - 7) + 26) % 26) + 97;
			Convertir a string el número ASCII;
			Concatenarle a var newString el string obtenido;
		}De otra forma{
			Crear una variable character que almacene el valor del índice actual transformado a su número equivalente en ASCII;
			Descifrar el número ASCII con la fórmula del Cifrado César modificada ((((character - 65) - 7) + 26) % 26) + 65;
			Convertir a string el número ASCII;
			Concatenarle a var newString el string obtenido;
		}
	}
	document.write del string ya descifrado.
	Retornar un alert con el string ya descifrado.
}




