# Lab 01 - IAM
Lab para configuração de permissões no IAM, de acordo com boas práticas da AWS.


### 1. Criação de Usuário

Nesta parte, vamos criar um usuário com permissões de administrador pelo AWS Console.

1.1. Acesse o AWS Dashboard para IAM (https://console.aws.amazon.com/iam/home)
1.2. Clique em **Users**
1.3. Clique em **Add User**

1.4. Defina o nome do usuário, escolhendo o tipo de acesso. *Programmatic Access*, para permitir utilização do CLI, ou *AWS Management Console Access*, para permitir login e acesso pelo console da AWS. Clique em **Next: Permissions**.

1.5. Na parte de grupos seria onde incluímos este usuário em algum grupo, mas vamos abordar a parte de grupos em outra parte deste tutorial.
1.6. Selecione a aba "Attach existing policies directly" escolha a permissão que esse usuário precisa. Neste tutorial, vamos escolher **AdminstratorAccess** (na prática, tenha muita atenção ao utilizar esse tipo de permissão). Clique em **Next: Tags**.
1.7. Nesta parte, podemos definir tags para facilitar o gerenciamento. Para este tutorial, não vamos usar tags. Clique em **Next: Review** e, por fim, em **Create User**.


### 2. Criação de Grupo

2.1. Para criar um grupo acesse o AWS dashboard do IAM, clique em **Groups** na parte esquerda da tela e, em seguida, clique em **Create New Group**
2.2. Defina o nome do grupo e clique em **Next Step**.
2.3. Escolha a permissão que vai estar associada a este grupo. Isso significa que qualquer usuário que seja adicionado a este grupo vai possuir essas permissões. Para este tutorial vamos escolher permissão de **AdministratorAccess** e clicar em **Next Step**.
2.4. Para finalizar, clique em **Create Group**.

### 3. Adicionar Usuários no Grupo

3.1. No grupo criado, clique em **Add Users to Group**.
3.2. Selecione o usuário que gostaria de adicionar ao grupo e clique em **Add Users**.


### 4. Adicionar MFA à conta Root

4.1. Acesse a tela principal do IAM Dashboard clique em **Activate MFA on your root account** e depois clique em **Manage MFA**
4.2. Clique em **Activate MFA**.
4.3. Escolha umas das três opções: a primeira é para adicionar o MFA Virtual, usando um aplicativo como Google Authenticator ou Authy, por exemplo, a segunda para MFA físico e a terceira para outro tipo de MFA. Para este tutorial, vamos utilizar **MFA Virtual**.
4.4. Utilize o Google Authenticator ou Authy para escanear o QR Code e obter o código para configurar.




