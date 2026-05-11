# SDD - Ejercicio 1: PokeAPI (Ditto)

- Objetivo: Conectar con PokeAPI y extraer datos específicos de un Pokémon.
- Endpoint: https://pokeapi.co/api/v2/pokemon/ditto
- Lógica de Extracción:
  1. Usar fetch() para pedir el "paquete" (Response).
  2. Usar .json() para "abrir la caja" y obtener el objeto (Data).
  3. Mapear 'data.abilities' para extraer nombres de habilidades.
- Herramienta de Control: console.log(data) para inspeccionar el objeto completo.
- Estándar: Clean Code (eliminar logs innecesarios tras la validación).