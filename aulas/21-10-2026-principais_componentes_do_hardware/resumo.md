# Resumo

- Aula: Base computacional — principais componentes do hardware
- Status: concluído

## O tema

O computador é um conjunto de peças com papéis claros. A CPU pensa. A RAM guarda o que está em uso agora. O armazenamento guarda o que precisa ficar. A placa-mãe liga tudo. Os periféricos são a ponte com a pessoa.

## Mapa rápido

| Componente | Papel | Sem ele |
| --- | --- | --- |
| CPU | Cérebro: executa instruções | Nada processa |
| RAM | Memória de trabalho | Programas não cabem em execução |
| Placa-mãe | Integra as peças | As peças não se falam |
| Armazenamento | Persistência sem energia | Tudo some ao desligar |
| Periféricos | Interação com o usuário | Não dá para digitar, ver ou ouvir |

## CPU — o cérebro

A CPU (Central Processing Unit) é feita de um número gigantesco de transistores microscópicos. Cada transistor é uma chave minúscula: deixa a corrente passar ou a interrompe. Com bilhões dessas chaves, a CPU executa instruções em sequência e processa dados e comandos.

### Características principais

- Clock (GHz): quantos ciclos a CPU faz por segundo. Um hertz é um ciclo por segundo. Giga = bilhão. Mais clock, em geral, mais oportunidades de trabalho por segundo. Não é o único fator de velocidade.
- IPC (Instruções por ciclo): quantas instruções a CPU consegue avançar em um ciclo de clock. Duas CPUs com o mesmo GHz podem ter desempenho diferente se uma tiver IPC maior.
- Eficiência energética: quanto trabalho entrega por watt. Importante em notebook e celular, onde bateria e calor limitam o desempenho.

Desempenho bruto costuma depender de clock e de IPC juntos. Eficiência diz quanto disso você aguenta sem esgotar a bateria ou superaquecer.

### Tecnologias modernas

- Pipeline: a execução da instrução é dividida em etapas (buscar, decodificar, executar…). Enquanto uma instrução está numa etapa, outra já está na seguinte. É uma linha de montagem.
- Multithreading: um núcleo aparenta executar mais de um fluxo de instruções ao mesmo tempo, aproveitando momentos ociosos.
- Multicore: várias CPUs menores (núcleos) no mesmo chip. Podem trabalhar em paralelo.
- Cache L1, L2 e L3: memórias muito rápidas dentro ou junto da CPU. Guardam dados e instruções que a CPU tende a reutilizar. L1 é a menor e a mais rápida, bem perto do núcleo. L2 é um pouco maior e um pouco mais lenta. L3 é maior ainda e compartilhada entre núcleos em muitos processadores. Sem cache, a CPU ficaria esperando a RAM o tempo todo.

### Curiosidade: transistor nanométrico

O transistor moderno nasce numa pastilha de silício. Em fábricas chamadas fabs, o silício passa por fotolitografia: luz desenha o circuito em camadas, como um carimbo óptico extremamente preciso. Depósitos e corrosões de material criam as regiões que conduzem ou isolam. A medida em nanômetros (nm) indica a escala dessa miniaturização: um nanômetro é um bilionésimo de metro. Quanto menor a escala, mais transistores cabem no mesmo chip. A aula não detalha a química de cada etapa; o ponto é: o “cérebro” do PC é uma cidade de chaves elétricas fabricadas em escala nanométrica.

## RAM — memória de curto prazo

A RAM (Random Access Memory) armazena dados e programas em execução. É a mesa de trabalho: o que está aberto agora fica nela para a CPU acessar rápido.

### Por que curto prazo? Por que some ao desligar?

Porque a RAM comum (DRAM) é volátil. Ela guarda cada bit como uma carga elétrica minúscula em capacitores. Essa carga precisa ser reescrita o tempo todo (refresh). Sem energia, a carga some e o conteúdo some junto. Por isso é memória de curto prazo: serve enquanto o computador está ligado.

O armazenamento secundário (HD/SSD) existe exatamente para o que precisa sobreviver ao desligamento.

### Capacidade, velocidade e barramento

- Capacidade: medida em GB (gigabytes). Mais RAM permite mais programas e arquivos abertos ao mesmo tempo.
- Velocidade: quão rápido a RAM troca dados com o resto do sistema. Impacta o desempenho quando a CPU precisa de muita informação.
- Barramento: o caminho elétrico compartilhado por onde os dados trafegam entre peças (CPU, RAM, chips da placa-mãe). Pense numa avenida: largura e regras de tráfego limitam quantos dados passam por vez. A velocidade da RAM está ligada a como ela conversa com esse barramento.

### DDR1, DDR2, DDR3, DDR4, DDR5

DDR significa Double Data Rate: em termos simples, a memória aproveita melhor cada ciclo para transferir dados. O número (1, 2, 3…) é a geração. Cada geração é mais rápida e, em geral, mais eficiente, mas o encaixe físico e elétrico muda. Um pente DDR4 não entra num slot DDR5. A placa-mãe e a CPU definem qual geração você pode usar.

### Formato

Em desktops e muitos notebooks, a RAM vem em pentes (módulos) que se encaixam na placa-mãe. Em celulares e muitos tablets, os chips de memória ficam soldados na placa, integrados ao dispositivo.

## Placa-mãe — a base

A placa-mãe conecta CPU, memória e periféricos. É a base do sistema: soquete do processador, slots de RAM, conectores de disco, USB, vídeo e rede passam por ela.

### Evolução e onboard

Com o tempo, cada vez mais funções passaram a nascer na própria placa: vídeo, rede, áudio e controladores. Onboard significa integrado: o recurso vem na placa, sem precisar de uma placa extra só para aquilo.

Em celulares, a integração vai além. Muitos usam um SoC (System on a Chip): processador, GPU, controladores e, em arranjos próximos, memória e sensores num pacote muito compacto. A “placa-mãe” do celular é uma placa densa com quase tudo integrado.

## Armazenamento secundário — persistência

Diferente da RAM, o armazenamento secundário mantém os dados sem energia.

### HD (disco rígido)

Usa discos magnéticos que giram. Cabeças de leitura e gravação se movem sobre o prato. É mais lento, tem partes móveis (sujeito a desgaste e a impactos) e costuma oferecer mais capacidade por real.

### SSD (estado sólido)

Não tem prato girando. Guarda dados em chips de memória flash. É mais rápido e, em uso comum, mais resistente a tombos. Interfaces frequentes:

- SATA: conexão mais antiga, ainda comum; limita o teto de velocidade do SSD.
- NVMe: conexão moderna, em geral pelo barramento PCI Express; permite SSDs bem mais rápidos.

## Periféricos

São as peças de interação com o usuário e com o mundo: teclado, mouse, monitor, impressora, webcam, fone. Sem eles, o sistema processa e guarda, mas a pessoa não conversa com a máquina.

## Erro comum

Confundir RAM com SSD. Os dois “guardam”, mas em papéis diferentes. RAM é mesa de trabalho (volátil). SSD/HD é armário (persistente). Outro deslize: achar que só o GHz define a CPU. IPC, núcleos, cache e eficiência também pesam.

## Lacunas

A anotação não cita o professor nem marcas específicas. A explicação de cache, barramento, gerações DDR e a visão geral da fabricação nanométrica foram acrescentadas para responder às perguntas da aula, sem inventar detalhes de processo químico que não foram dados.
