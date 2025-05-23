# Resumo do Lab
Repositório contendo o resumo das lições aprendidas durante o desenvolvimento do lab na DIO.

# Microsoft Azure - Localizando Serviços por Categoria

## Tipos de Nuvem
- **Nuvem Pública**: Serviços oferecidos por provedores externos (Azure, AWS, Google Cloud) via internet, com pagamento por uso. Ideal para escalabilidade e redução de custos iniciais.
- **Nuvem Privada**: Infraestrutura dedicada a uma organização, oferecendo controle total e segurança reforçada. Pode ser hospedada localmente ou por terceiros.
- **Nuvem Híbrida**: Combinação dos modelos público e privado, permitindo flexibilidade para migrar cargas de trabalho conforme necessidades de segurança, custo ou conformidade.

## Modelos de Custos
### CAPEX (Capital Expenditure)
- Investimentos iniciais em hardware, infraestrutura e instalação.
- Registrado como ativo no balanço patrimonial, com depreciação ao longo do tempo.

### OPEX (Operational Expenditure)
- Gastos recorrentes com manutenção, energia e serviços gerenciados.
- Registrado como despesa operacional no período de uso.
- **Vantagem em nuvens públicas**: Elimina CAPEX inicial e permite pagamento proporcional ao consumo.

## Benefícios do Modelo Baseado em Consumo
- **Controle financeiro**: Pague apenas pelos recursos utilizados.
- **Escalabilidade**: Ajuste rápido de capacidade conforme demanda.
- **Eficiência**: Desligue recursos ociosos para otimizar custos.

## Serviços do Microsoft Azure
O Azure oferece soluções categorizadas para diversas necessidades:
- **Computação**: Máquinas virtuais, funções serverless.
- **Armazenamento**: Bancos de dados, blobs, tabelas.
- **Rede**: VPNs, balanceadores de carga, firewalls.
- **DevOps**: Pipelines de CI/CD, monitoramento.
- **Segurança**: Bastion Host, gerenciamento de identidade.


# Criando máquinas Virtuais na Azure

# Laboratório Prático: Criação de Máquina Virtual no Azure

## Processo Completo de Criação da VM

### 1. Configuração Básica
![Tela de configuração da VM](/images/vm-config.png)
*Configurações básicas da máquina virtual*

- **Assinatura**: Azure subscription 1
- **Grupo de recursos**: Lab-DIO_group
- **Nome da VM**: Lab-DIO
- **Região**: Brazil South
- **Tamanho**: Standard B1s (0.020 USD/hora)

### 2. Status de Implantação
A implantação foi concluída com sucesso:

![Implantação concluída](/images/next-steps.png)
*Confirmação de implantação bem-sucedida*

**Detalhes:**
- **Hora de início**: 23/05/2025, 19:00:11
- **ID de Correlação**: f37b7870-e6ab-41b5-a9e2-7466ea7dc4a9
- **Recursos criados**: VM, interface de rede, NSG, rede virtual e IP público


# Configurando uma instância de Banco de Dados na Azure

## 📌 Configuração do Servidor SQL
![Tela de criação do servidor](/images/db/server-config.png)
- **Nome do servidor**: `sqlserver-dio.database.windows.net`
- **Localização**: `Brazil South`
- **Autenticação**:
    - SQL + Microsoft Entra ID
    - Usuário admin: `vrobls`
- **Segurança**: Senha complexa definida

## 🛠️ Configuração do Banco de Dados
![Tela de criação do BD](/images/db/db-config.png)
- **Detalhes básicos**:
    - Nome: `db-dio-lab`
    - Camada: `Uso Geral`
    - Computação: `1 vCore`
    - Armazenamento: `32GB` (Redundância geográfica)
- **Rede**:
    - TLS 1.2 obrigatório
    - Acesso público restrito

## ✅ Implantação Concluída
![Tela de conclusão](/images/db/deployment-complete.png)
- **Status**: Criado com sucesso
- **ID da implantação**: `09c656d7-6de2-4167-8547-7e743ae5fbac`
- **Recursos criados**:
    - Servidor: `sqlserver-dio`
    - Banco de dados: `db-dio-lab`
    - Regras de conexão padrão

