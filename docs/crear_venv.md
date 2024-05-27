## Creación Entorno Virtual
Es muy recomendable usar un entorno virtual para su proyecto porque instalar o actualizar un paquete de Python puede causar efectos no intencionales en otro paquete. venv es la opción estándar.

Procediendo con el entorno venv, se debe crear un nuevo directorio para empezar.
```shell
mkdir my_app_name
cd my_app_name
```
Reemplazar my_app_name con el nombre de tu proyecto. Cambiar al nuevo directorio.

Luego, se debe configuar el entorno virtual.
```shell
python3 -m venv .venv
source .venv/bin/activate