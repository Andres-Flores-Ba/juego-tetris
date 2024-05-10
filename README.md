# tetris
## Objetivo 
El objetivo de este proyecto es hacer un juego tipo ascii art basado en el juego de tetris.
## Exploracion 

### Carpetas
- bin/ - Contiene los ejecutables del proyecto 
- src/ - Contiene el codigo fuente 
- include/ - Los archivos de cabecera 
- assets/ - Contiene los recursos del proyecto 
- docs/ - Contiene la documentacion del archivo 

# Descripcion 
- Se basa en tetrominós, figuras geométricas compuestas por cuatro bloques cuadrados unidos de forma ortogonal, las cuales se generan de una zona que ocupa 5x5 bloques en el área superior de la pantalla. 
- No hay consenso en cuanto a las dimensiones para el área del juego, que varía en cada versión.​ Sin embargo, dos filas de más arriba están ocultas al jugador.
- El jugador no puede impedir esta caída, pero puede decidir la rotación de la pieza (0°, 90°, 180°, 270°) y en qué lugar debe caer. 
- Cuando una línea horizontal se completa, esa línea desaparece, todas las piezas que están por encima descienden una posición y liberan espacio de juego y por tanto facilitando la tarea de situar nuevas piezas. La caída de las piezas se acelera progresivamente. 
- El juego acaba cuando las piezas se amontonan hasta llegar a lo más alto (3x5 bloques en el área visible), interfiriendo la caída de más piezas.

# Funcionamiento
## Dibujo.hpp
- Define la clase Dibujo, que representa un elemento gráfico que se puede dibujar en la pantalla.
- La clase contiene métodos para dibujar el objeto en una pantalla, desplazarlo en el eje X y Y, establecer su posición, verificar colisiones con otro objeto Dibujo y verificar si alcanza el fondo de la pantalla.
- También incluye un constructor predeterminado, un constructor con posición inicial, un constructor con contenido y posición inicial, y un destructor.
## Archivo.hpp
- Define la clase Archivo, que se encarga de leer un archivo de texto que contiene la información para crear un objeto Dibujo.
- El archivo se abre y lee línea por línea, donde cada línea representa una fila del contenido del dibujo.
- La clase proporciona un método para crear un objeto Dibujo a partir del contenido leído del archivo.
## main.cpp
- Contiene la función principal main donde se ejecuta la lógica principal del juego Tetris.
- En el main, se crean instancias de la clase Archivo para cada pieza de Tetris disponible.
- Luego, se crea una ventana de pantalla usando la biblioteca FTXUI y se inicia un bucle principal.
- Dentro del bucle principal, se hace que cada pieza caiga una tras otra hasta que alcance el fondo de la pantalla.
- Después de que una pieza llega al fondo, se reinicia el bucle y comienza a caer la siguiente pieza. Este proceso se repite indefinidamente.

# Instruciones 
- Una vez copiado todo el repositorio, escribir en la terminal "make run" para ver la animacion de las piezas caer