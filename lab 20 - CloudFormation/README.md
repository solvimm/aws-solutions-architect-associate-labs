# Lab 20 - CloudFormation


# 1. Criação de Aplicação no Beanstalk

1.1. Acesse o menu principal de serviços e encontre o **CloudFormation**.

1.2. Na página do serviço é possível ver todas as Stacks de CloudFormation que já foram criadas.

![Image 01](https://d2yblsmsldwfto.cloudfront.net/lab21/lab-20-cloudformation-01.png)

1.3. Clique em **Create stack** para criar uma stack nova


1.4. Selecione **Use a sample template** para usar um template ja pronto. É possível escrever seu próprio template, mas, para este lab, vamos utilizar um já pronto.

![Image 01](https://d2yblsmsldwfto.cloudfront.net/lab21/lab-20-cloudformation-02.png)


1.5. Preencha todos os dados necessários e lembre de guardar usuários e senhas que vão ser criados. Também é necessário escolher ou criar uma nova Key Pair, pois essa infraestrutura contém uma EC2.

1.6.  Após o preenchimento de todos os dados, clique em **Next**.

1.7. Nesse menu podemos deixar todas as configurações padrões, pois são configurações um pouco mais detalhadas para certos casos de uso. Vamos utilizar as configurações padrões para esse lab. Clique em **Next**.

![Image 01](https://d2yblsmsldwfto.cloudfront.net/lab21/lab-20-cloudformation-06.png)

1.8. No menu "Review" você pode revisar todas as configurações feitas nos passos anteriores de criação do CloudFormation. Clique em **Create stack** para iniciar a criação.

# 2. Acesso ao Ambiente Criado

2.1. Nesse painel é possível acompanhar os passos para a criação do ambiente.

![Image 01](https://d2yblsmsldwfto.cloudfront.net/lab21/lab-20-cloudformation-08.png)

2.2. Esse é o painel com a stack já criado e pronta para utilização. Agora vamos ver se o ambiente está funcionando.

![Image 01](https://d2yblsmsldwfto.cloudfront.net/lab21/lab-20-cloudformation-09.png)

2.3. Va no menu principal de serviços e acesse o **EC2**.

24. Selecione a instância que acabou de ser criada, copie e cole o IP Público em um navegador. Você deve obter essa página como resultado.

![Image 01](https://d2yblsmsldwfto.cloudfront.net/lab21/lab-20-cloudformation-10.png)
