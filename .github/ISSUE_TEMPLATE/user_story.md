---
name: Historia de Usuario
about: Plantilla para registrar Historias de Usuario (Metodología Ágil)
title: 'HU# - [Nombre de la historia ej: HU-CLI-01]'
labels: 'historia de usuario'
labels: 'Prioridad Media'
labels: 'Puntuacion Historia 1'
assignees: ''
---
<div align="center">
  <img src="https://pautonoticias.com/sites/default/files/Article/sena-colombia-logo-green39a900png-20250120.png" width="120" alt="Logo SENA">
</div>

## Descripción de la Historia

**COMO** [rol del usuario]
**QUIERO** [acción o funcionalidad que desea]
**PARA** [beneficio o valor que se obtiene]

### Criterios de Aceptación (Condiciones de Satisfacción)
- [ ] **Dado que** [contexto inicial], **cuando** [acción del usuario], **entonces** [resultado esperado].
- [ ] *Criterio 2...*
- [ ] *Criterio 3...*

## 1. Información General
| Atributo | Detalle |
| :--- | :--- |
| **Responsable** | [@usuario] |

## 2. Historia de Usuario (Narrativa Ágil)
**COMO** [Rol, ej. Asesora de Cartera]
**NECESITO** [Acción, ej. registrar los datos personales de un cliente]
**PARA** [Razón, ej. poder gestionarle créditos posteriormente]

## 3. Lógica de Negocio y Restricciones
*Reglas internas, cálculos y dependencias del sistema.*
- [ ] [Ej. El cliente debe ser mayor de 18 años]
- [ ] [Ej. No se permiten clientes duplicados por número de identificación]
- [ ] [Regla 3...]

## 4. Especificación de Datos (Backend / DB)
*Definir campos SQL, tipos de datos (VARCHAR, INT, BOOLEAN, FK) y restricciones (UNIQUE, NOT NULL).*

```sql
-- Estructura de tabla esperada:
-- campo_id: INT PRIMARY KEY AUTO_INCREMENT
-- nombre: VARCHAR(100) NOT NULL
-- tipo_identificacion: ENUM('CC', 'CE', 'NIT') NOT NULL
```
