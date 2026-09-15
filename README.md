# Entrega 1 — Modelo Conceitual (DER)
### Modelagem de um sistema de gestão de informações para uma organização de pequeno porte

> Este arquivo é o esqueleto do **README.md** do repositório GitHub do seu grupo.
> Preencha cada seção abaixo. Não apague os títulos — apenas substitua as instruções em *itálico* pelo conteúdo do seu projeto.
> O **DER** é anexado separadamente ao repositório (em imagem), mas sua justificativa entra neste README.
>
> **A organização escolhida pode ser de qualquer natureza:** empresa com fins lucrativos (livraria, lanchonete, pet shop), ONG, associação comunitária, cooperativa, instituições religiosas/comunitárias como igrejas, terreiros de religiões de matriz africana (candomblé, umbanda) ou outras. O que muda de um tipo para outro são os processos e as regras específicas — a estrutura do trabalho (levantamento de requisitos, modelagem conceitual, DER) é a mesma para todas. Termos como "empresa" e "negócio" usados abaixo devem ser lidos de forma ampla, no sentido técnico de modelagem de dados (ex.: "regras de negócio" = regras de funcionamento da organização, seja ela comercial, religiosa ou social).
>
> **Importante:** a organização precisa **existir de fato** — não é permitido inventar uma organização fictícia. O levantamento de requisitos e regras de negócio deve ser feito por meio de **pesquisa de campo na própria organização** (visitas, entrevistas com responsáveis, observação dos processos reais), então o grupo só deve escolher uma organização à qual **realmente tenha acesso**. Ao escolher, tomem cuidado com o porte: **nem tão pequena** que não gere dados suficiente para o trabalho (poucos processos, poucas entidades), **nem tão grande/complexa** que fique inviável de modelar nesta primeira etapa do curso.

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
- Loja comercial com fins lucrativos, de pequeno porte, com uma unidade e 2 pessoas trabalhando atualmente. Realiza vendas e atendimento aos clientes, comercializando diferentes tipos e tamanhos de fantasias.

- **Problemas e necessidades identificados:**
- Falta de controle sobre a entrada e saída de mercadorias, vendas, fechamento de caixa e fluxo de caixa.

- **Justificativa da escolha:**
- A loja foi escolhida por ser acessível ao nosso grupo e por não possuir um sistema de controle. Dessa forma, o projeto poderá propor uma solução para auxiliar no controle de estoque, vendas e fluxo de caixa.
  
- **Evidências da organização:**
- <img width="1600" height="1200" alt="WhatsApp Image 2026-09-15 at 18 51 17" src="https://github.com/user-attachments/assets/5375913f-bdce-4f64-876e-5687abf2521d" />
- https://maps.app.goo.gl/97rXVKvdabmSye7s7
- R. Alexandrino Pedroso, 264 - Loja 16 - Canindé, São Paulo - SP, 03031-030, Brasil
- https://www.instagram.com/lollyfantasias?stkn=MWg5dmlhdmF6ZngyNQ==
- 11 94708-2631

---

## 2. Processos de Negócio


- **Principais processos mapeados:**
CLIENTE
ID: 1 | Nome: Mariana Souza | Telefone: (11) 98765-4321 | Endereço: Av. Paulista, 1000 - São Paulo, SP
ID: 2 | Nome: Carlos Eduardo | Telefone: (21) 99876-5432 | Endereço: Rua das Flores, 45 - Rio de Janeiro, RJ

FUNCIONÁRIO
ID: 101 | Nome: Beatriz Lima | Cargo: Dona | Telefone: (11) 97654-3210
ID: 102 | Nome: Lucas Mendes | Cargo: Vendedor | Telefone: (11) 96543-2109

FORNECEDOR
CNPJ: 12.345.678/0001-90 | Nome: Magia & Fantasias Ltda | Telefone: (11) 3333-4444
CNPJ: 98.765.432/0001-10 | Nome: Distribuidora Cosplay Brasil | Telefone: (41) 3222-1111

FANTASIA
ID Fantasia: 501 | Nome: Fantasia Pirata dos Mares | Gênero: Unissex | Tamanho: M | Categoria: Adulto / Festas | Preço Venda: R$ 180,00 | Qtd Mínima: 2 | Qtd Disponível: 8 | CNPJ Fornecedor: 12.345.678/0001-90
ID Fantasia: 502 | Nome: Capa de Vampiro Clássica | Gênero: Masculino | Tamanho: G | Categoria: Halloween | Preço Venda: R$ 95,00 | Qtd Mínima: 5 | Qtd Disponível: 15 | CNPJ Fornecedor: 98.765.432/0001-10

