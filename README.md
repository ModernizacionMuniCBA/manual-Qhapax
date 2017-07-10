# manual-Qhapax
Manual de Qhapax, la plataforma de Gobierno Abierto de la Ciudad Córdoba

Este repositorio guarda la versión renderizada **EN DESARROLLO** de la documentación,
accesible desde https://modernizacionmunicba.github.io/manual-qhapax


## Intrucciones de actualización

Como aun no contamos con un servicio de integración continua al que delegar esta tarea de manera automática,
ni un servicio específico para documentación como *readthedocs* (al que probablemente migremos a futuro),
la actualización de la documentación se realizará de manera manual.

En el repo de qhapax, la carpeta `docs/_build` donde se genera el html (y otros formatos)
está excluida via `.gitignore`, y entonces podemos explicitamente asignar este repositorio como destino
remoto del contenido que nos interesa en `docs/_build/html`. El branch de destino es `gh-pages`
que es el que utiliza


```
cd docs/_build/html
git init
git remote add origin https://github.com/ModernizacionMuniCBA/manual-Qhapax.git
git pull
cd ../../
make html
cd -
git add .
git commit -m 'actulizacion de la doc'
git push origin gh-pages
```


