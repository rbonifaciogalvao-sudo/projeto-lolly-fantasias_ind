# Entrega 1 — Modelo Conceitual (DER)
---

## Metadados

- **Nomes dos alunos e RGM**
- Rafaela Bonifacio Galvão - 48178837
- Wilchid Vilsaint - 47443227
- Yago Lima de Queiroz - 48140597


## 1. Caracterização da Organização

- **Nome e natureza da organização:**
-Lolly Fantasias. Loja especializada na venda de fantasias infantis e adultas.

- **Contexto e porte:**
- Loja comercial com fins lucrativos, de pequeno porte, com uma unidade e 2 pessoas trabalhando atualmente. Realiza vendas e atendimento aos clientes, comercializando diferentes tipos e tamanhos de fantasias. A organização trabalha com diferentes categorias de fantasias, como Halloween, super-heróis, profissões e princesas.

- **Problemas e necessidades identificados:**
- A Lolly Fantasias apresenta dificuldades relacionadas ao controle e à organização das informações de suas atividades. Atualmente, não existe um controle sistematizado da entrada e saída de fantasias, das vendas realizadas, do fechamento de caixa e do fluxo de caixa. Também não há um controle adequado que permita acompanhar de forma organizada a quantidade de fantasias disponíveis em estoque. Essa falta de controle pode dificultar o acompanhamento das movimentações da loja e a consulta das informações necessárias para a realização das atividades. Dessa forma, identifica-se a necessidade de um sistema que permita organizar e centralizar essas informações, facilitando o controle do estoque, das vendas e das movimentações financeiras da organização.

- **Justificativa da escolha:**
- A loja foi escolhida por ser acessível ao nosso grupo e por não possuir um sistema de controle. Dessa forma, o projeto poderá propor uma solução para auxiliar no controle de estoque, vendas e fluxo de caixa.
  
- **Evidências da organização:**
- <img width="1600" height="900" alt="WhatsApp Image 2026-10-02 at 16 30 11" src="https://github.com/user-attachments/assets/ccd48c83-9b6d-43a6-b547-eedf4791bfdd" />
- https://maps.app.goo.gl/97rXVKvdabmSye7s7
- R. Alexandrino Pedroso, 264 - Loja 16 - Canindé, São Paulo - SP, 03031-030, Brasil
- https://www.instagram.com/lollyfantasias?stkn=MWg5dmlhdmF6ZngyNQ==
- (11) 94708-2631

---

## 2. Processos de Negócio

Atendimento e venda de fantasias: o cliente solicita uma ou mais fantasias, o funcionário verifica a disponibilidade, entrega as fantasias disponíveis e, após o pagamento, a venda é finalizada.
Verificação de disponibilidade: quando a quantidade de fantasias disponível na loja não é suficiente para atender à solicitação do cliente, o funcionário consulta o estoque para verificar e buscar as unidades restantes.
Abastecimento de fantasias: a loja realiza o recebimento de fantasias provenientes de fornecedores para manter os produtos disponíveis para venda.



*(vale 10% — Dimensão Procedimental)*

- **Principais processos mapeados:** *ex.: cadastro de clientes/beneficiários/fiéis, controle de estoque ou doações, vendas ou arrecadação, emissão de pedidos ou solicitações, entregas ou distribuição, organização de eventos/rituais/mutirões.*








- **Fluxogramas:** 
- <img width="1252" height="123" alt="image" src="https://github.com/user-attachments/assets/4eda3731-07f9-4f20-a531-aca333b033c3" />

---

## 3. Requisitos do Sistema
### 3.1 Requisitos Funcionais

O sistema deve permitir registrar a entrada de novas fantasias no estoque e controlar a saída das mercadorias quando uma venda for realizada. Dessa forma, será possível acompanhar a quantidade disponível de cada fantasia e identificar quando o estoque estiver baixo.
O sistema deve permitir registrar as vendas realizadas, informando as fantasias vendidas, suas respectivas quantidades, os valores e, quando necessário, o cliente relacionado à venda. O registro deve permitir consultar as vendas realizadas posteriormente.
O sistema deve permitir realizar o fechamento do caixa ao final do período, registrando e conferindo os valores movimentados durante o atendimento. O objetivo é possibilitar a conferência dos valores recebidos por meio das vendas.
O sistema deve permitir acompanhar as movimentações financeiras relacionadas às vendas, possibilitando visualizar os valores recebidos e auxiliar no controle financeiro da loja.






### 3.2 Requisitos Não Funcionais

