# Tutorial: Criando um Assistente de Delivery com AWS Step Functions e Bedrock
Este tutorial ensina a criar um Assistente de Delivery usando AWS Step Functions e Bedrock. O objetivo é oferecer uma experiência simples, onde mesmo quem não é da área de tecnologia possa acompanhar.

Índice
Introdução
Pré-requisitos
Passo a Passo
1. Configurando o AWS
2. Criando o Workflow com Step Functions
3. Integrando com Bedrock para Processamento de Texto
4. Testando o Assistente
Conclusão
Introdução <a name="introducao"></a>
Este tutorial mostra como criar um Assistente de Delivery, ou seja, um sistema que pode organizar e acompanhar pedidos de entrega, enviando atualizações automáticas. Usaremos AWS Step Functions para criar um fluxo de trabalho e AWS Bedrock para processar e gerar mensagens de texto de forma inteligente.

Pré-requisitos <a name="pre-requisitos"></a>
Conta na AWS (com acesso às Step Functions e ao Bedrock).
Conhecimento básico sobre navegação no AWS Console (opcional).
Passo a Passo <a name="passo-a-passo"></a>
1. Configurando o AWS <a name="1-configurando-o-aws"></a>
Acesse AWS Console.
Ative o AWS Step Functions e AWS Bedrock se ainda não estiverem ativados na sua conta.
Crie uma função do IAM com permissões de execução para as Step Functions.
2. Criando o Workflow com Step Functions <a name="2-criando-o-workflow-com-step-functions"></a>
No AWS Console, vá até AWS Step Functions e clique em Create State Machine.
Selecione o tipo de execução Standard.
No editor, comece com um modelo simples. Adicione estados como:
Receber Pedido: Armazena as informações do pedido.
Confirmar Pagamento: Checa o status de pagamento.
Notificar Cliente: Usa o Bedrock para enviar uma mensagem personalizada ao cliente sobre o status do pedido.
Salve e dê um nome ao seu workflow, como "Assistente de Delivery".
3. Integrando com Bedrock para Processamento de Texto <a name="3-integrando-com-bedrock-para-processamento-de-texto"></a>
Na AWS, abra Bedrock.
Crie uma função para gerar mensagens com base no status do pedido (exemplo: "Seu pedido está a caminho!").
Conecte essa função no seu fluxo de trabalho no Step Functions.
4. Testando o Assistente <a name="4-testando-o-assistente"></a>
Volte para o Step Functions e clique em Test para rodar o workflow.
Insira dados de teste, como um pedido fictício.
Veja as mensagens geradas e confirmadas em cada etapa.
Conclusão <a name="conclusao"></a>
Parabéns! Você criou um Assistente de Delivery que automatiza o acompanhamento de pedidos e notifica clientes. Este exemplo pode ser expandido para outros casos de uso.
