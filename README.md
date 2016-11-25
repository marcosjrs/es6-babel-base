Crear una carpeta llamada es6-tutorial, y dentro de ella dos carpetas mas, una llamada src para archivos fuente y otra llamada build donde Babel colocara los archivos compilados
Para crear un package.json con nuestra información (que nos irá pidiendo), ejecutamos:

npm init

Para instalar la interfaz de consola de  (cli) y un conjunto de configuraciones preestablecidas (preset) con las características mas utilizadas de ES6/2015, ejecutamos:

npm install --save-dev babel-cli babel-preset-es2015

A continuación crearemos un archivo .babelrc, donde indicaremos que presets utilizaremos en nuestra configuracion. Que será el babel-preset-es2015 instalado anteriormente.

echo '{ "presets": ["es2015"] }' > .babelrc

En la sección "scripts" del archivo package.json, añadiremos una línea de código para que indicar como debe compilar con npm.

 "build": "babel src -d build"

Ya podemos probar ES6, por ejemplo dentro de src podemos crear un archivo app.js con el siguiente código:

const sum = (a, b) => a+b;


Tras guardarlo podemos ejecutarlo mediante:

npm run build



Acto seguido tendremos un app.js dentro de nuestra carpeta build.

