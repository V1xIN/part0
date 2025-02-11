sequenceDiagram
    participant User as Usuario
    participant Browser as Navegador
    participant Server as Servidor

    User->>Browser: Accede a la URL de la aplicación SPA
    Browser->>Server: Solicita la página principal de la SPA
    Server->>Browser: Responde con el HTML inicial de la SPA
    Browser->>Browser: Carga el archivo JavaScript principal de la SPA
    Browser->>Server: Solicita los datos de las notas (GET /api/notes)
    Server->>Browser: Responde con la lista de notas desde la base de datos
    Browser->>Browser: Muestra las notas en la interfaz de usuario
    User->>Browser: Interactúa con la aplicación (e.g., crear una nueva nota)