- Segurança: Login por perfil de usuário e conformidade com a LGPD.
- Desempenho: O sistema deverá apresentar respostas às operações realizadas pelo usuário em até 3 segundos.
- Usabilidade: Tela de caixa simples e aviso visual de estoque baixo.
- Disponibilidade: Operacional durante todo o horário comercial.
- Confiabilidade: Cancelamento de vendas interrompidas para proteger o estoque.

---

## 4. Regras de Negócio

Regras Operacionais

- Venda e Estoque: Vendas só são finalizadas se houver QUANTIDADE DISPONIVEL em estoque.
- Alerta de Estoque: Notifica reposição quando o estoque atinge a QUANTIDADE MÍNIMA.
- Vínculo do Pedido: Todo pedido exige um CLIENTE, um FUNCIONÁRIO e ao menos uma VENDA.
- Origem do Produto: Toda fantasia deve estar vinculada a um FORNECEDOR cadastrado.
- Privacidade (LGPD): Dados do cliente (telefone e endereço) só são armazenados com autorização prévia.
- Pagamentos: O sistema aceita apenas Crédito, Débito, PIX e Dinheiro (sem vendas a prazo).

---
## 5. Dicionário de Dados Conceitual (Preliminar) 

'''''''''''''''HTML''''''''''''''''

"Cliente"

 Atributo | Descrição                 | Regra de negócio associada     |

NOME      |Nome do cliente.           |Deve ser informado no cadastro. |
TELEFONE  |Nº de telefone do cliente. |Pode ser utilizado para contato.|
ENDEREÇO  |Endereço do cliente.       |Deve ser informado quando necessário para entrega.|


"Funcionário"

| Atributo | Descrição                     | Regra de negócio associada                         |
|ID        |ID do funcionário.             |Deve ser atribuído na contratação e deve ser único. |
|NOME      |Nome do funcionário.           |Deve ser informado na contratação.                  |
|CARGO     |Cargo do funcionário.          |Deve corresponder à função do funcionário.          |
|TELEFONE  |Nº de telefone do funcionário. |Deve ser informado na contratação.                  |


"Venda"

| Atributo       | Descrição          | Regra de negócio associada                                              |
|ID_CLIENTE      |Id do cliente.      |Pode ficar sem preenchimento quando o cliente não estiver cadastrado.    |
|FORMA_PAGAMENTO |Forma utilizada para realizar o pagamento da venda.  |Deve ser informada no registro da venda.|
|DATA_VENDA      |Data em que a venda foi realizada.                   |Deve ser registrada no momento da venda.|



"Fantasia"

| Atributo             | Descrição | Regra de negócio associada |
|ID_FANTASIA           |Código identificador da fantasia. |Deve ser informado no cadastro da fantasia e deve ser único.|
|GÊNERO                |Gênero ao qual a fantasia é destinada. |Aceitar apenas valores definidos, Feminino ou Masculino.|
|NOME                  |Nome da fantasia.        |Deve ser informado no cadastro. |
|TAMANHO               |Tamanho da fantasia.     |Deve ser informado no cadastro. |
|CATEGORIA             |Categoria da fantasia.   |Deve pertencer a uma categoria cadastrada.|
|VALOR_UNITÁRIO        |Preço de cada item.     |Deve ser maior que zero. |
|QUANTIDADE_MINIMA |Quantidade mínima que deve ter no estoque. |A quantidade mínima de itens no estoque deve ser superior a 10.|
|QUANTIDADE_DISPONIVEL |Quantidade disponível no estoque. |Não pode ser negativa. |


"Fornecedor"

| Atributo | Descrição              | Regra de negócio associada |
|NOME      |Nome do fornecedor.     |Deve ser informado no cadastro do fornecedor.|
|TELEFONE  |Telefone do fornecedor. |Deve ser informado no cadastro do fornecedor.|
|CNPJ      |CNPJ do fornecedor.     |Deve ser único e informado no cadastro do fornecedor.|


---

## 6. Modelagem Conceitual (Entidades, Atributos, Relacionamentos)

- Cliente: representa as pessoas que realizam as compras na loja.
- Funcionário: representa a pessoa responsável pelo atendimento aos clientes e registro de vendas.
- Fantasia: representa os produtos que são comercializados na loja.
- Venda: representa cada venda realizada.
- Fornecedor: representa a pessoa responsável por vender as fantasias para a loja.

---

- Cliente: ID_cliente, nome, telefone e endereço.
- Funcionário: ID_funcionario, nome, cargo e telefone.
- Fantasia: ID_fantasia, gênero, nome, tamanho, categoria, valor unitário, quantidade mínima e quantidade disponível.
- Venda: ID_venda, data e forma de pagamento.
- Fornecedor: ID_fornecedor, nome, telefone e CNPJ.

