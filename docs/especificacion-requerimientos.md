# Especificación de Requerimientos

### RF-01 - [registro tutoria]

#### Resumen
El sistema deberá permitir que un profesor registre una nueva tutoría académica, proporcionando la información necesaria para que posteriormente los estudiantes puedan consultarla e inscribirse.
#### Entradas

| Entrada                        | Tipo de dato | Descripción                                                       |
| ------------------------------ | ------------ | ----------------------------------------------------------------- |
| Código del profesor            | String       | Código que identifica al profesor que ofrece la tutoría.          |
| Tema de la tutoría             | String       | Tema o contenido académico que será tratado en la tutoría.        |
| Fecha                          | Date         | Fecha en la que se realizará la tutoría.                          |
| Hora de inicio                 | Time         | Hora en la que comenzará la tutoría.                              |
| Cantidad máxima de estudiantes | Integer      | Número máximo de estudiantes que podrán participar en la tutoría. |


#### Reglas o condiciones
La fecha de la tutoría no puede ser anterior a la fecha actual.
La cantidad máxima de estudiantes debe estar entre 1 y 10.
El sistema deberá asignar automáticamente un identificador único a la tutoría.
El registro solo se realizará si todas las condiciones son válidas.
#### Salidas

| Salida                      | Tipo de dato   | Descripción                                                  |
| --------------------------- | -------------- | ------------------------------------------------------------ |
| Identificador de la tutoría | Integer/String | Identificador único asignado a la tutoría.                   |
| Mensaje de confirmación     | String         | Informa al profesor que la tutoría fue creada correctamente. |


#### Resultado esperado
La tutoría queda registrada correctamente en el sistema con un identificador único y el profesor recibe un mensaje de confirmación.


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


### RF-04 - [Nombre del requerimiento]

#### Resumen

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|

#### Reglas o condiciones

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|

#### Resultado esperado


## 4. Gestión de Versiones

### Ramas utilizadas

### Proceso de integración

### Conflictos encontrados
