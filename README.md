# Instalar-proxmox-en-VirtualBox
1. Configuramos la VM con la iso y los recursos.
(https://github.com/user-attachments/assets/d7066507-8ea8-41aa-87c6-97a07c280dd9")
<img width="776" height="552" alt="2" src="https://github.com/user-attachments/assets/915dc267-9006-48ba-a630-2abcf4efac20" /&gt;
<img width="779" height="553" alt="3" src="https://github.com/user-attachments/assets/5a885355-5717-4c35-b6c2-b26daebd0995" /&gt;

2. Usamos adaptador puente para poder tener conexión con el host.
<img width="809" height="514" alt="4" src="https://github.com/user-attachments/assets/63e1812e-ecc3-4ea8-ac9a-4b2c17f2e629" /&gt;

3. Activamos PAE/NX y Nested VT-x/AMD-v
<img width="811" height="514" alt="5" src="https://github.com/user-attachments/assets/17d3f335-9760-4831-9c77-661a9ee92db1" /&gt;

4. Si no deja activar Nested VT-x/AMD-v, usar la comanda: BoxManage modifyvm "nombre_de_vm" –nested-hw-virt on
<img width="970" height="508" alt="6" src="https://github.com/user-attachments/assets/0f1cc62d-86e8-4ab9-966f-dc20c09ede89" /&gt;

5. Iniciamos proxmox
<img width="1027" height="770" alt="7" src="https://github.com/user-attachments/assets/46c2d4eb-28cf-423e-8a8f-005a14cbbcf0" /&gt;

6. Seleccionamos el disco donde queremos instalarlo
<img width="1285" height="793" alt="8" src="https://github.com/user-attachments/assets/c4c51ad2-48f5-4e2d-a2f1-05eb3e0f5f7f" /&gt;

7. Seleccionamos, región, zona horaria e idioma del teclado
<img width="1279" height="800" alt="9" src="https://github.com/user-attachments/assets/358cf63a-a2cc-4df0-9407-4f406b0fea72" /&gt;

8. Ponemos contraseña
<img width="1280" height="802" alt="10" src="https://github.com/user-attachments/assets/309432c0-edc0-4a7c-97e6-fbbc420e1e70" /&gt;

9. Configuramos la red
<img width="1275" height="805" alt="11" src="https://github.com/user-attachments/assets/a9551076-d57d-4d24-add7-4284d8648af6" /&gt;

10. Comprobamos que sea todo correcto.
<img width="1277" height="802" alt="12" src="https://github.com/user-attachments/assets/e041e5b1-4239-4870-b0fc-58954bfd5f0d" /&gt;

11. Instalamos
<img width="1279" height="800" alt="13" src="https://github.com/user-attachments/assets/ca1537ac-1912-4ec7-814c-f4260afd66d7" /&gt;

12. Reiniciamos
<img width="1279" height="802" alt="14" src="https://github.com/user-attachments/assets/7a30545a-5e39-4159-a483-bab3c66db842" /&gt;

13. Iniciamos y copiamos la url
<img width="1278" height="799" alt="15" src="https://github.com/user-attachments/assets/73db15ab-8a23-45e2-a34e-e58314579073" /&gt;

14. Entramos al servidor con la url de antes
<img width="3432" height="1341" alt="16" src="https://github.com/user-attachments/assets/4d1ff76d-50ac-4d7b-98ba-7b91bf44b984" /&gt;

15. Al entrar nos saldrá este error
<img width="3438" height="1263" alt="17" src="https://github.com/user-attachments/assets/cfbb006d-995e-456b-a165-c3ec1f597535" /&gt;
<img width="3439" height="203" alt="18" src="https://github.com/user-attachments/assets/caea5e7d-cc85-44dc-83db-f725e3886a7a" /&gt;

16. Entraremos a pve –&gt; Repositories
<img width="3436" height="1269" alt="19" src="https://github.com/user-attachments/assets/8545a998-dee1-48a5-b78f-70e32bfce475" /&gt;

17. Seleccionaremos estos repositorios y le daremos a disable
<img width="3439" height="1265" alt="20" src="https://github.com/user-attachments/assets/5daec8fa-179f-47fd-8324-a5219c4a7de0" /&gt;
<img width="3439" height="1268" alt="21" src="https://github.com/user-attachments/assets/12893909-2a87-4c72-9b96-35f0e2015c5f" /&gt;

18. Dentro de disable pondremos esta opción
<img width="3439" height="1271" alt="22" src="https://github.com/user-attachments/assets/d1eff2ff-6fb4-46ca-8e72-617b83a0a4d8" /&gt;

19. Vamos a updates y hacemos un refresh
<img width="3439" height="1271" alt="23" src="https://github.com/user-attachments/assets/82b41de9-a3bf-4a10-884c-e677caed363e" /&gt;

20. Nos debería de salir esto.
<img width="796" height="495" alt="24" src="https://github.com/user-attachments/assets/29263bea-9eed-4663-83fb-7152c3a31821" /&gt;

21. Hacemos un upgrade
<img width="3438" height="1258" alt="25" src="https://github.com/user-attachments/assets/ea7e018f-d98b-46a1-836b-d3a84750fafb" /&gt;
<img width="3437" height="1392" alt="26" src="https://github.com/user-attachments/assets/2546c855-8ae0-4b97-ba44-9d80755147b5" /&gt;

22. El error desaparece y ya está listo para usar
<img width="3437" height="1311" alt="27" src="https://github.com/user-attachments/assets/6f9ae48c-e94a-49f7-b443-f751661675c7" /&gt;
