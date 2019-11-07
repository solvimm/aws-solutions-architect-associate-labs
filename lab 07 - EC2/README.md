# Lab 07 - EC2


# 1. Criação de EC2

1.1. No painel da AWS, acesso o serviço EC2

1.2. Clique em **Instances**.

1.3. Clique em "Launch Instance" para criar uma máquina virtual

![Image 01](https://d2yblsmsldwfto.cloudfront.net/lab07/lab-07-ec2-01.png)

1.4. O primeiro passo da criação da máquina virtual é a escolha da imagem e sistema operacional que vai ser usada na máquina virtual. Para este tutorial, selecione a Amazon Linux 2

![Image 02](https://d2yblsmsldwfto.cloudfront.net/lab07/lab-07-ec2-02.png)

1.5. O segundo passo é a escolha da família e do tamanho da máquina virtual. Para este lab, vamos selecionar a *t2.micro* e clicar em **Next: Configure Instance Details**.

![Image 03](https://d2yblsmsldwfto.cloudfront.net/lab07/lab-07-ec2-03.png)

1.6. O terceiro passo é um pouco mais detalhado. Nele são definidos quantidade de instancias, configurações de rede, tipo de aquisição, roles do IAM, proteções contra desligamento, opções de monitoramento, entre outras que podem ser visualizadas nas imagens a seguir. Neste lab, vamos subir apenas um servidor utilizando as configurações padrões. Clique em **Next: Add Storage**.

![Image 04](https://d2yblsmsldwfto.cloudfront.net/lab07/lab-07-ec2-04.png)

![Image 05](https://d2yblsmsldwfto.cloudfront.net/lab07/lab-07-ec2-05.png)

1.7. No passo 4 é onde são configurados os discos de armazenamento da instancia. Para este lab, vamos utilizar apenas o disco padrão.

![Image 06](https://d2yblsmsldwfto.cloudfront.net/lab07/lab-07-ec2-06.png)


1.7. No passo 5, configuramos as tags para facilitar o gerenciamento dos recursos. Clique em **Next: Configure Security Group**.

![Image 07](https://d2yblsmsldwfto.cloudfront.net/lab07/lab-07-ec2-07.png)


1.8. No passo 6, são feitas as configurações de acesso a instancia, através das configurações de **Security Groups**. Libere a porta 22 (SSH) para o seu IP e clique em **Review and Launch**.

![Image 08](https://d2yblsmsldwfto.cloudfront.net/lab07/lab-07-ec2-08.png)


1.9. No passo 7, revise todas as configurações feitas e clique em **Launch**.


![Image 08](https://d2yblsmsldwfto.cloudfront.net/lab07/lab-07-ec2-09.png)


1.10. Após a confirmação da criação da instancia, é necessário configurar qual chave de acesso ela vai utilizar. A criação só vai ser liberada após a criação e download de uma nova *Key Pair* ou a utilização de uma já existente e o consentimento do usuário de que sem essa chave não é possível acessar a instancia. Selecione **Create a new key pair**, defina seu nome e clique em **Download Key Pair**. Após o download, clique em **Launch Instances**.

![Image 08](https://d2yblsmsldwfto.cloudfront.net/lab07/lab-07-ec2-10.png)

1.11. Aguarde alguns instantes para a instância ser criada. Quando finalizado, selecione a instância e clique em connect. Uma tela terá aberta com as opções de realizar a conexão.

![Image 08](https://d2yblsmsldwfto.cloudfront.net/lab07/lab-07-ec2-11.png)