# GUIA DE INSTALACIÓN DE WEBSPHERE APPLICATION SERVER LIBERTY EN SKYTAP

_Para el desarrollo de este Despliegue se tiene como base una maquina Ubuntu 18.04.1 que se encuentra alojada en Skytap._



Indice

## Login y acceso a la maquina ubuntu en Skytap:

#### Para realizar de manera corracta el login y acceso a la maquina ubuntu debemos seguir los siguientes pasos:

_1. Acceder a la plataforma de Skytap, para esto debemos acceder desde algun Browser al siguiente link:_

```
https://cloud.skytap.com/
```
_2. Ahora debemos realizar el login con nuestras credenciales._

<p align="center">
 <img width="956" alt="login" src="https://user-images.githubusercontent.com/60987042/83697833-9549bf00-a5c5-11ea-8fe6-d0b404d6028b.PNG">
 </p>

_3. Al estar en la pagina principal de Skytap debemos dirigirnos a la sección de Environments y estando ahí debemos elegir el Environment en cual queramos trabajar._

<p align="center">
 <img width="850" alt="envi" src="https://user-images.githubusercontent.com/60987042/83697860-a1358100-a5c5-11ea-80cb-d7c9fa00a70a.PNG">
 </p>

_4. Ahora debemos hacer clic en la maquina que queremos trabajar_

<p align="center">
 <img width="949" alt="maquinas" src="https://user-images.githubusercontent.com/60987042/83697874-ab577f80-a5c5-11ea-8df4-c75cd91a394a.PNG">
 </p>


## Instalación del IBM Instalation Manager: 🚀

#### Para la correcta instalación del IBM IM en ubuntu debemos seguir los siguientes pasos:

_1. Inicialmente debemos descargar el instalador del IBM IM, y lo podemos hacer desde el siguiente link:_
```
https://www.ibm.com/support/fixcentral/swg/downloadFixes?parent=ibm~Rational&product=ibm/Rational/IBM+Installation+Manager&release=All&platform=All&function=fixId&fixids=1.8.2.0-IBMIM-LINUX-X86_64-20150303_1526&includeRequisites=1&includeSupersedes=0&downloadMethod=http
```
<p align="center">
<img width="439" alt="IBMIM" src="https://user-images.githubusercontent.com/60987042/83689743-33815900-a5b5-11ea-84a6-40a486002b4c.PNG">
</p>

_2.	Debemos abrir una terminal, la cual se puede abrir mediante el siguiente comando:_

```
Crtl+Alt+T
```
<p align="center">
<img width="551" alt="term" src="https://user-images.githubusercontent.com/60987042/83689785-45fb9280-a5b5-11ea-9474-639a35eaee67.PNG">
</p>

_3. Debemos dirigirnos a la capeta en la cual se descargo el instalador._

```
cd Desktop
```
ó
```
cd Descargas
```

_4.	Ahora debemos descomprimir el archivo que se descargo:_

```
unzip agent.installer.linux.gtk.x86_64_1.8.2000.20150303_1526.zip
```

_5. Ahora debemos ejecutar el comando de instalación	:_

```
./install
```

_6.	Al ejecutar el comando anterior se nos debe ejecutar una insterfaz grafica de instalación en la cual debemos dar clic en **NEXT**:_

<p align="center">
<img width="443" alt="installa" src="https://user-images.githubusercontent.com/60987042/83689938-7ba07b80-a5b5-11ea-8a51-3956488ba23c.PNG">
</p>

_7.	Debemos Aceptar los terminos y condiciones de la licencia y luego hacer clic en **NEXT**:_

<p align="center">
<img width="443" alt="Terminos" src="https://user-images.githubusercontent.com/60987042/83689965-86f3a700-a5b5-11ea-8670-3cb28fd784bb.PNG">
</p>  

_8.	Ahora debemos elegir la direccion de almacenamiento en la cual se va instalar, de forma predeterminada, se instalará en /opt/IBM; sin embargo, si lo desea, puede cambiar la ruta de instalación haciendo clic en Examinar:_

<p align="center">
<img width="441" alt="ruta" src="https://user-images.githubusercontent.com/60987042/83689999-9246d280-a5b5-11ea-8ce2-0de038bf702f.PNG">
</p>

_9.	Despues de aceptar los terminos, condiciones y seleccionar la ruta de instalción debemos dar clic en **Install**:_

<p align="center">
<img width="442" alt="Installfinal" src="https://user-images.githubusercontent.com/60987042/83690057-a4c10c00-a5b5-11ea-87f1-2908ef623c3c.PNG">
</p>

_10.	Por ultimo debemos verificar si el Installation Manager de IBM quedo correctamente instalado, para esto debemos dar clic en reiniciar y se debe abrir automaticamente:_

<p align="center">
<img width="444" alt="verify" src="https://user-images.githubusercontent.com/60987042/83690081-b0143780-a5b5-11ea-87fe-b58d78a4fe97.PNG">
</p>

## Instalación de Websphere Application Server Liberty en la maquina ubuntu mediante el Installation Manager de IBM 📦

