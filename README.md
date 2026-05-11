# 📘 PokeAPI: Aprendiendo a abrir la "Caja de Datos"

Este no es un proyecto de copiar y pegar. Es mi proceso de aprendizaje para entender cómo viajar por internet (APIs) y traer información de vuelta a mi consola de Ubuntu.

## 🧠 Mi Filosofía: Entender antes de Correr
He tardado en entregar porque **quiero saber lo que hago**. No me sirve que el código funcione si no entiendo cómo se conectan los "cables". He seguido el **Método Polya** y el **SDD** para no perderme en la documentación de la PokeAPI.

## 📦 Conceptos Clave (Mis Apuntes)
Para no liarme con el código, uso estas metáforas:
* **API**: El intermediario que nos da los datos.
* **JSON**: El formato en el que llegan los datos, parecido a un diccionario.
* **Desempaquetado**: Usar `.json()` para que el texto se convierta en carpetas y listas que JavaScript entienda.
* **Navegación**:
    * **El Punto (.)**: "Entra en la carpeta" para objetos.
    * **El Corchete ([ ])**: "Elige de la estantería" para listas (Arrays). ¡Siempre empezamos desde el 0!

## 🛠️ Lo que he construido (Ejercicio 1)
He creado una función asíncrona para llamar a **Ditto**. He usado `console.log(data)` no solo para ver el nombre, sino para inspeccionar el "mapa" completo de la API y validar la estructura de los datos.

```javascript
async function getPokemon(name) {  
  const url = `https://pokeapi.co/api/v2/pokemon/${name}`;  
  const response = await fetch(url); // Pedimos el paquete
  const data = await response.json(); // Abrimos la caja
  
  // Navegación por la carpeta de datos
  console.log("Nombre:", data.name);
  console.log("Altura:", data.height);
  console.log("Peso:", data.weight);
}

## 👤 Autora
Desarrollado con serenidad y código por **Ana**.

🔗 **Mi GitHub:** [Haz clic aquí para ver mi perfil](https://github.com/AnaBHernandez)