# assistentedelivery-aws
Resumo da aula: Criando um Assistente de Delivery com AWS Step Functions e Bedrock.

Projetos no Step Functions são chamados: máquina de estado. Cada máquina de estado controla um workflow.

😁Conhecendo um pouco Step Functions!!!

 No Step Functions clique em MÁQUINA DE TRABALHO, escolha um fluxo (pode ser em branco ou pré definido, que pode ser editado).
 
 Mudou de ideia🤔 clique em CANCELAR.
 Agora clique em step Functions, execute um fluxo rápido de trabalho em apenas alguns cliques e comece a usar.
  Clique em EXECUTAR UM HELLO WORD, INICIAR.
  Ao lado esquerdo tem todas as ações que podem ser executadas. Ao clicar em FLUXO é possível fazer tomadas de decisões, onde CHOICE=if; PARALELL  roda as coisas em paralelos; MAP serve para rodar alguns paralelos, mapear e guardar em algum lugar; PASS tranforma dados em outra coisa; WAIT= esperar;SUCESS marca algo como: sucesso; FAIL força uma ação de erro. PROCESS 53 OBJECT; PROCESS CVS FILE IN 53; PROCESS JSON HE IN 53 AGENTE DE SONDAGEM DE TRABALHOS são ações padronizadase pré-prontas.
  Cada "caixinha" é um estado que pode colocar configurações específicas.
 
 🤩Criando um Assistente de Delivery com AWS Step Functions e Bedrock!!!
 
 Clique em MÁQUINA DE ESTADO---NOVA MÁQUINA DE ESTADO---EXECUTE O ENCADEAMENTO DE PROMPTS DE IA COM AMAZON BEDROCK---USAR MODEL---IMPLEMENTAR E EXECUTAR---INICIAR EXECUÇÂO= falha.
  Clique em EDITAR MÁQUINA DE ESTADO---CONFIGURAÇÔES---VISUALIZAR NO IAM---ADICIONAR PERMISSÔES(ANEXAR POLÍTICAS)---ADICIONAR, voltar para o Step Functions, voltar para o projeto e clicar em INICIAR EXECUÇÂO---EDITAR MÁQUINA DE ESTADO---CONFIGURAÇÔES do inspetorr que fica ao lado direito, escolher o modelo da Bedrock e quais serviços utilizar que estejam disponíveis, clicar em EXECUTAR, vai dar erro.
 Clique em VISUALIZAR DETALHES DA ETAPA. Configure os modelos que não estão disponíveis em sua conta do serviço. Clicar na caixa que deu erro e selecionar em configuração e selecionar o modelo ao qual você está habilitado. Aperte em SALVAR---EXECUTAR---INICIAR EXECUÇÃO---STEP FUNCTIONS---CrIAR MÁQUINA DE ESTADOS---BEDROCK---PRÓXIMA---USAR MODELO---IMPLANTAR E EXECUTAR---CANCELAR PROMPT DE TESTE---EDITAR---CONFIGURAÇÂO---VISUALIZAR NO IAM---ADICIONAR PERMISSÕES---ANEXAR POLÍTICAS---PESQUISAR: Bedrock(ADICIONAR PERMISSÕES)--- voltar para o Step Functions---DESIGN---Selecionar os modelos que você tenha permissão---Adicionar nos bloquinhos e SALVAR.
 
 Clique na caixinha CONFIGURAÇÕES--- dentro d:
 "content":[
 )
 "type":
 "text": "ESCREVER O PROMPT QUE DESEJA AO ASSISTENTE DELIVERY"
 saída
 )"result_one.$": Body.generations[0],text" 
 Para configurar o que adicionamos, pegue SAÍDA e transforme dessa forma:
 )"result_one.$: Body.Content[0],text."
 Perceba que alterei na saída o: generations pelo Content (nome do lugar onde escrevi o prompt que desejei).
 Clique em SALVAR---EXECUTAR---colocar nos comentários prompts que não estão vindo no nosso bloquinho, sempre que minha ação não executa no começo posso mandar um Json inicial de entrada. Clique em INICIAR EXECUÇÃO---STATE VIEW.
 
