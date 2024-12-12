# Proceso de Búsqueda y Acceso a Sitios Web

El objetivo de este proceso es recorrer un archivo Excel que contiene una lista de sitios web. Los sitios web están ubicados en la columna **"WEBSITE"** del archivo. El proceso implicará acceder a cada URL y realizar una búsqueda de palabras clave dentro del contenido de la página web.

## Pasos del Proceso

### 1. Subida del Archivo Excel
- El usuario sube un archivo Excel (`.xlsx`) que contiene la columna **"WEBSITE"** con una lista de URLs a procesar.
  
### 2. Configuración de las Palabras Clave
- El usuario puede definir las palabras clave a buscar en los sitios web. Por defecto, se buscarán las siguientes palabras clave:
  - "denuncias"
  - "canal de denuncias"
  - "canal"
  - "canal ético"
  - "compliance"
  - **"more..."** (palabra clave adicional que puede ser personalizada)
  
### 3. Acceso al Sitio Web
- El sistema intentará hacer una solicitud HTTP a cada URL presente en la columna **"WEBSITE"** del archivo Excel.
  
### 4. Búsqueda de Palabras Clave
- El código buscará las palabras clave configuradas dentro del contenido de la página web descargada.
  
### 5. Acciones Según el Resultado de la Búsqueda
- **Si se encuentra una palabra clave**:
  - El sistema extraerá el link relacionado con la palabra clave encontrada en el sitio web.
  - El link o una breve descripción de hasta **300 caracteres** se insertará en una nueva columna llamada **"Resultado"** en el archivo Excel.
  
- **Si no se encuentra ninguna palabra clave o si ocurre un error**:
  - Si no se encuentra una palabra clave o si ocurre un error (como no poder acceder al sitio web), se insertará uno de los siguientes mensajes en la columna **"Resultado"**:
    - "Error al acceder: Sitio web no disponible"
    - "Página no encontrada"
    - "Acceso denegado"
    - "Palabras clave no encontradas"
  
### 6. Configuración del Código
El código será configurable para que:
- El usuario pueda elegir el nombre de la columna donde están los sitios web (por defecto se usa "WEBSITE").
- El usuario puede especificar las palabras clave a buscar.
- El código puede ser modificado para trabajar con otras configuraciones de archivo y procesos adicionales.

### 7. Generación del Archivo Excel Actualizado
- Después de procesar todos los sitios web, el sistema generará un archivo Excel actualizado con la nueva columna **"Resultado"** que contiene:
  - El link relacionado con la palabra clave encontrada.
  - El mensaje de error según el caso.

## Ejemplo de Columna "Resultado" en el Archivo

| **Website**             | **Resultado**                           |
|-------------------------|-----------------------------------------|
| `https://example.com`    | Link: `https://example.com/denuncia`    |
| `https://another.com`    | Error al acceder: Sitio web no disponible |
| `https://nosite.com`     | Palabras clave no encontradas        
