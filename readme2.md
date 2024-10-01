En este archivo de pondre solo los comandos utilizados, la capturas las enviare por esemtia.
Facendo uso de VScode, Docker e a imaxe de ubuntu da práctica anterior, describe no arquivo readme.md, cun formato claro, os pasos e comandos para:
1. Descargar e comprobar que unha imaxe está no teu equipo

(docker pull ubuntu)
(docker images)

2. Crear un contenedor sen nome, queda arrincado?, cómo obtés o nome?

(docker run -d ubuntu)
(docker ps -a)

3. Crea un contenedor coo nome 'u1', cómo accedes a el?

(docker run -dit --name u1 ubuntu)
(docker exec -it u1 bash)

4. Comproba a súa ip e fai ping a google.com

(docker inspect u1 | grep "IPAddress")

5. Crea un contenedor coo nome 'bono', pódes facer ping entre os contenedores?

(docker run -dit --name bono ubuntu)

6. Se pechas as terminales, qué pasa coo contenedor?
Los contenedores seguirán en ejecución si fueron iniciados con -d (en segundo plano).
7. Cánta memoria no disco duro ocupaches? usa docker para calculalo

(docker system df)

8. Cánta RAM ocupan os contenedores? Crea varios para calculalo

(docker stats)

9. Cómo fixeches para clonar o repositorio
Para clonar o repositorio use o comando git clone https://github.com/O luis/Tarea-1.git na terminal
10. Cómo engades o arquivo readme2.md
Para añadir el archivo use git add readme2.md
11. Os pasos a seguir para subir o arquivo que estás editando e o arquivo readme2.md
Verifique el estado del repositorio con git status, añadi los archivos con el comando git add readme2.md, use el comando git commit -m "Hola gente"(Un commit es como un "snapshot), y por ultimo para subir el archivo use git push origin (nombre de la rama que estoy usando), 

12. Cómo comprobarías que existen diferencias entre o teu repositorio local e o remote.
Primero, necesitas obtener la información más reciente del repositorio remoto con el comando git fetch origin, Después de hacer el fetch, puedes usar el siguiente comando para ver las diferencias entre tu rama local (por ejemplo, main) y la rama remota git diff origin/main, 


Entrega a tarefa enviando na resposta a dirección do teu repositorio coas respostas.

En lo personal no me dejo usar el comando ping en los contenedores (debido a que porque la herramienta ping no está instalada en la imagen de Ubuntu que estaba usando), asique busque en chat gpt, e instale “el comando”. Lo hize usadno los comandos:
apt-get update
apt-get install -y iputils-ping

