Práctica de Git y GitHub
1. Iniciar sesión en GitHub
- Entrar a https://github.com.
- Seleccionar Sign in.
- Ingresar correo o nombre de usuario y contraseña.
2. Configurar Git

Abrir Git Bash y ejecutar:
git config --global user.name "Tu Nombre"
git config --global user.email "tu-correo@gmail.com"


3. Clonar el repositorio
git clone URL_DEL_REPOSITORIO
cd NOMBRE_DEL_REPOSITORIO


4. Crear una rama
git checkout main
git pull origin main
git checkout -b nombre-apellido


5. Modificar un archivo

Abrir index.html, realizar un pequeño cambio y guardar.

6. Subir los cambios
git status
git add index.html
git commit -m "Actualizar titulo"
git push -u origin nombre-apellido


7. Crear un Pull Request
- Entrar al repositorio en GitHub.
- Seleccionar Pull requests → New pull request.
- Elegir main como base y tu rama como compare.
- Escribir un título y crear el Pull Request.
8. Revisar y combinar
- Un compañero revisa los cambios en Files changed.
- Si está todo bien, aprueba el Pull Request.
- El autor selecciona Merge pull request y confirma.
9. Actualizar el repositorio local
git checkout main
git pull origin main



Para recordar en el parcial:
- clone: descargar el repositorio.
- branch: crear una rama.
- add: preparar cambios.
- commit: guardar los cambios.
- push: subirlos a GitHub.
- pull: traer cambios.
- Pull Request: solicitar que tus cambios se incorporen a main.
- merge: combinar los cambios.
Importante: iniciar sesión en GitHub permite acceder a la cuenta. git config configura el nombre y correo que aparecen como autor de los commits; no inicia sesión.
