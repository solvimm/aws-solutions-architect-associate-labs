# Lab 19 - VPC Flow Logs


## 1. Criação de Grupo de Logs

1.1. Para iniciar o lab do VPC Flow Logs, é necessário fazer a criação de um grupo de FlowLogs no Amazon CloudWatch. Vá no menu de serviços e acesse o **CloudWatch**.


1.2. Na página inicial do CloudWatch, utilize o menu ao lado esquerdo e clique em **Logs**.

1.3. Na página  de Logs, clique em **Actions** e clique em **Create log group**

![Image 01](https://d2yblsmsldwfto.cloudfront.net/lab19/lab-19-vpc-flowlogs-01.png)


1.4. Defina um nome para o grupo e finalize a criação.


## 2. Configuração de VPC Flow Logs

2.1. Após ter o grupo de logs criado, acesse o menu de serviços e clique em **VPC**.

2.2. Na página inicial de VPC, acesse em **Your VPCs** no menu da esquerda para poder visualizar todas as VPCs criadas e escolher a VPC que deseja criar o FlowLogs.


2.3. Selecione a VPC e clique em **Actions** e, em seguida, clique em **Create flow fog** para iniciar a configuração do seu VPC Flow Logs Group.

![Image 02](https://d2yblsmsldwfto.cloudfront.net/lab19/lab-19-vpc-flowlogs-02.png)


2.4. Na página de criação, altere o **filter** para ```All``` e deixe o **Destination** enviando os logs para o CloudWatch.

2.5. No **Destination log group**, selecione o **Flow Logs Group** criado anteriormente no CloudWatch e clique em **Set Up Permissions** para criar a IAM Role que vai permitir a VPC escrever os Logs no CloudWatch.

![Image 03](https://d2yblsmsldwfto.cloudfront.net/lab19/lab-19-vpc-flowlogs-03.png)

2.6. Uma nova janela vai ser aberta para configuração da IAM Role, escolha um nome e clique em permitir. Após permitir, volte a página de configuração do VPC Flow Logs.

![Image 04](https://d2yblsmsldwfto.cloudfront.net/lab19/lab-19-vpc-flowlogs-04.png)

2.7. Clique na seta de atualização do IAM Role e selecione a IAM Role criada no passo anterior e, em seguida, clique em **Create* para finalizar.

![Image 05](https://d2yblsmsldwfto.cloudfront.net/lab19/lab-19-vpc-flowlogs-05.png)


## 3. Visualização de Logs

3.1. Para visualizar os logs, selecione a VPC onde o Flow Log foi criado e vá no menu **Flow logs**.

3.2. Clique no **Destination name** que está em azul para ir direto ao Flow Log Group. Você chegará na página para olhar os logs.

![Image 06](https://d2yblsmsldwfto.cloudfront.net/lab19/lab-19-vpc-flowlogs-06.png)

