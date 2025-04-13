# Tarea Postulación Desarrollador DevOps. Jr.

## Supuestos y comentarios
```
Usé el flujo de git flow. A través de "features" se crean y aceptan PR hacia la rama "develop". La rama "master" se debe mezclar con los cambios en "develop" a través de un "release" para finalmente desplegarse en el entorno de producción

Para ver los cambios en el contenedor se debe forzar un rebuild de la imagen para evitar que utilice la anterior (como docker compose up --build) o montar un volumen con el código de la aplicación.

SECRET_KEY no se ha expuesto en el código pero si en uno de los workflow runs de Github Actions (lo que aparece en el commit del primer workflow run)

```

### Instalaciones necesarias después de instalar conda
```
conda create -n test_devops python=3.8 --no-default-packages
conda activate test_devops
conda install -c conda-forge Django pytest-django
```

### Instrucciones para docker-compose
```
Las variables SECRET_KEY y DEBUG deben ser definidas en el entorno de ejecución
También hay que borrar las imágenes creadas en sucesivos builds. Se puede hacer con un script bash.
```