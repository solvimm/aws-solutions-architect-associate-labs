# Lab 13 - RDS com Alta Disponibilidade


# 1. Configuração de RDS Multi-AZ

1.1. Acesse o dashboard do RDS para encontrar o cluster RDS Aurora criado no Lab 12. Note que no cluster criado há apenas uma instância e veja em qual AZ está situada. No print deste exemplo, vemos que foi criado na AZ ```us-east-1d```.

 
1.2. Selecione o cluster criado, clique em **Actions** e, em seguida, selecione a opção **Add reader**.


![Image 01](https://d2yblsmsldwfto.cloudfront.net/lab13/lab-13-rds-01.png)

1.3. Selecione também uma instância ```db.t2.small``` e, em **Network & Security**, selecione uma zona de disponibilidade diferente da utilizada pela primeira instância do cluster. Neste caso, selecionamos ```us-east-1c```.

![Image 02](https://d2yblsmsldwfto.cloudfront.net/lab13/lab-13-rds-02.png)


1.4. Em **Settings**, insira um **DB instance identifier** para identificar a instância criada.

![Image 03](https://d2yblsmsldwfto.cloudfront.net/lab13/lab-13-rds-03.png)


1.5. Em **Monitoring**, habilite a função **Enable enhanced monitoring**.


1.6. Deixe as outras configurações com o padrão e clique em **Add reader**.


1.7. Após a criação, o cluster do RDS agora é Multi-AZ


# 2. Autoscaling de réplicas de leitura


2.1. Para habilitar autoscaling de réplicas de leitura no Amazon Aurora, é necessário selecionar o cluster, clicar em Actions e escolher **Add replica auto scaling**.

![Image 04](https://d2yblsmsldwfto.cloudfront.net/lab13/lab-13-rds-04.png)


2.2. Determine a **Policy name**, a Target metric e Target Value. Neste lab, vamos definir a regra de escala para *Average CPU utilization of Aurora Replicas* acima de 70%,

![Image 05](https://d2yblsmsldwfto.cloudfront.net/lab13/lab-13-rds-05.png)


2.3. Em **Cluster capacity details**, vamos definir sempre um mínimo de 2 réplicas de leitura e um máximo de 4.

![Image 06](https://d2yblsmsldwfto.cloudfront.net/lab13/lab-13-rds-06.png)

2.4. Clique em **Add policy** para finalizar.


2.5. Como a regra criada exige sempre um mínimo de duas réplicas de leitura, clique no botão de refresh na tela principal do RDS e, dentro de instantes, poderá observar uma réplica sendo criada automaticamente pela regra do autoscaling.


# 3. Backup Automático

3.1. Para habilitar o backup automático, selecione o cluster e clique em **Modify **.

3.2. Faça o scroll até a seção **Backup**.

3.3. Nessa seção, poderemos configurar o período de retenção (1 dia por default) e a janela de execução. Neste lab, vamos definir um período de retenção de 30 dias o início às 03h00 UTC.

![Image 07](https://d2yblsmsldwfto.cloudfront.net/lab13/lab-13-rds-07.png)

3.4. Clique em **Continue**. Em seguida, valide as configurações e clique em **Modify cluster** para aplicar as modificações.
