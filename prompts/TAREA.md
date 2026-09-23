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
Actua como desarrollador Java senior. Crea un sistema CRUD para gestionar productos en consola. El modelo de datos debe incluir id, nombre, precio y stock. El almacenamiento debe ser en memoria usando ArrayList. 

Restricciones: No uses librerias externas, valida que el precio y el stock no sean negativos, y maneja excepciones si el usuario ingresa texto en lugar de numeros.

Usa este estilo para el menu en consola:
1. Crear Producto
2. Listar Productos
3. Salir

Presenta primero una explicacion breve de la arquitectura de las clases y luego el codigo fuente completo ordenado por bloques limpios.
```
* **Qué cambió / Por qué:** Incorporé **Restricciones** específicas (validaciones de negocio y manejo de excepciones) junto con un **Ejemplo** de menú y un **Formato** de entrega estructurado para que el código sea profesional y directamente ejecutable.

## Componentes del prompt final

| Componente | Texto de mi prompt |
|------------|--------------------|
| **Rol** | Actua como desarrollador Java senior. |
| **Instruccion** | Crea un sistema CRUD para gestionar productos en consola. |
| **Contexto** | El modelo de datos debe incluir id, nombre, precio y stock. El almacenamiento debe ser en memoria usando ArrayList. |
| **Restricción** | No uses librerias externas, valida que el precio y el stock no sean negativos, y maneja excepciones si el usuario ingresa texto en lugar de numeros. |
| **Ejemplo** | Usa este estilo para el menu en consola: 1. Crear Producto... |
| **Formato** | Presenta primero una explicacion breve de la arquitectura de las clases y luego el codigo fuente completo... |

## Evaluacion del resultado

| Qué revisar | Cumple (Sí / No) |
|-------------|-------------------|
| ¿El CRUD funciona completamente desde consola en Java? | Sí |
| ¿Gestiona correctamente los atributos del producto (id, nombre, precio, stock)? | Sí |
| ¿Aplica la restricción de no usar librerías externas? | Sí |
| ¿Valida correctamente que los números ingresados no sean negativos? | Sí |

## Errores que evite
1. **Ser demasiado general:** Lo evité en la V3 definiendo estrictamente que la interfaz sea por consola y listando los campos exactos del modelo de datos.
2. **No indicar el formato:** Lo evité instruyendo explícitamente a la IA a separar la explicación arquitectónica previa del bloque de código fuente estructurado.