# COMANDOS ISO

`ping` → Es una herramienta de red usada para comprobar si un dispositivo es alcanzable en una red y medir el tiempo de respuesta.

---

# LINUX

`uname -a` → Nos muestra **información completa sobre el sistema operativo y el kernel**. `uname` significa *Unix Name* y la opción `-a` significa *all* (todo).

---

`dmesg` → El comando `dmesg` en sistemas Linux muestra los **mensajes del buffer del kernel.** Es necesario ejecutarlo con `sudo`.

---

---

`ip a` → Significa “IP adress” y sirve para mostrar las interfaces de red y sus direcciones IP.

---

`df -h` → Ver espacio en disco

---

`fdisk -l` → Información detallada sobre particiones

---

`man hier` → Muestra la página del manual que describe el estándar de jerarquía del sistema de archivos (FHS). `hier` viene de **hierarchy (jerarquía)** y describe directorios como:

- `/bin` → comandos básicos del sistema
- `/etc` → archivos de configuración
- `/home` → carpetas de usuarios
- `/var` → archivos variables (logs, colas, etc.)
- `/usr` → programas y recursos del sistema

---

`ls -l` → Lista archivos y carpetas en formato detallado.

---

#### Volúmenes lógicos y particiones

- `lsblk`→ Muestra los discos y particiones conectados al sistema. Se usa para identificar el disco donde vamos a trabajar.
- `fdisk`→ Herramienta para crear, eliminar o modificar particiones en un disco.
- `pvcreate`→ Inicializa una partición o disco como **volumen físico (PV)** para poder usarlo con LVM.
- `pvs`→ Muestra información sobre los **volúmenes físicos** existentes.
- `vgcreate`→ Crea un **grupo de volúmenes (VG)** uniendo uno o varios volúmenes físicos.
- `vgs`→ Muestra información sobre los **grupos de volúmenes**.
- `lvcreate`→ Crea un **volumen lógico (LV)** dentro de un grupo de volúmenes.
- `lvs`→ Muestra información sobre los **volúmenes lógicos**.
- `mkfs.ext4`→ Crea un sistema de archivos **ext4** en una partición o volumen lógico. Formato
- `mount`→ Monta un sistema de archivos para que el sistema operativo pueda acceder a él.

---

`mdadm` → Es la utilidad estándar de Linux para administrar arreglos RAID por software mediante el subsistema mdadm.

`apt update` → sirve para actualizar la lista de paquetes disponibles desde los repositorios. Se usa en distribuciones basadas en Debian.

`apt upgrade` → Instala las actualizaciones

---

`apt install ufw` → Instala el firewall

`ufw enable` → Activa el **firewall**.

`ufw status` → Comprueba el estado del firewall

`ufw disable` → desactiva el firewall

---

#### Monitorización

`top` → Herramienta de monitorización en tiempo real que muestra los procesos activos y el uso de recursos del sistema en distribuciones basadas en Linux.

`htop` → Herramienta interactiva y mejorada para monitorizar procesos en sistemas basados en Linux. Es una alternativa más visual y fácil de usar que top.

`btop` → Herramienta moderna de monitorización de recursos en sistemas basados en Linux. Es la evolución de bashtop y bpytop, con una interfaz mucho más visual, fluida y completa.

`glances` → Herramienta avanzada de monitorización integral para sistemas basados en Linux. A diferencia de top, htop o btop, muestra muchísima información en una sola pantalla y puede funcionar incluso en modo cliente-servidor para monitorizar equipos remotos.

`free` → Muestra información sobre el uso de memoria RAM y swap.

**grafana** → Es una **plataforma** de visualización y monitoreo usada para mostrar métricas, logs y datos en tiempo real mediante dashboards.

`journalctl` → En systemd se utiliza para ver y consultar los registros (logs) del sistema almacenados por `systemd-journald`, permitiendo filtrar eventos por servicio, fecha, usuario, prioridad o arranque del sistema.

---

`ss -tulnp` → Muestra los puertos y conexiones de red activas del sistema, incluyendo sockets TCP y UDP en escucha, junto con el proceso y PID asociado a cada puerto.

---

#### Gestión de hardware

`lscpu` → Información sobre la cpu

`lshw` → Información sobre el hardware

`ps` → Información sobre los procesos en ejecución

`ps aux` → Procesos de todos los usuarios, procesos sin terminar y la información detallada

`sar -u 1 5` → Muestra el uso de CPU del sistema cada 1 segundo durante 5 intervalos, indicando porcentajes de uso en usuario, sistema, espera (`iowait`) e inactividad (`idle`).

---

`cut` → Sirve para extraer partes específicas de texto de archivos o salidas de comandos.

`awk` → Sirve para procesar y analizar texto por columnas y patrones.

`cat` → Sirve para mostrar, unir y crear archivos de texto.

`grep` → Busca y/o filtra texto dentro de archivos o en la salida de otros comandos.

---

`cp -r /home/usuario/Documentos /media/usuario/backup_docs` → Copia de forma recursiva la carpeta `Documentos` y todo su contenido (subdirectorios y archivos) desde `/home/usuario/` hacia `/media/usuario/backup_docs`.

