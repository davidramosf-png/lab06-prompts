# Bitacora de prompts
Laboratorio 06: Fundamentos de Ingenieria de Prompts.
Herramienta de IA usada: ChatGPT / Gemini

## Ejercicio 2: Tokens y ventana de contexto

| Texto | Caracteres | Tokens |
|-------|------------|--------|
| Los estudiantes programan en Java. | 35 | 7 |
| The students program in Java. | 29 | 6 |
| desafortunadamente | 18 | 4 |

### Observación de la Ventana de Contexto:
Cuando pregunté por 'TiendaTec' en el mismo chat, el modelo recordó el nombre de la aplicación y la tecnología perfectamente porque la información seguía activa dentro de su ventana de contexto actual. Sin embargo, al abrir un chat nuevo y repetir la pregunta, la IA no supo responder o inventó un nombre debido a que cada sesión nueva inicia con la ventana de contexto completamente vacía.

## Ejercicio 3: Temperatura

| Temperatura | % de BiblioTec | Nombres en los 5 intentos |
|-------------|----------------|---------------------------|
| 0 | 100.0% | BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec |
| 0.5 | 78.4% | BiblioTec, LibroYa, BiblioTec, PrestaLibro, BiblioTec |
| 1 | 52.1% | BiblioTec, LectoGo, LibroYa, PaginaLibre, PrestaLibro |
| 1.8 | 31.5% | LectoGo, NubeDeTinta, LibroYa, PaginaLibre, BiblioTec |

### Análisis de Temperatura:
Al subir la temperatura, las respuestas se vuelven mucho más variadas, creativas y menos predecibles porque el modelo aplana las probabilidades de los tokens, dándole oportunidad a opciones menos comunes. El simulador nunca inventa un nombre completamente nuevo fuera de la lista porque la temperatura no añade conocimiento ni base de datos externa al modelo; solo modifica los criterios de riesgo al elegir entre los tokens que ya conoce.

## Ejercicio 4: Prompt vago vs estructurado

| Criterio | Prompt vago | Prompt estructurado |
|----------|-------------|---------------------|
| Menciona el objetivo del sistema | No | Sí |
| Menciona a los usuarios principales | No | Sí |
| Tiene exactamente 3 funcionalidades | No | Sí |
| Esta en 3 parrafos | No | Sí |
| Lo usaria en un informe real | No | Sí |

## Ejercicio 5: Anatomía de un prompt

| Componente | Texto de mi prompt |
|------------|--------------------|
| Rol | Actua como desarrollador Java profesional. |
| Instruccion | Crea una clase ejecutable en Java para gestionar los productos de una tienda... |
| Contexto | ... utilizando una clase Producto con los atributos codigo, nombre, precio y stock. |
| Ejemplo | Usa este estilo para los metodos: getPrecio(), setPrecio(double precio). |
| Formato | Explica primero la estructura de la clase de forma breve y luego presenta el codigo Java limpio. |

### Cambios por nivel:
* **Nivel 1:** La IA generó un programa sumamente básico y aleatorio (un Hola Mundo).
* **Nivel 2 (Rol):** El código se estructuró con mejores prácticas de programación, pero seguía siendo libre.
* **Nivel 3 y 4 (Contexto + Instrucción):** El modelo dejó de adivinar y construyó exactamente la entidad Producto con los atributos solicitados.
* **Nivel 5 (Formato + Ejemplo):** El resultado se ordenó de forma idónea para un reporte, respetando la nomenclatura exacta de los métodos pedidos.

## Ejercicio 6: Del prompt basico al profesional

```text
Actua como desarrollador Java. Crea un ejemplo de login para una aplicacion de escritorio utilizando Swing. El usuario debe ingresar correo y contrasena. Explica brevemente el funcionamiento y presenta el codigo organizado por clases.

Mejora el codigo anterior con estas restricciones: no uses librerias externas, valida que el correo contenga @ y que la contrasena tenga al menos 8 caracteres, y muestra los mensajes con JOptionPane.
```