# Desempe-o

# Descripción general
Mediapro es un sistema de gestion para la industria audiovisual que permite administrar producciones, personal técnico y creativo, equipos, loscalizaciones, procesos de rodaje y postproduccion.
En esta actividad se implementan eventos en MYSQL para automatizar procesos dentro del sistema.

# Instrucciones de uso

1. Abrir HeidiSQL o cualquier otro gestor de base de datos compatible con MYSQL.
   
3. Seleccionar la base de datos donde se ejecutarán los scripts.
   
4. Ejecutar el archivo scrip-Mediaproevents.txt, el cual contiene la base de datos y los eventos creados.

5. Antes de ejecutar los eventos primero hay que activarlos con la consulta:

   SET GLOBAL event_scheduler = ON;

   SHOW PROCESSLIST;

6. Verificar la creación de los eventos consultas como:

   SHOW EVENTS;

Notas
- Asegúrese de ejecutar primero el script de la base de datos antes de las funciones y triggers.
- Verifique que las tablas estén correctamente creadas antes de ejecutar los demás archivos.

# Estructura de módulos implementados
El sistema MediaPro se organiza en los siguientes módulos:

1. Módulo de Gestión de Clientes

   Encargado de administrar la información de los clientes que contratan producciones.

   * Tablas: Cliente


3. Módulo de Producción Audiovisual

   Gestiona la información general de las producciones.

   * Tablas: Produccion


3. Módulo de Personal Técnico

   Administra el personal involucrado en las producciones.

   * Tablas: Personal, Produccion_Personal


5. Módulo de Equipos Técnicos

   Gestiona los equipos utilizados en rodaje y su mantenimiento.

   * Tablas: Equipo_Tecnico, Mantenimiento, Produccion_Equipo


6. Módulo de Localizaciones

   Administra los lugares donde se realizan los rodajes.

   * Tablas: Localizacion, Produccion_Localizacion


7. Módulo de Planificación de Rodaje

   Organiza los días de rodaje, horarios y recursos utilizados.

   * Tablas: Plan_Rodaje, Plan_Rodaje_Escena, Plan_Rodaje_Actor, Plan_Rodaje_Equipo


8. Módulo de Escenas y Actuación

   Gestiona las escenas, actores y personajes involucrados.

   * Tablas: Escena, Actor, Personaje, Escena_Actor


9. Módulo de Material Grabado

   Almacena la información del material audiovisual generado.

   * Tablas: Material_Grabado, Audio


10. Módulo de Postproducción

   Gestiona procesos posteriores al rodaje.

   * Tablas: Postproduccion, Material_Postproduccion, Versiones, Aprobacion


11. Módulo de Distribución y Marketing

    Administra la distribución y promoción del contenido.

    * Tablas: Distribucion, Material_Promocional


12. Módulo de Automatización

    Encargado de la ejecución automática de procesos en la base de datos.

    * Events
