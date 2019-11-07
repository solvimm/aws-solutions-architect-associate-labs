# Lab 06 - CloudFront


# 1. Upload de Imagem para o S3

1.1. Acesse o S3 e realize o upload de uma imagem para um Bucket criado para este lab


# 2. Configuração do CloudFront

2.1. Acesse o console do CloudFront em  https://console.aws.amazon.com/cloudfront/home

2.2. Clique em **Create Distribution**.

![Image 01](https://d2yblsmsldwfto.cloudfront.net/lab06/lab-06-cloudfront-01.png)

2.3. Existem dois tipos de distribuição, WEB e RTMP. Para este lab, escolha a distribuição Web.

![Image 02](https://d2yblsmsldwfto.cloudfront.net/lab06/lab-06-cloudfront-02.png)


2.4. O primeiro passo é especificar o **Origin Domain Name**. O Origin Domain Name pode ser um Bucket do S3, uma instância EC2, um Load Balancer, por exemplo. Selecione o Bucket do S3 configurado anteriormente. 

2.5. Especifique o **Origin Path**. Se você quiser que o CloudFront solicite seu conteúdo de um diretório do seu recurso ou origem personalizada, insira o caminho do diretório começando com barra (/). O CloudFront inclui o caminho do diretório no valor de Origin Domain Name.

2.6. Em ***Origin ID**, você poderá usar o ID especificado para identificar a origem ou o grupo de origens para o qual o CloudFront roteará uma solicitação quando ela tiver o mesmo caminho padrão desse comportamento de cache. Ao escolher o **Origin Domain Name**, automaticamente este campo é preenchido.

![Image 03](https://d2yblsmsldwfto.cloudfront.net/lab06/lab-06-cloudfront-03.png)


2.7. Em **Restrict Bucket Access**, selecione a opção **Yes**. Isso fará com que os usuários acessem objetos em um bucket do Amazon S3 usando apenas URLs do CloudFront, e não do Amazon S3.

2.8. Neste lab, não vamos alterar as configurações padrões de **Default Cache Behavior Settings**. Clique em **Create Distribution**.

2.9. Aguarde o estado da distribuição mudar de **In Progress** para **Deployed**.

![Image 04](https://d2yblsmsldwfto.cloudfront.net/lab06/lab-06-cloudfront-04.png)


# 3. Acessar objeto a partir do CloudFront

3.1. Copie o **Domain Name** da distribuição do CloudFront configurada e retorne ao S3.

3.2. Acesse o bucket criado anteriormente, selecione a imagem que fez o upload e copie o nome da imagem.

3.3. Em seu navegador, acesse a página combinando o domain name com o nome da imagem para gerar a url.

Exemplo:

Domain Name:  d7ft7dsahus.cloudfront.net

Nome do arquivo de imagem: /logo-solvimm-nb-1.png

Cole no navegador: d7ft7dsahus.cloudfront.net/logo-solvimm-nb-1.png

3.4. Se todos os passos estiverem corretos, você deverá ver a imagem que está armazenada no Bucket do S3 através do CloudFront pelo navegador.


