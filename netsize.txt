echo "utilizamos echo para simplemente imprimir alguna para palabra, en este caso un encabezado"
echo "Tarea - 1"

echo "utilizamos cd .. para movernos hacia un directoria atrás"
cd ..

echo  "utilizamos cd y (nombre.del.directorio) a donde nos queremos ubicar"
cd Saavedra2013

echo "Utilizamos cat para imprimir el contenido del directorio objetivo y señalamos especificamente en nuestro caso n10.txt  y usamos wc -l para contar el número de líneas"
cat ../Saavedra2013/n10.txt |wc -l

echo "con -n 1 le damos la insrucción de ver la primera fila, con head le damos la instruccion del número de filas que queremos ver, con tr -d sirve para borrar, en este caso lo usamos para borrar los espacios entre los valores,  además usamos wc -c para contar el número de carácteres" 
head -n 1 ../Saavedra2013/n10.txt | tr -d " " | tr -d "\n" | wc -c


