📘 Apuntes de Desarrollo: Consumo de APIs - Ana PM
## 📚 Recursos 1. Conceptos Fundamentales
API: El intermediario que nos da los datos.
JSON: El formato en el que llegan los datos (parecido a un diccionario).
Endpoint: La dirección URL a la que llamamos (la "puerta" de la carpeta).

## 2. La Caja de Datos (const data)
Cuando recibimos información, la metemos en una variable.
Variable raíz: Es el contenedor de TODO. Normalmente la llamamos data.
Desempaquetado: Usamos .json() para que el texto se convierta en carpetas y listas que JavaScript entienda.

## 3. Navegación: Puntos y Corchetes
Esta es la parte más importante para no perderse en la documentación:
El Punto (.) -> "Entra en la carpeta"
Se usa para objetos.
Ejemplo: data.sprites (Entra en la mansión data y abre la habitación sprites).
El Corchete ([ ]) -> "Elige de la lista"
Se usa para listas (Arrays). ¡Siempre empezamos a contar desde el 0!
Ejemplo: data.abilities[0] (De la estantería de habilidades, coge la primera caja).

## 4. Cómo leer la Documentación (PokeAPI)
Identificar el Recurso: Buscar la sección principal (ej: "Pokemon").
Filtrar el ruido: No leer todo, buscar solo la propiedad que pide el cliente (CTRL+F).
Seguir los "Cables": Si un dato es una URL, significa que hay más información en otra carpeta.

🚨 SECCIÓN: Errores Comunes y Cómo Solucionarlos
## 1. El Error del "Archivo Solitario" (CORS / Seguridad)
Qué ves: Un mensaje rojo en la consola que dice Unsafe attempt to load URL o algo sobre el protocolo file://.
Por qué pasa: Has abierto el HTML haciendo doble clic desde la carpeta. El navegador no te deja hacer peticiones a internet por seguridad.
Solución: Abrir siempre el proyecto con Live Server (botón "Go Live" en VS Code). La URL debe empezar por http://127.0.0.1:5500.

## 2. El Error del "Enchufe Olvidado"
Qué ves: La consola está totalmente vacía, no sale ni un mensaje.
Por qué pasa: Se te ha olvidado conectar el JavaScript al HTML.
Solución: Añadir la etiqueta <script src="app.js"></script> justo antes de cerrar el </body>.

## 3. El Error de "Navegación Ciega" (Undefined)
Qué ves: Un error que dice Cannot read properties of undefined o simplemente sale undefined en la consola.
Por qué pasa: Te has saltado un paso en la ruta de puntos o has escrito algo mal.
Ejemplo malo: data.front_default (Error: falta entrar en .sprites).
Ejemplo bueno: data.sprites.front_default.
Solución: Usar siempre console.log(data) para ver el mapa completo y verificar los nombres de las "carpetas".

## 4. El Error de la "Lista Invisible" (Array)
Qué ves: Intentas acceder a un dato pero te sale un error porque no pusiste el número de posición.
Por qué pasa: Has olvidado que las propiedades con corchetes [ ] son listas.
Solución: Recuerda que las listas empiezan en 0. Si quieres la primera habilidad, es abilities[0], no abilities[1].