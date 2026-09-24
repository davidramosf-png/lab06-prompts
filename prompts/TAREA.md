# Tarea: Mi prompt profesional

## Funcionalidad elegida
Diseño y generación de un sistema CRUD básico en Java para la gestión de productos en un inventario local.

## Version 1: prompt basico
```text
Hazme un CRUD de productos en Java.
```
* **Qué cambió / Por qué:** Es el prompt inicial. Es demasiado general y la IA genera un código libre sin persistencia ni validaciones.

## Version 2
```text
Actua como desarrollador Java senior. Crea un sistema CRUD para gestionar productos (id, nombre, precio, stock). Usa una lista en memoria (ArrayList) para almacenar los datos.
```
* **Qué cambió / Por qué:** Añadí un **Rol** y el **Contexto** de almacenamiento en memoria para que el programa sea funcional y no requiera base de datos. El resultado mejoró pero no tiene control de errores.

## Version 3: prompt final
```text
Actúa como desarrollador Java. Crea un sistema CRUD básico para gestionar productos por consola. El modelo debe tener id, nombre, precio y stock, guardados en un ArrayList en memoria.

Restricciones: No uses librerías externas, valida que el precio y stock no sean negativos, y maneja excepciones sencillas si ingresan texto en vez de números.

Usa este formato para el menú:
1. Crear Producto
2. Listar Productos
3. Salir

Explica brevemente la estructura y luego presenta el código Java limpio.
```
* **Qué cambió / Por qué:** Incorporé **Restricciones** específicas (validaciones de negocio y manejo de excepciones) junto con un **Ejemplo** de menú y un **Formato** de entrega estructurado para que el código sea profesional y directamente ejecutable. La respuesta mejoró porque ahora valida precio y stock negativos, usa try-catch cuando se ingresan letras y respeta el menú que pedí.
## Componentes del prompt final

| Componente | Texto de mi prompt |
|------------|--------------------|
| **Rol** | Actúa como desarrollador Java. |
| **Instruccion** | Crea un sistema CRUD básico para gestionar productos por consola. |
| **Contexto** | El modelo debe tener id, nombre, precio y stock, guardados en un ArrayList en memoria. |
| **Restricción** | No uses librerías externas, valida que el precio y stock no sean negativos, y maneja excepciones sencillas si ingresan texto en vez de números. |
| **Ejemplo** | Usa este formato para el menú: 1. Crear Producto, 2. Listar Productos, 3. Salir. |
| **Formato** | Explica brevemente la estructura y luego presenta el código Java limpio. |
## Evaluacion del resultado

| Qué revisar | Cumple (Sí / No) |
|-------------|-------------------|
| ¿El CRUD funciona completamente desde consola en Java? | Sí |
| ¿Gestiona correctamente los atributos del producto (id, nombre, precio, stock)? | Sí |
| ¿El sistema permite crear y listar productos desde consola en Java? | Sí |
| ¿Valida correctamente que los números ingresados no sean negativos? | Sí |

## Errores que evite
1. **Ser demasiado general:** Lo evité en la V3 definiendo estrictamente que la interfaz sea por consola y listando los campos exactos del modelo de datos.
2. **No indicar el formato:** Lo evité instruyendo explícitamente a la IA a separar la explicación arquitectónica previa del bloque de código fuente estructurado.
