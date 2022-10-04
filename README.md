# Descripción

El código que se encuentra en este repositorio, es un ejemplo acerca de cómo se puede desplegar un contener de Docker mediante Terraform en AWS. 

El repositorio cuenta con diferentes archivos que son necesarios para que Terraform logre desplegar de forma correcta el contenedor. Dicho en otras palabras, son las instrucciones básicas que necesita Terraform, en cuanto a recursos computacionales, redes y seguridad para poder desplegar el contenedor. 

Algunos de los desafios con los cuales me encuentré fueron los siguientes:

- Para descargar Terraform tuve que conectarme a una VPN ya que mi país tiene restringido el acceso a esta herramienta.
- Poder instalarla de forma correcta también me tomó un par de minutos ya que daba diferentes errores, pero nada que no se pudiese solucionar con algunos blog en Internet.
- Una vez instalado Terraform, lo siguiente fue crear cada uno de los scripts que necesita Terraform para funcionar. Cabe destacar que los datos que contiene el código son de ejemplo. 
- En caso de querer desplegarlo realmente, se deben agregar todas las credenciales de AWS en un archivo llamado terraform.tfvars.tf. Por esta razón, es que en el archivo .gitignore incluye el nombre del mismo, dado que posee información que no debe ser visible al público. 
- Para este caso de ejemplo, se incluyó una VPC (Virtual Private Cloud) la cual permite aislar el contenedor y tenerlo más protegido mediante una subred virtual, para que así no esté conectado a Internet.
- Para encontrar la forma de desplegar un contenedor de Docker, debemos ir a la página oficial de Terraform, ya que la misma nos provisiona el template que debemos copiar y pegar en nuestro script.


Es importante mencionar, que el proceso no es muy largo, solo hay que entender la funcionalidad de cada script, y por supuesto que depende de lo que se desee desplegar. Debido a que puede contar con configuraciones adicionales para añadir una capa extra de seguridad, si es lo que se desea.

Algunos de los comando que se utilizan durante este proceso son los siguientes:

- Terraform init (para iniciar el directorio de trabajo que contiene los scripts de Terraform)
- Terraform plan (Se usa para obtener una previsualización de la infraestructura que se va a desplegar)
- Terraform apply (Se usa para aplicar todos los cambios en la infraestructura)
- Terraform destroy (Una vez el contenedor haya sido desplegado en AWS, para evitar cargos adicionales se debe usar el comando Terraform apply)

**Por último, mencionar que dicha tarea me tomó una hora. Lo suficiente como para descargar Terraform y configurar los diferentes scripts**
