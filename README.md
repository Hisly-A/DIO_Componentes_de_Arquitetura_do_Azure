# DIO - Componentes de Arquitetura do Azure
Construindo Arquiteturas no Azure


## 🔎 Infraestrutura Global da Azure	

> A Azure possui disponibilidade em mais de 60 regiões pelo mundo, e cada uma delas possui uma disponibilidade de serviços, residência de dados e conformidade diferentes, atendendo às regras das regiões onde se localizam.

<sub>Fonte: - <https://azure.microsoft.com/en-us/explore/global-infrastructure/geographies/></sub>


## Criação de um recurso na Azure

Abra o portal da [`Azure`](https://portal.azure.com), clique em **Grupos de recursos** no menu lateral do portal, e após clique em **+ Criar**.

![AZ04-01](https://github.com/user-attachments/assets/aaf27d86-4a4a-4bb1-9ef7-dc9d49da6620)

![AZ04-02](https://github.com/user-attachments/assets/2d830338-6d7d-472a-8506-c3cd4f8041d5)

Na próxima tela preencha os campos necesários nos grupos **Detalhes do projeto** e **Detalhes do recurso**.

![AZ04-03](https://github.com/user-attachments/assets/645778f5-7d57-4bf3-9250-9ef40cc2bd7d)

Após clique em **Avançar: Marcações**:

![AZ04-04](https://github.com/user-attachments/assets/76196b17-dca6-475f-b9cf-2969c1f85e81)

As marcações não são obrigatórias, mas servem para incluir um subtítulo para o recurso correspondente, como forma de detalhar para quê ele serve, se corresponde à um projeto ou centro de custo, o que ajuda a facilitar a identificação dos recursos no momento de receber a fatura pelo uso dos serviços de cloud na Azure.

Caso não deseje incluir uma marcação ou tag, basta clicar em **Avançar: Revisar + criar**.

![AZ04-05](https://github.com/user-attachments/assets/46c4edd6-5f85-4937-8208-4a56bb05bd2e)

Na próxima tela clique em **Criar**: 

![AZ04-06](https://github.com/user-attachments/assets/f2c43a01-059b-44df-a647-504796c64322)

Irá aparecer uma mensagem informando que seu grupo de recursos foi criado:

![AZ04-07](https://github.com/user-attachments/assets/ca9547bb-af30-466e-b66e-1c26e4d7c28e)

Abra o recurso criado e clique na opção **Log de atividade**, esse item armazena os logs de criação, alteração e exclusão e pode ser utlizado em casos de auditoria:

![AZ04-08](https://github.com/user-attachments/assets/13e9407e-15c0-4586-b748-c21f1d22846f)

![AZ04-09](https://github.com/user-attachments/assets/33f13d13-6597-4e89-8cb4-e9f7af87c5b1)

Clique na opção **IAM (Controle de acesso)**, nesta página é possível dar permissionamentos à um usuário ou remover os permissionamentos, sendo que o ideal é dar o menor permissionamento necessário a cada usuário:

![AZ04-10](https://github.com/user-attachments/assets/bea23087-dcbe-4f07-9ef8-390eee8bb9dc)

Na página **Bloqueios** é possível bloquear a exclusão de qualquer recurso:

![AZ04-11](https://github.com/user-attachments/assets/eefdc12b-8117-45eb-a7ea-b80136c0c169)

Na página **Visualizador de recursos** conforme os recursos vão sendo criados será criada automaticamente uma estrutura tipo *árvore da vida* para facilitar a visão:

![AZ04-12](https://github.com/user-attachments/assets/a01a9cd3-5c23-4fc1-adb6-819c4348443b)

Na página **Eventos** ficam os eventos automatizados criados pelos usuários na nuvem.

![AZ04-13](https://github.com/user-attachments/assets/4f72d61a-6b3e-4904-bedd-ebdb2d54c6f2)

![AZ04-14](https://github.com/user-attachments/assets/6f99101b-c6d3-437c-9fed-3e3d8930af60)

Na página **Implantações** se encontrarão as implantações criadas:

![AZ04-15](https://github.com/user-attachments/assets/9f194273-93ef-4ff5-89cf-a07d0ea9ce04)


## Adição de itens no grupo de recursos criado

Nos grupos de recursos também é possível incluir itens criados em outros locais, como por exemplo uma rede virtual.

Para testarmos, saia do grupo de recursos criado e pesquise por Rede Virtual no campo de pesquisa do Azure:

![AZ04-16](https://github.com/user-attachments/assets/36f76c22-8b4f-4a70-8c99-de1e7dd87417)

Clique em **+ Criar**:

![AZ04-17](https://github.com/user-attachments/assets/9515f0e4-6bad-4561-aeb3-73eea9bab3e2)

Informe os dados necessários para a criação e clique em **Analisar + criar**:

![AZ04-18](https://github.com/user-attachments/assets/0e973c94-2924-4fc3-971d-e970597fc266)

Após clique em **Criar**:

![AZ04-19](https://github.com/user-attachments/assets/c6ee59b3-beee-47f8-bbfa-4c99112e7f28)

Aguarde até que a implantação seja concluída:

![AZ04-20](https://github.com/user-attachments/assets/aae8ee60-0155-4361-a47f-7f33e3077a82)

Após a implantação finalizar clique em **Ir para o recurso**:

![AZ04-21](https://github.com/user-attachments/assets/9137c2f0-38c8-4215-9420-f1d322943b59)

Verifique o novo recurso criado:

![AZ04-22](https://github.com/user-attachments/assets/e8150a85-309c-4394-9922-2bff9c06bb81)

Retorne ao grupo de recursos e verifique que a rede virtual criada já se encontra adicionada a ele:

![AZ04-23](https://github.com/user-attachments/assets/801f1985-8b90-4624-974d-5678912a5210)

Repare também que a rede virtual foi criada na região Brazil South, enquanto o grupo de recursos foi criado nos Estados Unidos.

Voltando à página **Visualizador de recursos** é possível ver que a rede virtual criada já foi adicionada.

![AZ04-24](https://github.com/user-attachments/assets/75ab9655-b32d-410d-b7d0-4f6b2fe2c79e)

Na página **Implantações** também já é possível verificar a rede virtual implantada:

![AZ04-25](https://github.com/user-attachments/assets/cb104543-4071-4ce1-9535-52aa4ad1de09)

Também é possível verificar o template da rede virtual criada:

![AZ04-26](https://github.com/user-attachments/assets/88dd1cca-d79c-4cb2-803b-c8f243a78583)

E a página **Log de atividade** foi atualizada com os logs das tarefas executadas na criação da rede virtual:

![AZ04-27](https://github.com/user-attachments/assets/2389b611-5165-481f-8381-dcf1c2eeab75)


## Links utilizados

- https://azure.microsoft.com/en-us/explore/global-infrastructure/geographies/

- https://portal.azure.com/
