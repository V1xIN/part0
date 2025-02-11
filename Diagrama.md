# Diagrama de flujo: Crear una nueva nota
sequenceDiagram
    participant User as Usuario
    participant Browser as Navegador
    participant Server as Servidor

    User->>Browser: Escribe texto en el campo de entrada
    Browser->>Browser: Actualiza el estado local (nota pendiente)
    User->>Browser: Hace clic en el botón "Save"
    Browser->>Server: Envía solicitud POST con el texto de la nueva nota
    Server->>Server: Guarda la nueva nota en la base de datos
    Server->>Browser: Responde con la nueva lista de notas
    Browser->>Browser: Actualiza la interfaz mostrando la nueva nota
    User->>Browser: Ve la lista de notas actualizada
