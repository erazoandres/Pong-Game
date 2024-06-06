Descripción del Proyecto
Este proyecto es un juego de pinball desarrollado en Python utilizando la biblioteca tkinter para la interfaz gráfica y la biblioteca winsound para efectos de sonido. El objetivo del juego es manejar una bola que rebota en la pantalla, con el jugador controlando las paletas para evitar que la bola caiga fuera de la pantalla inferior. A lo largo del juego, el jugador debe golpear diferentes obstáculos estáticos y móviles para ganar puntos y obtener vidas extra. El juego termina cuando el jugador pierde todas sus vidas.

Descripción de las Funciones
1. destruirLogin()
Propósito: Destruir la ventana de inicio de sesión y guardar el nombre de usuario ingresado.
Funcionamiento:
Obtiene el nombre de usuario del campo de entrada.
Destruye la ventana de inicio de sesión.
Guarda el nombre de usuario en un archivo saves.txt.
2. aviso()
Propósito: Mostrar una ventana emergente cuando el jugador pierde todas sus vidas.
Funcionamiento:
Crea una nueva ventana emergente con un mensaje de advertencia.
Proporciona dos botones: uno para intentar de nuevo y otro para salir del juego.
Implementa funciones para cada botón que permiten al jugador decidir si quiere intentar nuevamente o salir.
3. randomColor()
Propósito: Generar un color aleatorio.
Funcionamiento:
Selecciona aleatoriamente un color de una lista de colores predefinidos y lo devuelve.
4. loadBotones()
Propósito: Crear y colocar los botones de inicio en la pantalla principal del juego.
Funcionamiento:
Crea un botón para comenzar el juego y lo coloca en la interfaz.
5. shootBall()
Propósito: Controlar el movimiento de la bola y gestionar la lógica de colisión y puntuación.
Funcionamiento:
Verifica las coordenadas de la bola y determina si ha chocado con los bordes de la pantalla.
Ajusta la dirección de la bola en función de las colisiones.
Reduce las vidas del jugador si la bola toca el borde inferior de la pantalla.
Llama recursivamente a sí misma usando root.after(35, shootBall) para crear un bucle de animación.
6. loadEnemiesStatics()
Propósito: Cargar y dibujar los obstáculos estáticos en el juego.
Funcionamiento:
Utiliza create_polygon para dibujar varios obstáculos de diferentes formas y colores en la pantalla de juego.
7. moverPaletas(event)
Propósito: Manejar el movimiento de las paletas controladas por el jugador.
Funcionamiento:
Detecta las teclas presionadas ('q' para la paleta izquierda y 'a' para la paleta derecha).
Actualiza las coordenadas de las paletas en función de la tecla presionada.
Actualiza la interfaz gráfica con los nuevos movimientos de las paletas.
8. enemigosMoviles()
Propósito: Controlar el movimiento de los obstáculos móviles.
Funcionamiento:
Mueve los obstáculos móviles en la pantalla.
Llama recursivamente a sí misma usando root.after(12, enemigosMoviles) para crear un bucle de animación.
9. main
Propósito: Configurar y ejecutar la ventana principal del juego.
Funcionamiento:
Crea la ventana principal del juego (root).
Configura el canvas donde se dibujan todos los elementos del juego.
Llama a las funciones para cargar los botones, obstáculos estáticos, y enemigos móviles.
Configura la detección de eventos de teclado para mover las paletas.
Ejecuta el bucle principal de tkinter usando root.mainloop().
Ejecución del Juego
Para ejecutar el juego, simplemente corre el script en un entorno Python con tkinter y winsound disponibles. Asegúrate de tener las imágenes necesarias (como BackMenu.png) y los archivos de sonido (como play.wav) en el directorio correcto. El juego comenzará con una ventana de inicio de sesión donde el usuario debe ingresar su nombre, y luego pasará a la ventana principal del juego una vez que el nombre se haya guardado.
