# <FONT COLOR=#8B008B>La plataforma ArduinoBlocks</font>

## <FONT COLOR=#007575>**Descripción del entorno**</font>
Para añadir bloques al programa arrastramos desde la barra de herramientas al área de programa, insertando dentro del bloque de inicialización o de bucle.

<center>

| Pantalla inicial de ArduinoBlocks |
|:|
|![Pantalla inicial de ArduinoBlocks](img/AB/pinicial.png)|

</center>

* Si no son funciones, todos los bloques fuera de los dos por defecto son ignorados.
* ArduinoBlocks genera el código de Arduino a partir de los bloques.
* El programa se puede compilar y subir directamente a la placa Arduino gracias a la aplicación ArduinoBlocks-Connector

<center>

| Descripciones de la pantalla inicial de ArduinoBlocks |
|:|
|![Descripciones de la pantalla inicial de ArduinoBlocks](img/AB/descpinicial.png)|

</center>

ArduinoBlocks genera el código de Arduino a partir de los bloques. Si deseamos ver o descargar el código podemos realizarlo desde el área de bloques.

<center>

| Ver el código generado por ArduinoBlocks |
|:|
|![Ver el código generado por ArduinoBlocks](img/AB/ver-codigo.png)|

</center>

Si hacemos clic en el botón "Información" accedemos a toda la información del proyecto para cumplimentar o editar y también nos permite hacer nuestro proyecto público.

<center>

| Información del proyecto |
|:|
|![Información del proyecto](img/AB/infor.png)|

</center>

Si hacemos clic en el botón archivos accedemos a las opciones que se describen en la imagen siguiente:

<center>

| Archivos del proyecto |
|:|
|![Archivos del proyecto](img/AB/archivos.png)|

</center>

Es muy interesante subir esquemas de montaje del proyecto realizados por ejemplo con Fritzing.

Si hacemos clic en el desplegable de la llave fija se muestra un menú que nos permite crear símbolos de una forma sencilla para diferentes dispositivos de visualización y también un enlace a información sobre RTTTL.

<center>

| Botón herramientas |
|:|
|![Botón herramientas](img/AB/herramienta.png)|

</center>

En la imagen siguiente se realiza la descripción del resto de botones e información disponible en esta barra.

<center>

| Resto de la barra de botones |
|:|
|![Resto de la barra de botones](img/AB/resto-botones.png)|

</center>

La imagen a la izquierda del nombre del proyecto es un enlace a una página de ArduinoBlocks con información de la placa usada.

Aunque ArduinoBlocks guarda de forma automática cada cierto tiempo, podemos hacerlo de forma manual pulsando sobre el disquete o sobre el desplegable. La principal utilidad es la de crear un nuevo proyecto a partir del actual pulsando la opción “Guardar como”, lo que abrirá el nuevo proyecto creado a partir del primero. También permite generar el proyecto para alumnos, cambiar de tipo de proyecto, o sea cambiar la placa usada dentro de las opciones disponibles y exportar el archivo a nuestro ordenador. La ventana para cambiar el tipo de proyecto se muestra en la imagen siguiente:

<center>

| Opciones para cambiar el tipo de proyecto |
|:|
|![Opciones para cambiar el tipo de proyecto](img/AB/cambiar-tipo.png)|

</center>

Si accedemos a Buscar proyectos podremos visualizar los compartidos por otros usuarios, completar las opciones de búsqueda que nos interesen, ver información del proyecto cómo los “Me gusta o Like”, ver el número de visualizaciones que tiene y visualizarlo nosotros mismos.

<center>

| Opciones de "Buscaar proyectos" |
|:|
|![Opciones de "Buscaar proyectos"](img/AB/buscar-pr.png)|

</center>

Al acceder a visualizar un proyecto compartido por otro usuario nos aparecerá un botón “importar a mis proyectos”, que nos permite crear una copia del proyecto en mis proyectos personales para poder modificarlo a nuestro gusto. Tenemos un botón “Me gusta” que nos permite valorar positivamente el trabajo realizado por el usuario.

<center>

| Visualizar un proyecto compartido |
|:|
|![Visualizar un proyecto compartido](img/AB/importar.png)|

</center>

## <FONT COLOR=#007575>**Estructura de un proyecto**</font>
Un proyecto Arduino tiene siempre dos estructuras importantes en su interior. Vamos a crear un ejemplo sencillo al que llamaremos Blink escogiendo tipo Arduino UNO.

<center>

| Estructura básica de un proyecto |
|:|
|![Estructura básica de un proyecto](img/AB/estructura.png)|

</center>

### <FONT COLOR=#AA0000>Blink</font>