---

#### Permisos y usuarios

`chmod` → cambia los **permisos** de acceso (lectura, escritura y ejecución) de archivos o carpetas.

| Número | Permiso | Significado |
| --- | --- | --- |
| 0 | `---` | Sin permisos |
| 1 | `--x` | Ejecutar |
| 2 | `-w-` | Escribir |
| 3 | `-wx` | Escribir + ejecutar |
| 4 | `r--` | Leer |
| 5 | `r-x` | Leer + ejecutar |
| 6 | `rw-` | Leer + escribir |
| 7 | `rwx` | Leer + escribir + ejecutar |

`chown` → cambia el **propietario** de un archivo o directorio.

`chgrp` → cambia el **grupo** asociado a un archivo o directorio.

| Letra | Significado | Valor |
| --- | --- | --- |
| `r` | Lectura (read) | 4 |
| `w` | Escritura (write) | 2 |
| `x` | Ejecución (execute) | 1 |
| `-` | Sin permiso | 0 |
- `rwx` → propietario
- `r-x` → grupo
- `r--` → otros

---

---

---

# WINDOWS

`ipconfig /all` → ver/configurar información completa sobre la red.

---

`mbr2gpt` → Es una herramienta incluida en Windows 10/11 y Windows Server para convertir discos MBR (Master Boot Record) a GPT (GUID Partition Table). 

- `/validate` → comprueba la compatibilidad, NO convierte el disco.
- `/convert` → lo convierte.

---

`diskmgmt.msc` → Abre la herramienta de **Administración de discos en Microsoft Windows**.

---

`Get-FileHash` → Es un comando de PowerShell usado para **calcular el hash de un archivo.**

**Algoritmos hash comunes:**

- MD5 (obsoleto, inseguro)
- SHA-1 (obsoleto)
- SHA-256 / SHA-512 (seguros y recomendados)
- bcrypt, scrypt, Argon2 (especiales para contraseñas)

---

`GetProcess`→ En PowerShell, permite ver los procesos en ejecución

---

`GetCounter -ListSet *` → En PowerShell, `GetCounter`sirve para consultar métricas de rendimiento del sistema. `-ListSet *` muestra **todos los conjuntos de contadores de rendimiento** disponibles en Microsoft Windows.

---

#### Registro y análisis de sucesos

`Get-WinEvent` → es un comando de PowerShell usado para leer eventos y logs de Microsoft Windows.

- `Get-WinEvent -LogName system` → Obtiene los eventos del registro **Sistema**.
- `|` → Pipe → Envía el resultado al siguiente comando.
- `where { }` → Filtra los eventos según una condición.
- `$_` → Representa cada evento individual.
- `eq "Error"` → Filtra eventos de nivel **Error**.
- `or` → Operador lógico **O**.
- `eq "Crítico"` → Filtra eventos de nivel **Crítico**.
- `and` → Operador lógico **Y**.
- `ge (get-date).AddHours(-24)` → Muestra solo eventos de las **últimas 24 horas**.
- `get-date` → Fecha actual
- `.AddHours(-24)` → Resta 24 horas
- `ge` → Mayor o igual que

#### Ejemplos de eventos importantes

| ID | Significado |
| --- | --- |
| 4624 | Inicio de sesión exitoso |
| 4625 | Login fallido |
| 6005 | Inicio del Event Log |
| 6006 | Apagado del sistema |

---

`Copy-Item -Path 'C:\Users\Usuario\Documentos' -Destination 'D:\Backup\Documentos' -Recurse -Force` → (PowerShell) copia toda la carpeta `Documentos` y su contenido (incluyendo subcarpetas, archivos ocultos y de sistema) desde `C:\Users\Usuario\Documentos` hacia `D:\Backup\Documentos`, sobrescribiendo archivos existentes si es necesario gracias a `-Force`.

---

`Compress-Archive` → Se utiliza para comprimir archivos y carpetas en un archivo `.zip` desde PowerShell.

---

`Select-Object` → Se utiliza para seleccionar propiedades específicas de objetos o limitar la cantidad de resultados mostrados en la salida de un comando.

---

`Get-Service` → Muestra la lista de servicios del sistema Windows, incluyendo información como nombre, estado (Running/Stopped) y tipo de servicio.

---

`Sort-Object CPU -Descending` → Ordena objetos según el valor de la propiedad `CPU` de mayor a menor, normalmente para mostrar primero los procesos que más CPU consumen.

---

`Test-Connection` → Se utiliza para comprobar la conectividad de red hacia un equipo o dirección IP, funcionando de forma similar al comando `ping`.

---

`Get-NetTCPConnection` → Muestra las conexiones TCP activas del sistema, incluyendo direcciones IP locales/remotas, puertos, estado de la conexión y proceso asociado.

---

`Get-NetAdapter` → Muestra los adaptadores de red del sistema Windows, incluyendo nombre, estado, velocidad, dirección MAC y tipo de interfaz de red.

---