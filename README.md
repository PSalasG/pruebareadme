# Laboratorio 6
# Pablo Salas Gómez, C27061
## Enunciado 1
El código correspondiente al enunciado 1 utiliza las librerías “time” y “random” para simular el cambio de temperatura y humedad de un medio. Se usó la clase EventManager para recopilar diferentes eventos que puedan ocurrir en una lista y poder realizar ciertas operaciones con estos como suscribirlos, desuscribirlos y notificar su estado mediante funciones callback encargadas de esto. La clase RealTimeDataManager se utilizó para simular un cambio de temperatura y humedad con respecto al tiempo, utilizando valores aleatorios a partir de un valor base. En esta se crea una instancia de la clase EventManager con la cuál se suscribe el evento del cambio de temperatura y humedad y se notifica sobre estos cambios. En el código principal se creó la instancia de la clase RealTimeDataManager y se suscribió su evento a la clase EventManager, después se utilizó la librería threading para iniciar el proceso de cambios de temperatura de forma indefinida hasta que se detenga mediante una interrupción del teclado.
## Enunciado 2
En el código correspondiente al enunciado 2 se desarrolló una calculadora que presenta diversas opciones para realizar cuatro tipos de operaciones: suma, resta, multiplicación y divisíon, y tambien presenta una opción para terminar el proceso y cerrar la calculadora. Primeramente se piden dos números al usuario con los cuales se relizará la operación, después se pide la operación que desea realizar o si desea cerrar la calculadora, esto se hace mediante una función que verifica que los valores introducidos por el ususario sean correctos y si lo son retorna estos valores. Seguidamente se creó una lista la cual almacena las cuatro opciones de operación que realiza la calculadora con la respectiva función lambda que realiza esta operación, estas funciones lambda son pasadas como callback a una función que recibe los números ingresados por el usuario y con el callback realiza la operación y retorna su resultado para imprimirlo al stdout.
## Resultados
Al ejecutar el archivo eventos_tiempo_real.py se comienza a imprimir en la terminal la confirmación de que hubo un cambio y los nuevos valores de temperatura y humedad, con un mensaje como el siguiente: Datos en tiempo real actualizados: {"temperatura": valor_temperatura, "humedad": valor_humedad}. Este mensaje se repite cada tres segundos, ya que es el tiempo en el que ocurre un cambio de estos valores y se detiene hasta que el usuario precione una tecla del teclado.

Al ejecutar el archivo calculadora_lambda.py se piden 2 números al usuario, si se escriben valores que no sean números se envia un mensaje de error y se vuelven a solicitar los números, seguidamente se pide de la operación deseada, si esta no coincide con alguna de las 5 opciones se envia un mensaje de error y se vuelven a solicitar los datos, si en la operación se escribe alguno de los símbolos +, -, * o /, se imprime el resultado de la operación y se vuelven a solicitar los datos para otra operación, si en la operación se escribe "exit" se imprime un mensaje de finalización y se termina la ejecución del programa.
