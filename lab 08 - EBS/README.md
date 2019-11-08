# Lab 08 - EBS


## 1. Criação de EC2

1.1. Como primeiro passo, crie uma instância EC2 como no Lab 07, exceto na parte de configuração de storage

1.2. No passo 4, para configurar o storage, adicione 3 discos EBS, dos tipos Provisioned IOPS SSD, Cold HDD e Throughput Optimized HDD, como tamanho padrão de cada um.

![Image 01](https://d2yblsmsldwfto.cloudfront.net/lab08/lab-08-ebs-01.png)

1.3. Conclua a criação da EC2 como no Lab 07.


# EBS Lab

## 2. Modificação de EBS

2.1. Após a criação do servidor, de volta na tela inicial de EC2, na aba esquerda, clique em **Volumes** para ver os discos EBS.

2.2. Em **Volumes**, podemos ver os discos criados, os tipos e a qual instância estão conectados. Além disso podemos alterar tamanho, o tipo dos discos e definir um nome como descrição.

2.3. Selecione um dos discos EBS criados e clique em **Actions** e, em seguida, clique em **Modify Volume**. 

2.4. Nesse menu é possível alterar o *Volume Type* e o *Size* do disco EBS. Observação importante: Não é possível diminuir o tamanho de um disco EBS, apenas aumentar.

![Image 02](https://d2yblsmsldwfto.cloudfront.net/lab08/lab-08-ebs-02.png)

2.5. Altere o tipo e o tamanho do volume. Depois dessa alteração, é necessário entrar no servidor virtual e expandir o disco.

![Image 03](https://d2yblsmsldwfto.cloudfront.net/lab08/lab-08-ebs-03.png)


## 3. Criação de Snapshot

3.1. Selecione o volume que deseja criar o snapshot, clique em "Actions" e, em seguida, clique em **Create a Snapshot**.

![Image 04](https://d2yblsmsldwfto.cloudfront.net/lab08/lab-08-ebs-04.png)

3.2. Defina uma descrição e adicione as tags desejadas para o snapshot criado.

![Image 05](https://d2yblsmsldwfto.cloudfront.net/lab08/lab-08-ebs-05.png)

3.3. Por fim, clique em **Create Snapshot**.


## 4. Criação de instância a partir de snapshot

4.1. Para criar uma instância EC2 a partir de um snapshot gerado, selecione o snapshot, clique em **Actions** e clique e **Create AMI**.

![Image 06](https://d2yblsmsldwfto.cloudfront.net/lab08/lab-08-ebs-06.png)

4.2. Defina um nome para a AMI, o tamanho do disco e clique em **Create**.

![Image 07](https://d2yblsmsldwfto.cloudfront.net/lab08/lab-08-ebs-07.png)

4.3.Para utilizar a AMI criada, vá em instances e clique em **Launch Instances**.

4.4. No passo 1 é possível selecionar **My AMIs** no menu da esquerda. Selecione a AMI criada e crie a instância a partir dela.

![Image 08](https://d2yblsmsldwfto.cloudfront.net/lab08/lab-08-ebs-08.png)
