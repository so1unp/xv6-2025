# Guía de Instalación de QEMU

Esta guía describe la instalación de QEMU en Linux y la configuración necesaria para ejecutar xv6, un sistema operativo educativo basado en Unix.

## 1. Dependencias (opcional)
Antes de instalar QEMU, es recomendable actualizar los paquetes del sistema.

Si utilizas una distro basada en Debian (por ejemplo, Ubuntu):
```bash
sudo apt update && sudo apt upgrade -y  # Para distribuciones basadas en Debian
```

Si tienes una distro basada en Fedora:
```bash
sudo dnf update -y                      # Para distribuciones basadas en Fedora
```

## 2. Instalar QEMU
Para distribuciones basadas en Debian (Ubuntu, Debian):
```bash
sudo apt install -y qemu qemu-system-x86
```
Para distribuciones basadas en Red Hat (Fedora, CentOS):
```bash
sudo dnf install -y qemu qemu-system-x86
```
Para Arch Linux:
```bash
sudo pacman -S qemu
```

## 3. Probar la instalación de QEMU
Una vez instalado QEMU, verificaremos su funcionamiento ejecutando una máquina virtual con arquitectura x86 clásica.

### Modo Gráfico
Ejecuta el siguiente comando para iniciar QEMU con una simple BIOS en modo gráfico:
```sh
qemu-system-i386
```

Debe aparecer una nueva ventana en donde, luego de presentar el inicio de ejecución de una máquina virtual, aparece el mensaje `No booteable device` o similar.

Para cerrar la ventana se puede presionar `Ctrl+Alt+q`.

### Modo No Gráfico (--nographics)
Para ejecutar QEMU en modo no gráfico, usar el siguiente comando:
```sh
qemu-system-i386 --nographic
```
QEMU iniciará sin interfaz gráfica y mostrará la salida en la terminal.

Para salir de este modo, presiona `Ctrl+a x`.

