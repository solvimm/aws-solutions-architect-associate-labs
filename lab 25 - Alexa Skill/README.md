# Lab 24 - Alexa Skill

## 1. Criado o Lambda de execução

1.1. Como criado no último lab, entre no console da AWS e na aba de Serviços escolha o serviço **Lambda**. Clique em **Create a function**.

1.2. Selecione **Browse serverless app repository**, filtre por **alexa-skills-kit-nodejs-factskill** e selecione esse repositório, depois clique em **Deploy** e aguarde aproximadamente 2 minutos para o final do deploy.

![Image 04](https://d2yblsmsldwfto.cloudfront.net/lab25/lab-25-alexa-skill-01.png)

1.3. Depois disso, selecione o lambda criado no console e copie seu ARN.

## 2. Criando a Skill

2.1. Entre no painel de desenvolvedor da alexa [https://developer.amazon.com/alexa/console/ask](https://developer.amazon.com/alexa/console/ask)

2.2. Entre com seu e-mail pessoal e clique em **Create Skill**

2.3. Crie um nome para skill e selecione **Portuguese (BR)** em Default language e clique em **Create skill**.

2.4. Clique em **Invocation** e escreva a frase que será usada para na Alexa (ex: solvimm treinamentos)

2.5. No canto esquerto clique em **endpoint** e depois em **AWS Lambda ARN** e adicione ARN da sua Lambda no campo default region. Copie o valor do campo ***Your Skill ID**

2.8. Volte no console do lambda e remova o trigger **Alexa Skill Kit**

2.9. Ainda no lambda, clique no para adicionar um novo trigger, escolha o tipo **Alexa Skill Kit** e add o valor do campo ***Your Skill ID** copiado anteriormente e clique em **Add** e depois **Save** no Lambda

2.10. Volte no console de desenvolvimento da Alexa e Clique em **Salve Model**, depois em **Build Model** e espera alguns minutos para o termino.

2.11. Clique Test para entrar na parte de teste das skills. Depois digite ou fale **solvimm treinamentos**
que a Alexa irá chamar o lambda criado anteriormente e depois retornar uma **fan fact em inglês**

2.12. Volta no Console do lambda e edite o código, substituindo a variável data pra (adicine mais linhas no arquivo se desejar:

'''
const data = [
  'O tempo máximo de duração do lambda é de 15 minutos.',
  'Route53 é o serviço de DNS da Amazon.'
];
'''

2.13.  Também substitua o valor da variável **GET_FACT_MESSAGE** para **Aqui vai um fato interessante: **

2.14. Salve o lambda e teste novamente no console da Alexa.

![Image 05](https://d2yblsmsldwfto.cloudfront.net/lab24/lab-24-serverless-04.png)