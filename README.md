# README #

### Introducción

Implementación de servidor hecho en Py3, utilizando librerías tales cómo:

* threading
* socket
* connection
* errno
* os
* base64
* genericpath
* optparse --> módulo deprecado

### Run

Arrancamos el servidor

```sh

python3 server.py

```

En otra consola, nos conectamos al servidor vía telnet:

```sh

telnet 0.0.0.0 19500

```

Envíamos request y vemos su devolución.

En la carpeta testdata estan los archivos del servidor inicialmente vacia

Request posibles:

- > get_metadata (nombre de archivo dentro de test data) : devuelve los metadatos de un archivo del server 

- > get_slice (nombre de archivo dentro de testdata) inicio offset : devuelve un trozo de un archivo desde el byte inicio hasta offset

- > get_file_listing : devuelve una lista con todos los archivos dentro del servidor

- > quit : se desconecta del servidor

### Futuros Cambios

* Se podría abrir un puerto y hacer que se pueda conectar al servidor via internet.
* Se podría agregar otros comandos para que haya otras funcionalidades.
* Se podría implementar el multithread con asyncio.

### Tests
Arrancamos el servidor

```sh

python3 server.py

```
en otra consola ejecutamos

```sh

python3 server-tests.py

```
### Bibliografía Complementaria ###

* [Socket](https://docs.python.org/es/3/library/socket.html)
* [Threads](https://docs.python.org/es/3.8/library/threading.html#thread-objects)
* [Multithreaded Server Socket Example](http://net-informations.com/python/net/thread.htm)
* [asyncio](https://docs.python.org/3/library/asyncio.html)
* [Tutorial asyncio](https://www.dabeaz.com/tutorials.html)
* [Seek, Read Files](https://docs.python.org/3/tutorial/inputoutput.html)
* [Manejo de Errores](https://docs.python.org/es/3/tutorial/errors.html)
* [Excepciones](https://docs.python.org/es/3.8/library/exceptions.html)
