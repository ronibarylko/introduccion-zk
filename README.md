# introduccion-zk

## Créditos
Estos ejercicios están basados en los [zk adventures](https://github.com/eryxcoop/zk-adventures/) que desarollé siendo parte de [Eryx](https://github.com/eryxcoop).

## Como usar

### Jupyter Notebook
First time:
use `pwd` to get the global path to this repo and replace it in the command below.
```bash
docker run -v /global/path/to/this/repo:/home/sage/zk-intro --name sage-intro-zk -p 8888:8888 sagemath/sagemath:latest sage-jupyter
```
Check out URL of the logs to navigate to the sage notebook: `http://127.0.0.1:8888/?token=some-random-token`

If you already ran the above you can open it back with

```bash
docker start sage
```

To recover the URL you can use (you may need to wait a bit after the command above)
```bash
docker logs sage
```

If you are having permission issues, you may try. 
`chmod -R a+w /path/to/introduccion-zk/exercises`
There may be cleaner alternatives to give write permissions to the container.


### Vs Code
Para usar vscode, abrir el repo adentro del container.
En la terminal correr
```bash
sage --notebook
```
Copiar la url que va a tener la forma de 
```
http://127.0.0.1:8888/tree?token=abc123token
```
Abrir uno de los notebooks, clickear en la parte de arriba a la derecha `kernel` > `change kernel` > `add new kernel` > `existing jupyter server` > pegar la url > `Ok`
