Billing Alarm Lab

AWS Budget

Abra o console do AWS Budget em 
https://console.aws.amazon.com/billing/home?#/budgets

Na parte superior da página, escolha Create budget (Criar orçamento)



Em Select budget type (Selecionar tipo de orçamento), escolha Cost budget (Orçamento de custo)






Escolha Set up your budget (Configurar seu orçamento).


Em Name (Nome), insira o nome do orçamento. O nome do orçamento deve ser exclusivo na sua conta e pode usar A-Z, a-z, espaços e os seguintes caracteres: _.:/=+-%@.
Em Period (Período), escolha a frequência com que você deseja que o orçamento redefina o gasto previsto e real. O período pode ser Monthly (Mensal), Quarterly (Trimestral) para cada três meses e Annually (Anual) para todo ano. 

 
Você também pode personalizar futuros valores previstos em orçamento para Monthly (Mensal) e Quarterly (Trimestral) usando o recurso de planejamento do orçamento.


Em Budgeted Amount (Valor orçado), informe o valor total que você deseja gastar nesse período de orçamento. Em Orçamentos de planejamento Monthly (Mensal) e Quarterly (Trimestral), insira o valor que você deseja gastar em cada período planejado.


 
 
 
Escolha Configure alerts (Configurar alertas).


Em Configure alerts (Configurar alertas), para Alert 1 (Alerta 1), escolha Actual (Real) para criar uma notificação para gastos reais e Forecast (Previsão) para criar uma notificação para gastos previstos. Em Alert threshold (Limite de alerta), insira o valor para o qual você deseja ser notificado. Insira um valor absoluto ou uma porcentagem. Por exemplo, para um orçamento de 200 USD, se você quiser ser notificado ao atingir 160 USD (80% de seu orçamento), insira 160 para um orçamento absoluto ou 80 para uma porcentagem do orçamento.





Ao lado do valor, escolha Dollar amount para ser notificado quando o valor limite é ultrapassado e % of budgeted amount (% do valor orçado) para ser notificado quando a porcentagem limite do orçamento é ultrapassada.
(Opcional) Em Email contacts (Contatos de e-mail), digite os endereços de e-mail para os quais você deseja que as notificações sejam enviadas e escolha Add email contact (Adicionar contato de e-mail). Separe vários endereços de e-mail com uma vírgula. Uma notificação pode ter até 10 endereços de e-mail.


Escolha Confirm budget (Confirmar orçamento)










Revise as configurações do orçamento e escolha Create (Criar).






-----



Billing Alarm Lab

Criando um alarme de Billing

Abra o console do CloudWatch em https://console.aws.amazon.com/cloudwatch/.

OBS: Se necessário, altere a região para Leste dos EUA (Norte da Virgínia). Os dados de métrica de faturamento são armazenados nessa região e representam as despesas em todo o mundo.

Na parte esquerda da página, escolha Billing 


Em Bliing, escolha Create Alarm





Em Specify metric and conditions, você tem os seguintes parâmetros Metric name (nome da metrica), Currency (Moeda), Static e Period (Período)



Em Conditions, observe que possuem dois tipos de Threshold. O primeiro é Static (onde é usado um valor como limite) e o segundo é Anomaly detection (onde é usado uma banda como limite). Escolha o primeiro (Static). Logo abaixo, está o campo Whenever EstimatedCharges is… , lá é onde você definirá a condição do alarme em relação ao limite determinado (maior, maior ou igual, menor ou igual e menor). E em than… será necessário definir o valor limite (valor que deve estar em dólares). Feito isso, escolha Next.



Em Configure actions será necessário criar um SNS Topic (Tópico do SNS). Selecione Create new topic. Em Create a new topic… determine o nome do tópico (o nome deve ser único). E o email que irá receber a notificação. Após isso escolha create topic.
Um ponto importante é que após criar o tópico, vá ao email que foi informado na criação, e clique no link para realizar o subscribe no Tópic. Por fim, escolha Next.



Em Add a description, defina o nome do alarme e uma descrição (opcional) do mesmo. Por fim, escolha Next.



Após isso, confira todas as informações referentes a criação do alarme e clique em Create Alarm.



