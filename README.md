# Crystal Reports para SAP
En esta guía se abordará la instalación y uso de **Crystal Reports** en el entorno de SAP Business One. 

---

## Instalación del ecosistema para Crystal Reports SAP

### Instalación de SQL Server
1. Instalar **SQL Server**.
2. Instalar **SQL Server Management Studio (SSMS)**.
3. Ingresar a la instancia de SQL Server creada.
4. Dirigirse a **Security > Logins > sa**.
5. Configurar una nueva contraseña para el usuario `sa`.
6. En el apartado **Status** de `sa`, habilitar la opción **Login** seleccionando **Enable**.
7. En **Management Studio**, hacer clic derecho sobre la instancia principal de SQL Server > **Properties** > **Security**, habilitar la opción **SQL Server and Windows Authentication Mode**.

### Verificación de protocolos TCP
1. Acceder a **SQL Server Configuration Manager**.
2. Habilitar el protocolo **TCP/IP**:
   - Hacer clic derecho en **TCP/IP** y seleccionar **Enable**.
   ![TCP_Opciones](https://github.com/user-attachments/assets/ba15b6b3-f0d8-4699-b515-2a6fd83e5579)
3. Reiniciar la instancia de SQL Server:
   - Ir a la opción de servicios en SQL Server Configuration Manager, seleccionar la instancia y elegir **Restart**.


---

## Instalación de SAP Business One
1. Seleccionar el idioma de instalación.
2. Elegir la opción **Realizar configuración**.
3. Seleccionar la opción para instalar el directorio de infraestructura local.
4. Configurar una clave de acceso (contraseña) y confirmarla.
5. Escoger el motor de base de datos, especificando el nombre de la instancia (por ejemplo, `nombrepc\sqlserver_name`).
6. Proveer las credenciales configuradas para el usuario `sa` en SQL Server.

### Menu ASistente de configuracion
### Menú del Asistente de Configuración
1. Seleccionar **Repository**.
2. Crear una base de datos de prueba (**Create Demo**).
3. Deseleccionar **Remote Support Platform**.
4. Seleccionar todas las herramientas del servidor.
5. Elegir todas las herramientas de implementación, excepto:
   - **Data Transfer Workbench**
   - **SAP Business One Studio**
6. Seleccionar la base de datos de prueba más cercana al país (en este caso, Guatemala).
7. Configurar el uso de certificados autofirmados:
   - **Usar certificado autofirmado > Usar certificado autofirmado**.
8. Continuar con el asistente de instalación:
   - Aceptar el mensaje sobre la carpeta compartida y el archivo `config.xml`.
   - Proceder con las opciones por defecto hasta finalizar.
   - Si salen ventanas de instalacion que piden user id y compañia poner cualquiera y realizar una configuración normal de dicho componente.
9. En caso de que **Browser Access Service** muestre un error al final de la instalación, ignorarlo si no hay otros errores.
10. No seleccionar nada en el apartado de reestablecer
11. Escoger en Siguiente y Finalizar

---



## Primera vez ingresando a SAP Business One
1. Seleccionar la opción **Modificar sociedad**.
2. Escoger el servidor SQL configurado.
3. Seleccionar la base de datos de prueba (demo) configurada previamente.
4. Ingresar las credenciales predeterminadas:
   - Usuario: `manager`
   - Contraseña: `manager`
5. Aceptar el mensaje inicial del sistema.
6. Cancelar la configuración de contabilizaciones periódicas cuando sea solicitada.



---

## Instalación de Crystal Reports
1. Realizar una instalación típica, seleccionando el idioma deseado.
2. Finalizar la instalación.
3. Buscar el acceso directo de Crystal Reports en la barra de tareas de Windows:
   - Acceder al directorio donde está instalado.
   - Crear un acceso directo al escritorio o al menú de inicio.
   ![CrystalReportAccesoDirecto](https://github.com/user-attachments/assets/b3f90464-4b7a-4b58-bbbe-86f103e497e3)

---

## Notas Importantes
- **Período de prueba:** SAP Business One ofrece un mes de prueba gratuito. 
- **Opciones para extender la prueba:**
   - Desinstalar y reinstalar el software.
   - Utilizar una máquina virtual con una configuración predefinida.  
     [Descargar Máquina Virtual Configurada](https://dmoncada-my.sharepoint.com/:f:/g/personal/services_moncadaservices_tech/EnNQdKu14D1Oq7GkmOV5imABMNPoJHdqGlM86KZXu3VJNA?e=t0vOde)
