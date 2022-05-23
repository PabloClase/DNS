Pasos a seguir:
1º Cambiamos la red de la maquina virtual a Red Nat.

2º Cambiamos el netplan para que se ajuste a la ip de nuestra red nat.

3º Update y upgrade e installar dnsutils -y 

4º Installar bind9 -y

5º Editar el archivo /etc/bind/named.conf.options y quitamos el dns de google del netplan 8.8.8.8

6º Copia de seguridad de db.local  -->   sudo cp /etc/bind/db.local /etc/bind/db.pablo.net

7º Editamos el archivo recientemente creado y tras ello comprobamos si funciona correctamente:
named-checkzone pgv.net /etc/bind/db.pgv.net

8º Editamos el archivo /etc/bind/named.conf.default.zones reiniciamos bind y comprobamos que funciona correctamente

9º Iniciamos otra maquina virtual y editamos el archivo /etc/hosts

10º Comprobamos que existe haciendo un ping a la direccion del sitio o accediendo a el desde el navegador
