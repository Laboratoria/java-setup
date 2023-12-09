# Tutorial de preparación para comenzar a programar en Java

¡Hola! 👋 ¿Cómo estás?

En esta página encontrarás información relacionada con la preparación de tu computadora para empezar a programar en Java.

## ¿Cómo preparar mi entorno de desarrollo?

Además de instalar Java en tu computadora, necesitarás un entorno de desarrollo integrado (IDE) que te ayude a crear tu código. Sigue los tutoriales a continuación para realizar esta configuración.

## 1. Instala Java

Instala y configura Java.

### Paso 1. Visita el sitio de Oracle y descarga

Descarga JDK Development Kit 21.0.1 desde el [sitio de Oracle](https://www.oracle.com/java/technologies/downloads/#jdk17-linux) según tu sistema operativo.
Asegúrate de descargar el paquete comprimido adecuado para tu sistema operativo.

#### Para Windows
- Recomiendo descargar el archivo en formato ```.exe``` para simplificar la instalación.

#### Para Linux (Ubuntu)
- Recomiendo descargar el archivo en formato ```tar.gz``` para facilitar la instalación.

### Paso 2. Ejecuta el instalador

Después de que se complete la descarga del archivo de instalación, ejecuta el programa de instalación.

#### Para Windows

- Ejecuta el programa de instalación y haz clic en "Siguiente" en todas las pantallas presentadas. El proceso es simple y rápido.

#### Para Linux

- Abre un terminal, ve a la carpeta "Downloads" y copia el archivo de instalación al directorio de tu elección con el siguiente comando

```bash
cp jdk-<versión>.tar.gz <ruta-completa-de-tu-directorio>
```

- Cambia al directorio que elegiste

```bash
cd /<ruta-completa-de-tu-directorio>
```

- Descomprime el archivo con el siguiente comando

```bash
tar -zvxf jdk-<versión>.tar.gz
```

### Paso 3. Configuración de Java

La configuración implica la creación de las variables de entorno JAVA_HOME y CLASSPATH. Estas variables son importantes para que los programas encuentren dónde se instaló el JDK.

#### Para Windows

- Ejecuta los siguientes comandos en el símbolo del sistema

```bash
setx JAVA_HOME "<directorio-donde-jdk-fue-instalado>"
setx CLASSPATH "%JAVA_HOME%\lib"
setx PATH "%PATH%;%JAVA_HOME%\bin"
```

- Cierra el símbolo del sistema.

#### Para Linux

- Abre el terminal y edita el archivo /etc/profile con el siguiente comando

```bash
sudo gedit /etc/profile
```

- Agrega las siguientes líneas al principio del archivo ```/etc/profile```

```txt
JAVA_HOME=directorio-donde-jdk-fue-instalado
CLASSPATH=.;$JAVA_HOME/lib
PATH=$PATH:$JAVA_HOME/bin
export JAVA_HOME
export CLASSPATH
export PATH
```

- Guarda el archivo y reinicia tu máquina para que se apliquen los cambios.

### Paso 4. Prueba la configuración

- Abre el terminal en Linux o el símbolo del sistema en Windows y ejecuta el siguiente comando:

```bash
java -version
```

> La salida del terminal debe ser algo similar a la imagen a continuación, donde puedes leer la versión de Java instalada.

![java version](./assets//java-version.jpeg)

## 2. Instalar IDE

Para trabajar con Java se puede utilizar diferentes IDEs pero recomendamos los siguientes

### IntelliJ

#### Paso 1. Visita el sitio de IntelliJ y descarga

Recomiendo que uses [IntelliJ IDEA](https://www.jetbrains.com/idea/) 
en la versión 2023.2 Community Edition. El sitio de IntelliJ te redirige a descargar la Ultimate Edition,
pero puedes encontrar las versiones Community que recomiendo [aquí](https://www.jetbrains.com/pt-br/idea/download/other.html).

Asegúrate de descargar el archivo adecuado para tu sistema operativo.

#### Paso 2. Ejecuta el instalador de IntelliJ

##### Para Windows

- Ejecuta el programa de instalación y haz clic en "Siguiente" en todas las pantallas presentadas.

> En este [guía de instalación](https://www.jetbrains.com/help/idea/run-for-the-first-time.html#windows) de IntelliJ encontrarás más información sobre cómo personalizarlo.

##### Para Linux (Ubuntu)

- Abre un terminal, ve a la carpeta "Downloads" y copia el archivo de instalación al directorio de tu elección con el siguiente comando

```bash 
cp ideaIC-<versión>.tar.gz <ruta-completa-de-tu-directorio>
```

- Cambia al directorio que elegiste

```bash 
cd /<ruta-completa-de-tu-directorio>
```

- Descomprime el archivo con el siguiente comando

```bash 
tar -zvxf ideaIC-<versión>.tar.gz
```

- Para iniciar IntelliJ, cambia al directorio que se creó con el siguiente comando

```bash 
cd idea-IC-<versión>
```

- Ahora abre IntelliJ con el siguiente comando:

```bash 
./bin/idea.sh
```

- Este comando iniciará varios archivos de configuración en el directorio de configuración de IntelliJ:

```bash    
~/.config/JetBrains/IdeaIC2023.2.
```

[OPCIONAL] Añade un ícono de acceso directo para abrir IntelliJ más fácilmente.

- Primero, crea el archivo intellij.desktop con el siguiente comando:

```bash 
sudo gedit /usr/share/applications/intellij.desktop
```

> Este comando abrirá una ventana para editar un archivo de texto que inicialmente estará vacío.

- Añade el siguiente texto a este archivo, asegurándote de agregar la ruta correcta al directorio donde descomprimiste IntelliJ:

```txt
[Desktop Entry]
Version=13.0
Type=Application
Terminal=false
Icon[en_US]=<ruta al directorio donde descomprimió IntelliJ>/bin/idea.png
Name[en_US]=IntelliJ
Exec=<ruta al directorio donde descomprimió IntelliJ>/bin/idea.sh
Name=IntelliJ
Icon=<ruta al directorio donde descomprimió IntelliJ>/bin/idea.png
```

- Guarda el archivo, ciérralo y ahora abre el icono de IntelliJ que has creado en tus aplicaciones de Ubuntu 🚀

#### Paso 3. Crea tu primer proyecto 

Puedes seguir la siguiente (guía)[https://drive.google.com/file/d/1F4qS2ZticeHaEtktijCzFC6KSD4Yev0j/view?usp=drive_link] para crear tu primer proyecto y ponerlo a prueba 

### VSCode

#### Paso 1. Visita el sitio de VSCode y descarga

- Visita la página de descargas de [VSCode](https://code.visualstudio.com/download).
- Selecciona la versión que corresponda a tu sistema operativo (Windows, Linux o Mac).
- Descarga el archivo y sigue las instrucciones de instalación.

#### Paso 2. Configurar VSCode para Java

- Abre VSCode.
- Ve a la sección de extensiones (puedes usar el atajo `Ctrl+Shift+X`).
- Busca `Java Extension Pack` y haz clic en `Install`.
- Reinicia VSCode.

> Puedes seguir los pasos de la siguiente [documentación oficial](https://code.visualstudio.com/docs/java/java-tutorial) de VSCODE 🫡

#### Paso 3. Crea tu primer proyecto 

Puedes seguir la siguiente (guía)[https://drive.google.com/file/d/13YecWGDqNeUzwaPKA7YuAMGV4FRf-wY7/view?usp=drive_link] para crear tu primer proyecto y ponerlo a prueba 