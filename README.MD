<h1> Sistema de registro </h1>
-Estado del proyecto: Finalizado


Este proyecto permite agregar nombres a una lista y luego realizar un sorteo para elegir un "amigo secreto" al azar.

## 📌 Requisitos

- HTML con un campo de entrada (`input`) y listas (`ul`) con los IDs adecuados.
- Un entorno que soporte JavaScript (navegador web).

## 📜 Código JavaScript

```js
const inputAmigo = document.getElementById('amigo');
const listaAmigos = [];
const ulListaAmigos = document.getElementById('listaAmigos');
const ulResultado = document.getElementById('resultado');

function agregarAmigo() {
    listaAmigos.push(inputAmigo.value);
    ulListaAmigos.innerHTML += `<li>${inputAmigo.value}</li>`;
}

function sortearAmigo() {
    const random = Math.floor(Math.random() * listaAmigos.length);
    const amigoSecreto = listaAmigos[random];
    ulResultado.innerHTML = `<li>El amigo secreto es: ${amigoSecreto}</li>`;
}
```

## 📖 Explicación

### `agregarAmigo()`
- Toma el valor ingresado en el campo `input` y lo agrega a la lista `listaAmigos`.
- Luego, actualiza la lista en pantalla (`ulListaAmigos`).

### `sortearAmigo()`
- Selecciona un amigo al azar de la lista `listaAmigos`.
- Muestra el nombre del amigo seleccionado en la lista `ulResultado`.

## 🎯 Uso

1. Ingresar un nombre en el campo de texto y presionar el botón "Agregar".
2. Una vez agregados los amigos, presionar el botón "Sortear".
3. El nombre del amigo secreto se mostrará en pantalla.

## 🚀 Mejoras futuras
- Evitar nombres duplicados.
- Validar la entrada del usuario.
- Permitir eliminar nombres de la lista antes del sorteo.
