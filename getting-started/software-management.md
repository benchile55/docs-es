# Gestor de software (programas y paquetes)

**Mabox Linux** es una distribución  **Manjaro** *basada*, y usa los repositorios oficiales de Manjaro Linux (*de la rama estable*) y algunos paquetes propios del repositorio de Mabox.

Mabox Linux, al igual que Manjaro es una distribucion de tipo *rolling-release*, y esto quiere decir que usted tendrá acceso directo a las versiones de programas más actualizados.

El gestor de paquetes y programas es llamado Pamac (también esta disponible el comando de terminal pacman  y también el asistente popular de terminal llamado  yay).

Por defecto en Mabox se ejecuta la miniaplicacion de pamac en la bandeja de sistema, así que usted estara siiempre informado acerca de posibles actualizaciones.

------

## Pamac

![Pamac](../img/pamac.jpg)

Pamac es una herramienta poderosa para administrar sus paquetes y programas por medio de una interfaz visual/gráfica.
Pamac le permite la búsqueda de paquetes y programas (de acuerdo a categorias de grupos, de estado, de su origen de descarga), y puede instalar y quitar fácilmente.

La miniaplicación de Pamac reside en la bandeja de sistema ( en el panel) y le anuncia la disponibilidad de acttualizaciones de paquetes y permite una forma conveniente y simple de actualizar.

Con Pamac  podemos configurar varios aspectos del gestor de programas, por ejemplo:

- ajustar la frecuencia de revisión de las actualizaciones
- seleccionar las descargas del servidor mas veloz y su localizacion geográfica próxima a su país
- ajustar el número de las versiones del paquete que permanecerán guardadas en la disco cache de su  sistema (esto le permite regresar a usar un paquete antiguo en algunos casos, cuando el paquete de la ultima actualizacion no sirve en su  sistema y le causa problemas)
- habilitar el repositorio asistente de linux **AUR** 
*[AUR]: Repositorio de usuario de Arch 

<div class="gal">
    <a href="../../img/pamac_pref1.png" title="Pamac preferences - General"><img src="../../img/pamac_pref1.png" alt="" /></a>
    <a href="../../img/pamac_pref2.png" title="Pamac preferences - Advanced"><img src="../../img/pamac_pref2.png" alt="" /></a>
    <a href="../../img/pamac_pref3.png" title="Pamac preferences - Third party"><img src="../../img/pamac_pref3.png" alt="" /></a>
    </div>
---

## Línea de comando - yay

**Yay** es un reemplazo conveniente de pacman porque opera con todos los repositorios de paquetes incluyendo al repositorio de  AUR (Arch User Repository) .

Funciona velozmente desde la terminal  y soporta la mayoría de la sintáxis que usamos con Pacman.


###Actualización del sistema

Para llevar a cabo una actualizacion global de Mabox con yay, simplemente escriba en la terminal y presione la tecla enter:

```
yay
```

Este comando asistente revisará todas las actualizaciones disponibles de todos los  repositorios asi tambien de los paquetes que instaló desde AUR.
Si usted anota  `yay -Syu`  como es habitual de hacer operará  del mismo modo. Lo mismo pasa con `yay -Syyu` (en estecaso para forzar una recarga de todas las bases de datos con los paquetes de sus sistema).


### Instalando paquetes

As an argument we pass the name of the package we want to install. Here, for example, the gdu – pretty fast disk usage analyzer written in Go.
```bash
# search for gdu package
yay gdu
# Yay will search for available packages – both in the repositories and in AUR
# – it will list them and let us choose a package to install.

# install gdu immadietely
yay -S gdu

# install multiple packages
yay -S gimp blender inkscape
```
### Removing packages
To remove a package as with yay, use the -R option. For example:
```
yay -R gdu
```

### Yay statistics
You can also use yay to show some interesting statistics about installed packages.
```
yay -Ps
```
For more info about yay usage:
```
man yay
```

---
