🇧🇷 Projeto de demonstração de integração de API usando apenas HTML e JavaScript (Frontend). Permite enviar mensagens para um canal do Discord em tempo real via Webhook sem a necessidade de um servidor backend.

⚙️ Explicação Detalhada (README.md)
🚀 Sobre o Projeto
Este é um projeto minimalista e educacional criado para demonstrar o conceito de interoperabilidade e automação entre uma aplicação web (um simples arquivo HTML) e um serviço externo (Discord) através de sua API.

O principal objetivo é enviar mensagens em tempo real para um canal configurado no Discord, provando que é possível executar ações em serviços de terceiros usando apenas código frontend.

🌐 Como Funciona
O projeto se baseia em três pilares técnicos principais:

A URL Secreta (Webhook):

Um Webhook é um endereço HTTP único fornecido pelo Discord, que funciona como uma "caixa de correio" dedicada.

Este endereço é codificado diretamente no JavaScript (hardcoded), o que elimina a necessidade de um campo de URL na interface e simplifica o uso, focando na demonstração.

O Comando JavaScript (fetch):

Ao clicar no botão "Enviar Mensagem", o JavaScript executa a função fetch.

Esta função realiza uma requisição POST (o método usado para enviar dados) diretamente para o endereço do Webhook.

A Linguagem Universal (JSON):

A mensagem e o nome de usuário são formatados em JSON (JavaScript Object Notation), que é o padrão de comunicação para a maioria das APIs web.

O código envia este pacote JSON ao Discord:

JSON

{
  "content": "A mensagem digitada pelo usuário",
  "username": "O nome personalizado"
}
O Discord recebe o pacote JSON, verifica a validade do Webhook e publica a mensagem no canal associado, respondendo com um código de sucesso (204 No Content).

🛠️ Tecnologias Utilizadas
HTML5: Estrutura base da página.

Tailwind CSS (CDN): Estilização rápida e responsiva.

JavaScript: Lógica principal para fazer a requisição API.
