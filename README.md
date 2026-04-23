# Automacao-Atendimento-Loja-De-Carros
Este projeto consiste em um fluxo de automação para atendimento via WhatsApp, integrado a uma Inteligência Artificial, focado em otimizar a experiência do usuário e a eficiência do processamento.
1. Controle de Concorrência (Debounce)
Implementei uma lógica de Debounce utilizando Redis para lidar com mensagens enviadas em sequência pelo cliente.

O sistema aguarda um intervalo de 10 segundos antes de processar a resposta.

Caso uma nova mensagem chegue nesse intervalo, a execução anterior é identificada como obsoleta e encerrada automaticamente.

Isso evita respostas duplicadas e reduz custos de processamento de IA.

2. Persistência de Perfil e Estado
Utilizei o Redis como banco de dados em memória para:

Identificação de Usuário: Captura e armazenamento do nome de perfil do WhatsApp para fornecer um atendimento personalizado.

Gestão de Sessão: Controle do tempo de última interação para disparar fluxos de reativação ou transição para atendimento humano.

3. Integração Multimodal
O fluxo está preparado para processar:

Texto: Respostas via modelo de linguagem.

Áudio: Integração com OpenAI Whisper para transcrição e processamento de mensagens de voz.

🛠️ Tecnologias Utilizadas
n8n: Orquestração do fluxo de automação.

Redis: Banco de dados de alta velocidade para controle de estado e cache.

OpenAI API: Inteligência Artificial para processamento de linguagem natural.

WhatsApp API (UAZAPI): Interface de comunicação.
