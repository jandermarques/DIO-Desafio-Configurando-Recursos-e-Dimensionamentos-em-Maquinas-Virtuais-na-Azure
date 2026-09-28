# ☁️ README - Configurando Recursos e Dimensionamentos em Máquinas Virtuais na Azure

## 📖 Introdução
As **Máquinas Virtuais (VMs)** do Azure são recursos de computação sob demanda que permitem executar sistemas operacionais e aplicações em um ambiente totalmente gerenciado pela nuvem da Microsoft. Elas oferecem flexibilidade para diferentes cenários, desde testes e desenvolvimento até cargas de trabalho críticas em produção.

---

## 🔎 Tipos de Opções de VM no Portal Azure

### 1. **Máquina Virtual do Azure**
- **Descrição**: Criação manual e personalizada de uma VM, escolhendo sistema operacional, tamanho, rede e armazenamento.
- **Vantagens**:
  - Flexibilidade total de configuração.
  - Ideal para cenários específicos ou complexos.
- **Desvantagens**:
  - Processo mais detalhado e demorado.
  - Requer maior conhecimento técnico.

### 2. **Máquina Virtual do Azure com Configuração Predefinida**
- **Descrição**: Modelos prontos com configurações otimizadas (ex.: Windows Server, Ubuntu, Dev/Test).
- **Vantagens**:
  - Agilidade na criação.
  - Configurações recomendadas pela Microsoft.
- **Desvantagens**:
  - Menor flexibilidade.
  - Pode não atender necessidades muito específicas.

### 3. **Mais VMs e Soluções Relacionadas**
- **Descrição**: Catálogo de soluções completas, como clusters de Kubernetes, ambientes SAP ou pacotes de software.
- **Vantagens**:
  - Integração com soluções empresariais.
  - Escalabilidade e automação.
- **Desvantagens**:
  - Complexidade maior.
  - Custos mais elevados.

---

## 🏷️ Modelos de VM e Famílias

| Família | Características | Ideal para |
|---------|-----------------|------------|
| **A-series** | Econômicas, baixo custo | Testes, desenvolvimento, cargas leves |
| **D-series** | Balanceadas, CPU e memória | Aplicações empresariais, bancos de dados pequenos |
| **E-series** | Otimizadas para memória | Processamento de dados, análise, SAP HANA |
| **F-series** | Alto desempenho de CPU | Simulações, cálculos intensivos |
| **M-series** | Grande capacidade de memória | Workloads críticos, bancos de dados grandes |
| **N-series** | GPU dedicada | IA, Machine Learning, renderização gráfica |

---

## ⚙️ Passo a Passo - Criando uma Máquina Virtual no Portal Azure

### 1. Acessar o Portal
- Entre em [portal.azure.com](https://portal.azure.com).
- Faça login com sua conta corporativa ou pessoal.

### 2. Criar um Grupo de Recursos (se necessário)
- No menu lateral, clique em **Grupos de Recursos**.
- Clique em **+ Criar**.
- Defina:
  - Nome do grupo.
  - Região (ex.: *Brazil South*).
- Clique em **Revisar + Criar** e depois em **Criar**.

### 3. Criar a Máquina Virtual
- No menu lateral, clique em **Máquinas Virtuais**.
- Clique em **+ Criar** → **Máquina Virtual do Azure**.

### 4. Configurações Básicas
- **Assinatura**: Selecione sua assinatura.
- **Grupo de Recursos**: Escolha o grupo criado.
- **Nome da VM**: Defina um nome (ex.: `VM-Dev01`).
- **Região**: Escolha a região desejada.
- **Imagem**: Selecione o sistema operacional (Windows, Linux).
- **Tamanho**: Escolha a família e modelo de VM (ex.: D2s_v3).
- **Usuário/Admin**: Defina nome de usuário e senha/chave SSH.

### 5. Configurações de Rede
- **Rede Virtual**: Selecione ou crie uma nova VNet.
- **Sub-rede**: Escolha a sub-rede.
- **IP Público**: Defina se deseja acesso externo.
- **Portas de Entrada**: Configure acesso remoto (RDP para Windows, SSH para Linux).

### 6. Revisar e Criar
- Clique em **Revisar + Criar**.
- Valide as configurações.
- Clique em **Criar**.

---

## 🔑 Permissionamento
O acesso às VMs é controlado pelo **Azure RBAC**:
- **Owner**: Controle total.
- **Contributor**: Gerencia recursos, sem alterar permissões.
- **Reader**: Apenas leitura.
- **Custom Roles**: Criadas para necessidades específicas.

No Portal:
- Vá até o **Grupo de Recursos** ou **VM**.
- Clique em **Controle de Acesso (IAM)**.
- Clique em **+ Adicionar** → **Atribuição de função**.
- Escolha o papel (ex.: Reader).
- Selecione o usuário ou grupo.
- Clique em **Salvar**.

---

## ✅ Conclusão
As Máquinas Virtuais do Azure oferecem flexibilidade para diferentes cenários, desde ambientes simples de teste até workloads críticos. A escolha entre **configuração manual**, **predefinida** ou **soluções completas** depende da necessidade do projeto. Com o passo a passo acima, você pode criar sua primeira VM no Portal Azure de forma prática e segura.
