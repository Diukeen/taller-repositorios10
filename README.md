# Práctica de Git y GitHub – Ariadna Krsteff

1\. Iniciar sesión en GitHub

- Entrar a [https://github.com](https://github.com?utm_source=chatgpt.com).
- Seleccionar Sign in.
- Ingresar el correo o nombre de usuario y contraseña.

2\. Configurar Git

```
git config --global user.name "Ariadna Krsteff"
git config --global user.email "CORREO_DE_ARIADNA"
```

3\. Clonar el repositorio

```
git clone URL_DEL_REPOSITORIO
cd NOMBRE_DEL_REPOSITORIO
```

4\. Crear una rama

```
git checkout 
git pull origin 
git checkout -b ariadna-krsteff
```

5\. Modificar un archivo

Abrir `index.html`, realizar un pequeño cambio y guardar.

6\. Subir los cambios

```
git status
git add index.html
git commit -m "Ariadna Krsteff actualiza el titulo"
git push -u origin ariadna-krsteff
```

7\. Crear un Pull Request

- Entrar al repositorio en GitHub.
- Seleccionar Pull requests → New pull request.
- Elegir `main` como base y `ariadna-krsteff` como compare.
- Escribir un título y crear el Pull Request.

8\. Revisar y combinar

- Un compañero revisa los cambios en Files changed.
- Si está todo bien, aprueba el Pull Request.
- Ariadna selecciona Merge pull request y confirma.

9\. Actualizar el repositorio local

```
git checkout main
git pull origin main
```

Para recordar en el parcial:

- `clone`: descargar el repositorio.
- `branch`: crear una rama.
- `add`: preparar cambios.
- `commit`: guardar los cambios.
- `push`: subirlos a GitHub.
- `pull`: traer cambios.
- `Pull Request`: solicitar que tus cambios se incorporen a `main`.
- `merge`: combinar los cambios.

Reemplazar CORREO_DE_ARIADNA por el correo que Ariadna tiene registrado en GitHub.
