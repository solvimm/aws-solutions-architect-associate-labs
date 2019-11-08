# Lab 22 - VPC Endpoints


# 1. Criação de VPC Endpoint

1.1. Para criar um VPC Endpoint para o S3, abra o console de Amazon VPC em https://console.aws.amazon.com/vpc/.

1.2. Certifique-se de selecionar a Região correta, no menu superior direito.

1.3. Na coluna lateral, clique em **Endpoints**. Em seguida, clique em **Create Endpoint**.
![Image 01](https://d2yblsmsldwfto.cloudfront.net/lab22/Lab-01-endpoints.png)

1.4. Na etapa seguinte, mantenha a opção **Service category** marcada como **AWS services**.
![Image 02](https://d2yblsmsldwfto.cloudfront.net/lab22/Lab-02-endpoints.png)

1.5. Na opção **Service Name**, selecione o serviço correspondente ao **S3 (Type=Gateway)**.
![Image 03](https://d2yblsmsldwfto.cloudfront.net/lab22/Lab-03-endpoints.png)


1.6. Abaixo, na opção **VPC**, clique no menu e selecione o **vpc-id** correspondente a sua VPC
![Image 04](https://d2yblsmsldwfto.cloudfront.net/lab22/Lab-04-endpoints.png)

1.7. Na opção seguinte **Configure route tables**, selecione as route tables que receberão as rotas para do **vpc-endpoint**.
![Image 05](https://d2yblsmsldwfto.cloudfront.net/lab22/Lab-05-endpoints.png)

1.8. Na opção **Policy**, mantenha selecionado **Full Access**. Clique em **Create Endpoint**.
![Image 06](https://d2yblsmsldwfto.cloudfront.net/lab22/Lab-06-endpoints.png)

1.9. Após este passo, você receberá um aviso confirmando a criação do endpoint. Clique em **Close**.
![Image 07](https://d2yblsmsldwfto.cloudfront.net/lab22/Lab-07-endpoints.png)

# 2. Validação


2.1. Verifique se o endpoint é exibido no painel.
![Image 08](https://d2yblsmsldwfto.cloudfront.net/lab22/Lab-08-endpoints.png)

2.2. Após alguns minutos, verifique se a rota foi inserida na **route table** corretamente.

2.3. Para isso, entre no painel de **Route Tables**, selecione a tabela de rotas, e clique na aba **Routes**. Se tudo estiver correto, deve existir uma linha contendo a regra de roteamento, com Target para o id do vpc-endpoint (vpce-xxxxxxxxxxx) criado.
![Image 09](https://d2yblsmsldwfto.cloudfront.net/lab22/Lab-09-endpoints.png)


