# Proceso de Búsqueda y Acceso a Sitios Web

El objetivo de este proceso es recorrer el archivo `test.xlsx` que contiene una lista de sitios web en la columna **("WEBSITE")**. El proceso implicará acceder a cada URL y realizar una búsqueda de palabras clave dentro del contenido del sitio web.

## Pasos del Proceso

### 1. Acceso al Sitio Web
- Se accederá a cada URL en la columna **("WEBSITE")** del archivo `test.xlsx`.
- El sistema intentará hacer una solicitud HTTP a cada URL de la lista.

### 2. Búsqueda de Palabras Clave
- Se buscarán las siguientes palabras clave en el contenido de cada página web:
  - "denuncias"
  - "canal de denuncias"
  - "canal"
  - "canal ético"
  - "compliance"
  -  "more..."

### 3. Acciones Según el Resultado de la Búsqueda
- **Si se encuentra una palabra clave**:
  - Se extraerá el link asociado con la palabra clave encontrada.
  - El link o una breve descripción de hasta 300 caracteres se insertará en la nueva columna llamada **"Resultado"** en el archivo Excel.
  
- **Si no se encuentra ninguna palabra clave o si ocurre un error**:
  - En el archivo Excel, en la columna **"Resultado"**, se insertará una de las siguientes descripciones según el problema detectado:
    - "Error al acceder: Sitio web no disponible"
    - "Página no encontrada"
    - "Acceso denegado"
    - "Palabras clave no encontradas"
