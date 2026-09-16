<div align="center">

# Control de Activos — Power App

Aplicación para registrar, consultar y controlar los activos de la organización.

</div>

## Descripción

**ControlActivosPowerApp** centraliza la gestión del inventario de activos y su ciclo de vida. La solución permite mantener la información actualizada, consultar la asignación y ubicación de cada activo, y facilitar el seguimiento de altas, bajas, traslados y mantenimientos.

## Funcionalidades

- Alta, edición y consulta de activos.
- Registro de código, categoría, marca, modelo, número de serie y estado.
- Asignación de activos a personas, áreas o ubicaciones.
- Seguimiento de movimientos, entregas, devoluciones y traslados.
- Consulta y filtrado del inventario.
- Registro de evidencias y observaciones.
- Control de permisos según el perfil del usuario.
- Indicadores para apoyar la administración del inventario.

## Componentes de la solución

La solución está construida sobre Microsoft Power Platform y puede incluir los siguientes componentes:

- **Power Apps:** interfaz de usuario y lógica de la aplicación.
- **Power Automate:** notificaciones, aprobaciones y automatizaciones.
- **Origen de datos:** Dataverse, SharePoint u otra fuente configurada para la solución.
- **Conectores:** servicios necesarios para consultar o actualizar la información.

> Los nombres concretos de tablas, listas, flujos y conexiones dependen del entorno donde se haya desplegado la aplicación.

## Roles recomendados

| Rol | Responsabilidades |
|---|---|
| Administrador | Configuración, catálogos, permisos y mantenimiento de la solución. |
| Inventario | Altas, bajas, movimientos y conciliación de activos. |
| Responsable de área | Consulta y validación de activos asignados. |
| Usuario | Consulta de sus activos y confirmación de entregas o devoluciones. |

## Requisitos

- Cuenta de Microsoft 365 con acceso al entorno de Power Platform.
- Permisos de lectura y escritura en el origen de datos.
- Acceso a las conexiones utilizadas por la aplicación y sus flujos.
- Navegador compatible con Power Apps o aplicación móvil de Power Apps.

## Configuración y despliegue

1. Importar la solución administrada o no administrada en el entorno objetivo.
2. Configurar las variables de entorno y las referencias de conexión.
3. Verificar permisos sobre tablas, listas, aplicaciones y flujos.
4. Validar catálogos, estados, ubicaciones, áreas y perfiles.
5. Activar los flujos dependientes.
6. Compartir la aplicación con los grupos de seguridad correspondientes.
7. Ejecutar las pruebas funcionales con usuarios de cada rol.

## Operación

1. Crear o importar los catálogos necesarios.
2. Registrar los activos con un identificador único.
3. Asignar cada activo a su responsable o ubicación.
4. Registrar cualquier cambio mediante un movimiento, evitando modificar el historial.
5. Revisar periódicamente los activos sin asignar, fuera de servicio o pendientes de devolución.
6. Exportar o respaldar la información conforme a las políticas de la organización.

## Buenas prácticas

- Mantener identificadores únicos y formatos consistentes.
- No eliminar registros históricos; utilizar estados de baja o inactividad.
- Limitar el acceso a datos personales mediante roles y grupos de seguridad.
- Probar los cambios en un entorno de desarrollo antes de publicarlos.
- Documentar modificaciones en tablas, flujos, permisos y conexiones.
- Revisar periódicamente propietarios, conexiones y ejecuciones fallidas de los flujos.

## Solución de problemas

**La aplicación no carga:** comprobar el entorno seleccionado, las referencias de conexión y el acceso del usuario.

**No se guardan cambios:** validar permisos de escritura, campos obligatorios y disponibilidad del origen de datos.

**No llegan notificaciones:** revisar que el flujo esté activo, sus conexiones sean válidas y no existan ejecuciones fallidas.

**No aparecen registros:** comprobar filtros, permisos de lectura y la sincronización con el origen de datos.

## Seguridad y datos

La información debe gestionarse conforme a las políticas internas de seguridad y protección de datos. Los accesos deben asignarse mediante grupos de seguridad y bajo el principio de mínimo privilegio. No deben almacenarse contraseñas, secretos ni datos sensibles directamente en la aplicación.

## Mantenimiento

Antes de cada publicación:

- comprobar la solución en un entorno de prueba;
- revisar dependencias y conexiones;
- verificar los flujos y permisos;
- realizar una prueba de alta, edición, asignación y movimiento;
- documentar la versión y los cambios realizados.

## Soporte

Para reportar un incidente, incluir el entorno, usuario afectado, fecha y hora, operación realizada, mensaje de error y capturas sin información sensible.

## Licencia

Uso interno de la organización. La licencia y las condiciones de distribución deben definirse según las políticas corporativas.
