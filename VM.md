

---

# Como Criar uma Máquina Virtual no Microsoft Azure

Criar uma máquina virtual (VM) no Azure é um processo simples, mas que envolve escolhas importantes que podem afetar o desempenho, a resiliência e o custo do serviço. A seguir, apresento um passo a passo com detalhes sobre as opções de disponibilidade, suas vantagens, características, e como elas influenciam os custos.

---

## 1. Acessando o Portal do Azure

1. Acesse o [Portal do Azure](https://portal.azure.com) com suas credenciais.
2. No painel principal, procure por **Máquinas Virtuais** ou clique em **Criar um Recurso** e selecione **Máquina Virtual**.

![Tela Inicial - Portal do Azure](https://github.com/liliane-sougarc/Projetos-Azure-Dio/blob/main/tela.img/maquinas%20virtuais%201.png)

---

## 2. Configurando a Máquina Virtual

### a) **Assinatura e Grupo de Recursos**
Selecione sua **assinatura** do Azure e o **grupo de recursos** onde deseja criar a VM. Se necessário, crie um novo grupo para organizar melhor seus recursos.

### b) **Região (Localização)**
Escolha a **região** onde a máquina virtual será hospedada. Isso pode influenciar o custo, já que os preços variam entre regiões.

---

## 3. Escolha do Tipo de Máquina Virtual

### a) **Imagem do Sistema Operacional**
Selecione o sistema operacional que sua VM usará, como:

- **Windows Server** (várias versões)
- **Linux** (Ubuntu, Red Hat, CentOS, etc.)

### b) **Tamanho da Máquina Virtual**
O tamanho da VM determina sua capacidade de processamento e armazenamento. As opções variam de acordo com a série:

- **B-series (Básico)**: Adequada para cargas de trabalho leves e intermitentes.
- **D-series**: Equilibrada para cargas de trabalho gerais.
- **F-series**: Otimizada para uso intensivo de CPU.

A escolha do tamanho afeta diretamente o custo da máquina virtual.

---

## 4. Disponibilidade e Redundância

### a) **Conjuntos de Disponibilidade (Availability Sets)**
Utilize **Conjuntos de Disponibilidade** para garantir que suas VMs estejam em racks físicos diferentes no datacenter, protegendo contra falhas de hardware. Essa opção aumenta a **resiliência**, mas também o custo.

### b) **Zonas de Disponibilidade (Availability Zones)**
Com **Zonas de Disponibilidade**, suas VMs são distribuídas entre diferentes datacenters em uma mesma região, proporcionando uma camada extra de redundância. Isso garante maior **alta disponibilidade**, porém a um custo mais elevado.

> **Nota sobre custos**: Zonas de Disponibilidade são mais caras devido à complexidade de infraestruturas necessárias para garantir a resiliência entre diferentes datacenters.

### c) **Escalabilidade e Autoescala**
Se o seu projeto requer escalabilidade, você pode habilitar a **autoescala**, que permite ao Azure ajustar automaticamente a quantidade de recursos (VMs) conforme a demanda. Isso pode aumentar o custo em períodos de alta demanda.

---

## 5. Configuração de Rede e Segurança

- **IP Público**: Decida se a VM terá um IP público para acesso remoto. 
- **Grupo de Segurança de Rede**: Configure as regras de firewall, como a abertura de portas específicas (por exemplo, porta 3389 para RDP ou porta 80 para HTTP).

> **Dica**: Utilize boas práticas de segurança ao configurar as regras de firewall, limitando o acesso ao mínimo necessário.

---

## 6. Revisão e Criação

Após configurar todos os parâmetros da máquina virtual, clique em **Revisar e Criar**. O Azure fará uma verificação de suas configurações. Se tudo estiver correto, clique em **Criar** para iniciar o provisionamento.

![Revisão Final - Criar Máquina Virtual](path/to/image2.png)

O processo de criação pode levar alguns minutos. Após a criação, você poderá acessar a VM usando o IP público ou por meio de uma conexão VPN.

---

## Vantagens de Usar Máquinas Virtuais no Azure

- **Escalabilidade**: Fácil de aumentar ou reduzir a capacidade conforme a demanda.
- **Alta Disponibilidade**: As opções de **Conjuntos de Disponibilidade** e **Zonas de Disponibilidade** ajudam a manter suas VMs funcionando mesmo em caso de falhas de hardware.
- **Custo-Efetivo**: As VMs de **B-series** são ideais para economizar em cargas de trabalho mais leves.
- **Segurança**: Grupos de Segurança de Rede permitem controlar o acesso de forma robusta e eficiente.

---

## Impacto das Escolhas de Disponibilidade nos Custos

- **Conjuntos de Disponibilidade**: Aumentam a resiliência ao distribuir VMs em racks diferentes dentro de um datacenter. O custo extra é justificado pela proteção contra falhas.
- **Zonas de Disponibilidade**: Oferecem redundância entre datacenters em uma mesma região. Isso proporciona uma proteção mais robusta, mas a um custo mais elevado.
- **Escalabilidade**: O uso da autoescala ajusta automaticamente a quantidade de VMs, o que pode gerar variação nos custos conforme a demanda.

Para saber mais sobre preços de máquinas virtuais no Azure, consulte a [Calculadora de Preços do Azure](https://azure.microsoft.com/en-us/pricing/calculator/).

---

Agora você está pronto para criar e gerenciar suas próprias máquinas virtuais no Azure, aproveitando ao máximo as vantagens de escalabilidade, resiliência e segurança.

---

**Imagens**:
1. ![Tela Inicial - Portal do Azure](Apresentacao-Lab-Azure_Dio\tela.img\maquinas virtuais 1.png)
2. ![Revisão Final - Criar Máquina Virtual](Apresentacao-Lab-Azure_Dio\tela.img\maquinas virtuais 2.png)

---

