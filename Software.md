# Funcionamiento de software

El sistema de adquisición consiste en un arreglo de módulos sensoriales en la muñeca, que recibe señales, entran al circuito condicional donde es procesado y terminan en el GUI (Graphical User Interface) en la terminal o CPU.
En el microprocesador está integrado un convertidor análogo a digital que convierte las señales que recibe en señal analogica o señal digital.
El dispositivo utiliza con un circuito digital que funciona gracias a la resistencia ARM del sensor, al que se le otorga 5k ohm, donde al realizar el proceso del circuito, R1 y R3 son capaces de obtener la señal del voltaje que produce el sensor sin causar ninguna distorsión. C1, R6 y R7 tienen la tarea de mandar un filtro de alta capacidad de resistencia.
El dispositivo requiere estar conectado a una computadora a la cual se le mandarán las señales de la pulsera desde el microcontrolador en forma de estructuras de datos. Los datos constan de señales de 24 canales que se almacenarán en el buffer del equipo, después se restaurarán en 2 tipos diferentes de señales, 12 de fuerza estática y 12 de ondas de pulso dinámico para procesarlo más a fondo en el programa, donde se le aplicara un filtro para poder remover las distorsiones que consiste de 50Hz de poder de frecuencia como interferencia a las señales, esto se realiza para remover la línea base de impresión y después poder mostrar la gráfica del pulso 3D. La razón por la cual los 50Hz de poder de frecuencia funcionan como filtro es porque la fórmula que se utiliza para calcular las ondas no calcula el ancho y amplio de la pulsera y esta frecuencia muestra una correcta interpolación cúbica correcta en las direcciones “x” y “y”.

[<- Portada](README.md)
||||
[Calibración del sensor empaquetado ->](Calibracion.md)
