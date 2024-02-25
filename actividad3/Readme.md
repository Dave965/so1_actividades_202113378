## David Abraham Noriega Zamora
## 202113378
## 24/2/2024

---

* MOVER A CARPETA :
El primer paso es mover el servicio a la carpeta `/etc/systemd/system/`

```bash
sudo mv saludo.service /etc/systemd/system/
```

* RECARGA Y HABILITACIÓN SERVICIO:
esto genera que nuestro archivo sea reconocido y habilita nuestro
servicio

```bash
sudo systemctl daemon-reload
sudo systemctl enable saludo.service
```

* INICIAR SERVICIO:
iniciamos el servicio con el comando systemctl start

```bash
sudo systemctl start saludo.service
```

- VERIFICAR:
el estado del servicio

```bash
sudo systemctl status saludo.service
```