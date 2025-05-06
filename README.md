## 🐳 docker_app: Aprendiendo Docker desde Cero
Este proyecto es mi espacio de práctica para aprender Docker desde lo más básico. Incluye una pequeña aplicación en Flask, un Dockerfile, un docker-compose.yml y un resumen de los comandos más utilizados que fui recopilando mientras exploraba.

## 📦 ¿Qué contiene este repositorio?
app.py: una aplicación sencilla en Flask para probar la creación de imágenes y contenedores.

Dockerfile: define cómo construir la imagen de la aplicación.

docker-compose.yml: facilita el levantamiento de servicios con un solo comando.

requirements.txt: lista de dependencias necesarias para la aplicación.

README.md: este archivo, con notas y comandos útiles que fui recopilando.

## 🛠️ Comandos útiles de Docker
Aca algunos comandos que fui utilizando:

```
docker run imagen               # Ejecuta un contenedor desde una imagen
docker run -d imagen            # Ejecuta en segundo plano
docker run -p 5000:5000 imagen  # Mapea puertos (host:contenedor)
docker ps                       # Lista contenedores activos
docker ps -a                    # Lista todos los contenedores
docker stop contenedor          # Detiene un contenedor
docker start contenedor         # Inicia un contenedor detenido
docker rm contenedor            # Elimina un contenedor
docker images                   # Lista imágenes locales
docker rmi imagen               # Elimina una imagen
docker pull imagen              # Descarga una imagen desde Docker Hub
docker exec -it cont bash       # Accede al contenedor con bash
docker logs contenedor          # Muestra los logs del contenedor
docker build -t nombre .        # Crea una imagen desde un Dockerfile
docker-compose up -d            # Levanta servicios definidos en docker-compose
```


## 🚀 ¿Cómo probar la aplicación?
Clona el repositorio:

```
git clone https://github.com/devenzo35/docker_app.git
cd docker_app
```
Construye la imagen:

```
docker build -t mi_app .
```
Ejecuta el contenedor:

```
docker run -p 5000:5000 mi_app
```

Abre tu navegador en http://localhost:5000 para ver la aplicación en funcionamiento.

📬 Contacto
Si tenés dudas o querés compartir ideas sobre Docker o desarrollo en general:

GitHub: @devenzo35

Email: enzocuellar12@gmail.com

