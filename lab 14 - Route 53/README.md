# Lab 14 - Route 53

Abra o console de Amazon Route 53 em https://console.aws.amazon.com/route53/home

# 1. Compra de domínio

1.1. **IMPORTANTE: Não iremos concluir a compra do domínio para não gerar custos nesse lab. Iremos só realizar os passos para mostrar como seria, e cancelar no final.**

1.2. No painel do Route 53, selecione **Domain Registration**.

1.3. Busca um domínio que gostaria e clique em **Check** para validar se está disponível. Caso esteja, clique em **Continue**.

![Image 01](https://d2yblsmsldwfto.cloudfront.net/lab14/lab-14-route53-01.png)

1.4. Nesta tela, é só preencher as informações cadastrais para concluir a compra.



# 2. Configuração de domínio em EC2

2.1. No painel do Route 53, selecione **Hosted zones** no menu da esquerda e, em seguida, clique em **Create Hosted Zone**.

2.2. Insira um nome de domínio. Para este exemplo, vamos utilizar **treinamentosolvimm.com.br**. Clique em **Create**.

2.3. Clique em **Create Record Set**. Em Name, definimos o sub-domínio que iremos configurar. Para este lab, utilizaremos ec2, para configurar o acesso à EC2 em **ec2.treinamentosolvimm.com.br**.

2.4. No campo **Type**, seleciona ``A - IPv4 address```

2.5. No campo **Value**, insira o IP da EC2 configurada no lab anterior, com uma página web.

2.6. Para **Routing Policy**, deixe em ```Simple```.

![Image 02](https://d2yblsmsldwfto.cloudfront.net/lab14/lab-14-route53-02.png)


2.7. Por fim, clique em **Create**. Para isso funcionar, seria necessário ter um domínio válido adquirido.