
# Tutorial: Criando um Assistente de Delivery com AWS Step Functions e Bedrock

Este tutorial ensina a criar um Assistente de Delivery usando AWS Step Functions e Bedrock. O objetivo é oferecer uma experiência simples, onde mesmo quem não é da área de tecnologia possa acompanhar.

## Índice
1. [Introdução](#introducao)
2. [Pré-requisitos](#pre-requisitos)
3. [Passo a Passo](#passo-a-passo)
    - [1. Configurando o AWS](#1-configurando-o-aws)
    - [2. Criando o Workflow com Step Functions](#2-criando-o-workflow-com-step-functions)
    - [3. Integrando com Bedrock para Processamento de Texto](#3-integrando-com-bedrock-para-processamento-de-texto)
    - [4. Testando o Assistente](#4-testando-o-assistente)
4. [Conclusão](#conclusao)

---

### Introdução <a name="introducao"></a>
Este tutorial mostra como criar um Assistente de Delivery, ou seja, um sistema que pode organizar e acompanhar pedidos de entrega, enviando atualizações automáticas. Usaremos **AWS Step Functions** para criar um fluxo de trabalho e **AWS Bedrock** para processar e gerar mensagens de texto de forma inteligente.

### Pré-requisitos <a name="pre-requisitos"></a>
- Conta na AWS (com acesso às Step Functions e ao Bedrock).
- Conhecimento básico sobre navegação no AWS Console (opcional).

### Passo a Passo <a name="passo-a-passo"></a>

#### 1. Configurando o AWS <a name="1-configurando-o-aws"></a>
1. Acesse [AWS Console](https://aws.amazon.com/console/).
2. Ative o **AWS Step Functions** e **AWS Bedrock** se ainda não estiverem ativados na sua conta.
3. Crie uma função do IAM com permissões de execução para as Step Functions.

#### 2. Criando o Workflow com Step Functions <a name="2-criando-o-workflow-com-step-functions"></a>
1. No AWS Console, vá até **AWS Step Functions** e clique em **Create State Machine**.
2. Selecione o tipo de execução **Standard**.
3. No editor, comece com um modelo simples. Adicione estados como:
   - **Receber Pedido**: Armazena as informações do pedido.
   - **Confirmar Pagamento**: Checa o status de pagamento.
   - **Notificar Cliente**: Usa o Bedrock para enviar uma mensagem personalizada ao cliente sobre o status do pedido.
4. Salve e dê um nome ao seu workflow, como "Assistente de Delivery".

#### 3. Integrando com Bedrock para Processamento de Texto <a name="3-integrando-com-bedrock-para-processamento-de-texto"></a>
1. Na AWS, abra **Bedrock**.
2. Crie uma função para gerar mensagens com base no status do pedido (exemplo: "Seu pedido está a caminho!").
3. Conecte essa função no seu fluxo de trabalho no Step Functions.

#### 4. Testando o Assistente <a name="4-testando-o-assistente"></a>
1. Volte para o Step Functions e clique em **Test** para rodar o workflow.
2. Insira dados de teste, como um pedido fictício.
3. Veja as mensagens geradas e confirmadas em cada etapa.

### Conclusão <a name="conclusao"></a>
Parabéns! Você criou um Assistente de Delivery que automatiza o acompanhamento de pedidos e notifica clientes. Este exemplo pode ser expandido para outros casos de uso.


### Links Úteis
AWS Step Functions: https://aws.amazon.com/pt/step-functions/

AWS Step Functions Examples: https://github.com/aws-samples/aws-stepfunctions-examples

Serverless e Amazon Bedrock: https://aws.amazon.com/pt/blogs/aws-brasil/como-criar-um-assistente-virtual-de-baixa-latencia-com-multiplos-modelos-usando-serverless-e-amazon-bedrock/

 
