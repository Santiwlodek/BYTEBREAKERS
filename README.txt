BYTEBREAKERS — EL ÚLTIMO SISTEMA
Versión actualizada

ARCHIVOS
- index.html: estructura principal.
- styles.css: identidad visual, pantallas, inventario y banco privado.
- script.js: preguntas centralizadas, validación, progreso, ítems y banco.

EJECUCIÓN
1. Extraé los archivos en una misma carpeta.
2. Abrí index.html con Chrome, Edge o Firefox.
3. No requiere instalación ni servidor.

CONTENIDO
- 6 sectores y 30 preguntas en total.
- 6 preguntas de desarrollo corto (20 %) y 24 de opción múltiple.
- Las opciones múltiples se presentan en orden aleatorio.
- Los ítems tienen cantidades limitadas, efectos jugables y se guardan en LocalStorage.
- La exploración de sectores, los desafíos determinados y los sectores perfectos otorgan recompensas.
- El banco privado utiliza exactamente el mismo arreglo de preguntas que la partida.
- Calculadora binaria biofuturista: conversión en ambos sentidos con 8 interruptores (0–255).
- Se habilita una sola vez por desafío/pregunta individual; cada pregunta nueva tiene su propio registro persistente en LocalStorage. Se cierra a los 15 segundos. Si se recarga la página durante una activación, el uso permanece consumido. Los guardados anteriores se migran bloqueando únicamente el primer desafío de cada sector que ya figuraba como usado.
- El temporizador sigue corriendo al cambiar de modo o manipular interruptores; cerrar manualmente también consume el uso.

BANCO DE PREGUNTAS Y SEGURIDAD
El banco solicita la contraseña configurada por el usuario. La comprobación utiliza un hash
local y la clave no se muestra en la interfaz. Sin embargo, esta versión funciona íntegramente
en el navegador y no tiene autenticación de servidor: una persona con conocimientos técnicos
puede inspeccionar o modificar el JavaScript, recuperar el hash o alterar la validación. Por
lo tanto, el acceso es una barrera básica de interfaz, no una protección de seguridad real.
Para proteger contenido de forma efectiva se necesitaría un servidor que valide credenciales.

GUARDADO
El progreso y el inventario se guardan en LocalStorage del navegador. Si se borra el almacenamiento
del sitio o se utiliza otro navegador/dispositivo, el progreso no se transfiere.
