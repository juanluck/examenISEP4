# Ejercicio JMeter del examen de prácticas de ISE

Este repositorio es una versión modificada del repositorio de la práctica 4 [iseP4JMeter](https://github.com/davidPalomar-ugr/iseP4JMeter) (puede consultar el enlace para más información). En su mayor parte el repositorio actual es un clon del anterior pero se han introducido dos cambios. **Usted deberá averiguar de que cambios se tratan y ser capaz de modificar un test plan en JMeter que se le facilitará a continuación para que se ejecute de forma correcta**

---
## Pasos previos

1. Asegúrese que no tiene ningun contenedor ni imagen anterior desplegada en su máquina (aquella donde utilice docker), para ello:

**Elimine todos los contenedores en ejecución:**

```
docker rm -f $(docker ps -aq)
```

**Elimine todas las imagenes existentes:**

```
docker rmi -f $(docker images -aq)
```

2. Clone el repositorio actual en la máquina donde vaya a desplegar la aplicación.
3. Despliegue la aplicación con `docker-compose up`
4. Finalmente, compruebe que la aplicación se ha desplegado bien ejecutando el script `./pruebaEntorno.sh`. Consulte al profesor si hay algún problema al llegar a este punto.


---
## Configuración previa de JMeter

Una vez haya descargado el test plan [desde este enlace](https://mega.nz/file/c15XhIgD#CxiaAqWNEmjr9h_cK6YnksO1cBW5KDB5BBMCE-pmFEA) y lo tenga abierto en JMeter, deberá realizar los siguientes pasos previos a la resolución del ejercicio:

1. Vaya a `Test Plan - examen` y modifique el valor de la variable `HOST` por el de la IP que tenga la máquina donde ha desplegado la aplicación con `docker-compose up`.
2. En `CSV Data Set Config` introduzca la ruta en su máquina al fichero [./jMeter/alumnos-examen.csv](https://github.com/juanluck/examenISEP4/blob/main/jMeter/alumnos-examen.csv) que habrá descargado desde este repositorio.

---
## Resolución del ejercicio

Si ha llegado a este punto del ejercicio comprobará que al ejecutar el test plan de JMeter se producen dos errores tanto para la petición POST como para la petición GET (puede verlos en `View Results Tree`).

Amigo Sherlock, su trabajo consiste en localizar y arreglar estos dos errores y obtener un test plan que ejecute ambas peticiones de forma correcta. **Una vez lo tenga, no olvide guardar el resultado en el fichero .jmx**
