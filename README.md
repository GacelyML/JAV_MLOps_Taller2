# JAV_MLOps_Taller2
## Por Brayan Carvajal, Juan Pablo Nieto y Nicolas Rojas
## Taller 2 - Desarrollo en contenedores

Cree un archivo `docker-compose.yaml` que ejecute un contenedor de desarrollo basado en el comando de docker descrito anteriormente. Acceda a la interfaz gráfica de Jupyter que despliega este componente y ejecute los ejemplos vistos en clase [TFDV](../Validacion_de_datos/TF/TFDV.ipynb) y [ML_Metadata](../Transformacion_de_datos/ML_Metadata.ipynb).

Tenga en cuenta que es posible que necesite elementos nuevos en esta imagen, valide el funcionamiento y proponga como agregar los elementos faltantes.

## Solución

Se creo el archivo docker-compose.yaml el cual levanta el servicio solicitado con el comando 

- Instale docker siguiendo las instrucciones en la [documentación oficial](https://docs.docker.com/get-docker/).
- Clone este repositorio con el siguiente comando:
    ```shell
    git clone https://github.com/GacelyML/JAV_MLOps_Taller2
    ```
- Ubíquese en la carpeta recién creada:
    ```shell
    cd JAV_MLOps_Taller2
    ```
- Cree el servicio con el siguiente comando:
    ```shell
    docker compose up
    ```
- Al finalizar la creación del servicio, en la consola se obtendrá un token de acceso que permitira ingresar desde un navegador web en [localhost:8888](http://127.0.0.1:8888/lab?token=XXXX)

Para instalar nuevas dependencias de python o del sistema que modifiquen la imagen base tensorflow/tfx:1.12.0 se propone el diseño de un dockerfile que permita generar una nueva imagen a partir de esta base, instalando las dependencias requeridas y ejecutando este archivo desde el docker-compose.yaml 