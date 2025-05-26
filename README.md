# Guía de Uso: Componentes

![Insignia de estado de construcción de Travis CI](https://travis-ci.org/GoogleChrome/howto-components.svg?branch=master)

"Guía de Uso: Componentes" es [una subsección de la sección de Arquitectura de Fundamentos Web](https://developers.google.com/web/fundamentals/web-components/examples/), la cual contiene una recopilación de componentes web que implementan patrones comunes de UI web utilizando tecnologías modernas como Custom Elements v1 y ESnext. Esta sección se enfoca especialmente en accesibilidad, rendimiento y mejora progresiva. El propósito de estos componentes es servir como un recurso educativo. Se espera que los usuarios lean e interpreten sus implementaciones. Cabe aclarar que **NO** son una biblioteca de UI destinada a ser utilizada en producción.

## Demos

Puedes ejecutar las demostraciones localmente, después de haberlas construido:

```
npm install  # si aún no lo has hecho
npm run build
python -m SimpleHTTPServer  # o cualquier servidor local que prefieras
```

En tu navegador, navega a `http://localhost:8000/docs` (o el puerto desde el cual estás ejecutando el servidor local).

También puedes ejecutar,

```
npm run watch
```

para compilar de forma continua cada vez que un archivo cambie.

### FundamentosWeb

Para generar el contenido de [WebFundamentals](https://github.com/Google/WebFundamentals), ejecuta el script `build-webfundamentals.sh`. Este creará una carpeta `webfundamentals`. Su contenido debe ser movido al repositorio de WebFundamentals. Si se han creado nuevos componentes, deben ser añadidos manualmente al [Índice de Contenidos de Componentes Web de WebFundamentals](https://github.com/google/WebFundamentals/blob/master/src/content/en/fundamentals/web-components/_toc.yaml).

## Pruebas

Las pruebas son escritas usando [Mocha](https://mochajs.org/) y [Chai](http://chaijs.com/). Cada componente tiene pruebas.

### Local

Las pruebas se ejecutan usando [Karma](https://karma-runner.github.io/1.0/config/browsers.html). Ejecuta las pruebas con

```
$ npm test
```

Esto asume que Chrome, Firefox y Safari están instalados ya que las pruebas se ejecutan en todos estos navegadores (utilizando el [Polyfill de Custom Elements v1](https://github.com/webcomponents/custom-elements)).

### Local + Docker (o Travis)

Las pruebas también pueden ejecutarse en un contenedor de [Docker](https://www.docker.com/) (tal como lo hacemos en Travis):

```
$ npm run docker
```

Esto construye una imagen de docker `googlechrome/howto-components` y la ejecuta. Las pruebas dockerizadas utilizan solo Chrome.

## Versiones preliminares

Todas las ramas y PRs se construyen y cargan en Travis CI. La versión preliminar puede ser vista en `http://dash-elements.surma.link/<commit hash>`.

## Licencia

Copyright 2017 Google, Inc.

Licenciado a la Apache Software Foundation (ASF) bajo uno o más acuerdos de licencia de colaborador. Consulta el archivo NOTICE distribuido con este trabajo para obtener información adicional sobre la propiedad de derechos de autor. La ASF licencia este archivo bajo la Licencia Apache, Versión 2.0 (la “Licencia”); no puedes utilizar este archivo excepto en cumplimiento de la Licencia. Puedes obtener una copia de la Licencia en

http://www.apache.org/licenses/LICENSE-2.0

A menos que sea requerido por ley aplicable o se acuerde por escrito, el software distribuido bajo la Licencia se distribuye en una base “TAL CUAL”, SIN GARANTÍAS O DECLARACIONES DE NINGÚN TIPO, ya sean expresas o implícitas. Consulta la Licencia para conocer los permisos específicos y las limitaciones bajo la Licencia.

Por favor ten en cuenta: este no es un producto de Google.