VENDA
ID: 1001 | Data Venda: 15/10/2026 | Forma Pagamento: Cartão de Crédito | ID Cliente: 1 | ID Funcionário: 101
ID: 1002 | Data Venda: 16/10/2026 | Forma Pagamento: PIX | ID Cliente: 2 | ID Funcionário: 101

ITEM_VENDA
ID: 1 | Quantidade: 1 | Valor Unitário: R$ 20,00 | ID Venda: 1001 | ID Fantasia: 501
ID: 2 | Quantidade: 2 | Valor Unitário: R$ 40,00 | ID Venda: 1002 | ID Fantasia: 502

<img width="3619" height="276" alt="Fluxograma" src="https://github.com/user-attachments/assets/ef0c548a-1762-4364-ac81-30f385c6caba" />

---

## 3. Requisitos do Sistema


### 3.1 Requisitos Funcionais
- O sistema deve 




*O que o sistema precisa FAZER (ex.: "o sistema deve permitir registrar uma venda").*



### 3.2 Requisitos Não Funcionais
Segurança: Login por perfil de usuário e conformidade com a LGPD.

Desempenho: Respostas do sistema em até 3 segundos.

Usabilidade: Tela de caixa simples e aviso visual de estoque baixo.

Disponibilidade: Operacional durante todo o horário comercial.

Confiabilidade: Cancelamento de vendas interrompidas para proteger o estoque.

---

## 4. Regras de Negócio

Regras Operacionais

Venda e Estoque: Vendas só são finalizadas se houver QUANTIDADE DISPONIVEL em estoque.

Alerta de Estoque: Notifica reposição quando o estoque atinge a QUANTIDADE MINIMA.

Vínculo do Pedido: Todo pedido exige um CLIENTE, um FUNCIONÁRIO e ao menos um ITEM_VENDA.

Origem do Produto: Toda fantasia deve estar vinculada a um FORNECEDOR cadastrado.

Restrições Organizacionais

Privacidade (LGPD): Dados do cliente (telefone e endereço) só são armazenados com autorização prévia.

Política de Trocas: Alterações ou cancelamentos exigem autorização do Gerente em até 7 dias.

Pagamentos: O sistema aceita apenas Crédito, Débito, PIX e Dinheiro (sem vendas a prazo).

---
## 5. Dicionário de Dados Conceitual (Preliminar)
*(vale 10% — Dimensão Procedimental - Segue o modelo do arquivo 02-03g_Exemplo_Dicionario_Dados.pdf)*

Para cada entidade identificada, liste:

| Atributo | Descrição | Regra de negócio associada |
|----------|-----------|------------------------------|
| *nome do atributo* | *o que ele representa* | *se houver alguma regra (obrigatoriedade, valores possíveis, etc.)* |

*Mantenha o dicionário organizado e padronizado (mesmo formato de tabela para todas as entidades).*

**Atenção à privacidade:** se forem usados exemplos de valores para ilustrar os atributos, esses exemplos devem ser **fictícios** — não utilize dados reais de clientes, fiéis, beneficiários, doadores ou funcionários da organização (nomes, CPFs, contatos etc.), mesmo que tenham sido observados durante a pesquisa de campo. Os exemplos devem apenas ser **coerentes com as operações reais** observadas.

---

## 6. Modelagem Conceitual (Entidades, Atributos, Relacionamentos)
*(vale 7,5% na dimensão conceitual)*

- **Entidades reconhecidas:** *liste e justifique brevemente cada uma.*
- **Atributos e classificações:** *quais atributos pertencem a cada entidade.*
- **Relacionamentos pertinentes:** *como as entidades se conectam.*
- **Restrições e políticas organizacionais aplicadas ao modelo.**

---

## 7. Diagrama Entidade-Relacionamento (DER)
*(vale 20% — é o item de maior peso da entrega)*

- Anexe o DER (em imagem).
- O diagrama deve representar corretamente:
  - Entidades
  - Atributos
  - Relacionamentos
  - **Cardinalidades**
- O modelo deve ser **consistente** e já demonstrar potencial de **escalabilidade e integração** (pensando nas próximas etapas do projeto).

---

## 8. Justificativa Técnica
*(vale 7,5% — sozinho, é o subcritério de maior peso dentro da Dimensão Conceitual)*

*Explique e defenda as decisões de abstração e modelagem tomadas: por que essas entidades, esses atributos, esses relacionamentos e essas cardinalidades — e não outras alternativas possíveis?*

---

## 9. Uso de Inteligência Artificial


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
