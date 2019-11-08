# Lab 23 - Network Access Control List


### 1. Criação de NACL

1.1.No painel inicial, vá até o serviço **VPC**

1.2. Em **Security** acesse a opção **Network ACLs**. Clique no botão **Create network ACL**

1.3. Em **Name tag** digite o nome ```MyWebNACL```


1.4. Em **VPC** selecione a VPC padrão e clique no botão **Create**

1.5. Confirme a criação da nova NACL e a regra ```DENY``` na aba **Inbound Rules**.

### 2. 

2.1. Crie uma aplicação no Elastic Beanstalk seguindo o lab do Beanstalk, caso não tenha feito ainda.


2.2. Confirme se a aplicação de exemplo do Beanstalk está no ar


2.3. Em **Subnet associations** clique no botão **Edit subnet associations**

2.4. Selecione a subnet usada pela instancia do Beanstalk

2.5. Carregue novamente a página da aplicação do Beanstalk e confirme que a aplicação não está mais respondendo


2.6. Em **Inbound Rules** clique no botão **Edit inbound rules**


2.7. Clique em "Add Rule" e adicione as regras:
```
Rule #: 100,  Port Range: 80, Allow / Deny: ALLOW
Rule #: 200,  Port Range: 443, Allow / Deny: ALLOW
```

2.8. Clique no botão **Save**.


2.9. Em **Outbound Rules** e clique no botão **Edit outbound rules**.


2.10. Clique em **Add Rule** e adicione as regras:

```
Rule #: 100,  Port Range: 80, Allow / Deny: ALLOW
Rule #: 200,  Port Range: 443, Allow / Deny: ALLOW
Rule #: 300,  Port Range: 1024 - 65535, Allow / Deny: ALLOW
```

2.11 Clique no botão **Save**


2.12. Carregue novamente a página da aplicação do Beanstalk e confirme que a aplicação está respondendo corretamente


