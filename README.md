# Instalar Proxmox en VirtualBox

Guía paso a paso para la instalación y configuración inicial de Proxmox VE dentro de un entorno virtualizado con VirtualBox.

---

## 🚀 Configuración de la Máquina Virtual

### 1. Configuración inicial
Configuramos la VM asignando la ISO de Proxmox y los recursos de hardware necesarios (Memoria RAM y CPU).

![Paso 1](https://github.com/user-attachments/assets/d7066507-8ea8-41aa-87c6-97a07c280dd9)
![Paso 2](https://github.com/user-attachments/assets/915dc267-9006-48ba-a630-2abcf4efac20)
![Paso 3](https://github.com/user-attachments/assets/5a885355-5717-4c35-b6c2-b26daebd0995)

### 2. Configuración de Red
Usamos el **Adaptador puente** (Bridged Adapter) para que la VM tenga visibilidad directa en la red local y conexión con el host.

![Paso 4](https://github.com/user-attachments/assets/63e1812e-ecc3-4ea8-ac9a-4b2c17f2e629)

### 3. Aceleración y Virtualización Anidada
Es crucial activar **PAE/NX** y **Nested VT-x/AMD-v** para que Proxmox pueda ejecutar contenedores y VMs internas.

![Paso 5](https://github.com/user-attachments/assets/17d3f335-9760-4831-9c77-661a9ee92db1)

> [!TIP]
> **4. Si no puedes activar Nested VT-x/AMD-v desde la interfaz:**
> Abre una terminal en tu host y ejecuta el siguiente comando:
> ```bash
> VBoxManage modifyvm "nombre_de_tu_vm" --nested-hw-virt on
> 
🛠️ Proceso de Instalación de Proxmox
5. Inicio del instalador
Iniciamos la VM y seleccionamos la opción de instalar Proxmox VE.

6. Selección de disco
Elegimos el disco virtual donde se realizará la instalación.

7. Localización y Teclado
Configuramos el país, la zona horaria y la distribución del teclado.

8. Credenciales de Administrador
Establecemos la contraseña para el usuario root y un correo electrónico de contacto.

9. Configuración de Red IP
Asignamos la IP estática, la puerta de enlace y el DNS.

10. Resumen y Confirmación
Verificamos que todos los datos sean correctos antes de proceder.

11. Instalación y Reinicio
Esperamos a que finalice la instalación y reiniciamos la máquina virtual.

🌐 Acceso a la Interfaz Web
12. Obtener URL de acceso
Al iniciar, Proxmox mostrará la URL de administración (normalmente https://tu-ip:8006).

13. Login
Entramos al servidor mediante el navegador. (Ignora la advertencia de certificado SSL ya que es un certificado auto-firmado).

🔧 Configuración de Repositorios (Post-Instalación)
Es común ver un error de "No Subscription" al principio. Vamos a corregirlo para poder actualizar el sistema.

14. Identificar el aviso
15. Gestionar Repositorios
Vamos a PVE -> Repositories.

16. Desactivar repositorios de suscripción
Seleccionamos los repositorios que requieren suscripción paga y hacemos clic en Disable.

17. Añadir repositorio "No-Subscription"
Añadimos el repositorio comunitario gratuito.

18. Actualizar el sistema
Vamos a Updates, pulsamos Refresh y luego Upgrade.
