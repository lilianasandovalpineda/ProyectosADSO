# 📋 Plantilla Guía para Especificación y Diagramación de Casos de Uso UML
### Servicio Nacional de Aprendizaje (SENA) | Regional Boyacá – Centro Minero
**Programa de Formación:** Tecnólogo en Análisis y Desarrollo de Software (ADSO)  
**Competencia:** `220501093` - Evaluar requisitos de la solución de software de acuerdo con metodologías de análisis y estándares.  
**Resultado de Aprendizaje (RAP):** `RAP 02` - Modelar las funciones del software de acuerdo con el informe de requisitos técnicos.

---

## 📌 1. Propósito del Repositorio

Este repositorio contiene la **plantilla estándar institucional**, ejemplos prácticos orientadores y lineamientos metodológicos para que los aprendices de proyectos formativos documenten y modelen rigurosamente las funcionalidades de sus sistemas de información mediante el Lenguaje Unificado de Modelado (**UML**).

El objetivo es articular los **Requisitos Funcionales (RF)** levantados en las fases iniciales del ciclo de vida del software con especificaciones formales y diagramas de interacción entre actores y el sistema.

---

## 📁 2. Estructura del Repositorio

```bash
├── docs/
│   ├── Formato_Plantilla_Casos_de_Uso_UML_SENA.pdf   # Formato guía oficial en blanco con ejemplos
│   ├── Ejemplo_Caso_de_Uso_SIGEPE_SENA.pdf           # Ejemplo práctico completo aplicado a proyecto
│   └── diagramas/                                    # Imágenes y exportables de diagramas UML (.png, .svg)
├── templates/
│   ├── plantilla_caso_de_uso.md                     # Plantilla editable en Markdown
│   └── plantilla_caso_de_uso.docx                   # Plantilla editable para procesadores de texto
└── README.md                                         # Guía metodológica e instructivo de uso
```

---

## 🚀 3. Instrucciones Paso a Paso para Aprendices

Para diligenciar correctamente la documentación de cada caso de uso en su proyecto formativo, siga este flujo de trabajo:

```
[1. Identificar RF] ➔ [2. Modelar Diagrama UML] ➔ [3. Exportar Imagen/SVG] ➔ [4. Diligenciar Especificación] ➔ [5. Control de Versiones]
```

### Paso 1: Identificación y Alcance
* Revise la matriz de requisitos de su proyecto formativo.
* Tome un Requisito Funcional (ej. `RF01`, `RF02`, etc.) y delimite el objetivo exacto que persigue el usuario al interactuar con el sistema.

