## Git muestra aún el anterior usuario

Descripción:
Al hacer push, o intentar eliminar una rama, niega el servicio y muetra un viejo o anterior usuario registrado.

mensaje:

```
$ git push origin master

remote: Permission to CorrectUsername/CorrectRepo.git denied to OldUsername.
fatal: unable to access 'https://github.com/rogerskev17/KnightQuest/': The requested URL
returned error: 403
```

Estoy en windows, y lo solucioné colocando aparte de git `$ git config user.name "name"`, `$ git config user.email "email"` el comando:

`$ git config credential.username "new_username"
`
