S3 Criação de Bucket Lab

No painel inicial, ir até o serviço do S3

Clicar em "Criar bucket"

Escolher um nome para o bucket e a região em que ele deve ficar.
OBS: O nome do bucket deve ser único
Você ainda tem a opção de copiar as configurações de outro bucket ja existente, mas como estamos criando um bucket padrão, deixe isso em branco.

No menu de "Configurar opções", você pode configurar o versionamento, logs, tags, registro de atividades e criptografia, mas vamos entrar em mais detalhes mais a frente.
No menu "Definir permissões" é onde configuramos o acesso ao bucket e seus objetos. Por padrão o acesso ao bucket e objetos é bloqueado e é extremamente recomendado que fique dessa forma.No menu "Análise" é possível revisar as configurações feitas nos menus anteriores.
Revise as configurações e clique em "Criar bucket"Nessa tela podemos ver o bucket criado
Clique no bucket para abrir e fazer upload de arquivos.Clique em "Carregar" para fazer upload de objetosClique em "Adicionar arquivo" e escolha o objeto que deseja por no bucketNo menu "Definir permissões" podemos configurar os acessos permitidos ao objeto.No menu "Definir propriedades" é possível escolher em qual serviço do S3 o objeto vai ser armazenado.Além de configurações de criptografia e tagsNo menu "Análise" é possível revisar as configurações feitas nos menus anteriores e por fim fazer o upload do arquivo. Nessa imagem vemos o arquivo já disponível no bucket criado. Clique em cima do objeto para copiar a URL de acesso ao objeto.Depois de clicar no objeto, é possível ver as informações referentes a ele e a URL para acesso público. Copie e cole a URl em algum navegador e tente fazer o acesso
Esse é o resultado de uma consulta a URL de um objeto privado no bucket do S3, mas vamos alterar ele para público...Volte na página do bucket e acesse o menu "Permissões", você vai ver a checkbox "Bloquear todo o acesso público" marcada, desmarque-a e clique em "Salvar"Por segurança, a AWS colocou uma caixa de confirmação para afirmar que essa não é uma ação acidental. Novamente, segundo as melhores práticas, todos os buckets devem ser privados.Após a confirmação, voltei ao objeto, clique em "Tornar público" e copie e cole novamente a URL de acesso ao objeto em um navegador.Como resultado você conseguirá visualizar o objeto.


