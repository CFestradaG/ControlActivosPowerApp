# Manual de usuario: Control de Activos

**Aplicación:** Control de Activos (Power Apps Canvas).  
**Versión del paquete:** 1.0.3 (**versión interna de la solución:** 1.0.0.3).  
**Revisión:** 30 de septiembre de 2026.

## 1. Propósito

La aplicación permite consultar activos por sede, revisar su ubicación y estado, registrar movimientos y consultar el historial asociado. También incluye una vista de usuarios y bodegas, herramientas de análisis del inventario y generación de formatos PDF para determinados movimientos.

## 2. Requisitos de acceso

- Tener una cuenta de Microsoft 365 habilitada para Power Apps.
- Tener permiso para abrir la aplicación y consultar o actualizar las listas de SharePoint que utiliza.
- Contar con un registro autorizado en la lista `Acceso` y permiso para consultar la sede seleccionada. La aplicación busca el usuario a partir de la cuenta de Microsoft 365.
- Para generar formatos, deben estar disponibles la conexión de SharePoint y el flujo **Formato**.
- Para escanear códigos, abrir la aplicación en un dispositivo compatible con cámara y conceder el permiso correspondiente.

Si la aplicación indica que el usuario no tiene acceso, solicita autorización al administrador o al ServiceDesk.

## 3. Ingresar a la aplicación

1. Abre **Control de Activos** en Power Apps.
2. En la pantalla inicial, selecciona la **Sede** que vas a consultar.
3. Pulsa **Ingresar**. El botón se habilita después de seleccionar una sede.
4. Si tu usuario está autorizado, la aplicación abre la pantalla principal y usa la sede seleccionada para consultar los activos.
5. Si aparece un aviso de falta de acceso, contacta al responsable de la aplicación o al ServiceDesk.

La aplicación utiliza la identidad de Microsoft 365; no presenta un campo de contraseña propio.

## 4. Navegación

El menú principal contiene estas secciones:

| Sección | Uso |
|---|---|
| **Inicio** | Consultar indicadores y movimientos recientes. |
| **Activos** | Buscar activos, revisar sus datos y movimientos, y registrar activos o movimientos. |
| **Usuarios** | Buscar usuarios o bodegas y revisar los activos y movimientos asociados a una ubicación seleccionada. |
| **Inventarios** | Filtrar y revisar el inventario en una tabla; copiar filas seleccionadas. |

En pantallas pequeñas, el menú aparece en una fila separada. El botón de actualizar recarga las listas de activos, movimientos y usuarios/bodegas. El nombre de la sede en la barra superior permite volver a la pantalla de selección de sede.

## 5. Inicio: indicadores y movimientos recientes

La sección **Inicio** presenta gráficos con cantidades de activos agrupadas por tipo, marca y estado para la sede seleccionada. También muestra los últimos 100 movimientos.

Para revisar un movimiento reciente:

1. Usa las pestañas de operación para mostrar **Todos** o una operación específica.
2. Selecciona una fila del historial.
3. Pulsa el botón de consulta (icono de ojo) para abrir los detalles del movimiento.
4. Cierra la consulta para volver al listado.

## 6. Consultar activos

1. Abre **Activos**.
2. Escribe parte o todo el código en **Buscar activo**. La búsqueda filtra por coincidencia dentro del código del activo y por la sede seleccionada.
3. Pulsa el control de escaneo en un dispositivo compatible; el código leído se coloca en la búsqueda y filtra los resultados.
4. Selecciona un activo de los resultados para mostrar sus datos.
5. Revisa los datos del activo y, en **Historial de movimientos**, consulta sus operaciones anteriores. El historial permite búsqueda y selección de un movimiento.

La ficha del activo está configurada como consulta. Las fuentes revisadas no muestran una acción general para editar todos sus campos; los cambios de ubicación y estado se realizan al registrar movimientos.

## 7. Registrar un activo

Desde **Activos**, usa el botón de agregar para abrir **Registro de Activo**. Completa los campos disponibles en el formulario, que pueden incluir:

- tipo de propiedad y código;
- serie, tipo de activo, marca y modelo;
- empresa, unidad de negocio y orden de compra;
- sede, ubicación, bodega y estado;
- observaciones y archivos adjuntos.

Las opciones de tipo de activo, marca y modelo dependen del catálogo de modelos. Para habilitar **Guardar**, completa código, serie, tipo de activo, marca, modelo, sede, descripción, unidad de negocio, responsable, empresa, bodega, tipo de propiedad y orden de compra. Al guardar el activo, la aplicación registra también el movimiento **Alta**, que deja el activo en estado **Disponible**. Se muestra una notificación al completar el registro.

## 8. Registrar una asignación u otro movimiento

Los movimientos dejan historial y actualizan la ubicación o el estado del activo. Las operaciones disponibles dependen del origen y destino: **Alta**, **Asignación**, **Préstamo**, **Traslado**, **Diagnóstico** y **Baja**.

1. En **Activos**, busca y selecciona el activo. En el detalle, pulsa el botón de registro de movimiento.
2. Selecciona el usuario o la bodega de destino usando el botón de búsqueda correspondiente. En **Usuarios**, el campo busca por código de usuario/bodega.
3. Completa el número de caso o referencia (el formulario muestra como ejemplo `TI-RQ-123`).
4. Comprueba el activo, el origen, el destino y la sede que aparecen en el formulario.
5. Selecciona la operación que corresponda. La lista de operaciones se restringe según si el origen y el destino son bodega o usuario.
6. Completa los campos adicionales que se muestren, como observaciones, empresa o unidad de negocio para ciertos traslados.
7. Pulsa **Guardar**. La aplicación habilita el guardado cuando están completos el caso, activo, origen, operación y destino.

