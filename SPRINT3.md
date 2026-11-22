# Sprint 3 — Diccionarios de datos y validaciones

Cambios aplicados:

- Protección de las claves primarias en los seis diccionarios.
- `Nombre` y `Apellido` obligatorios e inmodificables tras guardar por primera vez (`DD_COMMIT`).
- Validación de los campos obligatorios definidos en la base de datos.
- Botón **Despedir** en la ficha de entrenador para dejar su equipo a `NULL` sin eliminarlo.
- Desplegables de nacionalidad de jugador y entrenador, enlazados al tipo `NACION` de `CodeMast`/`CodeType`.

## Paso necesario en DataFlex Studio (una sola vez)

En **Tools → Validation Code Maintenance**, crear el tipo `NACION` (descripción: `Nacionalidades`) y estos códigos de ejemplo (valor y descripción pueden coincidir): `Español`, `Alemán`, `Argentino`, `Italiano`, `Francés`, `Brasileño`, `Inglés` y `Belga`.

`CodeMast.Code` admite como máximo 10 caracteres. Algunos datos de ejemplo existentes contienen nacionalidades más largas (por ejemplo, `Neerlandés` y `Mozambiqueño`), por lo que será necesario normalizarlas a códigos cortos si se quieren editar esos registros con la nueva validación. No se han cambiado datos existentes automáticamente.

Después, compilar y ejecutar la WebApp en Windows y comprobar que **Despedir** conserva el entrenador y deja su `EquipoID` vacío (`NULL` en MySQL). La compilación no se ha ejecutado en este entorno, que no dispone de DataFlex.
