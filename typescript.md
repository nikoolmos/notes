# Typescript

### ¿Cómo generar un tipo a partir de la firma de una función?

Para generar un tipo tomando como base los argumentos de una función se puede implementar el siguiente código:

```
function calcularVelocidadMedia(posicion1: number, posicion2: number, tiempo: number) : number {
    return 0;
}

type Argumentos = Parameters<typeof calcularVelocidadMedia>;
```
De esta manera el tipo `Argumentos` correspondería con un array con la siguiente estructura:

```
[posicion1: number, posicion2: number, tiempo: number]
```

Es importante destacar que:
* Es necesario utilizar el operador `typeof` delante del nombre de la función.
* Es necesario utilizar el tipo auxiliar `Parameters`.
* El tipo construido es un array (tupla).

### ¡Cómo puedo generar un tipo a partir del valor de retorno de una función?

Para generar un tipo a partir del valor de retorno de una función se puede implementar el siguiente código:

```
function retornarUsuario() {
    return {
        nombre: 'nicolas',
        apellido: 'olmos'
        edad: 31,
    };
}

type MiNuevoTipo = ReturnType<typeof retornarUsuario>;
```
