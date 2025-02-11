sequenceDiagram
    participant User as Usuario
    participant Browser as Navegador
    participant Server as Servidor

    User->>Browser: Escribe texto en el campo de entrada
    Browser->>Browser: Actualiza el estado local con el texto de la nueva nota
    User->>Browser: Hace clic en el botón "Save"
    Browser->>Server: Envía solicitud POST con el texto de la nueva nota (POST /api/notes)
    Server->>Server: Guarda la nueva nota en la base de datos
    Server->>Browser: Responde con la nueva lista de notas (incluyendo la nueva)
    Browser->>Browser: Actualiza la interfaz mostrando la nueva lista de notas
    User->>Browser: Ve la nueva nota en la lista
