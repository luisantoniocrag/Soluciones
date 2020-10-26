## Eliminar todas las ramas con git bash, menos una (Ejemplo master)

Primero asegura de tener los permisos adecuados y configurar guardar tus credenciales
`$ git config credential.helper store`

y configurar tus usuarios correctamente.

https://github.com/luisantoniocrag/Soluciones/blob/main/git/viejo-nombre-usuario.md

Con este comando puedes eliminar todas las ramas menos una.

```
git branch -r | grep 'origin' | grep -v 'rama-que-no-quieres-eliminar$' | grep -v HEAD | cut -d/ -f2- | while read line; do git push origin :heads/$line; done;
```

Ejemplo:
```
git branch -r | grep 'origin' | grep -v master$ | grep -v HEAD | cut -d/ -f2- | while read line; do git push origin :heads/$line; done;
```