---

- Um Cliente pode efetuar nenhuma ou várias Vendas. (Cliente 0,N — Venda 0,1) 
- Uma Venda pode estar associada a nenhum ou a um Cliente. (Venda 0,1 — Cliente 0,N)
- Um Funcionário pode realizar nenhuma ou várias Vendas. (Funcionário 0,N — Venda 1,1)
- Uma Venda é realizada por um único Funcionário. (Venda 1,1 — Funcionário 0,N)
- Uma Fantasia está relacionada a um Fornecedor, enquanto um Fornecedor pode estar relacionado a várias Fantasias.  (Fantasia 1,1 — Fornecedor 0,N)
- Uma Venda deve conter uma ou várias Fantasias. (Venda 1,N — Fantasia 1,N)
- Uma Fantasia pode estar presente em uma ou várias Vendas. (Fantasia 1,N — Venda 1,N)

---

- Um cliente pode estar ou não cadastrado para conseguir realizar uma venda.
- Uma venda deve possuir pelo menos um item, garantindo que não exista uma venda sem produto.
- Cada venda deve estar associada a um Funcionário, permitindo identificar quem realizou o registro.
- Uma Fantasia deve estar associada a um Fornecedor, conforme a organização do cadastro de produtos.

---

## 7. Diagrama Entidade-Relacionamento (DER)


<img width="1112" height="671" alt="image" src="https://github.com/user-attachments/assets/c76557de-5dd6-46ee-aad2-10640ae79119" />


---

## 8. Justificativa Técnica
As entidades CLIENTE, FUNCIONÁRIO, VENDA, FANTASIA e FORNECEDOR foram escolhidas por representarem os principais elementos identificados durante a entrevista realizada com a loja. A definição das entidades buscou representar os aspectos mais relevantes do funcionamento da organização e possibilitar um maior controle das informações.

Os atributos da entidade FANTASIA foram definidos com base na forma como a própria loja identifica e organiza suas fantasias. Dessa forma, foram considerados dados como gênero, nome, tamanho, categoria, valor e quantidade disponível. Também foram adicionados identificadores (ID) às entidades para garantir que cada registro pudesse ser identificado de forma única, evitando ambiguidades e facilitando os relacionamentos entre as entidades.

A entidade CLIENTE foi mantida no modelo mesmo que a loja atualmente não possua um cadastro de clientes, pois, no sistema proposto, seu registro possibilitaria relacionar vendas aos respectivos clientes. Isso pode contribuir para o controle das operações, identificação de possíveis irregularidades e análise das vendas, permitindo observar quais produtos apresentam maior movimentação e retorno para a loja.

A entidade FUNCIONÁRIO foi incluída porque o funcionário é responsável pela realização das vendas e pelo atendimento na loja. O relacionamento entre FUNCIONÁRIO e VENDA permite identificar quem realizou cada operação, facilitando o controle das vendas mesmo em situações de troca ou desligamento de funcionários.

A entidade VENDA foi criada para possibilitar um controle mais sólido e específico das vendas realizadas pela loja, registrando informações importantes de cada operação. Já a entidade FORNECEDOR foi incluída para identificar a origem das fantasias adquiridas pela loja. Dessa forma, caso uma fantasia apresente algum problema, como falta de itens ou defeito, será possível identificar o fornecedor responsável.

Em relação às cardinalidades, CLIENTE e VENDA foram relacionados de forma que uma venda possa ocorrer sem um cliente cadastrado ou estar relacionada a um único cliente cadastrado, pois o cadastro de clientes é opcional. FUNCIONÁRIO e VENDA foram relacionados considerando que cada venda é realizada por um funcionário, enquanto um mesmo funcionário pode realizar várias vendas.

A relação entre VENDA e FANTASIA considera que uma venda pode conter uma ou várias fantasias, pois a loja pode realizar vendas tanto no varejo quanto no atacado. Da mesma forma, uma mesma fantasia pode estar presente em várias vendas, pois as fantasias não são itens únicos, permitindo que diferentes clientes adquiram o mesmo modelo e tamanho.

A relação entre FANTASIA e FORNECEDOR permite que uma fantasia esteja relacionada a vários fornecedores e que um fornecedor forneça várias fantasias. Essa decisão considera que diferentes fornecedores podem oferecer modelos semelhantes ou iguais, inclusive com preços diferentes.

Durante a modelagem, a entidade ITEM_VENDA foi retirada porque seus atributos representavam informações que poderiam ser diretamente associadas à entidade FANTASIA. Dessa forma, esses atributos foram incorporados à FANTASIA, evitando informações duplicadas e tornando o modelo mais adequado à realidade observada na loja.

