# Web del dominio

Repositorio inicial para publicar el sitio web en cPanel desde GitHub.

## Cómo funciona

Cada vez que se suban cambios a la rama `main`, GitHub Actions usará SSH para copiar los archivos al servidor cPanel, dentro de:

`~/public_html/`

## Secretos necesarios en GitHub

Estos secretos se crean dentro del repositorio de GitHub:

- `SSH_PRIVATE_KEY`
- `SSH_HOST`
- `SSH_USER`
- `SSH_PORT`

La clave pública ya debe estar importada y autorizada en cPanel.
