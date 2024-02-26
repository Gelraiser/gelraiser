# Crear un nuevo respositorio en la web de GitHub
Desde la pagina principal de github.com:
- Clic en el boton verde "New"
- Seleccionar el check de "Add a README file"
- Seleccionar el lenguaje de programacion deseado en el desplegable "Add .gitignore"
- Clic en el boton "Create Repository"

# Clonar el respositorio en el equipo local
En el repositorio en la web de github
- Clic en el desplegable verde "<> Code"
- Copiar la URL del repositorio bajo la pestaña HTTPS

En la carpeta donde vamos a almacenar el repositorio en nuestro PC y con Git instalado:
- Abrir el terminal de Git con boton derecho del raton --> Git Bash Here
- Ejecutar el comando git clone {URL_REPOSITORIO} . Ejemplo: git clone https://github.com/Machacas-ATV/proyecto_prueba.git
- Ejecutar el comando exit para cerrar la terminal de Git

# Crear una rama para desarrollar
Estando en la rama main:
- Traer los cambios de la rama main desde la nube: git pull origin main
- Crear la rama de desarrollo y moverse a ella: git checkout -b nombreproyecto_X

# Subir cambios a la rama de desarrollo
Al terminar de desarrollar en la rama nombreproyecto_X, estando en ella hacemos:
- Anadir todos los archivos deseados con cambios al staging area:
  git add . (para anadir todos los archivos con cambios)
  git add nombrearchivo.extension (para anadir solo los archivos deseados)
- (OPCIONAL) Sacar los archivos del staging area:
  git restore --staged . (para sacar todos los archivos)
  git restore --staged nombrearchivo.extension (para sacar solo los archivos deseados)
- Traer los cambios de la rama nombreproyecto_X: git pull origin nombreproyecto_X
- Realizar el commit en la rama nombreproyecto_X: git commit -m "mensaje"
- Subir los cambios a la rama nombreproyecto_X: git push

# Mergear cambios de la rama desarrollo a la rama principal
- Cambiar a la rama main: git checkout main
- Traer los cambios de la rama main desde la nube: git pull origin main
- Traer los cambio de la rama de desarrollo a la rama main: git merge nombreproyecto_X
- Subir los cambios a la rama main: git push

# Para finalizar, borramos la rama de desarrollo
- Borrar la rama de desarrollo en local: git branch -d nombreproyecto_X
- Borrar la rama de desarrollo en la nube: git push origin :nombreproyecto_X
