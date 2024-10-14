<h1>En este archivo de pondre solo los comandos utilizados, la capturas las enviare por esemtia.
Facendo uso de VScode, Docker e a imaxe de ubuntu da práctica anterior, describe no arquivo readme.md, cun formato claro, os pasos e comandos para:</h1>
<h2>1. Descargar e comprobar que unha imaxe está no teu equipo</h2>

(docker pull ubuntu)
(docker images)

<h2>2. Crear un contenedor sen nome, queda arrincado?, cómo obtés o nome?</h2>

(docker run -d ubuntu)
(docker ps -a)

<h2>3. Crea un contenedor coo nome 'u1', cómo accedes a el?</h2>

(docker run -dit --name u1 ubuntu)
(docker exec -it u1 bash)

<h2>4. Comproba a súa ip e fai ping a google.com</h2>

(docker inspect u1 | grep "IPAddress")

<h2>5. Crea un contenedor coo nome 'bono', pódes facer ping entre os contenedores?</h2>

(docker run -dit --name bono ubuntu)

<h2>6. Se pechas as terminales, qué pasa coo contenedor?</h2>

Los contenedores seguirán en ejecución si fueron iniciados con -d (en segundo plano).

<h2>7. Cánta memoria no disco duro ocupaches? usa docker para calculalo</h2>

(docker system df)

<h2>8. Cánta RAM ocupan os contenedores? Crea varios para calculalo</h2>

(docker stats)

<h2>9. Cómo fixeches para clonar o repositorio</h2>

Para clonar o repositorio use o comando git clone https://github.com/O luis/Tarea-1.git na terminal

<h2>10. Cómo engades o arquivo readme2.md</h2>

Para añadir el archivo use git add readme2.md

<h2>11. Os pasos a seguir para subir o arquivo que estás editando e o arquivo readme2.md</h2>

Verifique el estado del repositorio con git status, añadi los archivos con el comando git add readme2.md, use el comando git commit -m "Hola gente"(Un commit es como un "snapshot), y por ultimo para subir el archivo use git push  (nombre de la rama que estoy usando), 

<h2>12. Cómo comprobarías que existen diferencias entre o teu repositorio local e o remote.</h2>

Primero, necesitas obtener la información más reciente del repositorio remoto con el comando git fetch origin, Después de hacer el fetch, puedes usar el siguiente comando para ver las diferencias entre tu rama local (por ejemplo, main) y la rama remota git diff origin/main, 


Entrega a tarefa enviando na resposta a dirección do teu repositorio coas respostas.

En lo personal no me dejo usar el comando ping en los contenedores (debido a que porque la herramienta ping no está instalada en la imagen de Ubuntu que estaba usando), asique busque en chat gpt, e instale “el comando”. Lo hize usadno los comandos:
apt-get update
apt-get install -y iputils-ping