Vamos a hacer que al iniciar (o hacer reset) se envíe el mensaje por el puerto serie “Inicialización del proyecto Blink”. Para ello procedemos como se ve en la imagen siguiente.

<center>

| Configuración de Inicializar para el proyecto Blink |
|:|
|![Configuración de Inicializar para el proyecto Blink](img/AB/config-inicializar.png)|

</center>

### <FONT COLOR=#AA0000>ArduinoBlocks connector</font>
Es una aplicación puente entre la plataforma on-line ArduinoBlocks y el hardware Arduino. La aplicación recibe el código generado por ArduinoBlocks, lo compila y lo sube a la placa Arduino.

Está disponible para los principales sistemas operativos. En el área de descargas de Arduinoblocks.com se puede obtener la última versión y más información sobre el proceso de instalación y configuración. [Connector](http://www.arduinoblocks.com/web/site/abconnector).

<center>

| Aspecto de la página de descarga de Connector |
|:|
|![Aspecto de la página de descarga de Connector](img/AB/AB-connector.png)|

</center>

Para poder grabar nuestro proyecto en la placa Arduino necesitamos tener activado Connector. En la imagen siguiente vemos el icono y el programa en ejecución.

<center>

| ArduinoBlocks Connector |
|:|
|![ArduinoBlocks Connector](img/AB/conecctor.png)|

</center>

Ya podemos grabar el firmware directamente en nuestra placa a través de Connector. Para ello conectamos la placa a un puerto USB y hacemos clic en Subir y al cabo de unos instantes veremos algo similar a lo de la imagen siguiente:

<center>

| Blink subido correctamente |
|:|
|![Blink subido correctamente](img/AB/blink-subido.png)|

</center>

Ya hemos probado la comunicación entre la plataforma y nuestro equipo y podemos continuar con el proyecto Blink.

### <FONT COLOR=#AA0000>Continuación de Blink</font>
Consultando el pinout de la placa Arduino UNO vemos que en el pin 13 está conectado el LED L, como vemos en la imagen siguiente. Vamos a hacerlo parpadear.

<center>

| LED onboard conectado a D13 |
|:|
|![LED onboard conectado a D13](img/AB/LED-L.png)|

</center>

Colocamos el bloque de escritura de pin en Bucle y lo configuramos para el pin 13. Situamos un bloque de retardo que configuramos a 500 milisegundos. Montamos el programa que vemos en la imagen siguiente:

<center>

| Programa Blink |
|:|
|![Programa Blink](img/AB/programa-blink.png)|

</center>

 Ya podemos subir el programa a nuestra placa y comprobar el funcionamiento. En la imagen siguiente vemos el resultado en la consola.

<center>

| Consola en el programa Blink |
|:|
|![Consola en el programa Blink](img/AB/blink-ejecucion.png)|

</center>

### <FONT COLOR=#AA0000>Análisis del código</font>
Veamos el código por bloques y linea a línea. En la imagen siguiente tenemos relacionados los dos bloques principales con sus líneas de código correspondientes.

<center>

| Código del programa Blink |
|:|
|![Código del programa Blink](img/AB/codigo.png)|

</center>

A continuación vemos el código del bloque Inicializar.

***
~~~
void setup()
{
  	pinMode(13, OUTPUT);
	Serial.begin(9600);
	Serial.flush();
	while(Serial.available()>0)Serial.read();

	Serial.println(String("Inicialización del proyecto Blink"));

}
~~~
***

* Establecemos el pin 13 como salida: <font color="grey">pinMode(13, OUTPUT);</font>
* Inicializamos la consola con una velocidad de transmisión de 9600 baudios: <font color="grey">Serial.begin(9600);</font>
* Espera a que la transmisión de datos de salida serie termine: <font color="grey">Serial.flush();</font>
* Consulta si el número de bytes (caracteres) disponibles para lectura desde el puerto serie es mayor que cero: <font color="grey">while(Serial.available()>0)Serial.read();</font>
* Mandamos el mensaje entrecomillado a la consola: <font color="grey">Serial.println(String("Inicialización del proyecto Blink"));</font>

El código del bloque Bucle es el siguiente:

***
~~~
void loop()
{
  	digitalWrite(13, HIGH);
  	delay(500);
  	digitalWrite(13, LOW);
  	delay(500);

}
~~~
***

* Establecemos un nivel alto en el pin 13 mediante escritura digital: <font color="grey">digitalWrite(13, HIGH);</font>
* Retardo de medio segundo: <font color="grey">delay(500);</font>
* Establecemos un nivel bajo en el pin 13 mediante escritura digital: <font color="grey">digitalWrite(13, LOW);</font>
* Retardo de medio segundo: <font color="grey">delay(500);</font>
