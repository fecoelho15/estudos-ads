# Resumo

- Aula: Base computacional — a evolução dos computadores em quatro gerações
- Status: concluído

## O tema

A base computacional desta aula é a troca do componente que representa o bit. Esse componente só precisa fazer uma coisa: deixar a corrente passar ou interrompê-la. Ligado e desligado são esses dois estados. Cada geração troca a chave, não o significado do bit. Com a troca, a máquina fica menor, gasta menos energia, custa menos e sai do laboratório.

Dois problemas puxam essa história. A Enigma mostra um cálculo grande demais para uma pessoa terminar a tempo. A Apollo mostra uma máquina que precisava caber na cápsula. As quatro gerações são o caminho entre esses dois limites.

## Ligado, desligado, corrente e bit

No computador digital, a menor informação cabe em dois estados. A aula chama esses estados de ligado e desligado. Eles descrevem a corrente elétrica no circuito.

A corrente é o movimento de cargas elétricas pelo condutor. A válvula, o transistor e o transistor dentro do chip funcionam como uma chave sobre essa corrente.

- Ligado: a chave deixa a corrente passar. O ponto do circuito fica num nível alto de tensão.
- Desligado: a chave interrompe a corrente. O mesmo ponto fica num nível baixo, próximo de zero.

O bit (binary digit, dígito binário) é o nome dessa informação. A máquina não guarda a palavra "ligado". Ela guarda um de dois níveis de tensão, e a leitura converte o nível em número. A convenção mais comum é:

- nível alto, corrente passando, lê-se como 1
- nível baixo, corrente interrompida, lê-se como 0

Um bit é um único 0 ou um único 1. Vários bits juntos passam a representar números, letras e instruções. Uma lâmpada acesa ou apagada já é um bit. No computador, no lugar da lâmpada, há um nível de tensão.

A ideia do bit não muda de uma geração para outra. O que muda é a chave que abre e fecha a corrente: da válvula enorme ao transistor microscópico do microprocessador.

## O que foi visto

### Dois problemas

Na Segunda Guerra, a Alemanha cifrava mensagens com a Enigma. As combinações eram tantas que testá-las à mão não cabia no tempo da guerra. Alan Turing, em Bletchley Park, ajudou a transformar esse teste num procedimento de máquina. O nome na anotação aparece como Allan; a grafia é Alan. O ponto da aula não é a biografia: um estado ligado ou desligado, repetido em escala, enfrenta um problema que a pessoa não fecha sozinha.

O projeto Apollo precisava de computador a bordo: leve, pequeno e confiável. Não havia como levar uma máquina do tamanho de uma sala. O Apollo Guidance Computer, usado na cápsula, foi construído com circuitos integrados. A restrição de espaço empurra a miniaturização que as gerações seguintes realizam.

### Geração 1 — válvulas termiônicas (anos 1940)

A válvula conduz ou interrompe a corrente. Esse é o ligado ou desligado da primeira geração. O componente era grande, frágil, esquentava e consumia muita energia.

O caso da aula é o ENIAC, apresentado em 1946: cerca de 18 mil válvulas, uma sala inteira e dezenas de quilowatts. Ele marca o início da era digital eletrônica e também o limite dela. A máquina calculava, mas quase não saía do laboratório.

### Geração 2 — transistores (anos 1950)

O transistor foi criado em 1947, nos Bell Labs. Nos computadores dos anos 1950, ele substitui a válvula. Os primeiros ocupavam alguns milímetros e gastavam bem menos energia. Caem o tamanho, o calor, o consumo e o custo. Rádios e outros eletrônicos encolhem pelo mesmo motivo. A aula chama isso de início da microeletrônica.

### Geração 3 — circuitos integrados (anos 1960)

O circuito integrado, o chip, é uma pastilha de silício com um circuito inteiro miniaturizado. Em vez de montar milhares de peças uma a uma, muitas delas nascem na mesma pastilha. A ideia aparece no fim dos anos 1950 (Jack Kilby em 1958 e Robert Noyce em 1959) e chega aos computadores na década de 1960.

É aqui que o computador deixa de ser só equipamento de pesquisa e passa a ser produto comercial. O exemplo de tamanho da própria aula continua valendo: o computador da Apollo cabe na cápsula porque usa circuitos integrados, não válvulas.

### Geração 4 — microprocessadores

O microprocessador concentra a unidade central de processamento num único chip. O primeiro comercial é o Intel 4004, de 1971. A aula olha para o efeito disso na década de 1980: PCs mais potentes, mais baratos e ligados por redes locais e pela internet, a rede mundial.

O videogame entra como computador especializado. O programa é o jogo. O que esse aparelho destaca é o gráfico e a interação com quem joga, não uma planilha nem um cálculo científico.

## Por que importa

Sem a troca de componente, o computador permanece uma sala quente e cara. A válvula prova que dá para calcular com estados elétricos. O transistor prova que dá para fazer isso pequeno. O circuito integrado prova que dá para vender a máquina. O microprocessador prova que ela cabe em casa, no trabalho e num console.

## Exemplo

O ENIAC ocupa uma sala e queima válvulas. Um chip de microprocessador ocupa a palma da mão e faz o papel da unidade central. Entre os dois está a exigência da Apollo: se a máquina não diminuir, ela não viaja.

## Erro comum

Tratar circuito integrado e microprocessador como a mesma coisa. Todo microprocessador é um circuito integrado. Nem todo circuito integrado é um microprocessador. O chip da geração 3 pode ser memória ou um circuito específico. O da geração 4 é a CPU inteira num chip.

Outro deslize é datar a geração 4 só pelos anos 1980. O componente nasce em 1971. Os anos 1980 são a década em que PC, rede e videogame se espalham, que é o recorte da aula.

## Lacunas

A anotação não traz o professor, não descreve a física interna da válvula nem do transistor, e não avança para uma quinta geração. A relação entre corrente, ligado/desligado e bit foi acrescentada para fechar o tema, no nível da chave elétrica.
