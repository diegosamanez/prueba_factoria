### Repositorios
- Backend
    [https://githubt.com](https://githubt.com).

- Frontend
    [https://githubt.com](https://githubt.com).

### Backend
```
git clone https://githubt.com
```
una vez clonado descargar las dependencias y preparar para hacer build
```
npm i
```
configurar el archivo .env.example en este archivo configuraremos los datos de acceso a nuestra base de datos:
PORT=3333
HOST=0.0.0.0
NODE_ENV=production
APP_KEY=g2pLkancNEgCHLz3uxjYRmfIFok2yVxz
DRIVE_DISK=local
DB_CONNECTION=mysql
MYSQL_HOST=localhost
MYSQL_PORT=3306
MYSQL_USER=lucid
MYSQL_PASSWORD=
MYSQL_DB_NAME=lucid
Vamos a nuestro gestor de base de datos MySql cuyas credenciales pusimos en el archivo .env.example y creamos la base de datos. Ejm "lucid" y ejecutamos el comando:
```
node ace migration:run
```
A continuación:
```
npm run build
```
nos dirigimos a la carpeta ./build y ejecutamos 
```
npm ci --production 
```
finalmente
```
npm start
```
Y ya tenríamos corriendo el backend

### Frontend
```
git clone https://githubt.com
```
una vez clonado descargar las dependencias y preparar para hacer build
```
npm i && npm run build
```
y levantamos el servidor frontend
```
npm run preview
```

### Explicación del Desarrollo
Elegí una arquitectura APIRest, de esa forma separo el frontend del backend como entidades independientes

Para el desarrollo del Backend opté por un clasico MVC con el framework AdonisJS agregando tambien el patron Repository lo que ayudaba a tener mas legible el Modelo que practicamente era un DTO al solo modelar la entidad y no tener en la clase ningun método que tenga que ver con la base de datos, Ademas de ser escalable, legible y acorde con el principio de responsabilidad única, elegí este Framework ya que este y Laravel son los que más he utilizado profesionalmente.

En la parte Frontend utilicé la librería React principalmente para la interaccion con el usuario, ademas de otras bibliotecas como Jest para los test.
Aquí me enfoqué en crear Componentes rendericen fragmentos de código para no repetirlo basicamente, desglozando el código en parte gráfica y context (los archivos tsx) y lógica (los archivos ts) teniendo cada archivo un unico proposito y que se vea de una manera mucho mas simple y facil de entender.