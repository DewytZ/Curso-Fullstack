```mermaid
sequenceDiagram
    participant navegador
    participant servidor

    Note right of navegador: El JavaScript añade la nota a la lista y la dibuja en el HTML localmente

    navegador->>servidor: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    Note right of navegador: Envía la nota en formato JSON { "content": "...", "date": "..." }
    servidor-->>navegador: HTTP status code 201 Created

    Note right of navegador: No hay más peticiones, la página no se recarga