Assim, as decisões de abstração e modelagem foram tomadas a partir das informações obtidas na entrevista e das necessidades identificadas para o sistema proposto, buscando representar os principais elementos da loja, evitar duplicidade de informações e estabelecer relacionamentos que correspondam ao funcionamento das vendas, dos produtos, dos funcionários e dos fornecedores.


## 9. Uso de Inteligência Artificial

*(documentação obrigatória — não é opcional se o grupo usou IA em qualquer etapa: pesquisa, escrita, organização de ideias ou revisão de texto)*

Se o grupo usou alguma ferramenta de IA (ChatGPT, Claude, Gemini, Perplexity etc.) em qualquer parte do trabalho, registre **para cada uso relevante**:

| Item | O que registrar |
|------|------------------|
| **Ferramenta e etapa** | Qual IA foi usada e em qual parte do trabalho (ex.: pesquisa sobre o setor da organização, redação do README, organização dos requisitos, revisão ortográfica/gramatical). |
| **Motivação** | Por que o grupo recorreu à IA nesse ponto específico. |
| **Prompt(s) utilizados** | Texto exato (ou muito próximo) do que foi perguntado/pedido à IA. |
| **Resposta recebida** | Resumo ou trecho relevante da resposta da IA. |
| **Fontes consultadas e verificadas** | Se a IA citou fontes/dados, quais foram checadas pelo grupo e como (ex.: comparação com o que foi observado na visita de campo). |
| **Trechos rejeitados ou corrigidos** | O que da resposta da IA foi descartado, editado ou corrigido manualmente, e por quê. |
| **Justificativa da escolha final** | Por que o grupo manteve, adaptou ou rejeitou o que a IA sugeriu. |
| **Reflexão crítica** | Limites, vieses ou erros identificados no uso da IA nessa etapa (ex.: informação desatualizada, alucinação, generalização incorreta sobre o tipo de organização). |

*Se o grupo não usou nenhuma ferramenta de IA, declare isso explicitamente nesta seção.*

---

## Critérios Atitudinais (20%)
**Estes critérios NÃO constam explicitamente como item de entrega no README.** Eles são avaliados por meio de **Avaliação 360º entre os integrantes do grupo** (cada membro avalia os colegas de equipe) e, no caso da Colaboração, também pela **colaboração equilibrada no histórico de commits** do repositório GitHub — não pela leitura do restante do repositório nem pela apresentação:

- **Participação (5%):** envolvimento nas discussões técnicas e nas decisões do grupo.
- **Comprometimento (5%):** cumprimento de prazos e responsabilidades assumidas.
- **Colaboração (5%):** respeito às contribuições dos colegas, cooperação na construção do projeto e colaboração equilibrada no histórico de commits do repositório GitHub.
- **Autonomia (5%):** busca independente de soluções e proposta de melhorias.

---

## Resumo dos Pesos

| Dimensão | Peso total |
|----------|-----------|
| Conceitual (contexto, requisitos/regras, modelagem, justificativa técnica) | 30% |
| Procedimental (requisitos, fluxogramas, dicionário de dados, DER) | 50% |
| Atitudinal (participação, comprometimento, colaboração, autonomia) | 20% |

**Entrega final:** README.md completo + DER + Dicionário de Dados em HTML (com exceção dos cursos GTI) anexado no repositório GitHub do grupo.








### **Uso de Inteligência Artificial**

| Item | O que registrar |
| --- | --- |
| **Ferramenta e etapa** | **Gemini (Google)** — Utilizada nas etapas de organização de requisitos, criação de dados fictícios, estruturação da modelagem conceitual, elaboração do Dicionário de Dados e mapeamento de regras de negócio a partir do DER. |
| **Motivação** | Agilizar a estruturação teórica do relatório, garantir a padronização das tabelas de requisitos e obter exemplos de dados fictícios coerentes com o Diagrama Entidade-Relacionamento da loja de fantasias. |
| **Prompt(s) utilizados** | • *"cria os dados fictícios de um cliente de uma loja de fantasias e para a loja tambem, de acordo com as coisas que tem na imagem"* <br>

<br> • *"3.2 Requisitos Não Funcionais (...) diminui"* <br>

<br> • *"Regras de Negócio (...) diminui"* <br>

<br> • *"6. Modelagem Conceitual (...) e o 6 seria como"* <br>

