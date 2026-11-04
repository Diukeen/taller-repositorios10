¡Perfecto! Entonces el parcial va a ser parecido al ejercicio que hicieron en clase. Te conviene practicar con tu compañero el mismo recorrido, pero agregando desde el principio la configuración de identidad de Git y el inicio de sesión en GitHub.

Hay algo importante para explicarle: Git y GitHub son dos cosas distintas. Configurar el nombre y correo en Git no inicia sesión en GitHub; son pasos separados.

Te dejo una guía ordenada para que puedan practicar juntos.

# Práctica para el parcial – Git y GitHub

## 1. Iniciar sesión y preparar Git

Primero, entrar a GitHub:

1. Abrir [https://github.com](https://github.com?utm_source=chatgpt.com)
2. Presionar Sign in.
3. Ingresar el correo electrónico o nombre de usuario.
4. Ingresar la contraseña.
5. Si solicita un código de verificación, completarlo.

[Lecture 7 - CS50x 2026](https://images.openai.com/static-rsc-4/Fl-ul-kaMAsV-UPjwd6ycJbfJyaKzm4yMWTu2JJvoyBQuYCJkkegQHltuwWwuAjIEaos2QWA-_0KEiGjFNnWtv_2EgtueWtXzEq_UbrUfRwWPy-A4X3GDV1lsrPdHj4VLdNbir_1OzqPfJNrUobipP_3rmYFwbuo7N4fcwxs2EE?purpose=inline)

[cs50.harvard.edu](https://cs50.harvard.edu/x/2026/notes/7/?utm_source=chatgpt.com)

Después, configurar Git en la terminal.

Abrir Git Bash y escribir:

```
git config --global user.name "Tu Nombre"
git config --global user.email "tu-correo@example.com"
```

Reemplazar los ejemplos por los datos propios.

Para comprobar que quedaron guardados:

```
git config --global --list
```

Esto configura la identidad que aparecerá como autora de los commits.

## 2. Clonar el repositorio

Una vez iniciada la sesión, entrar al repositorio que les indique el docente.

1. Presionar Code.
2. Seleccionar HTTPS.
3. Copiar la dirección.

[Top 20 Git-Befehle mit Beispielen: Ein praktischer Leitfaden | DataCamp](https://images.openai.com/static-rsc-4/0OHv2l4o8u9FvXCNZAXoR1TTVJoaBr7AkEjsGaxHDPe_QQMJnJ41Un7_dwg13rHAmjFsiMFNmRygwdZBozKboEoGrLWejMnWljK6EHO7pYRcBv7drWVT0E1NeK2CgNi9eN7IsQ6Xyp8ib_0WtJys7ENS37nXcaUgtF-EkEZpXLE?purpose=inline)

[datacamp.com](https://www.datacamp.com/de/blog/git-commands?utm_source=chatgpt.com)

En Git Bash:

```
git clone URL_DEL_REPOSITORIO
```

Entrar a la carpeta:

```
cd NOMBRE_DEL_REPOSITORIO
```

Si usan VS Code:

```
code .
```

Esto descarga el proyecto a la computadora y lo abre en el editor.

## 3. Crear una rama propia

Primero comprobar que estamos en la rama principal:

```
git status
git branch
```

Actualizar la rama principal:

```
git checkout main
git pull --ff-only origin main
```

Crear nuestra rama:

```
git checkout -b nombre-apellido
```

Por ejemplo:

```
git checkout -b esteban-matlach
```

¿Qué significa? Estamos creando una rama independiente para trabajar sin modificar directamente `main`.

## 4. Modificar un archivo

Abrir el proyecto en VS Code y hacer un cambio sencillo.

Por ejemplo, abrir `index.html` y cambiar el título de la página.

Antes:

```
<h1>Mi tienda</h1>
```

Después:

```
<h1>Mi tienda online</h1>
```

Guardar con `Ctrl + S`.

## 5. Guardar los cambios con Git

Verificar qué modificamos:

```
git status
```

Revisar los cambios:

```
git diff
```

Preparar el archivo:

```
git add index.html
```

Crear el commit:

```
git commit -m "Actualizar titulo de la tienda"
```

Subir la rama a GitHub:

```
git push -u origin esteban-matlach
```

## 6. Crear el Pull Request

Volver a GitHub y entrar al repositorio.

1. Buscar Compare & pull request.
2. Si no aparece, entrar a Pull requests → New pull request.
3. Seleccionar `main` como base.
4. Seleccionar nuestra rama como compare.
5. Escribir un título y una descripción.
6. Presionar Create pull request.

[Submitting your work (GitHub) - BMEVIAUAC16 Data-Driven Software Development Lab](https://images.openai.com/static-rsc-4/c31AjYsFWR7akuUqbIS-Jab2mQsWBPDBOcfvFIQECzAw0pthuEQ-MY_6NVbyZpZCoblNWisTqFo16mfwCGFfKLZIPW52169_jtyzuuDiti0eAfwruZ0FKK4R8jibufKs5A8Hcg4zhH3Y8RUCH62qz_g2m5syKhqYQJdJEE3Dou8?purpose=inline)

[bmeviauac01.github.io](https://bmeviauac01.github.io/datadriven-lab/en/GitHub/?utm_source=chatgpt.com)

Ejemplo de descripción:

- Modifiqué el título de la tienda.
- Comprobé que el cambio se visualice correctamente en el navegador.

## 7. Revisar y fusionar

El compañero entra al Pull Request y revisa:

- Qué archivo se modificó.
- Qué línea se cambió.
- Si el cambio está bien realizado.

Si está correcto, puede aprobarlo con Review changes → Approve → Submit review.

Después, el autor puede seleccionar:

Merge pull request → Confirm merge.

Esto incorpora los cambios a `main`.

## 8. Actualizar la rama principal

Una vez fusionado el Pull Request:

```
git checkout main
git pull --ff-only origin main
```

Así descargamos los cambios que fueron aprobados y fusionados.

## 9. Algo importante: ¿cuándo se inicia sesión desde Git?

Esto puede aparecer durante el parcial.

Hay que diferenciar tres cosas:

| Acción                   | Para qué sirve                  |
| ------------------------ | ------------------------------- |
| Iniciar sesión en GitHub | Acceder a nuestra cuenta.       |
| `git config user.name`   | Configurar el nombre del autor. |
| `git config user.email`  | Configurar el correo del autor. |

Cuando ejecuten `git push`, Git puede solicitar autenticación.

- Si aparece una ventana del navegador, iniciar sesión con la cuenta de GitHub y autorizar el acceso.
- Si solicita credenciales en la terminal, ingresar el usuario de GitHub y utilizar un Personal Access Token (PAT) como contraseña, no la contraseña normal de GitHub.

Importante: clonar un repositorio público no requiere iniciar sesión, pero para subir cambios a un repositorio privado o protegido necesitan autenticarse y tener permisos de escritura.

## 10. Machete para memorizar

El recorrido completo

GITHUB

1. Iniciar sesión.
2. Copiar URL HTTPS.

GIT BASH

```
git config --global user.name "Nombre"
git config --global user.email "correo"

git clone URL
cd carpeta

git checkout main
git pull --ff-only origin main

git checkout -b mi-rama

# Modificar archivo

git status
git add .
git commit -m "Mi cambio"
git push -u origin mi-rama
```

GITHUB

3\. Crear Pull Request.\
4\. Revisar cambios.\
5\. Aprobar.\
6\. Hacer Merge.

GIT BASH

```
git checkout main
git pull --ff-only origin main
```

## 11. Simulacro para tu compañero

Te recomiendo que le des esta consigna sin mostrarle los comandos:

Situación: sos integrante de un equipo que desarrolla una tienda online.

1. Iniciá sesión en GitHub.
2. Configurá tu nombre y correo en Git.
3. Cloná el repositorio que te indique tu compañero.
4. Creá una rama llamada `cambiar-titulo`.
5. Modificá el título de `index.html`.
6. Guardá los cambios.
7. Hacé un commit.
8. Subí tu rama a GitHub.
9. Creá un Pull Request hacia `main`.
10. Explicá qué es un Pull Request y para qué sirve el Merge.

Tres preguntas que sí o sí debería poder responder:

- ¿Por qué trabajamos en una rama y no directamente en `main`?
- ¿Qué diferencia hay entre `commit` y `push`?
- ¿Qué diferencia hay entre Pull Request y Merge?

Mi consejo es que vos hagas de profesor: dejalo ejecutar los pasos solo y preguntale qué hace cada comando. Si puede explicar el recorrido sin mirar la guía, está bastante bien preparado para el parcial.
