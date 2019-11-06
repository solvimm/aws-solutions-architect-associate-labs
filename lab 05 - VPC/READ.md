# Lab 05 - VPC (Virtual Private Cloud)

##### 1. Criação de VPC

  1.1. Faça login no console da AWS e acesso o serviço Amazon VPC em: https://console.aws.amazon.com/vpc/

  1.2. No canto superior direito do console, escolha a região na qual deseja criar a sua VPC

  1.3. No canto superior esquerdo, selecione **VPC Dashboard**. Para começar a criar uma VPC, clique em **Launch VPC Wizard**.
￼
  1.4. Na página **Step 1: Select a VPC Configuration**, escolha **VPC with Public and Private Subnets (VPC com sub-redes públicas e privadas)** e depois clique em **Select** (Selecionar).

  1.5 Na página Step 2: VPC with Public and Private Subnets (Etapa 2: VPC com sub-redes públicas e privadas), defina estes valores:
￼
- IPv4 CIDR block (Bloco CIDR IPv4): 10.0.0.0/16
- IPv6 CIDR block (Bloco CIDR IPv6): nenhum bloco CIDR IPv6
- VPC name (Nome da VPC): tutorial-vpc
- Public subnet's IPv4 CIDR (CIDR IPv4 da sub-rede pública): 10.0.0.0/24
- Availability Zone (Zona de disponibilidade): us-west-2a
- Public subnet name (Nome da sub-rede pública): Tutorial public
- Private subnet's IPv4 CIDR (CIDR IPv4 da sub-rede privada): 10.0.1.0/24
- Availability Zone (Zona de disponibilidade): us-west-2a
- Private subnet name (Nome da sub-rede privada): Tutorial Private 1
- Service endpoints (Endpoints de serviço): ignore este campo
- Enable DNS hostnames (Habilitar nomes de host DNS): Yes
- Hardware tenancy (Locação de hardware): Default

  1.6. Ao terminar as configurações, clique em **Create VPC**.


##### 2. Criação de Subnet

  2.1. Para criar uma subnet adicional, acesso novamente pelo console a página da Amazon VPC

  2.2. Para adicionar a segunda subnet privada à VPC, selecione **VPC Dashboard**, escolha **Subnets** e **Create subnet**.
￼
  2.3. Na página **Create Subnet**, defina esses valores:
￼
- Name tag (Tag de nome): Tutorial private 2
- VPC: escolha a VPC que você criou na etapa anterior, por exemplo: vpc-identifier (10.0.0.0/16) | tutorial-vpc
- Availability Zone (Zona de disponibilidade): us-west-2b
- Escolha uma Zona de disponibilidade que é diferente da que você escolheu para a primeira sub-rede privada.
- IPv4 CIDR block (Bloco CIDR IPv4): 10.0.2.0/24

  2.4. Quando terminar, clique em **Create**. Em seguida, clique em **Close** na página de confirmação.

  2.5. Para garantir que a segunda subnet privada que você criou use a mesma tabela de rotas que a primeira, selecione **VPC Dashboard**, clique em **Subnets** e escolha a primeira subnet privada que você criou para a VPC, Tutorial private 1.

  2.5. Abaixo da lista de subnets, selecione a guia **Route Table**, e observe o valor de Route Table, por exemplo, rtb-98b613fd.
￼
  2.6. Na lista de subnets, desmarque a primeira sub-rede privada.

  2.7. Na lista de subnets, escolha a segunda subnet privada Tutorial private 2 e depois escolha a guia **Route Table**.

  2.8. Se a tabela de rotas atual não for a mesma que a tabela de rotas da primeira subnet privada, escolha **Edit route table association**. Em **Route Table ID**, escolha a tabela de rotas que você anotou antes, por exemplo: rtb-98b613fd. Em seguida, para salvar a seleção, clique em **Save**.

