<h1>Branching and merging</h1>
----
Los siguientes ejercicios los debes realizar en tu máquina real, no es necesario que los subas a un repositorio en github. Indica los pasos seguidos para realizar cada ejercicio en este mismo fichero.

1. Crea un directorio llamado **branch_time**
- mkdir branch_time

2. Cámbiat a dicho directorio.
- cd branch_time

3. Inicializa un repositorio vacío.
- git init

4. Crea un fichero llamado first.txt después añade y haz commit con un solo comando.
- touch first.txt && git add first.txt && git commit -m "Primer fichero"

5. Crea una nueva rama llamada **amazing_feature**.
- git branch amazing_feature

6. Cámbiate a dicha rama.
- git cheackout amazinf_feature

7. Crea un fichero llamado best.txt con el contenido "This is the best file".
- nano best.txt y añadimos "This is the best file", salvamos y salimos. 

8. Añade el fichero al área de preparación.
- git add best.txt

9. Haz commit del fichero con el mensaje "added best.txt".
- git commit -m "added best.txt"

10. Vuelve a la rama master.
- git checkout master

11. Une(merge)la rama feature a la rama master.
- git merge amazing_feature

12. Borra la rama feature.
- git branch -d amazing_feature

13. Crea la rama conflict y cámbiate a ella con un solo comando.
- git checkout -b conflict

14. Crea tu propio conflicto al mezclar dos ramas!Para ello trabaja en el mismo fichero en dos ramas separadas y une(merge)las dos ramas. Arregla los conflictos y finaliza la unión. En el mundo real nunca intentarás crear un conflicto en una unión de ramas, pero es importante que no te sientas intimidado por los conflictos al realizar una unión de ramas y ser capaz de arreglarlos con confianza.
- Creamos el fichero conflicto en la rama conflict: 
    - nano conflicto.txt
- Lo subimos al área de trabajo y realizamos el commit:
    - git add conflicto.txt
    - git commit -m "generando conflicto entre ramas"
- Nos cambiamos de rama a la master
    - git checkout master
- Creamos el fichero conflicto en la rama master:
    - nano conflicto.txt
    - git add conflicto.txt
    - git commit -m "generando conflicto entre ramas"
- Al tratar de unir (merge) las ramas nos salta un conflicto con el fichero.
    - git marge conflict
    - git status para obtener más información
- Para solucionarlo editamos desde la rama master que es la que nos encontramos el fichero conflicto.txt y resolvemos manualmente el conflicto generado anteriormente.
    - nano conflicto.txt (editamos y corregimos)
    - git add conflicto.txt (lo subimos al área de trabajo)
    - git commit -m "conflicto resuelto." (añadimos el commit)
    - git merge conflict (unimos las ramas)
