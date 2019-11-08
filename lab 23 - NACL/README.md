# Lab 23 - Network Access Control List


### 1. Criação de NACL

1.1.No painel inicial, vá até o serviço **VPC**
![Image 01](https://d2yblsmsldwfto.cloudfront.net/lab23/imagem_1.png)

1.2. Em **Security** acesse a opção **Network ACLs**. Clique no botão **Create network ACL**
![Image 02](https://d2yblsmsldwfto.cloudfront.net/lab23/imagem_2.png)

1.3. Em **Name tag** digite o nome ```MyWebNACL```

1.4. Em **VPC** selecione a VPC padrão e clique no botão **Create**
![Image 03](https://d2yblsmsldwfto.cloudfront.net/lab23/imagem_3.png)


1.5. Confirme a criação da nova NACL e a regra ```DENY``` na aba **Inbound Rules**.
![Image 04](https://d2yblsmsldwfto.cloudfront.net/lab23/imagem_4.png)


### 2. 

2.1. Crie uma aplicação no Elastic Beanstalk seguindo o lab do Beanstalk, caso não tenha feito ainda.

2.2. Confirme se a aplicação de exemplo do Beanstalk está no ar
![Image 05](https://d2yblsmsldwfto.cloudfront.net/lab23/imagem_5.png)


2.3. Em **Subnet associations** clique no botão **Edit subnet associations**
![Image 06](https://d2yblsmsldwfto.cloudfront.net/lab23/imagem_6.png)

2.4. Selecione a subnet usada pela instancia do Beanstalk
![Image 07](https://d2yblsmsldwfto.cloudfront.net/lab23/imagem_7.png)

2.5. Carregue novamente a página da aplicação do Beanstalk e confirme que a aplicação não está mais respondendo
![Image 08](https://d2yblsmsldwfto.cloudfront.net/lab23/imagem_8.png)

2.6. Em **Inbound Rules** clique no botão **Edit inbound rules**
![Image 09](https://d2yblsmsldwfto.cloudfront.net/lab23/imagem_9.png)

2.7. Clique em "Add Rule" e adicione as regras:
```
Rule #: 100,  Port Range: 80, Allow / Deny: ALLOW
Rule #: 200,  Port Range: 443, Allow / Deny: ALLOW
```
![Image 10](https://d2yblsmsldwfto.cloudfront.net/lab23/imagem_10.png)

2.8. Clique no botão **Save**.
![Image 11](https://d2yblsmsldwfto.cloudfront.net/lab23/imagem_11.png)

2.9. Em **Outbound Rules** e clique no botão **Edit outbound rules**.
![Image 12](https://d2yblsmsldwfto.cloudfront.net/lab23/imagem_12.png)

2.10. Clique em **Add Rule** e adicione as regras:

```
Rule #: 100,  Port Range: 80, Allow / Deny: ALLOW
Rule #: 200,  Port Range: 443, Allow / Deny: ALLOW
Rule #: 300,  Port Range: 1024 - 65535, Allow / Deny: ALLOW
```

2.11 Clique no botão **Save**
![Image 13](https://d2yblsmsldwfto.cloudfront.net/lab23/imagem_13.png)

2.12. Carregue novamente a página da aplicação do Beanstalk e confirme que a aplicação está respondendo corretamente
![Image 14](https://d2yblsmsldwfto.cloudfront.net/lab23/imagem_14.png)


