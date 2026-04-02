```mermaid
sequenceDiagram
    participant navegador
    participant servidor

    navegador->>servidor: GET https://studies.cs.helsinki.fi/exampleapp/spa
    activate servidor
    servidor-->>navegador: el archivo HTML
    deactivate servidor

    navegador->>servidor: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate servidor
    servidor-->>navegador: el archivo CSS
    deactivate servidor

    navegador->>servidor: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    activate servidor
    servidor-->>navegador: el archivo JavaScript
    deactivate servidor

    Note right of navegador: El navegador comienza a ejecutar el código JavaScript que rellena la página

    navegador->>servidor: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate servidor
    servidor-->>navegador: [{ "content": "HTML is easy", "date": "2023-1-1" }, ... ]
    deactivate servidor

    Note right of navegador: El navegador ejecuta la función que renderiza las notas
