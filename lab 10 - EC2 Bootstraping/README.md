# Lab 10 - EC2 Boostrap


### 1. Criação de Instância

1.1. Siga as instruções do Lab 07 para a criação de EC2 até o passo 3, onde serão realizadas configurações na EC2

1.2. No campo **User data**, dentro de **Advanced Details**, adicione o código:

```
#!/bin/bash
yum update -y
yum install httpd -y
service httpd start
chkconfig httpd on
cd /var/www/html
echo "<html><h1>Hello World - Treinamento Solvimm para AWS Certified Solutions Architect</h1></html>" > index.html
```

Esse código executará um bash script para atualizar os pacotes do yum, iniciar o serviço https e criar uma página index.html com informações básicas dentro do diretório ```/var/www/html```

1.3. Siga o Lab 07 até chegar no passo 6, para configuração do Security Group

1.4. Autorize a porta 80 para o source *Anywhere*, ou 0.0.0.0/0

1.5. Conclua a criação da instância


### 2. Teste do Boostrap

2.1. Ao finalizar a criação da instância, selecione a mesma e acesse a aba **Description**.

2.2. Copie o valor do campo IPV4 Public IP e cole no navegador

![Image 01](https://d2yblsmsldwfto.cloudfront.net/lab10/lab-10-ec2-01.png)

2.3. Será exibida uma página web exibida com o resultado da execução do código no EC2 Bootstrap

![Image 02](https://d2yblsmsldwfto.cloudfront.net/lab10/lab-10-ec2-02.png)