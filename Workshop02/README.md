# Workshop 02 - Parte 2  
**Curso ISW811 - Segunda semana**

## Configuración inicial y levantado de máquina

1. Ir a la carpeta del proyecto con el siguiente comando:
   
```bash
   cd ~/ISW811/K/webserver
   ```
2. Levantar la máquina virtual con el siguiente comando:
   
```bash
   vagrant up
   ```

1. Conectarse a la máquina con el siguiente comando:
   
   ```bash
   vagrant ssh
   ```

   ![EVIDENCIA-1](./images/Configuración%20inicial%20y%20levantado%20de%20máquina.png)


## Crear carpeta para imágenes Y COMANDO

```bash
   mkdir imágenes
   ```

## Notas sobre Markdown y Visual Studio Code

1. Crear archivo vacío con el siguiente comando:
 
```bash
   touch README.md
   ```

![EVIDENCIA-2](./images/Notas%20sobre%20Markdown%20y%20Visual%20Studio%20Code.png)


2. Títulos en Markdown: 
   
   UTILIZAMOS 

    #Título principal (ALMOHADILLA)

    ##Título secundario (DOBLE ALMOHADILLA)

    ![EVIDENCIA-3](./images/Títulos%20en%20Markdown.png)

3. Vista previa del archivo Markdown:
   
   UTILIZAMOS

   Ctrl + Shift + V

   ![EVIDENCIA-4](./images/Vista%20previa%20del%20archivo%20Markdown.png)

4. Exportar archivo Markdown a PDF:

   UTILIZAMOS

   Ctrl + Shift + P > Buscar: Markdown PDF: Export (pdf)

   ![EVIDENCIA-5](./images/Exportar%20archivo%20Markdown%20a%20PDF.png)

5. Instalar extensiones recomendadas en VS Code:

    Markdown PDF

    Markdown Shortcuts

    ![EVIDENCIA-6](./images/Instalar%20extensiones%20recomendadas%20en%20VS%20Code.png)

## Agregar una imagen

Copiar una imagen a la carpeta imágenes/ dentro del proyecto.
Luego insertarla en el Markdown con:


![EVIDENCIA-7](./images/Ingresar%20a%20la%20VM%20-1.png)

![EVIDENCIA-8](./images/Ingresar%20a%20la%20VM%20-%202.png)



## Cambiar el nombre de la máquina virtual

1. Ingresar a la VM con el siguiente comando:
   
```bash
   vagrant ssh
   ```
2. Cambiar el nombre del host con el siguiente comando:

 ```bash
   sudo hostnamectl set-hostname webserver
   ```
3. Editar el archivo /etc/hosts con el siguiente comando:
   
```bash
  sudo nano /etc/hosts
   ```
4. Cambiar la línea con el siguiente comando:

 ```bash
  127.0.1.1 bookworm
   ```
   POR:

```bash
  127.0.1.1 webserver
   ```
5. Guardar cambios 

    Ctrl + O → Enter

    Ctrl + X para salir

6. Salir de la máquina virtual con el siguiente comando:

 ```bash
  exit
   ```

   ![EVIDENCIA-9](./images/Cambiar%20el%20nombre%20de%20la%20máquina%20virtual.png)

## Inicializar repositorio Git y hacer el primer commit

Solo la primera vez en tu máquina: configurar tus datos

 ```bash
git config --global user.email "katherineprendas2004@gmail.com"
git config --global user.name "Katherine Prendas"
   ```
   
1. Inicializar el repositorio Git con el siguiente comando:
   
 ```bash
 git init
   ```
2. Agregar el archivo README.md con el siguiente comando: 

 ```bash
  git add README.md
   ```
3. Crear el primer commit con el siguiente comando:
   
```bash
  git commit -m "Inicializar repositorio con Readmi.md"
   ```
4. Ver historial de commits con el siguiente comando:

 ```bash
  git log
   ```

![EVIDENCIA-10](./images/Inicializar%20repositorio%20Git%20y%20hacer%20el%20primer%20commit.png)

## Instalación del stack LAMP

1. Actualizar los paquetes con el siguiente comando: 
   
```bash
  sudo apt-get update
   ```

2. Instalar servicios necesarios con el siguiente comando:

 ```bash
  sudo apt-get install vim vim-nox curl apache2 mariadb-server mariadb-client php8.2 php8.2-curl php8.2-bcmath php8.2-mysql php8.2-mcrypt php8.2-xml php8.2-zip php8.2-mbstring
   ```

3. Una vez finalizada la instalación, apagar la máquina con el siguiente comando: 
   
```bash
  vagrant halt
   ```
## Créditos

Taller desarrollado por Katherine Prendas en clase del curso de aplicaciones web utilizando sotfware libre con el profesor Misael Matamoros 

Correo: katherineprendas2004@gmail.com