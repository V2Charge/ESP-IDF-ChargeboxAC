# ESP-IDF-ChargeboxAC

Repositorio con ESP-IDF versión 5.5.2 modificado para V2C Controlbox AC

## Requisitos previos

### Acceso de lectura y escritura al puerto serie a través de USB

```bash
sudo usermod -a -G dialout $USER
```

> **Nota:** Después de ejecutar este comando, es necesario cerrar sesión y volver a iniciarla para que los cambios surtan efecto.

## Pasos de instalación

### Paso 1: Instalar dependencias

```bash
sudo apt-get install git wget flex bison gperf python3 python3-pip python3-venv python3-setuptools cmake ninja-build ccache libffi-dev libssl-dev dfu-util libusb-1.0-0
```

### Paso 2: Clonar el repositorio

```bash
git clone --recursive https://github.com/V2Charge/ESP-IDF-ChargeboxAC.git
cd ESP-IDF-ChargeboxAC
```

### Paso 3: Instalar ESP-IDF

```bash
cd esp-idf
./install.sh
```

### Paso 4: Configurar variables de entorno

Ejecutar cada vez que se abra una nueva terminal:

```bash
. ./esp-idf/export.sh
```

O añadir un alias al archivo `~/.bashrc`:

```bash
alias get_idf='. $HOME/ESP-IDF-ChargeboxAC/esp-idf/export.sh'
```

## Uso

Una vez configurado el entorno, puedes compilar y flashear proyectos:

```bash
idf.py set-target esp32
idf.py build
idf.py -p /dev/ttyUSB0 flash monitor
```

## Estructura del repositorio

- `esp-idf/` - ESP-IDF v5.5.2 modificado para V2C
- `iot-middleware-freertos/` - Middleware IoT para Azure

## Licencia

V2C
