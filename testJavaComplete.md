# VARIABLES #

## 1- Responde las siguientes preguntas en la sección de comentarios:

### 1. ¿Qué es una variable y para qué sirve?

- Una variable es un espacio que se reserva en memoria y que sera utilizado 
para guardar un dato.
- Es aconsejable que usemos nombres significativos, que nos hagan intuir con facilidad que 
datos guardamos en ella.
- Se trata de una cuestion practica, pues siempre resultara mas facil recordar el nombre
precioVenta que la direccion de memoria 34D0 en hexadecimal o numeros binarios.
- Reglas que impone JAvaScrippt:
- Pueden contener tanto letras como numeros. Es decir caracteres alfanumericos.
- Pero siempre el primer caracter debera ser una letra o un guion bajo.
- No se admiten espacios en blanco ni otros símbolos como pueden ser: $ % + ( ) / -, etc.
- Se ha establecido el convencionalismo de utilizar minúsculas en los nombres de variables, 
excepto en el caso de que se componga de dos palabras, en cuyo caso la primera letra de
la segunda palabra se suele escribir en mayúsculas la primera letra. 
- Aunque esto no es estrictamente necesario cumplirlo.
- No llevan tildes
- No podemos usar las palabras reservadas para nombrar la variable.
- En Js existen tres formas de crear una variable, var, let y const.

### 2. ¿Cuál es la diferencia entre declarar e inicializar una variable?

- Declarar una variable consiste en 'informar' al programa de que vamos a  necesitar ese espacio de memoria, como lo vamos a llamar y que tipo de datos
guardaremos en el. Ej: 
    let nombre;
- Inicializar una variable se le llama a la primera vez que se dice cual va a ser ese dato  que vamos a guardar en ese espacio de memoria. Ej:
    let nombre = 'Rodrigo';

### 3.  ¿Cuál es la diferencia entre sumar números y concatenar strings?

-  La diferencia entre sumar numeros y concatenar es que al sumar numeros, se hace la  operacion matematica, es decir, 7 + 8 = 15, pero al concatenar strings no se hace la  operacion matematica, sino se colocan los dos strings juntos, por ejemplo, "7" + "8" ="78".

### 4. ¿Cuál operador me permite sumar o concatenar?

- El operador que permite sumar y concatenar es el +.

## 2- Determina el nombre y tipo de dato para almacenar en variables la siguiente información:

- Nombre 'String'
- Apellido 'String'
- Nombre de usuario en Platzi 'String'
- Edad  'Number'
- Correo electrónico 'String' 
- Mayor de edad 'Boolean'
- Dinero ahorrado 'Number'
- Deudas 'Number'

## 3- Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.

```js

var name, surname, userName, age, mail, adult, savedMoney, debt, realMoney;

name = "Rodrigo Nicolas";
surname = "Villarreal";
userName = "villaRodrigo11"
age = 21;
mail = "villarrealrodrigo.n@gmail.com";
adult = true;
savedMoney = 10000;
debt = 7000;
realMoney = savedMoney - debt;

```
 
## 4- Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:

- Nombre completo (nombre y apellido)
- Dinero real (dinero ahorrado menos deudas)

```js

var name, surname, userName, age, mail, adult, savedMoney, debt, realMoney;

name = "Rodrigo Nicolas";
surname = "Villarreal";
userName = "villaRodrigo11"
age = 21;
mail = "villarrealrodrigo.n@gmail.com";
adult = true;
savedMoney = 10000;
debt = 7000;
realMoney = savedMoney - debt;

console.log("Mi nombre completo es " + name + " " + surname);
console.log("Mi dinero real es " + realMoney);

```

# FUNCIONES #

## 1️- Responde las siguientes preguntas en la sección de comentarios:

### 1. ¿Qué es una función?

-  Una funcion es un conjunto de instrucciones que forman parte de un mismo proceso. Nos permiten encapsular bloques de codigo para reutilizarlos y ejecutarlos en el futuro.

### 2. ¿Cuándo me sirve usar una función en mi código?

- Una funcion en mi codigo sirve para no repetir las instrucciones y calculos que necesitemos  para nuestro programa muchas veces, sino hacer una sola funcion que haga esas instrucciones y calculos cuando lo necesite sin volverlo a escribir en el codigo.
- Tambien sirve para ordenar y mejorar la legibilidad de nuestro codigo.

### 3. ¿Cuál es la diferencia entre parámetros y argumentos de una función?

-  La diferencia es que los parametros son las variables que ponemos al hacer una funcion, y los argumentos son los valores que se pasan a la funcion cuando es invocada.
-  Ej:
    function sum(a, b){ <----- Parametros = a y b.
    return a + b;
    }

    const result = sum(7,4);  <--------- Argumentos = 7 y 4.

