# Teclado_IA
🧠 ¿Qué hace mi proyecto?
Mi proyecto es un teclado virtual inteligente que controlo con la punta de mi dedo usando la cámara. No necesito tocar nada, solo mover mi mano frente a la cámara. El sistema detecta el movimiento y me permite:

Escribir letras cuando dejo mi dedo quieto sobre una tecla virtual.

Borrar todo lo escrito cuando abro completamente la mano.

Escuchar un sonido cada vez que escribo, como si fuera un clic de teclado.

Recibir sugerencias de palabras conforme voy escribiendo, para facilitar la escritura.

🔌 ¿Qué programas o archivos uso?
Mi sistema se compone de tres archivos que se comunican entre sí:

entrenar_prefijos.py:
Aquí entreno un modelo para sugerirme palabras que comiencen con ciertas letras. Uso un archivo de texto (corpus.txt) como base de aprendizaje.

entrenar_trigramas.py:
Entreno otro modelo que aprende secuencias de tres palabras (trigramas). Esto me ayuda a que el sistema sugiera palabras que probablemente seguirían en mi oración.

teclado_mano_avanzado.py:
Este es el archivo principal. Aquí uso la cámara para detectar mi mano, muestro el teclado en pantalla y manejo todo lo visual, los sonidos, las sugerencias y la escritura.

🧰 ¿Qué herramientas y librerías uso?
OpenCV: Para mostrar la cámara y dibujar el teclado en pantalla.

MediaPipe: Para detectar mi mano y seguir la punta de mi dedo.

Pygame: Para reproducir sonidos cuando escribo.

Pickle: Para guardar y cargar los modelos entrenados de predicción de palabras.

Collections (defaultdict): Para manejar mejor los datos y contar repeticiones de palabras.

💡 ¿Cómo funciona todo junto?
Primero, entreno los modelos con los archivos entrenar_prefijos.py y entrenar_trigramas.py usando un archivo de texto como base. Esto me permite tener sugerencias inteligentes.

Después, ejecuto teclado_mano_avanzado.py. Este archivo activa la cámara, detecta la punta de mi dedo, dibuja el teclado en la pantalla y me deja escribir con gestos. El sistema:

Usa los modelos entrenados para dar sugerencias.

Detecta si abro la mano para borrar.

Reproduce sonidos cuando escribo.

Es totalmente visual e interactivo, sin necesidad de teclado físico.
