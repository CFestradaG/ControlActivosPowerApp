# Historial de Cambios

## 1.0.3 - 30/09/2026

**Versión interna de la solución:** 1.0.0.3.

### Aplicación
- Se incorporó la validación de acceso con la lista `Acceso` y la selección de sede al ingresar.
- Se actualizaron la búsqueda y consulta de activos, el registro de movimientos y la consulta de usuarios y bodegas.
- Se incorporó el alta de activos con registro automático del movimiento **Alta**.
- Se añadieron filtros de inventario por sede, estado, tipo de activo y marca, con indicadores agrupados y copia de filas seleccionadas.
- Se incluyen formatos PDF para entrega y traslado de responsabilidad.

### Flujos
- **Formato:** agrega el PDF como adjunto al registro de movimiento en SharePoint y devuelve la dirección del archivo.
- **Notificación Asignación Activos:** envía un correo al responsable, con copia a quien creó el movimiento, para las operaciones Asignación y Préstamo.

## 1.0.0 - 16/09/2026

### Aplicación
- Creación de Control Activos.
- Registro de equipos.
- Asignación de usuarios.

### Flujos
- Flujo de aprobación.
- Flujo de actualización de historial.

### Responsable
- Cruz Francisco Estrada Gregorio