## 2️- Convierte el siguiente código en una función, pero cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:

    const name = "Juan David";
    const lastname = "Castro Gallego";
    const completeName = name + lastname;
    const nickname = "juandc";

    console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");

```js

const name = "Juan David ";
const lastname = "Castro Gallego";
const completeName = name + lastname;
const nickname = "juandc";

console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");

function presentation(name, lastname, nickname){
    return frase = "Mi nombre completo es " + name + ' ' + lastname + "pero prefiero que me digas " + nickname;
}

presentation ("Rodrigo Nicolas","Villarreal ", "Villa")

```

# CONDICIONALES #

## 1️- Responde las siguientes preguntas en la sección de comentarios:

### 1. ¿Qué es un condicional?

- Un condicional es para cuando se necesita realizar decisiones y llevar a cabo diferentes acciones acordes dependiendo de distintas entradas, y nos permite evaluar si es TRUE or FALSE.
- Son la forma en que ejecutamos un bloqe de codigo u otro dependiendo de alguna condicion o validacion.

### 2. ¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?

- Existen muchos tipos de condicionales, en if ... else, que es la mas comun, lo que se dice con
este condicional es que si (if) la condcion dentro reotrna verdadero(true), entonces ejecute el codigo A, sino (else) ejecuta el codigo B.
Ej:
    if (condición) {
        código a ejecutar si la condición es verdadera
    } else {
        ejecuta este otro código si la condición es falsa
        }

Agregando else if, cuando se necesita alguna otra mas condicion.

Otro condiconal es el switch, es muy parecido al if ...else, pero para cuando hay muchos mas
casos a comparar si son true or false, ej: 
    switch (expresion) {
        case choice1:
            ejecuta este código
            break;

        case choice2:
            ejecuta este código
            break;

 Se pueden incluir todos los casos que quieras

        default:
        por si acaso, corre este código
            
        }
    
El condicional if (con el else y else if) nos permite hacer validaciones completamente distintas(si asi queremos) en cada validacion o condicional. En cambio, en el switch todos los cases se comparan con la misma variable o condicion que definimos en el switch. 

### 3. ¿Puedo combinar funciones y condicionales?

- Podemos encadenar una respusta desde un condional a otro pero no podemos
combinarlo dentro de una misma expresión. Si podemos ocuparlos de forma separada y
luego encadenar una acción dependiendo del resultado.

## 2️- Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:

const tipoDeSuscripcion = "Basic";

switch (tipoDeSuscripcion) {
   case "Free":
       console.log("Solo puedes tomar los cursos gratis");
       break;
   case "Basic":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
       break;
   case "Expert":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
       break;
   case "ExpertPlus":
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
       break;
}

```js

let tipoDeSuscripcion = "Expert";

    if(tipoDeSuscripcion === "Basic"){
        console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
    }else if(tipoDeSuscripcion === "Free"){
        console.log("Solo puedes tomar los cursos gratis");
    }else if(tipoDeSuscripcion === "Expert"){
        console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
    }else if(tipoDeSuscripcion === "ExpertPlus"){
        console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
    }else {
        console.log("No tienes ninguna suscripcion en Platzi");
    }

```

## 3️- Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo  con if (sin else ni else if).

💡 Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar 
este comportamiento con arrays u objetos y un solo condicional. 😏

```js

let tipoDeSuscripcion = ['Basic', 'Free', 'Expert', 'ExpertPlus'];

let infoDeSuscripcion = ["Puedes tomar casi todos los cursos de Platzi durante un mes",
"Solo puedes tomar los cursos gratis",
"Puedes tomar casi todos los cursos de Platzi durante un año",
"Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año"]

let userSuscription = prompt("Cual suscripcion deseas? \n Basic \n Free \n Expert \n ExpertPlus")

for(let i=0; i < tipoDeSuscripcion.length; i++){
    if(userSuscription == tipoDeSuscripcion[i]){
        console.log("Te suscribiste al plan "+ tipoDeSuscripcion[i] + " y " + infoDeSuscripcion[i])
    }
    }

```

# CICLOS #

## 1️- Responde las siguientes preguntas en la sección de comentarios:

### 1. ¿Qué es un ciclo?

- Un ciclo es un bucle, es decir, un conjunto de sentencias que se repite una numero determinado de veces hasta que se cumpla cierta condicion.

### 2. ¿Qué tipos de ciclos existen en JavaScript?

- Existen el tipo de ciclo For, Sintaxsis:

    for(var valorInicio; condicion; incremento) {
    instrucciones dentro del bucle
    }

    Dentro del paréntesis podemos distinguir las tres partes siguientes:
    1. La primera en la cual damos el valor inicial a la/s variable/s que  controlarán que el bucle se ejecute. 
    2. La segunda en la que se establece la condición que se debe cumplir para continuar la ejecución del bucle.
    3. La tercera en la que variamos los valores a la/s variable/s de control del bucle.

