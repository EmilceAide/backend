# GitFlow GROUP

Es importante asegurarse de que todas las ramas estén actualizadas con la última versión de master antes de comenzar a trabajar en ellas y también de realizar pruebas y revisiones antes de fusionar las ramas en master para asegurarse de que todo funciona correctamente. Además, es recomendable utilizar un flujo de trabajo de ramificación adecuado, como Gitflow, para mantener un control adecuado del flujo de trabajo del repositorio.


Puede hacerse manualmente o utilizando alguna herramienta como GitKraken o Sourcetree, que facilitan la implementación de GitFlow.

1. Crear una rama develop a partir de master:

```bash
git checkout -b develop master
git push -u origin develop
```
Esta rama se utilizará para integrar las características y solucionar los problemas antes de incorporarlos a la rama principal.

2. Crear una rama de característica a partir de develop para desarrollar una nueva función o característica:

```bash
git checkout -b feature/nombre-de-la-caracteristica develop
```
Esta rama se utilizará para desarrollar la característica de forma aislada del resto del código.

3. Desarrollar y probar la característica en la rama de característica.

Una vez que se ha completado la característica, fusionarla en la rama develop:

```bash
git checkout develop
git merge --no-ff feature/nombre-de-la-caracteristica
git push origin develop
```
4. Crear una rama de lanzamiento a partir de develop para preparar la versión para su lanzamiento:

```bash
git checkout -b release/nombre-de-la-version develop
```
En esta rama se pueden realizar pruebas finales y correcciones antes de la liberación.

5. Fusionar la rama de lanzamiento en master y develop y etiquetar la versión:

```bash
git checkout master
git merge --no-ff release/nombre-de-la-version
git tag -a nombre-de-la-version -m "Mensaje del tag"
git push origin master
git checkout develop
git merge --no-ff release/nombre-de-la-version
git push origin develop
```
6. Eliminar la rama de lanzamiento:

```bash
git branch -d release/nombre-de-la-version
git push origin --delete release/nombre-de-la-version
```
7. Crear una rama de corrección a partir de master en caso de encontrar un error en la versión liberada:

```bash
git checkout -b hotfix/nombre-del-error master
```
En esta rama se solucionará el error y se fusionará en master y develop.

8. Fusionar la rama de corrección en master y develop y etiquetar la versión corregida:

```bash
git checkout master
git merge --no-ff hotfix/nombre-del-error
git tag -a nombre-de-la-version-corregida -m "Mensaje del tag"
git push origin master
git checkout develop
git merge --no-ff hotfix/nombre-del-error
git push origin develop
```
9. Eliminar la rama de corrección:
```bash
git branch -d hotfix/nombre-del-error
git push origin --delete hotfix/nombre-del-error
```




# STEPS
1. Invitar colaborador
2. Colaborador acepta invitación
3. Colab. aplica clonar repo con:
```bash
git clone <dir/donde se encuentra el repo>
```
3. Colab. crea su rama:
```bash
git branch colab1
```
4. Colab. se para en su rama:
```bash
git checkout colab1
```
5. Job en nuestro code
6. Aplica:
```bash
git status
```
7. Los pasos para pushear:
```bash
git add .
git commit -m "message commit"
```
8. En esta instancia si queremos podemos volver a agragar cambios al code y repetir los pasos:
```bash
git add .
git commit -m "message new commit"
```
9. Ahora si queremos visualizar los commits realizados aplicamos:
```bash
git log
# o de una vista abreviada
git log --oneline
```
10. Podemos si necesitamos checkear las diferencia entre un commit y otro con:
```bash
git diff <codeCommit1> <codeCommit2> 
```
11. Realizamos status de nuevo a modo de verificar que para los últimos cambios agregados (con el add) se le ha asignado un commit title
```bash
git status
```
## Steps IMPORTANT
12. Ahora nos pasamos a la rama principal nuestra
```bash
git checkout master
# o de haber asignado otra rama como la principal momentanea como develop, ir allí
git checkout develop
```
13. Previo a subir nuestro cambio realizamos una actualización con:
```bash
git pull origin develop
# en nuestro caso seguiremos como nuestra rama principal provisoria con la rama develop
```
14. Ahora debemos combinar lo que trabajamos en nuestra rama con la rama principal (que en nuestro caso es develop)
```bash
git merge colab1 
# Recordar estar parado en la rama que para nosotros es la rama principal y tener actualizados los últimos cambios generales (que vienen de arriba, juju)
```
15. Y finalmente, continuando parados en la rama principal (en nuestro ejemplo la develop)
```bash
git push origin develop
```
## Ahora el otro (u otros) colaborador/es (colab2)
16. Para actualizar los cambios del colab1, debe:
    - Estando en la rama principal
```bash
git checkout develop
```
    - Hacer un pull (una actualización)
```bash
git pull origin develop
```    
## CONFLIC *** Tener en cuenta que, si hacemos los cambios en la misma rama (rama principal) y en un mismo espacio de code
17. Para este caso si colab1 pushea esos cambios y luego intenta pushear el colab2 sin previamente actualizar, va a aparecer un cartel amarillo avisando que no tenemos los últimos cambios. Para ello se aconseja que:
    - colab2 realice
    ```bash
    git pull origin develop
    ```    
    - Devuelve una advertencia, pero igualmente allí, ahora hacemos el push de nuevo:
    ```bash
    git push origin develop
    ```   
    - Ahora nos dará otra advertencia de que no podemos hacer esa actualización, y para ello debemos resolver el conflicto desde el gitHub con la solución paso a paso de conflictos o desde nuestro propio code de la siguiente manera:
        - Detectando los errores (advertencias) y limpiando y dejando lo considerado correcto
        - Ahora solicitamos status
        ```bash
        git status
        ``` 
        - Y reiteramos hacer el add y commit desde nuestra rama colab2
        ```bash
        git add .
        git commit -m "refactor code ..."
        ``` 
        - Nos pasamos a la rama principal
        ```bash
        git checkout develop
        ``` 
        - Y pushear
        ```bash
        git push origin develop
        ``` 

### EXTRA
Para eliminar una rama usamos:
```bash
git branch -D colab1
```
Y nos responderá que esa rama ha sido eliminada
Enjoy!!!

