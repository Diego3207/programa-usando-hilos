# Programa Capaz de Restaurar Estado de Ejecucion
Materia: Computación Tolerante a Fallas<br>
Maestro: MICHEL EMANUEL LOPEZ FRANCO<br>
Nombre: Diego Alonso Mercado Brizuela<br>
Carrera: Ingeniería en Computación<br>
Código: 215425636<br>
Fecha: 10/09/2023<br>
Sección: D06<br>

## Introducción
Un hilo es una unidad básica de utilización de CPU, la cual contiene un id de hilo, su propio program counter, un conjunto de registros, y una pila; que se representa a nivel del sistema operativo con una estructura llamada TCB (thread control block).
Los hilos comparten con otros hilos que pertenecen al mismo proceso la sección de código, la sección de datos, entre otras cosas. Si un proceso tiene múltiples hilos, puede realizar más de una tarea a la vez (esto es real cuando se posee más de un CPU).
Un demonio, a diferencia de los hilos tradicionales, no forma parte de la esencia del programa, sino de la máquina de Java. Los demonios son usados generalmente para prestar servicios en un segundo plano a todos los programas que puedan necesitar el tipo de servicio proporcionado.
## Pruebas en Android Studio
En esta práctica se utilizaron hilos para asegurar la tolerancia a fallas. Un hilo principal, el cual se encarga de procesar tareas obtenidas desde una cola de tareas:
<br>
<img
src="https://github.com/Diego3207/programa-usando-hilos/blob/main/prueba%201.png">
<br>
Y un hilo secundario, el cual se encarga de estar revisando constantemente el estado del hilo principal. En caso de que el hilo principal falle, el hilo secundario retoma la tarea de procesamiento desde donde se quedó el hilo principal.
<img
src="https://github.com/Diego3207/programa-usando-hilos/blob/main/prueba%202.png">
Para causar una falla en el hilo principal de manera deliberada, se hace una división entre 0, esto puede ocurrir con un 33% de probabilidad al procesarse una tarea.
# Conclusiones
Un hilo en programación es una idea bastante eficiente, ya que permite dividir una tarea compleja en partes más pequeñas como en divide y vencerás, por lo que aplicarlo a cualquier ámbito o lenguaje puede ser una diferencia en estabilidad de la aplicación, como de velocidad, por que si un hilo llega a falla el hilo principal o el proceso principal aún funcionará y el usuario no sufrirá pérdidas de tiempo y estrés.
