# Prompts utilizados para la realización del proyecto

Este proyecto fue desarrollado con asistencia de **Claude (Anthropic)** como herramienta de apoyo académico. A continuación se detallan las sesiones utilizadas y su propósito:

## Sesión 1 — Desarrollo del proyecto
🔗 https://claude.ai/share/4d2a85fe-6c7a-4b92-b8c1-91fb6067659c

Se utilizó para el diseño e implementación del sistema completo:
- Diseño de la arquitectura por capas (MVC)
- Implementación de herencia múltiple, clases abstractas y mixins
- Desarrollo de los decoradores `@decorador_interfaz`, `@manejar_errores` y `@validar_cedula`
- Implementación del algoritmo Módulo 10 para validación de cédula ecuatoriana
- Lógica de cálculo de descuentos por permisos remunerados y no remunerados
- Uso de funciones de orden superior (`map`, `filter`, `reduce`) en estadísticas
- Corrección de errores y validaciones (cédulas duplicadas, tipos de datos, etc.)

## Sesión 2 — Estudio y comprensión del código
🔗 https://claude.ai/share/aefb6b15-0247-472e-80d7-931eb45dcab0

Se utilizó para estudiar y entender a fondo cada componente del proyecto:
- Recorrido por las capas del sistema (Models → Core → Controllers → View)
- Explicación de conceptos POO aplicados: `@classmethod`, `@staticmethod`, ABC, Mixin, decoradores, inyección de dependencias
- Repaso con preguntas de evaluación previo a la entrega
- Corrección del flujo de validación de cédula en `EmpleadoController`
- Generación del diagrama de arquitectura por capas

## Sesión 3 — Complemento al desarrollo del proyecto
🔗 https://claude.ai/share/8739d16d-94a8-4763-acca-79a6286ff2d5

Sesión complementaria utilizada durante la construcción del sistema:
- Apoyo en la implementación de funcionalidades adicionales
- Revisión y refinamiento de la lógica de negocio
- Ajustes en la estructura del código y buenas prácticas POO

## Sesión 4 — Complemento al desarrollo del proyecto
🔗 https://claude.ai/share/a56cdadb-03c6-4eac-ba77-c0dc5c4f554c

Sesión complementaria utilizada durante la construcción del sistema:
- Apoyo en la implementación de funcionalidades adicionales
- Revisión y refinamiento de la lógica de negocio
- Ajustes en la estructura del código y buenas prácticas POO

---






# Sistema de Gestión de Permisos del Personal

Aplicación de consola desarrollada en **Python puro** (sin frameworks ni librerías externas) que gestiona el registro de empleados, tipos de permisos y solicitudes de permisos laborales, con cálculo automático de descuentos y persistencia en archivos JSON.

---

## Autores

- Jhoan Ariel Cevallos Villavicencio
- Jean Pierre Jiménez Bajaña
- José Antonio Torres Torres
- Jhonatan Gabriel Castro Belfor
- Elian Wladimir Galeas Barén

| Campo | Detalle |
|---|---|
| **Materia** | Programación Orientada a Objetos |+
| **Docente** | Ing. Daniel Vera |
| **Fecha** | 2026 |

---

## Requisitos

- Python **3.10 o superior**
- No requiere instalar librerías externas
- Compatible con Windows, Mac y Linux

---

## Cómo ejecutar

```bash
# Desde la carpeta raíz del proyecto
python main.py
```

---

## Estructura del proyecto

```
PRACT_PERMISOS/
│
├── main.py                        # Punto de entrada del programa
│
├── core/                          # Núcleo del sistema
│   ├── interfaces.py              # Clase abstracta ICrud (contrato CRUD)
│   ├── mixins.py                  # CalculosMixin (validaciones y cálculos)
│   ├── decoradores.py             # Color, Pantalla, decorador_interfaz, manejar_errores, validar_cedula
│   └── json_manager.py            # Lectura y escritura de archivos JSON
│
├── models/                        # Entidades del dominio
│   ├── empleado.py                # Clase Empleado
│   ├── tipo_permiso.py            # Clase TipoPermiso
│   └── permiso.py                 # Clase Permiso
│
├── controllers/                   # Lógica CRUD por entidad
│   ├── empleado_controller.py     # CRUD de empleados + validación de cédula
│   ├── tipo_permiso_controller.py # CRUD de tipos de permiso
│   ├── permiso_controller.py      # CRUD de permisos + estadísticas con HOF
│   └── stats_controller.py        # Estadísticas generales del sistema
│
├── views/                         # Interfaz de usuario en consola
│   └── menu_principal.py          # Menú principal de navegación
│
├── data/                          # Persistencia en archivos JSON
│   ├── empleados.json
│   ├── tipos_permisos.json
│   └── permisos.json
│
└── docs/
    ├── diagrama_de_clases.excalidraw
    └── diagrama_de_procesos.excalidraw
```

---

## Funcionalidades