#### Para la correcta instalación de WebSphere application Server Liberty en ubuntu debemos seguir los siguientes pasos:

_1. Inicialmente debemos descargar el instalador del WAS Liberty, y lo podemos hacer desde la pagina oficial de WAS Liberty o IBM:_
```
passport advantage
```
_2.	Debemos abrir una terminal, la cual se puede abrir mediante el siguiente comando:_

```
Crtl+Alt+T
```
<p align="center">
<img width="551" alt="term" src="https://user-images.githubusercontent.com/60987042/83689785-45fb9280-a5b5-11ea-9474-639a35eaee67.PNG">
</p>

_3. Debemos dirigirnos a la capeta en la cual se descargo el instalador._

```
cd Desktop
```
ó
```
cd Descargas
```

_4.	Ahora debemos descomprimir el archivo que se descargo:_

```
unzip was.repo.19009.liberty.core.zip
```

_5. Despues de tener descomprimido el archivo de instalación, debemos abrir el Installation Manager de IBM y para esto ejecutamos en una terminal el siguiente comando :_

```
sudo ./opt/IBM/InstallationManager/eclipce/launcher
```

_6. Teniendo abierta la interfaz grafica del IBM IM debemos dar clic en **Archivo** y luego en **Preferencias**:_

<p align="center">
 <img width="353" alt="w1" src="https://user-images.githubusercontent.com/60987042/83696493-3b93c580-a5c2-11ea-9513-342ac9f8ebd2.PNG">
</p>

_7. Damos clic en **Añadir Repositorio**:_

<p align="center">
 <img width="722" alt="añadir" src="https://user-images.githubusercontent.com/60987042/83696537-4f3f2c00-a5c2-11ea-8f20-41cd1c3b62f7.PNG">
</p>

_8. Dando clic en examinar debemos buscar el archivo que tiene el nombre **repository.config**, el cual se encuentra dentro de la carpeta que se extrajo del instalador._

<p align="center">
 <img width="573" alt="repository-config" src="https://user-images.githubusercontent.com/60987042/83696565-5bc38480-a5c2-11ea-9243-bc11ba8b5c4b.PNG">
</p>

_9. Damos clic en **Ok** y despues en **Aceptar**, este proceso nos debe añadir el archivo de instalación al IBM IM._

_10. Ahora demos dar clic en **Aplicar** y luego en **Aceptar**, este proceso nos llevara de nueva al menu principal de IBM IM._

<p align="center">
 <img width="468" alt="Apli" src="https://user-images.githubusercontent.com/60987042/83696579-64b45600-a5c2-11ea-83de-2fcc05a0201a.PNG">
</p>

_11. El siguinete paso es dar clic en el Boton Intalar._

<p align="center">
 <img width="470" alt="clic-install" src="https://user-images.githubusercontent.com/60987042/83696602-7dbd0700-a5c2-11ea-8c92-6322a762faf1.PNG">
</p>

_12. Al completar el paso anterior se nos debe abrir una nueva ventana en la cual debemos seleccionar el paquete que queremos instalar en este caso es el de WebSphere Application Server Liberty, y al seleccionarlo debemos dar clic en **Siguiente**_

<p align="center">
 <img width="540" alt="was" src="https://user-images.githubusercontent.com/60987042/83696620-8dd4e680-a5c2-11ea-8091-228c27f70835.PNG">
</p>

_13. Al terminar el paso numero 12 de debe abrir una nueva ventana las cual nos indica los prerequisitos para la instalación en la cual tambien debemos dar clic en **Siguiente**._


_14. Ahora nos debe aparecer la ventana de **Terminos y Condiciones** a las cuales debemos darle **Aceptar** y dar clic en **Siguiente**._


_15. Luego vienen las ventanas de **ubicación** en la cual debemos elegir la ruta de instalación, **Caracteristicas** en la cual nos da un informa detallado del Software que vamos a instalar y por ultimo una ventana de resumen en la cual se nos debe habilitar el Boton de **Instalar**._

<p align="center">
 <img width="539" alt="resu" src="https://user-images.githubusercontent.com/60987042/83696648-9a593f00-a5c2-11ea-969c-d012b8b36f27.PNG">
</p>


_16. Al dar clic en **Instalar**, se va a iniciar este proceso el cual demora unos minutos, pero al terminar tendremos lista la instalación de WebSphere Application Server Liberty en nuestra maquina ubuntuy la forma de verificarlo es la siguiente:_
 
 _En una terminal de ubuntu debemos colocar los siguiente comandos en su orden:_
 
 ```
cd /opt/IBM/WebSphere/Liberty/bin/
```
```
sudo ./productInfo version
```

_Estos comandos nos daran una respuesta como la siguiente:_

<p align="center">
 <img width="493" alt="info" src="https://user-images.githubusercontent.com/60987042/83696687-af35d280-a5c2-11ea-80ac-d73e163b5c20.PNG">
</p>

## Autores ✒️

_Equipo IBM Cloud Tech sales Colombia._

 
