# Instalacion y Configuracion de Java para asdm.jnlp

_Se describe el proceso utilizado para configurar Java en Linux Mint 20 para poder utilizar el ASDM de CISCO_

## Descargando 🚀

_Descargar Java JRE (Linux x64):[La pagina oficial de Java](https://java.com/en/download/linux_manual.jsp) y mover el contenido a /usr/java_

```
sudo mkdir /usr/java
sudo mv ~/Downloads/jre*.tar.gz /usr/java
cd /usr/java
sudo tar zxvf jre*.tar.gz
sudo rm jre*.tar.gz
```
_Agregar las siguientes lineas al archivo /etc/profile_


```
sudo nano /etc/profile
export JAVA_HOME="/usr/java/jre1.x.x_xxx"
export PATH=$JAVA_HOME/bin:$PATH
```
_Guardar y Salir_

Luego aplicar el perfil

```
source /etc/profile (o reiniciar)
```

### Instalación 🔧

_Ejecutar la siguiente linea de comandos para descargar y abrir con java_


```
javaws https://ipaddress:port/admin/public/asdm.jnlp
```
