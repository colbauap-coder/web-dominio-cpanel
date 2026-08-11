# Siguiente paso: crear el repositorio en GitHub

Ahora ya existe una carpeta local:

`C:\Users\hordr\Desktop\web-dominio-cpanel`

Pero todavía falta crear el repositorio en GitHub. Sin repositorio, GitHub no tiene dónde guardar los secretos ni desde dónde ejecutar el despliegue.

## Qué hacer en GitHub

1. Entrar a GitHub.
2. Crear un repositorio nuevo.
3. Nombre sugerido: `web-dominio-cpanel`.
4. No hace falta agregar README desde GitHub, porque esta carpeta ya tiene uno.
5. Crear el repositorio.

Después de eso, se conecta esta carpeta local con el repositorio de GitHub.

## Luego se crean los secretos

Dentro del repositorio nuevo:

`Settings` → `Secrets and variables` → `Actions` → `New repository secret`

Crear:

| Nombre | Valor |
| --- | --- |
| `SSH_PRIVATE_KEY` | contenido completo de `C:\Users\hordr\.ssh\cpanel_deploy` |
| `SSH_HOST` | host o IP del servidor cPanel |
| `SSH_USER` | usuario de cPanel |
| `SSH_PORT` | puerto SSH, normalmente `22` |

## Importante

No hay que pegar la contraseña de cPanel en GitHub.

La contraseña solo sirve para entrar a cPanel. La conexión automática usará la llave SSH.
