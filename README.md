# pokemon-anil

Scripts para Linux:

Descargar partida descargar_partida.sh:

#!/bin/bash

# Variables de configuración
REPO_URL="https://github.com/usuario/repo.git"
LOCAL_DIR="/ruta/a/la/carpeta/local"
BRANCH="main"

# Borrar la carpeta local
rm -rf $LOCAL_DIR

# Clonar la última versión del repositorio
git clone --branch $BRANCH $REPO_URL $LOCAL_DIR

--------------------------------------------------------------------------

Guardar partida (guardar_partida.sh):

#!/bin/bash

# Variables de configuración
REPO_URL="https://github.com/usuario/repo.git"
LOCAL_DIR="/ruta/a/la/carpeta/local"
BRANCH="main"

# Acceder a la carpeta local
cd $LOCAL_DIR

# Asegurarse de que se han guardado los cambios
git add .
git commit -m "Actualizar carpeta"

# Subir los cambios al repositorio
git push --set-upstream $REPO_URL $BRANCH

# Borrar la carpeta actual en GitHub
git rm -r --cached .
git commit -m "Borrar carpeta actual en GitHub"
git push

--------------------------------------------------------------------------
--------------------------------------------------------------------------

Para Windows:

Descargar partida(descargar_partida.bat):

@echo off

:: Variables de configuración
set REPO_URL=https://github.com/usuario/repo.git
set LOCAL_DIR=C:\ruta\a\la\carpeta\local
set BRANCH=main

:: Borrar la carpeta local
rmdir /s /q %LOCAL_DIR%

:: Clonar la última versión del repositorio
git clone --branch %BRANCH% %REPO_URL% %LOCAL_DIR%

--------------------------------------------------------------------------

Guardar partida(guardar_partida.bat):

@echo off

:: Variables de configuración
set REPO_URL=https://github.com/usuario/repo.git
set LOCAL_DIR=C:\ruta\a\la\carpeta\local
set BRANCH=main

:: Acceder a la carpeta local
cd %LOCAL_DIR%

:: Asegurarse de que se han guardado los cambios
git add .
git commit -m "Actualizar carpeta"

:: Subir los cambios al repositorio
git push --set-upstream %REPO_URL% %BRANCH%

:: Borrar la carpeta actual en GitHub
git rm -r --cached .
git commit -m "Borrar carpeta actual en GitHub"
git push