Al guardar, la aplicación registra el movimiento en SharePoint y actualiza la ubicación y el estado del activo según la operación. Para **Asignación** y **Préstamo**, el flujo de notificación envía un correo al responsable, con copia a quien registró el movimiento. Conserva la referencia del caso para facilitar la trazabilidad.

## 9. Consultar usuarios y bodegas

1. Abre **Usuarios**.
2. Escribe el código completo del usuario o de la bodega en **Buscar usuario / bodega** y ejecuta la búsqueda.
3. Selecciona el registro para consultar sus datos.
4. Revisa las pestañas de movimientos o activos cargados para esa ubicación. Las tablas permiten búsqueda.
5. Para registrar un movimiento relacionado con esa ubicación, usa la acción de movimiento disponible en el detalle y completa el origen/destino según corresponda.

Esta sección permite consultar los registros de usuarios y bodegas; no incluye el registro de nuevos usuarios o bodegas.

## 10. Consultar inventarios y copiar resultados

1. Abre **Inventarios**.
2. Selecciona los filtros disponibles: sede, estado, tipo de activo y marca.
3. Usa el botón de filtro para actualizar resultados e indicadores.
4. Usa el botón de borrar filtros para limpiar las selecciones.
5. Revisa la tabla de activos. Si necesitas copiar datos, selecciona una o más filas y pulsa el control de copia. Los campos se copian como texto tabulado, apto para pegar en una hoja de cálculo.

Los indicadores agrupan activos por marca, sede, tipo, estado y modelo. Si los filtros no encuentran filas, los indicadores resumen el inventario completo mientras la tabla permanece vacía.

## 11. Consultar un movimiento y generar un formato

1. Abre un movimiento desde **Inicio** o desde el historial de un activo/usuario.
2. Selecciónalo y pulsa el icono de consulta para abrir sus detalles.
3. Para movimientos de **Asignación**, **Traslado** o **Préstamo**, pulsa el botón de formato de entrega. La aplicación prepara un documento con los datos del movimiento y del activo.
4. Revisa las páginas del documento y pulsa el icono de imprimir/generar.
5. El flujo **Formato** adjunta el PDF al movimiento en SharePoint y la aplicación descarga el archivo.
6. Para **Asignación** o **Traslado**, el botón con icono de persona abre el formato de traslado de responsabilidad. Genera el PDF desde esa pantalla.

La notificación por correo de **Asignación** y **Préstamo** es independiente de la generación del PDF: se envía al responsable y copia a quien registró el movimiento.

## 12. Mensajes y solución de problemas

| Situación | Qué revisar |
|---|---|
| No puedes ingresar | Que hayas seleccionado una sede y que tu correo esté autorizado en la lista de acceso. Si no, solicita acceso al administrador/ServiceDesk. |
| No aparecen activos | Confirma la sede seleccionada, el código ingresado y tus permisos de lectura en SharePoint. |
| No aparecen usuarios o bodegas | Busca por el código completo y confirma que el registro exista y esté disponible en la lista. |
| No se habilita Guardar | Completa caso, activo, origen, operación y destino; al registrar un activo, completa todos los campos indicados en esa sección. |
| No se guarda un registro | Revisa errores del formulario y permisos de escritura en las listas de SharePoint. |
| No se genera o descarga el PDF | Comprueba la conexión de SharePoint, que el flujo **Formato** esté habilitado y que el movimiento exista. Revisa también si el navegador bloqueó la descarga. |
| No aparece el adjunto | Actualiza el registro y valida que el flujo tenga permisos para crear adjuntos en la lista de movimientos. |
| El lector no abre | Verifica que el dispositivo tenga cámara y que Power Apps tenga permiso para utilizarla. |

## 13. Buenas prácticas

- Confirma la sede, el código del activo y el destino antes de guardar.
- Usa el número de caso o referencia correspondiente a la operación.
- Registra cada cambio mediante un movimiento para conservar el historial.
- Verifica el PDF y el adjunto en el movimiento correspondiente antes de dar por concluida una entrega.
- No compartas capturas que expongan datos personales o información interna.
- Si detectas un error, anota la sede, el activo, el número de caso, la fecha/hora y el mensaje mostrado; evita repetir la operación hasta confirmar si se guardó.

## 14. Componentes de datos

La aplicación usa SharePoint como origen de datos. En las fuentes se identifican estas listas o tablas:

| Lista | Uso observado |
|---|---|
| `Activos` | Datos, estado, sede, ubicación, adjuntos y responsable del activo. |
| `Movimientos` | Operación, caso, activo, origen, destino, observaciones e historial. |
| `Bodega_usuario` | Códigos y datos de usuarios/bodegas, empresa, sede y tipo de ubicación. |
| `Modelo_Activos` | Catálogo de tipos, marcas, modelos e imágenes. |
| `Acceso` | Comprobación de autorización durante el ingreso. |
| `Sede`, `Empresa` | Opciones utilizadas en los formularios. |

La aplicación también invoca el flujo de Power Automate **Formato** para adjuntar el PDF al movimiento correspondiente.