- El ciclo For .. In, que se trata de una estructura de control derivada del for, Sintaxsis:

    for(indice in array) {
    ...instrucciones dentro del for
        }
    
    Esta estructura nos permite recorrer todos y cada uno de los elementos contenidos en un array.  Ej:

        var colores = [“Rojo”, “Verde”, “Azul”, “Negro”];

        for(i in colores) {
        alert(colores[i]);
        }


- El ciclo While, que segun la condiciond e entrada indicada al comienzo del bucle, permite que las instrucciones de su interior se ejecuten varias veces o ninguna. Sintaxis:

    while(condicion) {
    …
    }

    While repetirá mientras se cumpla la condición de entrada.

- Y el ciclo Do...While, es muy similar al While, pero a diferencia de que en el otro puede que no se ejecute ninguna vez, do while se ejecutara al menos la primera vez. Sintaxsis:
    
    do {
    …
    } while(condicion);

    La condicion se situa al final del bucle, es decir se mirara si se cumple una vez ejecutadas las intrucciones de su interior. Es por esto que al menos la primera vez se realizara el bucle, despues se observara la condicion, si se sigue cumpliendo se volvera a Do, en caso contrario no se volvera y proseguira con la siguiente instruccion inmediata al bucle.

### 3. ¿Qué es un ciclo infinito y por qué es un problema?

Un ciclo infinito es cuando no se llega a cumplir la condicion de salida del bucle, y se repetiria indefinidamente.

### 4. ¿Puedo mezclar ciclos y condicionales?

Si si se puede, esto se llama anidamiento. Lo que si debemos tener en cuenta es que sentencias pertenecen a uno y cuales a otro, ya que una incorreccion a la hora de cerrar los distintos bloques, puede generar porblemas en la ejecucion del programa.

## 2️- Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:

for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
}

```js

var i = 0;

while(i < 5) {
    console.log("El valor de i es " + i);
    i++;
}

var i = 0;

do {
    console.log("El valor de i es: " + i);
    i++;
}while(i < 5);

```

for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}

```js

var i = 10

while(i > 1){
    console.log("El valor de i es: " + i);
    i--;
}

do{
     console.log("El valor de i es: " + i);
    i--;
} while(i > 1);
```

## 3️- Escribe un código en JavaScript que le pregunte a los usuarios cuánto es 2 + 2.

 Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.
💡 Pista: puedes usar la función prompt de JavaScript.

```js

do{
    var answer = prompt('Cuanto es 2 + 2?');
    if(answer == 4) console.log("Perfecto")
}while(answer != 4)

// ----------------------------------------------------------------------------------- //

while (answer != 4) {
    var answer = prompt('Cuanto es 2 + 2?');
    if(answer == 4) console.log("Perfecto")
}

```

# ARRAYS Y OBJETOS #

## 1️- Responde las siguientes preguntas en la sección de comentarios:

### 1. ¿Qué es un array?
    
- Los arrays son un tipo especial de datos que podriamos describir como una coleccion de variables. 
- Una lista de elementos.

```js
const array = [1, 'jaja', true. false];

```

### 2. ¿Qué es un objeto?
- Un objeto es un entidad independiente con propiedades y tipos.

```js

const obj = {
    name: 'Car',
    model: 'X',
    year: 2021,
}

```

### 3- ¿Cuándo es mejor usar objetos o arrays?

- Los arrays se utilizan cuando almacenamos múltiples valores de una sola variable, mientras que un objeto puede contener múltiples variables con sus valores. 
- Un array también se puede considerar como un objeto y tiene la mayoría de las funcionalidades del objeto.

### 4. ¿Puedo mezclar arrays con objetos o incluso objetos con arrays?

- Si, los arrays pueden guardar objetos. Y los objetos pueden guardar arrays entre sus propiedades.
        

## 2️- Crea una función que pueda recibir cualquier array como parámetro  e imprima su primer elemento.

```js

var a = [1, 2, 3, 4, 5];

function firstArray(a){
    return answer = a[0];
}
firstArray(a);

```

## 3️- Crea una función que pueda recibir cualquier array como parámetro  e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).

```js

let names = ['Carlos', 'Juan', 'Tristan', 'Miguel']

for(i in names){
    console.log(names[i]);
}

// -----------------------------------------//

let names = ['Carlos', 'Juan', 'Tristan', 'Miguel']

function allArrays(names){
    for (let i = 0; i < names.length; i++){
        console.log(names[i])
    }
}
```
## 4️- Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).

```js

var myHouses = {
tenant: "Ramiro",
type: "Classic",
year: 1983, 
};

for(i in myHouses){
    console.log(myHouses[i]);
}


```