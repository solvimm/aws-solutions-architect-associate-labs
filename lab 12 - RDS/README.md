# Lab 12 - RDS (Relational Database Service)


# 1. Criação de RDS

1.1. Acesse o dashboard do RDS e clique em **Create database**.

![Image 01](https://d2yblsmsldwfto.cloudfront.net/lab12/lab-12-rds-01.png)

1.2. Em **Choose a database creation method**, selecione a opção **Standard create**.

![Image 02](https://d2yblsmsldwfto.cloudfront.net/lab12/lab-12-rds-02.png)

1.3. Escolha a Engine do RDS. Para o Lab escolhemos Aurora. Em edição, selecione **Amazon Aurora with MySQL compatibility**. Em database location, selecione **Regional**.

![Image 03](https://d2yblsmsldwfto.cloudfront.net/lab12/lab-12-rds-03.png)

1.4. Em **Database features**, selecione **One writer with multiple readers**.

![Image 04](https://d2yblsmsldwfto.cloudfront.net/lab12/lab-12-rds-04.png)

1.5. Em **Templates**, selecione **Production**.

![Image 05](https://d2yblsmsldwfto.cloudfront.net/lab12/lab-12-rds-05.png)

1.6. Em **Settings*, defina um nome para o seu banco de dados. Configura também as credenciais.

![Image 06](https://d2yblsmsldwfto.cloudfront.net/lab12/lab-12-rds-06.png)

1.7. Em **DB instance size**, para esse lab, selecione a opção **Bustable classes**, pois possui configurações com menor custo. Selecione a **db.t2.small **.

![Image 07](https://d2yblsmsldwfto.cloudfront.net/lab12/lab-12-rds-07.png)

1.8. Em **Availability and durability**, selecione **Don't create and Aurora replica**. Faremos isso em outro lab.

![Image 08](https://d2yblsmsldwfto.cloudfront.net/lab12/lab-12-rds-08.png)

1.9. Por fim, deixe as configurações de rede e VPC padrões e clique em **Create database**.

![Image 09](https://d2yblsmsldwfto.cloudfront.net/lab12/lab-12-rds-09.png)

1.10. De volta à tela inicial do RDS, poderá ver o banco de dados recém criado.

![Image 10](https://d2yblsmsldwfto.cloudfront.net/lab12/lab-12-rds-10.png)