CLASSIFICADOR DE EMAILS COM N8N --

Automação inteligente de atendimento por e-mail, utilizando o N8N e Gemini pra classificar mensagens e gerar respostas de forma contextual e eficiente.

GERAL --

Este projeto foi desenvolvido pra automatizar o processamento, classificação e resposta de e-mails recebidos em uma conta do Gmail.  
O fluxo distingue entre mensagens do tipo Comercial e Técnico, acionando o agente correto para gerar uma resposta.  

O objetivo é reduzir o tempo de resposta, melhorar a experiência do cliente e padronizar a comunicação, tudo de forma automatizada com IA.

ESTRUTURA--

1. Gmail Trigger 
   - Detecta novos e-mails recebidos e inicia o fluxo.  

2. (IF) 
   - Verifica condições iniciais como remetente, assunto ou palavras-chave.  

3. Padronização  
   - Faz uma limpeza e uniformização do texto do e-mail antes da análise.  

4. Classificador de E-mail 
   - Usa o Google Gemini como modelo para classificar o e-mail em duas categorias:  
     - Comercial — mensagens sobre preços, planos, pagamentos ou contratação.  
     - Técnico — mensagens com dúvidas técnicas, suporte ou problemas em produtos.  

5. Agente Comercial / Agente Técnico
   - Cada agente é um subworkflow, que gera a resposta ideal com base no tipo de e-mail identificado.  

   *Responder E-mail   
   - Envia automaticamente a resposta gerada na mesma thread da mensagem original.

OQ EU USEI --
 [n8n](https://n8n.io)  -------- Plataforma de automação no-code 
 [Google Gemini API](https://ai.google.dev/gemini-api) ------  Classificação semântica e compreensão de texto 
 [Gmail API](https://developers.google.com/gmail/api) ------- Envio e recebimento de mensagens 


SUB AGENTES --

Agente Comercial: responde dúvidas sobre planos, preços, assinaturas e formas de pagamento.  
Agente Técnico: responde dúvidas de suporte, falhas em produtos e instruções técnicas.  

Cada agente possui um prompt personalizado e pode ser treinado o ajustado da forma que você quiser.
