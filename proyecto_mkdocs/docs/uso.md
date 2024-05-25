## Uso
Este repositorio dispone de tres programas para utilizar. `app.py` muestra una barra de progreso que se actualiza dinámicamente para mostrar el progreso de una larga tarea de computación. La aplicación correspondiente al archivo `pc.py` muestra algo de información de tu máquina en tiempo real(cada vez que recargues la página). Por otro lado, La aplicación correspondiente al archivo `uber_pickups.py` permite visualizar los datos de recogida de Uber en la ciudad de Nueva York. Puedes seleccionar la hora mediante una barra deslizadora.

Hay varias maneras de usar, igualmente válidas si se usan entornos virtuales o no.
1. Para inicializar un proyecto debes crear un archivo `archivo.py` y modificarlo según el programa que desees crear. Aquí es donde escribirás la lógica de tu app. Puedes copiar los archivos `.py` que estan en este repositorio.
Para correr esa aplicación, se debe ejecutar:
```shell
streamlit run "archivo".py
```
2. Utilizar el archivo de Containerfile. En el caso de que requieras clonar el repositorio y obtener los archivos debes generar la imagen, antes del contenedor, a partir del [Containerfile](https://github.com/andresbuten2002/Proyecto-Integrador-Final/blob/main/Containerfile) que se encuentran en esta carpeta, principalmente el Dockerfile. Para hacerlo, debes ejecutar los siguientes comandos:

```shell
docker built -t "nombre de la imagen:tag" .
```

Con la imagen ya creada, procedes a crear el contenedor. Para ello debes implementar el siguiente comando:
```shell
docker run -it --network host "nombre de la imagen:tag"
```
Para correr algunas de las apps, debes ejecutar el siguiente comando:

```shell
streamlit run "archivo".py
```

La aplicación ya debería correr en la dirección IP de tu localhost y el puerto 8501. Puedes acceder desde otro dispositivo mediante la dirección IP correspondiente y el puerto 8501.

3. La tercer manera de correr la aplicación es accediendo a la imagen ya creada en DockerHub. El repositorio se encuentra en: [bocha2002/streamlit](https://hub.docker.com/repository/docker/bocha2002/streamlit/general). Allí deber implementar el siguiente comando para obtener el archivo de Dockerfile. Recuerda que debes haber iniciado sesión con `docker login` en tu terminal.

```shell
docker pull bocha2002/streamlit:1.0
```

Una vez que ya tienes la imagen descargada solo debes levantar el contenedor. Para ello debes implementar el siguiente comando:
```shell
docker run -it --network host bocha2002/streamlit:1.0
```
De la misma manera que antes, debes elegir que app ejecutar, modificar o crear una nueva. Después, en la dirección de (http://localhost:8501) ya tienes tu app corriendo. Puedes acceder desde otro dispositivo mediante la dirección IP correspondiente y el puerto 8501.