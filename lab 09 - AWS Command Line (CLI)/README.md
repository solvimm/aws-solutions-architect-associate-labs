# Lab 09 - CLI (Command Line Interface)


### 1. Configuração de Credenciais

1.1. Como primeiro passo, você deve ter o access key e secret key do seu usuário para configurar as credenciais para utilizar o CLI. Para criar essas credenciar, acesso o IAM e clique em **Users**.

1.2. Selecione o seu usuário e clique em **Security Credentials**

1.3. Clique em **Create Access Key**.

1.4. Faça o download das credenciais configuradas


### 2. Instalação de CLI

2.1. Para instalar a CLI, siga as instruções em https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html de acordo com o seu Sistema Operacional. Caso já possua o pip3 instalado, basta executar o comando:

```
$ pip3 install awscli --upgrade --user
```

2.2. Para verificar que a CLI foi instalada corretamente, execute o comando:

```
$ aws --version
aws-cli/1.16.246 Python/3.7.4 Linux/4.14.133-113.105.amzn2.x86_64 botocore/1.12.236
```

2.3. Para configurar as suas credenciais, execute o comando:

```
$ aws configure --profile cli-lab
```

Nesse momento, irá preencher os campos com as credenciais configuradas no passo 1:

```
AWS Access Key ID [None]: [YOUR ACCESS KEY ID]
AWS Secret Access Key [None]: [YOUR SECRET ACCESS KEY]
Default region name [None]: us-east-1
Default output format [None]: json
```

Como o usuário foi configurado com permissão de administrador, as credenciais permitem executar todos os comandos via CLI.

2.4. Para validar que as credenciais foram configuradas corretamente, execute o comando para ver as credenciais configuradas para o perfil [cli-lab]:

```
$ cat ~/.aws/credentials 
```

### 3. Utilizando a CLI

3.1. O primeiro teste será listar os buckets existentes no S3, com o comando:

```
$ aws s3 ls --profile cli-lab
```

3.2. Para criar um novo bucket, execute o comando a seguir, substituindo *mybucket* por um nome único de bucket:

```
$ aws s3 mb s3://mybucket --region us-east-1 --profile cli-lab
```

3.3. Para validar que o bucket foi criado corretamente, execute novamente o comando para listar buckets e validar que o novo bucket agora existe

```
$ aws s3 ls --profile cli-lab
```
