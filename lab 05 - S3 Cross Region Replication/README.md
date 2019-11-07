# Lab 05 - Cross Region Replication no S3


1. Acesse o bucket que deseja fazer a configuração e clique na aba **Gerenciamento**. 

![Image 01](https://d2yblsmsldwfto.cloudfront.net/lab05/lab-05-s3-01.png)

2. Em seguida, clique em **Replicação** e em seguida clique em **Adicionar regra**. 

3. Nessa tela, configura-se as regras de replicação, podendo selecionar todos os objetos, apenas objetos com um prefixo pré-determinado ou tag. Para este lab, vamos replicar todos os objetos.

![Image 02](https://d2yblsmsldwfto.cloudfront.net/lab05/lab-05-s3-02.png)

4. No menu "Definir destino", escolhemos um bucket ja existente para replicação, ou a criação de um novo. Neste lab, vamos optar por criar um novo.

![Image 03](https://d2yblsmsldwfto.cloudfront.net/lab05/lab-05-s3-03.png)

5. Também é possível definir qual a categoria de armazenamento do S3 que as réplicas serão salvas e se vamos alterar a propriedade do objeto para o proprietário do bucket de destino. Para esse lab, manteremos as opções padrão.

6. Com a criação do novo bucket, é necessário colocar um novo nome único e definir a região onde o bucket de replicação vai ser criado.

7. Após a definição do destino, precisamos dar permissão, através de IAM Role, para o bucket de origem criar um bucket de destino e fazer a cópia de arquivos nele.

![Image 04](https://d2yblsmsldwfto.cloudfront.net/lab05/lab-05-s3-04.png)

8. No menu **Revisar**, é possível ver as configurações feitas nos menus anteriores. Clique em **Confirmar**.

9. Após a confirmação, verifique se o bucket de destino foi criado.

10. Acesse o bucket de origem e faça o upload de um arquivo de teste

11. Acesse o bucket de replicação  e verifique se o objeto foi replicado

12. Acesso novamente o bucket de origem e exclua o arquivo

13. Acesse novamente o bucket de replicação e verifique se o objeto replicado ainda permanece salvo