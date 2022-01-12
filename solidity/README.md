*introduccion*

- la importancia de web3 y solidity
- agrega la desentralizacion a la web3

*solidity sintaxis*
- `Pragma`
- Todos los contratos comienzan con la sentencia pragma el cual senAla la version de 
solidity a utilizar puede ser puntual o un rango de versiones

- `contract`
- para comenzar la declaracion del contrato

- `constructor`
- es igual que la programacion orientada a objetos
*code*
- `touch Estructura.sol` creamos un archivo con la extencion de .sol
```sol
//SPDX-License-Identifier: GPL-3.0 /*esto especifica la licensia de codiigo abierto*/

pragma solidity >=0.7.0 <0.9.0;  	/*este es el rango de solidity que vamos a usar*/

contract Estructura {
	
	constructor(){
		
	}
}



```
*tipos de datos*
- Numeros enteros
-	`int`
-	`uint`sin numeros negativos
- Bool
- address = almacenan direcciones de ethereum, sirve para relacionar cuentas y contratos
- string
- bytes = representa una cadena de bytes sin un formato especifico
- local variables = son variables que se alojan de forma temporal para utilizarse dentro del ambito de una funcion
- state variables = son variables que se almacenan en el contrato y que mantienen si valor aun despues de finalizada la ejecucion de la funcion.
- msg = valores relacionados con la configuracionn del; mensaje
- tx = valores relacionada con la transaccion actual
- block = valores relacionados con el bloque actual

- agregamos algunos tipos de datos al archivo Estructura.sol
- `Estructura.sol`
```diff
	// SPDX-License-Identifier: GPL-3.0

	pragma solidity >=0.7.0 <0.9.0;

	contract Estructura{
+	int cantidad;
+	uint cantidad_sin_signo;
+	address direccion;
+	bool firmado;
	
+	constructor(bool esta_firmado){
+		direccion = msg.sender;
+		firmado = estaFirmado;
	}
	}
```
- struct = tipo de dato estructurado que nos permite almacenar informacion de distintos tipos en un solo esquema
- array estaticos
- array dinamicos

- hagamos otro contrato
- `DatosEstructurados.sol`
```sol
// SPDX-License-Identifier:GPL-3.0

pragma solidity >=0.7.0 <0.9.0;

contract Clase{
	struct Alumno{
		string nombre;
		unit documento;
		}
	Alumno[] public alumnos; /*public te deja acceder una vez hagas el deploy*/

	constructor(){
		alumnos.push(Alumno({nombre:"juan",documento:1234}));
	}
}
```
- con este codigo ya abriamos almacenado al alumno dentro del contrato






