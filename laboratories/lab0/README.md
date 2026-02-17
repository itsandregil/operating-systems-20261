# Solución Reto #1

1. Usando la terminal shell crear un directorio en la ruta `~/operating-systems-20261/laboratories/lab0`.

```bash
mkdir -p laboratories/lab0
```

2. Navegar hasta el directorio recién creado.

```bash
cd laboratories/lab0
```

3. Imprimir la ruta absoluta del directorio y luego enviarla al archivo `~/operating-systems-20261/laboratories/lab0/path.txt`.

```bash
pwd > path.txt
```

4. Con un solo comando crear los directorios:
   - `example`
   - `music`
   - `photos`
   - `projects`

```bash
mkdir example music photos projects
```

5. Con un solo comando crear los archivos `<<ruta_de_directorio>>/file{1,2,3…,100}` (es decir, cada carpeta recién creada debe tener 100 archivos con los nombres `file1`, `file2`, …, `file100`).

```bash
for DIR in example music photos projects
do
touch ${DIR}/file{1..100}.txt
done
```

6. Por cada uno de los directorios, borrar los primeros 10 archivos y los últimos 20.

```bash
for DIR in example music photos projects
do
touch ${DIR}/file{1..100}.txt
done
```

7. A la carpeta `projects` mover los directorios: `example`, `music` y `photos`.

```bash
mv example music photos projects/
```

8. Los archivos (no los directorios) de la carpeta `projects` deben ser eliminados con la opción verbosa y enviar el resultado a `~/operating-systems-20261/laboratories/lab0/output.txt`.

```bash
rm -v file*.txt > output.txt
```
