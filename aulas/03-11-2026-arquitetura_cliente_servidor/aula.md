# Aula

- Data: 03/11/2026
- Disciplina: Desenvolvimento web em HTML5, CSS, JavaScript e PHP
- Tema: Arquitetura cliente-servidor
- Professor:

## Anotações

Fonte: página da disciplina no Notion, exportada em PDF em 03/11/2026. O PDF está em `materiais/`.

### Ideia central

A arquitetura separa tarefas entre cliente e servidor. Cada lado roda em uma plataforma própria, e os dois lados interagem.

### Cliente

Começa a comunicação. Pede o serviço ao servidor e faz a interface com o usuário. Pode ser computador, tablet ou smartphone. O processo tem início e fim definidos.

### Servidor

Oferece o serviço. Em geral é mais robusto, fica ligado o tempo todo, tem mais poder de processamento e atende muita gente ao mesmo tempo. Recebe o pedido, processa e devolve a resposta que o usuário vê.

### Ciclo

Requisição e resposta. O cliente pede um serviço. A aplicação guardada no servidor executa esse serviço. A resposta volta para quem pediu.

### Origem

O modelo surgiu na Xerox PARC, nos anos 1970. A premissa era separar dados e recursos de processamento. No modelo centralizado da época, o mainframe guardava os dados e também processava.

### Ambiente de exemplo

Rede interna de uma empresa. Máquinas servidoras oferecem arquivos, dados, impressão e e-mail. Máquinas clientes consomem esses recursos. No desenho do material, os quatro serviços ficam em cima de uma linha comum e os clientes (1, 2 e N) se ligam por baixo.

### Quatro camadas

O material cita como benefício a separação dos papéis de usuários, aplicações, dados e web. Não explica cada papel.

### GET e POST

Os dois enviam informação.

- GET: a informação vai no endereço.
- POST: a informação vai no corpo da mensagem, e o endereço não muda.

O texto fala em “ambos os arquivos”, mas esses arquivos não vieram no PDF.
