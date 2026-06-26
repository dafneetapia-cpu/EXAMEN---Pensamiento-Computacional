# EXAMEN  -  Pensamiento-Computacional
Composición tipográfica interactiva y generativa reactiva al sonido en tiempo real. Inspirada en las vanguardias históricas (Dadaísmo y Constructivismo). Desarrollado en p5.js.
# Composición Interactiva Dadaísta: Destruye el Orden
**Autora:** Dafne Catalina Tapia Sandoval  
**Carrera:** Diseño  
**Asignatura:** Pensamiento Computacional  

---

## 🔗 Enlaces del Proyecto
* [Ejecutar Proyecto en p5.js (Link Público)](PONER_AQUI_EL_LINK_DE_PRESENTACION)
* [Revisar Código en p5.js (Link Editable)](PONER_AQUI_EL_LINK_DE_EDITOR)

---

## 1. Descripción General
### Descripción Objetiva
Este proyecto es un afiche digital interactivo programado en p5.js. El sistema cambia su comportamiento y su aspecto visual a través de diferentes pantallas o "estados", reaccionando tanto a las teclas que presiona el usuario como al volumen de un archivo de audio en tiempo real.

* **Qué se ve en pantalla:** El afiche comienza con una pantalla de inicio limpia y ordenada con la frase "DESTRUYE EL ORDEN" sobre una figura geométrica estricta (un signo de exclamación). Al avanzar, el orden se rompe por completo: las palabras empiezan a aparecer al azar, se superponen, cambian de tamaño según la música y son cruzadas por líneas que ensucian el espacio.
* **Inputs (Entradas):** Uso de teclas específicas (`ENTER`, `Espacio`, `S`, `R`) y el nivel de volumen del audio capturado con `analizador.getLevel()`.
* **Outputs (Salidas):** Modificación de los textos en tiempo real en la pantalla y la opción de descargar la imagen final como un archivo `.png`.

### Descripción Conceptual
* **Idea central:** Romper la estructura y las reglas tradicionales del diseño editorial mediante el uso del código y el azar controlado.
* **Referente de diseño:** Se inspira directamente en el **Dadaísmo**, usando tipografías pesadas, desorden, superposición y el quiebre de la retícula para quitarle la función de lectura tradicional al texto y volverlo una textura visual. También rescata las líneas de tensión geométricas del **Constructivismo** ruso.
* **Principios de diseño:** Contraste extremo, saturación del espacio, peso visual dinámico y el uso del color como separador de ambientes.

---

## 2. Sistema Computacional y Uso del Color
El código funciona de manera organizada usando las siguientes lógicas y elementos visuales:

* **El Color como Intención Visual:**
  * **Pantalla de Inicio:** Utiliza un fondo color Crema (`244, 236, 184`) para dar una sensación de papel o afiche impreso tradicional.
  * **Pantalla de Caos:** El fondo cambia drásticamente a un tono Azul Celeste (`84, 145, 197`), marcando un quiebre absoluto con el estado anterior.
  * **Lógica de Textos:** Para generar contraste y vibración cromática, las palabras normales alternan entre un color **Negro Tinta** (`17, 17, 17`) y un **Blanco Crema** (`247, 245, 240`) usando transparencias (alfa) para que se mezclen al superponerse. Además, ciertas palabras clave o números específicos (como "222" o "299") activan variaciones de color exclusivas para destacar dentro del desorden.
* **Variables y Procesos:** * Se usa la función `map()` para transformar los valores decimales pequeños del volumen del sonido en tamaños de letra grandes y visibles (de 15 a más píxeles).
  * Se usan bucles `for` para dibujar líneas de estructura de forma repetida en posiciones aleatorias.
* **Estados del Sistema:**
  * `estado == 1`: **Inicio.** T