- ✅ CRUD completo de Empleados
- ✅ CRUD completo de Tipos de Permiso
- ✅ CRUD completo de Permisos
- ✅ Validación de cédula ecuatoriana (algoritmo Módulo 10)
- ✅ Cálculo automático de valor hora y descuentos
- ✅ Estadísticas de permisos (remunerados, no remunerados, totales)
- ✅ Eliminación en cascada de permisos al eliminar empleado o tipo
- ✅ Persistencia automática en archivos JSON
- ✅ Interfaz de consola con colores ANSI
- ✅ Manejo de errores sin cortar la ejecución del programa

---

## Vista previa

### Menú principal
![Menú principal](PRACT_PERMISOS/docs/img/menu_principal.png)

### Menús del sistema
![Menú registrar](PRACT_PERMISOS/docs/img/menu_registrar.png)
![Menú consultar](PRACT_PERMISOS/docs/img/menu_consultar.png)
![Menú buscar](PRACT_PERMISOS/docs/img/menu_buscar.png)
![Menú eliminar](PRACT_PERMISOS/docs/img/menu_eliminar.png)
![Menú actualizar](PRACT_PERMISOS/docs/img/menu_actualizar.png)

### Empleados
![Registro de empleado](PRACT_PERMISOS/docs/img/registro_empleado.png)
![Consultar empleados](PRACT_PERMISOS/docs/img/consultar_empleados.png)
![Buscar empleado](PRACT_PERMISOS/docs/img/buscar_empleado.png)
![Eliminar empleado](PRACT_PERMISOS/docs/img/eliminar_empleado.png)
![Actualizar empleado](PRACT_PERMISOS/docs/img/actualizar_empleado.png)

### Tipos de permiso
![Registro de tipo de permiso](PRACT_PERMISOS/docs/img/registro_tipo_permiso.png)
![Consultar tipos de permiso](PRACT_PERMISOS/docs/img/consultar_tipo_permiso.png)
![Buscar tipo de permiso](PRACT_PERMISOS/docs/img/buscar_tipo_permiso.png)
![Actualizar tipo de permiso](PRACT_PERMISOS/docs/img/actualizar_tipo_permiso.png)

### Permisos
![Registro de permiso](PRACT_PERMISOS/docs/img/registro_permiso.png)
![Consultar permisos](PRACT_PERMISOS/docs/img/consultar_permisos.png)
![Buscar permiso](PRACT_PERMISOS/docs/img/buscar_permiso.png)
![Actualizar permiso](PRACT_PERMISOS/docs/img/actualizar_permiso.png)

### Estadísticas y resumen
![Estadísticas de permisos](PRACT_PERMISOS/docs/img/estadisticas_permisos.png)
![Resumen general](PRACT_PERMISOS/docs/img/resumen_general.png)

### Despedida
![Despedida](PRACT_PERMISOS/docs/img/despedida.png)

---

## Conceptos aplicados

| Concepto | Descripción | Archivo(s) |
|---|---|---|
| **Clases abstractas** | `ICrud` define el contrato CRUD obligatorio | `core/interfaces.py` |
| **Mixins** | `CalculosMixin` comparte validaciones entre controllers | `core/mixins.py` |
| **Decoradores** | Manejan errores, validan cédula y muestran encabezados | `core/decoradores.py` |
| **Herencia múltiple** | Todos los controllers heredan `ICrud` y `CalculosMixin` | `controllers/` |
| **HOF** | `map`, `filter`, `reduce` para estadísticas | `controllers/permiso_controller.py` |
| **Persistencia JSON** | Serialización con `to_dict` y `from_dict` | `core/json_manager.py` |
| **Expresiones regulares** | Validación de fechas y nombres | `core/mixins.py` |

---

## Reglas de negocio

### Cálculo de valor hora
```
valor_hora = sueldo / 240
```
> 240 = 8 horas × 30 días laborables al mes

### Cálculo de descuento por permiso
| Tipo permiso | Tipo | Fórmula |
|---|---|---|
| Remunerado (S) | D o H | `$0.00` (sin descuento) |
| No remunerado (N) | D (días) | `tiempo × 8 × valor_hora` |
| No remunerado (N) | H (horas) | `tiempo × valor_hora` |

### Eliminación en cascada
- Al eliminar un **empleado** → se eliminan todos sus permisos
- Al eliminar un **tipo de permiso** → se eliminan todos los permisos de ese tipo

### Validación de cédula ecuatoriana
1. Debe tener exactamente **10 dígitos numéricos**
2. Los 2 primeros dígitos representan la **provincia** (01-24)
3. El último dígito es verificado con el **algoritmo Módulo 10**

---

## Decisiones de diseño

- Se usó **JSON** en lugar de base de datos para mantener el proyecto sin dependencias externas y facilitar la revisión de datos.
- Los **decoradores** manejan errores y muestran encabezados para mantener los controllers limpios y enfocados en la lógica de negocio.
- El patrón **Mixin** evita duplicar validaciones en cada controller, siguiendo el principio DRY (Don't Repeat Yourself).
- La **separación de responsabilidades** mantiene cada clase con una única función: models almacenan datos, controllers manejan lógica, views manejan la interfaz.
- Los controllers reciben otros controllers como **parámetros** en lugar de crearlos internamente, facilitando la reutilización y evitando dependencias circulares.