<br> • *"5. Dicionário de Dados Conceitual (...)"* |
| **Resposta recebida** | Resumos estruturados de Requisitos Não Funcionais, tabelas e listas de dados fictícios, descrição detalhada dos pilares da modelagem conceitual (entidades, atributos, relacionamentos, restrições) e a estrutura completa em tabelas para o Dicionário de Dados. |
| **Fontes consultadas e verificadas** | Validação manual do modelo conceitual gerado comparando-o diretamente com o Diagrama Entidade-Relacionamento (DER) fornecido para garantir total consistência dos nomes de campos e cardinalidades. |
| **Trechos rejeitados ou corrigidos** | As primeiras respostas de Requisitos Não Funcionais e Regras de Negócio foram descartadas por serem muito extensas; foram solicitadas versões mais diretas e resumidas para adequação ao relatório. |
| **Justificativa da escolha final** | Mantiveram-se as versões resumidas dos Requisitos, das Regras de Negócio e o formato tabular do Dicionário de Dados, pois garantem clareza técnica e objetividade na documentação do projeto. |
| **Reflexão crítica** | A IA auxiliou na velocidade de escrita e organização dos tópicos. Contudo, foi necessária supervisão constante para garantir que os nomes dos atributos e cardinalidades não desviassem do DER original. |

---

### **Resumo da Avaliação e Entregáveis**

Como lembrete para o fechamento do seu projeto:

* **Critérios Atitudinais (20%):** Garantidos através do histórico de *commits* no GitHub e da Avaliação 360º (Participação, Comprometimento, Colaboração e Autonomia).
* **Estrutura Final do Repositório:** O arquivo `README.md` principal deve conter todas as seções (Requisitos, Processos, Regras de Negócio, Modelagem Conceitual e Uso de IA), acompanhado da imagem do DER e da versão HTML do Dicionário de Dados.

*(documentação obrigatória — não é opcional se o grupo usou IA em qualquer etapa: pesquisa, escrita, organização de ideias ou revisão de texto)*

Se o grupo usou alguma ferramenta de IA (ChatGPT, Claude, Gemini, Perplexity etc.) em qualquer parte do trabalho, registre **para cada uso relevante**:

| Item | O que registrar |
|------|------------------|
| **Ferramenta e etapa** | Qual IA foi usada e em qual parte do trabalho (ex.: pesquisa sobre o setor da organização, redação do README, organização dos requisitos, revisão ortográfica/gramatical). |
| **Motivação** | Por que o grupo recorreu à IA nesse ponto específico. |
| **Prompt(s) utilizados** | Texto exato (ou muito próximo) do que foi perguntado/pedido à IA. |
| **Resposta recebida** | Resumo ou trecho relevante da resposta da IA. |
| **Fontes consultadas e verificadas** | Se a IA citou fontes/dados, quais foram checadas pelo grupo e como (ex.: comparação com o que foi observado na visita de campo). |
| **Trechos rejeitados ou corrigidos** | O que da resposta da IA foi descartado, editado ou corrigido manualmente, e por quê. |
| **Justificativa da escolha final** | Por que o grupo manteve, adaptou ou rejeitou o que a IA sugeriu. |
| **Reflexão crítica** | Limites, vieses ou erros identificados no uso da IA nessa etapa (ex.: informação desatualizada, alucinação, generalização incorreta sobre o tipo de organização). |

*Se o grupo não usou nenhuma ferramenta de IA, declare isso explicitamente nesta seção.*

---

## Critérios Atitudinais (20%)
**Estes critérios NÃO constam explicitamente como item de entrega no README.** Eles são avaliados por meio de **Avaliação 360º entre os integrantes do grupo** (cada membro avalia os colegas de equipe) e, no caso da Colaboração, também pela **colaboração equilibrada no histórico de commits** do repositório GitHub — não pela leitura do restante do repositório nem pela apresentação:

- **Participação (5%):** envolvimento nas discussões técnicas e nas decisões do grupo.
- **Comprometimento (5%):** cumprimento de prazos e responsabilidades assumidas.
- **Colaboração (5%):** respeito às contribuições dos colegas, cooperação na construção do projeto e colaboração equilibrada no histórico de commits do repositório GitHub.
- **Autonomia (5%):** busca independente de soluções e proposta de melhorias.

---

## Resumo dos Pesos

| Dimensão | Peso total |
|----------|-----------|
| Conceitual (contexto, requisitos/regras, modelagem, justificativa técnica) | 30% |
| Procedimental (requisitos, fluxogramas, dicionário de dados, DER) | 50% |
| Atitudinal (participação, comprometimento, colaboração, autonomia) | 20% |

**Entrega final:** README.md completo + DER + Dicionário de Dados em HTML (com exceção dos cursos GTI) anexado no repositório GitHub do grupo.
