# Lab 11 - CloudWatch


# 1. Criação do Alarme

1.1. Acesse o console do CloudWatch em https://console.aws.amazon.com/cloudwatch/home. Atenção para utilizar a mesma região onde foram criadas instâncias EC2 nos labs anteriores.

![Image 01](https://d2yblsmsldwfto.cloudfront.net/lab11/lab-11-cloudwatch-01.png)


1.2. No menu do lado esquerdo da tela, clique em **Alarms**.

![Image 02](https://d2yblsmsldwfto.cloudfront.net/lab11/lab-11-cloudwatch-02.png)

1.3. Clique em **Create alarm**.

1.4. Nesta página você vai observar o gráfico de métricas e os diferentes tipos de métricas pré-existentes pela AWS que podemos escolher. Métricas de EBS, EC2, Logs, e SNS. Escolha quais métricas gostaria de usar e clique em Select Metric. Abaixo seguem exemplos de métricas para EC2:

![Image 03](https://d2yblsmsldwfto.cloudfront.net/lab11/lab-11-cloudwatch-03.png)


1.5. Para este lab, vamos escolher a métrica para utilização de CPU para a máquina EC2 que já tínhamos criado. Caso a CPU ultrapasse 70% o alarme dispara. Selecione **CPUUtilization** para o InstanceId da EC2 criada e clique em **Select metric**.


1.6. Em **Metric name**, defina um nome para a métrica.

1.7. Em **Period** escolha o período em que essa análise vai ser realizada. Para este lab, selecione 5 minutos.

![Image 04](https://d2yblsmsldwfto.cloudfront.net/lab11/lab-11-cloudwatch-04.png)


1.7. Em conditions mantenha em **Static** e selecione **Greater/Equal** para que o alarme avise quando a métrica ficar com valor igual ou superior a 70%, e clique em **Next**.

![Image 05](https://d2yblsmsldwfto.cloudfront.net/lab11/lab-11-cloudwatch-05.png)


1.8. Para notificação, deixe a opção padrão **In alarm**. Para SNS Topic, deixe o padrão e no campo *Send a notification to* inclua um email para receber a notificação em caso de acionamento do alarme. Clique next, adicione uma descrição se necessário e crie o alarme.

![Image 06](https://d2yblsmsldwfto.cloudfront.net/lab11/lab-11-cloudwatch-06.png)


# 2. Acionamento do Alarme

2.1. Para acionar o alarme, acesse a máquina via SSH ou pelo console.

2.2. Para fazer a utilização de CPU ultrapassar 70%, execute o seguinte comando no terminal:

```
$ fulload() { dd if=/dev/zero of=/dev/null | dd if=/dev/zero of=/dev/null | dd if=/dev/zero of=/dev/null | dd if=/dev/zero of=/dev/null & }; fulload; read; killall dd
```

2.3. Aguarde 5 minutos. Você receberá um email como o exemplo a seguir:

![Image 07](https://d2yblsmsldwfto.cloudfront.net/lab11/lab-11-cloudwatch-07.png)