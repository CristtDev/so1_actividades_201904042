# Servicios con systemd 🤖

Este repositorio contiene un archivo de unidad de systemd y un script para ejecutar un servicio que imprime un saludo y la fecha actual en intervalos regulares. De igual manera se implemento un servicio y script para imprimir un texto por en repetidas veces.

## Instalación 💻

1. Clona este repositorio en tu sistema o copia los archivos necesarios.
2. Asegúrate de que tanto el archivo `my-service.service` como `saludo-script.sh` estén en la misma ubicación. De igual manera para los archivos `servicio2.service` como `script-dinamico.sh`
3. Abre el archivo `my-service.service/ervicio2.service` en un editor de texto y modifica la línea `ExecStart` para que apunte a la ubicación completa de `saludo-script.sh/script-dinamico.sh`.
4. Reemplaza `nombre_de_usuario` en la sección `[Service]` con tu nombre de usuario en el sistema.

## Uso 👨🏿‍💻

1. Habilita el servicio para que se inicie en el arranque:

   ```
    sudo systemctl enable my-service.service
   ```

2. Inicia el servicio:

     ```
    sudo systemctl start my-service.service
   ```

3. Verifica el estado del servicio:

     ```
   sudo systemctl status my-service.service
   ```

4. Detén el servicio cuando desees:

     ```
    sudo systemctl stop my-service.service
   ```

5. Si realizas cambios en el archivo de unidad de systemd, no olvides recargar systemd:

     ```
    sudo systemctl daemon-reload
   ```

