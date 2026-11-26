# Resumo

- Aula: Introdução a banco de dados e SGBD
- Status: concluído

## O tema

Antes do banco de dados, cada programa costumava guardar seus próprios arquivos. Trocar informação entre aplicações era difícil e arriscado: a mesma pessoa ou o mesmo produto podia existir em cópias diferentes.

O Sistema Gerenciador de Banco de Dados (SGBD) centraliza os dados. As aplicações se conectam a ele. Os dados passam a ser naturalmente compartilhados. Uma alteração feita por um sistema fica disponível para os outros que usam o mesmo banco, dentro das regras de permissão e consistência.

## O que é um SGBD

SGBD é o software que cria, guarda, consulta, protege e organiza o banco de dados. Exemplos conhecidos no modelo relacional: MySQL, PostgreSQL, SQL Server, Oracle.

Ele não é a aplicação do usuário. A loja virtual, o app do banco e o sistema acadêmico são aplicações. O SGBD fica no meio: recebe pedidos, acessa os dados e devolve respostas.

## Processamento de dados

O caminho clássico:

1. Entrada: dados chegam (formulário, arquivo, sensor, outra aplicação).
2. Processamento: o computador transforma, calcula, valida, combina.
3. Saída: resultado aparece na tela, num relatório, noutro sistema ou de volta ao banco.

O banco de dados entra nesse ciclo como memória organizada: a saída de um processo pode virar entrada do próximo, sem reinventar o arquivo a cada programa.

## SGBD como middleware

Middleware é o “meio do caminho” entre duas pontas. Na aula, o SGBD é middleware entre a fonte de dados e as aplicações via web.

- De um lado: os dados persistentes.
- Do outro: sites, APIs e sistemas que precisam ler e gravar.
- No meio: o SGBD aplica regras, controla acesso, evita que dois programas estraguem o mesmo registro ao mesmo tempo e devolve o resultado em formato utilizável.

Sem esse meio, cada aplicação web teria de abrir arquivos brutos por conta própria. Com o SGBD, elas falam uma linguagem comum de consulta e gravação.

## Cinco modelos de banco de dados

A história dos bancos não começa no relacional. A aula apresenta cinco modelos, do mais simples ao que ainda busca espaço.

### 1. Modelo flat

Dados em linhas e colunas, como uma planilha ou um arquivo de tabela única. É direto de entender. Fica limitado quando as relações crescem: repetição de informação, pouca flexibilidade e risco de inconsistência.

### 2. Modelo hierárquico

Organiza os dados como uma árvore de cabeça para baixo: um pai, vários filhos. Exemplo mental: empresa → departamentos → funcionários. Bom para relações claras de “um para muitos”. Ruim quando um dado precisa de vários pais ou quando o caminho na árvore não basta.

### 3. Modelo em rede

Evolução do hierárquico. Além de subir e descer na hierarquia, dá para andar lateralmente. Um registro pode se ligar a vários outros com mais liberdade. Ganha poder de modelagem e perde simplicidade: navegar o grafo de ligações é mais trabalhoso.

### 4. Modelo relacional

Várias tabelas relacionadas entre si. Cada tabela tem linhas (registros) e colunas (atributos). A ligação se faz por chaves: por exemplo, o código do cliente na tabela de pedidos aponta para a tabela de clientes.

A aula chama esse modelo de estado da arte no sentido prático: é o mais usado em sistemas comerciais, com SQL como linguagem padrão de consulta. Equilibra estrutura, compartilhamento e ferramentas maduras.

### 5. Modelo orientado a objeto

Guarda dados no formato de objetos, próximos da programação orientada a objetos (atributos + comportamentos). A anotação da aula: ainda não estão em plena utilização e são mais pesados que o relacional. Em muitos projetos, o relacional continua sendo a escolha padrão; objetos aparecem em nichos ou em camadas da aplicação, não necessariamente no lugar do SGBD relacional.

## Comparar em uma olhada

| Modelo | Ideia | Forte em |
| --- | --- | --- |
| Flat | Uma tabela | Simplicidade |
| Hierárquico | Árvore (pai → filhos) | Estruturas rígidas de um para muitos |
| Rede | Ligações em várias direções | Relações mais flexíveis que a árvore |
| Relacional | Tabelas ligadas por chaves | Uso geral; estado da arte prático |
| Orientado a objeto | Dados como objetos | Aproximar banco e código OO |

## Linha do tempo da aula

- Década de 1960: armazenamento em fita magnética. Os dados eram lidos em sequência; acesso era mais lento e físico.
- Década de 1980: cópias de segurança (backup) ainda em fitas magnéticas. A fita continua útil para arquivo e recuperação, mesmo com discos no dia a dia.
- Década de 1990: surge com força o departamento de Tecnologia da Informação. Aparecem os datacenters: salas e prédios preparados para guardar e processar grandes volumes, medidos em TB (terabytes) de dados.

Essa linha mostra o salto: de fita e processamento pontual para ambientes centralizados que alimentam muitas aplicações ao mesmo tempo — o terreno natural do SGBD.

## Curiosidade: Charles Babbage

Charles Babbage (1791–1871) foi um matemático e inventor inglês. Projetou a máquina diferencial e, depois, a máquina analítica: um projeto de computador mecânico programável, com unidade de cálculo, memória e controle por cartões. Na época, a tecnologia da engenharia não chegou a construir a máquina analítica completa como ele imaginava.

A curiosidade entra na aula porque Babbage antecipa a ideia de uma máquina que processa dados de forma automática e reprogramável — o ancestral conceitual do processamento entrada → processamento → saída, muito antes dos SGBDs e dos datacenters.

## Erro comum

Achar que “banco de dados” e “SGBD” são a mesma coisa. O banco é o conjunto organizado de dados. O SGBD é o sistema que gerencia esse conjunto. Outro deslize: achar que só existe o modelo relacional. Ele é o estado da arte prático da aula, mas veio depois do flat, do hierárquico e do em rede.

## Lacunas

A anotação não cita o professor nem nomes comerciais de SGBD. Exemplos de produtos relacionais e o papel de chave nas tabelas foram acrescentados para fechar o tema. Detalhes internos de cada SGBD orientado a objeto não foram inventados além do que a aula registrou (pouco uso pleno; mais pesados que o relacional).
