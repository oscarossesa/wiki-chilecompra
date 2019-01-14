---
description: >-
  Este documento describe los pasos que deben seguirse para instalar y
  configurar un nuevo aplicativo.
---

# MVP5 - Banca Personas

## Información General

| Información General |  |
| :--- | :--- |
| Nombre del Proyecto |  |
| Fecha |  |
| Jefe de Proyecto |  |
| Nombre Módulo |  |
| Tipo del aplicativo | Web, Servicio Windows |

**Descripción funcional del proyecto**

Inyección periódica de proveedores no informados desde Mercado Publico hacia DIPRES \(Sistema Sigfe\). ****Reversa de presupuesto desde Mercado Publico a DIPRES \(Sistema Sigfe\) en la orden de compra

**Carpeta del empaquetado** 

\\vitara\Empaquetados\Candidatos\Activos\2018\11\20181128\_MVP5  

**Scripts de Bases de Datos: si**

## Instrucciones de instalación

### **Instalación Servicio Web Banca Personas**

* [ ] Crear un nuevo sitio web dentro del pool APISPRO llamado BancaPersonas en Framework 4. A continuación, copiar el contenido de la carpeta Servicio banca personas.
* [ ] Configuraciones webconfig servicio web banca personas:

```csharp
<!-- Datos usados para la cabecera -->
<add key="areaPorDefectoMesEjercicio" value="0807001"/>
<add key="sigfePartida" value="08"/>
<add key="sigfeCapitulo" value="07"/>
<add key="sigfeAreaTransaccional" value="001"/>
<add key="idProceso" value="01"/>

<!--oosses: mejoras 08/01/2019.-->
<add key="estadoPersona" value="VIGENTE"/> <!--Va en duro porque solo se estan informando proveedores vigentes-->
<add key="subClasificacion" value="01"/> <!--Se definio Enviar siempre 01 para las personas JURIDICAS-->
<add key="tipoIdentificacion" value="01"/> <!--01 para Rut y 02 para cualquier otro identificador-->

<!-- Flag para la ejecucion de la actualización de  -->
<add key="flgEnviarDatosProveedores" value="true"/>
<add key="carpetaMensajes" value="mensajes"/>

<!-- Credenciales para la conexion al servicio de Obtención de Periodo Activo Dipres -->
<add key="SigfeUser" value="chileCompraIOP" />
<add key="SigfeContrasena" value="usuario1234" />

<!-- URL del Servicio Dipres para el periodo abierto -->
<add key="SigfeUrlPeriodo" value="http://test-int.sigfe.gob.cl/cxf/public/chileCompra/buscarPeriodo" />

<!-- Credenciales para la conexion al servicio de Registro de Proveedores Dipres -->
<add key="SigfeUserRegistroPersonas" value="interMPSIGFE" />
<add key="SigfeContrasenaRegistroPersonas" value="usuario1234" />

<!-- URL del Servicio Dipres  -->
<add key="SigfeUrl" value="http://test-int.sigfe.gob.cl/cxf/public/chileCompra/registrarPersonas" />

<!--Configuraciones log-->
<add key="log4net.Config" value="log4net.config" />
<add key="log4net.Config.Watch" value="True" />
```

* [ ] Configuraciones log4net, verificar archivo log4net.config
* [ ] Ambientar conexión de los appender
  * [ ] LogAccionesMP.EnvioProveedores
  * [ ] LogAccionesMP.ErrorEnvioProveedores



### **Instalación Servicio Windows Banca Personas**

* [ ] Instalar servicio windows Banca Personas en servidor de aplicaciones.
* [ ] Configuraciones appconfig servicio windows



