# TPI ARQUI - Flask mínimo

App Flask con una sola ruta `/santi` que devuelve "Hola Santi".

## Correr en la VM Ubuntu

```bash
git clone <url-del-repo>
cd TPI-ARQUI
sudo apt update && sudo apt install -y python3-pip python3-venv
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
sudo venv/bin/python main.py
```

La app escucha en el puerto 80 de todas las interfaces (`0.0.0.0`), por eso se necesita `sudo`
(los puertos < 1024 requieren privilegios en Linux).

## Probar desde el SO anfitrión

Con la VM en red puenteada/NAT con IP accesible (por ejemplo `192.168.0.2`):

```
http://192.168.0.2/santi
```

Debería responder: `Hola Santi`
