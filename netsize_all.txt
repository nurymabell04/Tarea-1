echo "Utilizamos echo para imprimir un encabezado"
echo "Segunda parte de la tarea"

echo "nos ubicamos en la carpeta objetivo usando cd .."
cd ..

echo "con cd y nombre de la carpeta donde nos vamos a ubicar"
cd Saavedra2013

echo "En esta parte se imprimira el número de filas y columnas para cada red. Para ello utilizaremos un for y creamos un blucle"
echo "utilizamos el * para seleccionar todos los archivos"

echo "para contar el número de líneas y carácteres  usamos wc -l y -c, respectivamente"
echo "Número de filas" "Aquí tenemos nuestra variable y esta señalada por el signo de $" 
for N in ../Saavedra2013/*.txt; do cat $N | wc -l; done


echo "Número de columnas"
for M in ../Saavedra2013/*.txt; do head -n 1 $M | tr -d "\n" | wc -c; done