### Paso 2: Construcción del Diagrama UML
* Utilice una herramienta CASE recomendada:
  * [Draw.io](https://app.diagrams.net/)
  * [StarUML](https://staruml.io/)
  * [PlantUML](https://plantuml.com/)
  * Astah / Enterprise Architect
* **Reglas de Modelado UML:**
  * **Límite del Sistema (*Boundary*):** Debe encerrar todos los casos de uso del módulo.
  * **Actores (*Stickman*):** 
    * A la izquierda: Actor primario (inicia la interacción).
    * A la derecha: Actores secundarios o de apoyo (bases de datos, servicios OAuth, pasarelas de pago, APIs externas).
  * **Relación `<<include>>`:** Se usa para funcionalidades obligatorias que se ejecutan siempre como parte del caso de uso base (flecha discontinua que apunta al caso incluido).
  * **Relación `<<extend>>`:** Se usa para flujos opcionales, extensiones condicionales o excepciones (flecha discontinua que apunta al caso de uso base).

### Paso 3: Diligenciamiento de la Ficha Técnica
Reemplace los campos resaltados de la plantilla con información concisa, técnica y verificable. Evite ambigüedades.

---

## 📝 4. Plantilla de Especificación (Estructura Estándar)

A continuación se presenta la tabla en formato Markdown lista para ser copiada y completada por cada funcionalidad:

```markdown
| Campo | Detalle / Especificación |
| :--- | :--- |
| **Código** | `CU0# - Nombre_del_caso_de_uso` |
| **Versión** | 1.0 (Borrador / Revisión / Aprobado) |
| **Fecha de Creación** | DD/MM/AAAA |
| **Autor(es)** | Nombres y apellidos de los aprendices responsables |
| **Requisito(s) Asociado(s)** | `RF0#` - Código y descripción del requisito funcional según el informe técnico |
| **Descripción** | Resumen conciso del objetivo y resultado del caso de uso. |
| **Actor(es)** | **Principal:** Actor que ejecuta la acción.<br>**Secundario(s):** Sistemas, APIs o BD de apoyo. |
| **Precondiciones** | Requisitos y estados previos necesarios antes de ejecutar el flujo (ej. sesión activa, registros previos). |
| **Flujo Normal (Principal)** | **Acción del Actor:**<br>1. El actor selecciona la opción...<br>2. El actor ingresa los datos...<br>3. El actor confirma la operación...<br><br>**Acción del Sistema:**<br>1. El sistema despliega el formulario...<br>2. El sistema valida los datos en tiempo real...<br>3. El sistema almacena la información y confirma el éxito. |
| **Flujo Alternativo / Excepciones** | **2a. Datos incompletos o inválidos:**<br>- Sistema alerta los campos faltantes y no procesa el envío.<br>**3a. Duplicidad de clave única:**<br>- Sistema notifica la existencia del registro y cancela la duplicación. |
| **Postcondiciones** | Estado en el que queda la base de datos y la interfaz tras la finalización exitosa. |
| **Prioridad** | Alta / Media / Baja |
| **Reglas de Negocio (RN)** | Validaciones normativas o de lógica de dominio asociadas (ej. longitudes de clave, roles admitidos). |
| **Observaciones** | Dependencias técnicas, consideraciones de red o servicios de terceros. |
```

---

## 💡 5. Ejemplos Orientadores Disponibles

En la carpeta `docs/` se encuentran dos ejemplos de referencia analizados y resueltos:

1. **CU01 - Registrar Aprendiz:** Interacción estándar en el *Sistema de Gestión Formativa* con relación `<<include>>` hacia *Autenticarse en el sistema* y validaciones de datos duplicados.
2. **CU-ADSO-001 - Autenticar e Iniciar Sesión:** Manejo de flujo seguro con servidores de identidad OAuth, generación de tokens JWT, control de intentos fallidos y bloqueo preventivo de cuentas.
3. **CU03 - Registrar Préstamo de Equipos y Herramientas (SIGEPE):** Flujo completo con escaneo de código de barras, validación de estado disciplinario de aprendices y emisión de comprobantes digitales.

---

## ⚖️ 6. Criterios de Evaluación y Buenas Prácticas

| Aspecto | Criterio de Aceptación (SENA) |
| :--- | :--- |
| **Consistencia:** | Los nombres de los casos de uso deben iniciar con un **verbo en infinitivo** (ej. *Registrar*, *Consultar*, *Modificar*, *Eliminar*, *Emitir*). |
| **Trazabilidad:** | Todo caso de uso debe estar obligatoriamente vinculado al menos a un **Requisito Funcional (RF)**. |
| **Complitud de Flujos:** | El flujo normal debe describir claramente tanto la acción del actor como la respuesta reactiva del sistema. |
| **Manejo de Errores:** | Los flujos alternativos no deben dejarse en blanco; deben contemplar fallos de validación, cortes de red o denegaciones de permiso. |
| **Claridad de Actores:** | No confunda a los actores con componentes internos del software (un "botón" o un "formulario" no es un actor). |

---

## 👥 Equipo de Trabajo y Créditos

* **Centro:** SENA Centro Minero – Regional Boyacá (Sogamoso, Colombia)  
* **Coordinación:** Área de Teleinformática, Sistemas y Software (ADSO)  
* **Vigencia:** Año 2026
