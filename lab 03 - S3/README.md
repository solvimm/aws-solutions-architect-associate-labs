# Lab 03 - Criação de Bucket no S3


### 1. Criação de Bucket
1.1. No painel inicial, ir até o serviço do S3.

1.2. Clique em "Create Bucket".

1.3. Escolha um nome para o bucket e a região em que ele deve ficar. O nome do bucket deve ser único em toda a AWS, não só na sua conta.

![Image 01](https://d2yblsmsldwfto.cloudfront.net/lab03/lab-03-s3-01.png)

1.4. Existe a opção de copiar as configurações de outro bucket já existente. Como estamos criando um bucket padrão, deixe isso em branco.

1.5. No menu de "Configurar opções", pode-se configurar o versionamento, logs, tags, registro de atividades e criptografia do bucket. Para este lab, não faremos essas configurações. Clique em **Next**.

![Image 02](https://d2yblsmsldwfto.cloudfront.net/lab03/lab-03-s3-02.png)

1.6. No menu "Define Permissions" é onde se configura as permissões de acesso ao bucket e seus objetos. Por padrão o acesso público ao bucket e seus objetos é bloqueado e é extremamente recomendado que se mantenha dessa forma. No menu "Análise" é possível revisar as configurações feitas nos menus anteriores.

![Image 03](https://d2yblsmsldwfto.cloudfront.net/lab03/lab-03-s3-03.png)

1.7. Revise as configurações e clique em **Create Bucket**. Na próxima tela, poderemos ver o bucket criado.

![Image 04](https://d2yblsmsldwfto.cloudfront.net/lab03/lab-03-s3-04.png)


### 2. Upload de Objeto

2.1. Clique no bucket para abrir e fazer upload de arquivos. Clique em **Upload** para fazer upload de objetos.

2.2. Clique em **Add File** e escolha o objeto ou objetos que deseja subir para o bucket.

![Image 05](https://d2yblsmsldwfto.cloudfront.net/lab03/lab-03-s3-05.png)

2.3. No menu **Definir permissões** podemos configurar os acessos permitidos ao objeto. Mantenha as configurações padrões e clique em **Next**.

![Image 06](https://d2yblsmsldwfto.cloudfront.net/lab03/lab-03-s3-06.png)

2.4. No menu **Definir propriedades** é possível escolher em qual classe do S3 o objeto vai ser armazenado, além de configurações de criptografia e tags. Mantenha no *Standard*, que é o padrão, e clique em **Next**.

![Image 07](https://d2yblsmsldwfto.cloudfront.net/lab03/lab-03-s3-07.png)

![Image 08](https://d2yblsmsldwfto.cloudfront.net/lab03/lab-03-s3-08.png)

2.5. No menu **Análise** é possível revisar as configurações feitas nos menus anteriores e confirmar o upload do arquivo. Clique em **Upload**.

![Image 08](https://d2yblsmsldwfto.cloudfront.net/lab03/lab-03-s3-09.png)


### 3. Acessar Objeto Criado

3.1. Na próxima tela, é possível ver o arquivo já disponível no bucket criado. Clique no objeto.

3.2. Nessa tela, é possível ver as informações referentes ao objeto e a URL para acesso público. Copie a URl e cole no navegador e para tentar acessar o objeto.

3.3. Esse é o resultado de uma consulta a URL de um objeto privado no bucket do S3. Para esse lab, vamos deixa o acesso público para testes.

3.4. Para permitir o acesso público a objetos, volte na página do bucket e acesse o menu **Permissions**. Por padrão, o checkbox "Block all public access" está marcado. Desmarque o checkbox e clique em **Save**. Por segurança, é necessário confirmar essa ação. Lembramos que, segundo as melhores práticas, todos os buckets devem ser privados e esse lab é apenas para fins didáticos.

![Image 10](https://d2yblsmsldwfto.cloudfront.net/lab03/lab-03-s3-10.png)

3.5. Após a confirmação, selecione novamente o objeto e clique em **Make Public**.

3.6. Copie e cole novamente a URL de acesso ao objeto no navegador. Como resultado você conseguirá visualizar o objeto.


