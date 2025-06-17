## Workshop 03 - Parten 3

**Curso ISW811**

## Función del host y máquina virtual

- Función del host: Gestiona DNS, riesgoso modificar, guardado en PCs.
  
- Invitada: Máquina virtual.
  
- Anfitriona: PC físico.

### Inicio y acceso a Vagrant

1. Iniciar Vagrant: 
   
   ```bash
   cd ~/Desktop/ISW811/K/VMs/webserver
   ```
   
   ```bash
   vagrant up
   ```


![EVIDENCIA-1](./images/inicio%20y%20acceso%20a%20Vagrant.png)

2. Acceder a Vagrant:

 ```bash
   vagrant ssh
   ```

   
![EVIDENCIA-2](./images/Imagen2.png)


**Conceptos clave**

   - Vhost_alias: Configuración de alias virtual
   - Rewrite: Sobrescribe peticiones.

### Creación de repositorio y commit

1. Crear carpeta y repo:
   
 ```bash
   mkdir workshop03
   ```

 ```bash
  cd workshop03
   ```

```bash
  git init
   ```


2. Agregar y commit:

```bash
  git add .
   ```

```bash
  git commit -m "Inicializar Workshop 03"
   ```

![EVIDENCIA-3](./images/Imagen3.png)

### Verificación de red  

1. Ping a IP:

```bash
 ping 192.168.56.10
   ```

![EVIDENCIA-4](./images/Imagen4.png)


### Creación de sitios y carpetas

1. Crear carpetas en sites:

```bash
 cd /vagrant/sites
   ```

```bash
 mkdir assets images
   ```

```bash
ls -la
   ```

2. Crear archivos:
   
```bash
 mkdir css
   ```

```bash
touch index.html styles.css
   ```

3. Descargar imagen:

```bash
 curl -o images/patitos.jpg https://example.com/patitos.jpg
   ```

4. Abrir VS Code:Abrir proyecto en VS Code.

![EVIDENCIA-5](./images/Imagen5.png)

### Código de archivos

1. index.html

![EVIDENCIA-6](./images/Imagen6.png)

2. styles.css

![EVIDENCIA-7](./images/Imagen7.png)


### Configuración de dominio

1. Crear carpeta confs:


```bash
cd /vagrant
   ```
   
```bash
mkdir confs
   ```

```bash
ls -la
   ```

![EVIDENCIA-8](./images/Imagen8.png)

2. Crear archivo de dominio:


```bash
touch confs/kaprendas.isw811.xyz.conf
   ```

3. Copiar configuración:


```bash
sudo cp confs/kaprendas.isw811.xyz.conf
   ```

![EVIDENCIA-9](./images/Imagen9.png)

### Verificación y habilitación
 
1. Verificar sintaxis:

```bash
sudo apache2ctl configtest
   ```

2. Habilitar sitio:

```bash
sudo a2ensite kaprendas.isw811.xyz.conf
   ```

3. Reiniciar Apache:

```bash
sudo systemctl restart apache2
   ```

![EVIDENCIA-10](./images/Imagen10.png)

### Estado dentro de la VM

- Estás en /home/vagrant dentro de la VM.
  
- Al hacer cd /vagrant y ls -la, ves:
  
- Archivos y carpetas compartidas desde tu máquina Windows (~/Desktop/ISW811/K/VMs/webserver).
  
- Incluye kaprendas.isw811.xyz.conf (444 bytes, creado el 11/06/2025).
  
- Todo está sincronizado correctamente.
  
![EVIDENCIA-11](./images/Imagen11.png)

**Notas**
- cd /vagrant: Navega a la raíz compartida.
  
- Sincronización: Archivos como kaprendas.isw811.xyz.conf (444 bytes, creado el 11/06/2025) están sincronizados desde ~/Desktop/ISW811/K/VMs/webserver.

- "|": Tubería para redirigir salida.
 
![EVIDENCIA-12](./images/Imagen12.png)


### Verificación de archivo

1. Verificar kaprendas.isw811.xyz.conf:
   
```bash
cd /vagrant/confs
   ```
```bash
ls -la
   ```
![EVIDENCIA-13](./images/Imagen13.png)


2. Ejecutamos el comando para verificar que no existan errores en syntax 


![EVIDENCIA-14](./images/Imagen14.png)

3. Habilitamos el sitio: 

![EVIDENCIA-15](./images/Imagen15.png)

4. Reiniciamos apache 

![EVIDENCIA-16](./images/Imagen16.png)


5. Finalmente amos al navegador y buscamos “http://kaprendas.isw811.xyz” y debemos ver algo así: 


![EVIDENCIA-17](./images/Imagen17.png)



