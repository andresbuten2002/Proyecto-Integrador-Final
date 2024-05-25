# Instalación
1. Clonar el repositorio
```shell
git clone git@github.com:andresbuten2002/Proyecto-Integrador-Final.git
docker built -t "nombre de la imagen:tag" .
```
2. Instalar Streamlit localmente. Esto es opcional, ya que hay tres formas de usar las aplicaciones, tal como se demuestra más abajo.
```shell
pip install streamlit
streamlit hello #Validar instalación
```
3. Instalar requerimientos. Dentro del mismo se encuentra streamlit y psutils (necesario para una de las apps). Como contiene streamlit, se puede obviar el paso 2.
```shell
pip install -r requirements.txt
```

Streamlit requiere Python 3.8+.