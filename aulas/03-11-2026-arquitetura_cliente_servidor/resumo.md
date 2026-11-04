# Resumo

- Aula: Arquitetura cliente-servidor
- Status: concluído

## O tema

Na web, quem pede e quem atende não precisam ser a mesma máquina. A arquitetura cliente-servidor divide o trabalho: o cliente pede um serviço e mostra o resultado para a pessoa; o servidor guarda a aplicação, executa o pedido e responde. Cada lado pode estar em uma plataforma diferente. O que liga os dois é o ciclo de requisição e resposta.

Isso vale para o navegador no computador, no tablet ou no celular. O aparelho muda. O papel não muda: quem usa inicia o pedido; quem serve processa e devolve.

## Cliente e servidor

O cliente é a ponta da pessoa. Ele abre a conversa, requisita o serviço e faz a interface: tela, formulário, clique. O pedido tem começo e fim. Terminou a resposta, aquele ciclo acabou. O próximo clique começa outro.

O servidor é a ponta que disponibiliza o serviço. No material, ele aparece como máquina mais robusta, ligada o tempo todo, com mais capacidade de processamento e preparada para um número grande de usuários ao mesmo tempo. Não é “o computador da pessoa, só que maior”. É o lado que fica esperando pedidos e responde a muitos clientes.

| Papel | O que faz | No exemplo cotidiano |
| --- | --- | --- |
| Cliente | Inicia, pede, mostra | Navegador no celular pedindo uma página |
| Servidor | Recebe, processa, responde | Máquina que guarda o site e devolve a página |

## Requisição e resposta

O caminho descrito no material é curto:

1. O cliente solicita um serviço.
2. A aplicação que está no servidor executa esse serviço.
3. O servidor devolve uma resposta.
4. O usuário vê essa resposta.

Sem o pedido, o servidor não tem o que fazer para aquela pessoa. Sem a resposta, o cliente fica sem resultado. Os dois lados só fazem sentido juntos.

## De onde veio esse modelo

O material situa a criação na Xerox PARC, nos anos 1970. A premissa era separar duas coisas que, até então, moravam juntas: os dados e o processamento.

No modelo centralizado da época, o mainframe fazia os dois trabalhos. Guardava a informação e também calculava. O cliente-servidor quebra essa concentração: uma máquina pode guardar e oferecer o recurso; outras máquinas só consomem.

## O exemplo da rede da empresa

O ponto de partida do material é a rede interna de uma empresa, não ainda um site na internet.

Em cima da rede ficam servidores, cada um com um serviço:

- arquivos
- dados
- impressão
- e-mail

Embaixo ficam os clientes: Cliente 1, Cliente 2 e Cliente N. Todos se ligam à mesma linha e usam o que os servidores oferecem. O Cliente 1 não precisa ter a impressora, o arquivo e o correio dentro dele. Ele pede. O servidor correspondente entrega.

Esse desenho deixa a separação visível: poucos serviços compartilhados, muitos clientes consumindo.

## O que o material chama de quatro camadas

O texto aponta um benefício forte desse modelo: separar os papéis dos usuários, das aplicações, dos dados e da web. A frase está no material. A explicação de cada papel não está. O PDF ainda diz que um vídeo trataria desse modelo; o vídeo não veio na exportação.

## GET e POST

Perto do fim, o material compara duas formas de enviar informação. As duas mandam dados. Muda o lugar onde esses dados viajam.

- No GET, a informação vai no endereço. A URL carrega o que foi enviado, então o endereço muda conforme os dados.
- No POST, a informação vai no corpo da mensagem. O endereço permanece o mesmo.

O parágrafo fala em “ambos os arquivos”, como se houvesse dois exemplos de arquivo na página. Esses arquivos não apareceram no PDF: as páginas do meio da exportação saíram em branco, e sobrou só essa comparação.

Um jeito concreto de guardar a diferença, sem ir além do que o texto diz: buscar um nome numa página pode colocar esse nome no endereço (`.../busca?nome=ana`). Enviar os mesmos campos por POST deixa o endereço da página quieto e manda os campos no corpo do envio.

## Erro comum

Tratar cliente e servidor como a mesma coisa em máquinas diferentes, ou achar que “servidor” é só um computador mais potente. No material, a diferença é de papel: um pede e conversa com a pessoa; o outro oferece o serviço, processa e responde, em geral para muita gente e o tempo todo.

Outro deslize é achar que GET e POST são iguais porque os dois enviam informação. O material separa os dois pelo lugar: endereço, no GET; corpo da mensagem, no POST, com o endereço intacto.

## Lacunas

O PDF não traz o professor. As páginas 4 e 5 da exportação estão em branco: o título “Aplicações no modelo cliente X servidor” ficou sem conteúdo, e os “dois arquivos” citados no trecho de GET e POST não estão no arquivo. O modelo de quatro camadas é só nomeado (usuários, aplicações, dados e web), sem definição de cada camada. O exemplo do endereço com `busca?nome=ana` foi acrescentado para fixar a diferença escrita no material; ele não aparece no PDF.
