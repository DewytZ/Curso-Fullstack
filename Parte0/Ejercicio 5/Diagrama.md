```mermaid
sequenceDiagram
    participant navegador
    participant servidor

    navegador->>servidor: GET https://studies.cs.helsinki.fi/exampleapp/spa
    servidor-->>navegador: el archivo HTML

    navegador->>servidor: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    servidor-->>navegador: el archivo CSS

    navegador->>servidor: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    servidor-->>navegador: el archivo JavaScript

    Note right of navegador: El navegador comienza a ejecutar el código JavaScript que rellena la página

    navegador->>servidor: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    servidor-->>navegador: [{ "content": "HTML is easy", "date": "2023-1-1" }, ... ]

    Note right of navegador: El navegador ejecuta la función que renderiza las notas
