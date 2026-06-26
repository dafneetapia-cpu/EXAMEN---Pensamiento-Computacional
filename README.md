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
Este proyecto es un sistema visual interactivo avanzado desarrollado en p5.js que funciona como un afiche digital generativo y dinámico. El software está estructurado mediante un sistema de control de estados que evoluciona según las interacciones del usuario por teclado y el procesamiento de audio en tiempo real.

* **Qué se ve en pantalla:** El programa inicia con una interfaz minimalista de alto contraste que presenta la consigna "DESTRUYE EL ORDEN" superpuesta sobre una abstracción geométrica de un signo de exclamación centralizado. Al avanzar, muta a una composición tipográfica caótica donde las palabras se superponen, escalan y saturan la pantalla, cruzadas por líneas estructurales que aparecen aleatoriamente.
* **Inputs utilizados:** Eventos de teclado (`ENTER`, `Space`, `S`, `R`) y la amplitud/volumen capturado de un archivo de audio mediante la librería `p5.sound`.
* **Outputs generados:** Renderizado gráfico generativo continuo, modulación tipográfica paramétrica en tiempo real y exportación de archivos de imagen en formato `.png`.

### Descripción Conceptual
* **Idea central:** Explorar la transición entre el orden rígido y el caos absoluto a través del control algorítmico, cuestionando la legibilidad tradicional del diseño editorial mediante software.
* **Corriente o referente de diseño:** El proyecto se posiciona formalmente en el **Dadaísmo**, adoptando su naturaleza anti-arte, el uso del azar y el quiebre de las retículas tipográficas tradicionales. Asimismo, rescata sutiles líneas de tensión analítica propias del **Constructivismo** ruso.
* **Referentes visuales:** Inspirado en las piezas tipográficas de colages dadaístas históricos y afiches de exhibiciones de vanguardia donde el texto pierde su función netamente lingüística para convertirse en textura visual.
* **Principio de diseño explorado:** Contraste, jerarquía tipográfica dinámica, saturación espacial y el azar (`random`) operando bajo límites controlados.

---

## 2. Sistema Computacional
El sistema está construido de forma modular basándose en los siguientes componentes algorítmicos técnicos:

* **Inputs:** Lectura continua del volumen del archivo multimedia (`analizador.getLevel()`) y disparadores de eventos por teclado (`keyCode`).
* **Procesos:** * Mapeo matemático (`map()`) de la amplitud del sonido (rango de 0 a 0.5) para transformarlo en tamaños de letras proporcionales y legibles.
  * Estructuras de control cíclicas (`for loops`) para dibujar de forma iterativa líneas de interferencia visual en coordenadas aleatorias.
  * Condicionales dinámicos que alteran el color (`fill`) y posición (`baseY`) de las palabras clave según cadenas de texto específicas.
* **Estados:**
  * `estado == 1`: **Pantalla de Inicio.** Muestra el título fijo "DESTRUYE EL ORDEN" alineado con formas vectoriales estables (`quad`).
  * `estado == 2`: **Pantalla Caos (Experiencia Principal).** Activación del bucle de audio y renderizado del ecosistema tipográfico reactivo al volumen.
  * `estado == 3`: **Pantalla Final / Detención.** Congelamiento de la composición y apagado del buffer de audio (`audio.stop()`).
* **Eventos:** Transiciones de estado gatilladas por interacciones específicas de hardware (`ENTER` para iniciar el bucle, `Space` para detener el audio).
* **Outputs:** Un lienzo interactivo mutante y capturas físicas guardadas localmente.

---

## 3. Explicación de la Interacción
* **Flujo de datos:** El micrófono o el archivo de audio entrega valores numéricos infinitesimales al sistema. La variable `vol` captura este nivel y la función `map()` toma esa fluctuación natural y la normaliza a dimensiones de pixeles escalables.
* **Transformación y Respuesta:** Si la música sube de intensidad, el tamaño del bloque tipográfico principal se expande bruscamente multiplicando su escala, simulando un "golpe visual" que se superpone al resto de los elementos satélites, los cuales se distribuyen de forma aleatoria evitando colisionar rígidamente con el centro.

---

## 4. Recursos Multimedia Utilizados
* **Tipo de recurso:** Archivo de sonido integrado y procesado mediante `p5.Amplitude()`.
* **Función en el proyecto:** Cumple un rol lógico fundamental y estructural. No es decorativo; actúa como el motor algorítmico que define las dimensiones, colores y descalces tipográficos en pantalla. Sin el flujo del audio, la composición gráfica permanece estática.

---

## 5. Registro Visual y Diagrama de Flujo

### Diagrama de Flujo del Sistema
*(Asegúrate de cambiar 'diagrama.png' por el nombre real de tu archivo subido en tu GitHub)*
![Diagrama de Flujo Digital](diagrama.png)

### Proceso de Diseño y Capturas
* **Referentes de Vanguardia:**
  <table>
    <tr>
      <td><img src="1000244521.jpg" width="300" alt="Referente Dadaísta 1"></td>
      <td><img src="1000244535.jpg" width="300" alt="Referente Dadaísta 2"></td>
    </tr>
  </table>

* **Iteraciones del Software en Tiempo Real:**
  <table>
    <tr>
      <td><img src="24db003a-719d-44c4-b2a4-bc613988653c" width="250" alt="Pantalla de Inicio"></td>
      <td><img src="992104bb-9f45-4e84-a130-45c770f210b5" width="250" alt="Estado Caos Iteración 1"></td>
      <td><img src="8f0ef762-d52b-4e90-b5e8-ecb6fd547abd" width="250" alt="Estado Caos Iteración 2"></td>
    </tr>
  </table>

---

## 6. Reflexión Final
* **Principales decisiones tomadas:** Sustituir coordenadas absolutas rígidas por un sistema paramétrico basado en proporciones del lienzo (`width / 2`) para asegurar que el orden tipográfico inicial converse perfectamente con la geometría del `quad()` sin desfasarse.
* **Dificultades encontradas:** El control y depuración de la máquina de estados. Al principio, mezclar tipos de datos numéricos con hilos de texto (`"pantallaInicio"`) provocaba colisiones que congelaban las funciones clave de teclado. Asimismo, calibrar el rango de sensibilidad del analizador requirió imprimir registros continuos en la consola (`console.log`) para mapear el volumen real de manera óptima.
* **Aprendizajes obtenidos:** La programación creativa no es ajena al diseño tradicional, sino una extensión de este. Aprender a traducir postulados estéticos rupturistas del siglo XX (como el Dadaísmo) a lógica algorítmica estricta del siglo XXI permite entender el código como una herramienta de configuración plástica y espacial de infinitas posibilidades.
*
