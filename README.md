# Tarea-1
Resolución del ejercicio 1.10.3 Plant–Pollinator Networks
Enunciado 1

Pasos: 
 1. creamos un nuevo repositorio de Git en nuestra consola de Git Bash en una nueva carpeta, en mi caso "BioNM"
 2. copiamos el código de nuestro repositorio anteriormente creado en github.com y lo pegamos en nuestra consola usando el comando "git clone"
 3.  retrocedemos un directorio hacia atrás con el comando "c ../" y nos ubicamos en documentos, una vez ahí nos dirigimos hasta Saavedra2013 usando "cd"
         $ cd CSB/nix/data/Saavedra2013
         
 4. Ahora imprimo de manera más específica el contenido que deseo leer, usando el comando cat 
         $ cat ../Saavedra2013/n10.txt |wc -l
         con wc -l estoy indicando que imprima solo la primera fila 
         
 5. Ahora con el comando "head" le indico que imprima las 10 primeras filas 
         head -n 1 ../Saavedra2013/n10.txt | tr -d " " | tr -d "\n" | wc -c
         
 6. Luego con el comando "touch" creo mi archivo netsize.sh 
         $ touch netsize.sh
         
 7. Luego con el comando "nano" me abre un archivo para edición 
        $ nano netsize.sh
 
 8. en esto archivo ubico mi carpeta con cd y le doy las indicaciones con cat y head, guardo los cambios y ejecuto con el comando $ bash netsize.sh
       Tarea - 1
       14
       20
   
  9. Por último guardo mi archivo .sh en .txt usando el comando $ cp netsize.sh netsize.txt

Enunciado 2 
Pasos: 
1. Creo mi archivo usando el comando "touch" 
        $ touch netsize_all.sh
        
2. Ahora abro mi archivo de edición con el comando "nano" 
        $ nano netsize_all.sh
   en esto archivo ubico mi carpeta con cd y le doy las indicaciones con for, do y done para crear un bucle para que se impriman las filas y columas para cada red. Damos la instrucción de que se lean todos los archivos que terminen con .txt señalando con el * al final. con el do específicamos que archivos imprimir y cat para imprimirlo
   
   "Número de filas"
   for N in ../Saavedra2013/*.txt; do cat $N | wc -l; done
   
   "Número de columnas" 
   for M in ../Saavedra2013/*.txt; do head -n 1 $M | tr -d "\n" | wc -c; done

3. Por último guardo mi archivo .sh en .txt usando el comando $ cp netsize_all.sh netsize_all.txt


        
