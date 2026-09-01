# Especificación de Requerimientos

## 1. Descripción del sistema

## 2. Integrantes

- Nombre: Juan David Delgado
- Nombre: Jeronimo Mazo Diez
- Nombre: Juan José Ortega Aguilera

## 3. Requerimientos Funcionales

### RF-01 - [Nombre del requerimiento]

#### Resumen

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|

#### Reglas o condiciones

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|

#### Resultado esperado


### RF-02 - [Nombre del requerimiento]

#### Resumen

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|

#### Reglas o condiciones

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|

#### Resultado esperado


### RF-03 - [Nombre del requerimiento]

#### Resumen

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|

#### Reglas o condiciones

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|

#### Resultado esperado


### RF-04 - Cancelación de inscripción a tutoría

#### Resumen

Permitir que un estudiante que se encuentre inscrito en una tutoría pueda cancelar su participación.

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|
| código estudiantil | String | Código que identifica al estudiante que desea cancelar su inscripción. |
| identificador de la tutoría | String | Identificador único de la tutoría en la que el estudiante desea cancelar su participación. |

#### Reglas o condiciones

- El estudiante debe tener una inscripción previa en la tutoría.
- La tutoría debe existir.
- La tutoría no debe haber comenzado.
- Si alguna de las condiciones no se cumple, la cancelación no deberá realizarse.

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|
| mensaje de confirmación | String | Informa al estudiante que la cancelación fue realizada correctamente. |
| mensaje de error | String | Informa el motivo por el cual no fue posible realizar la cancelación. |

#### Resultado esperado

La inscripción del estudiante es eliminada, se libera nuevamente el cupo correspondiente de la tutoría y se informa al estudiante que la cancelación fue realizada correctamente.
