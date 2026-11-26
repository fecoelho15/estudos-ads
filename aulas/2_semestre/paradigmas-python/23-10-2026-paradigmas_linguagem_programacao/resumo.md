# Resumo

- Aula: Paradigmas e classificação das linguagens de programação
- Status: concluído

## O tema

Linguagens de programação se classificam por **nível** (quão perto estão da máquina ou do humano), por **geração** (histórico de abstração) e por **paradigma** (estilo de pensar o problema). Por baixo de tudo isso, o processador só entende bits.

## Classificação por nível

### Linguagem de máquina

É o conjunto de instruções nativas do processador. Só 0 e 1. Cada família de CPU (por exemplo, linha Intel i3, i5, i7) tem seu **instruction set**. Um programa em máquina de um processador não serve, em geral, para outro.

No exemplo da aula, uma instrução tem 16 bits: 4 bits para o código da operação e 6 bits para cada operando. Programar assim é possível, mas extremamente difícil de ler, escrever e depurar.

### Baixo nível

Aproxima-se da máquina e fala com hardware: processador, memória e registradores. Está ligada à arquitetura. A resposta da aula: as linguagens de baixo nível estão **distantes** da língua humana escrita.

**Assembly** foi o avanço: em vez de decorar sequências de bits, usam-se mnemônicos (`MOV`, `ADD`) das instruções reais. Ainda assim, o código Assembly precisa ser convertido para linguagem de máquina por um **assembler** (montador).

Exemplo mental da aula: colocar 2 no registrador AX, 1 no BX e somar. Em Python, a mesma ideia vira algo como `resultado = 2 + 1`, sem falar em registrador.

### Alto nível

Afasta-se da máquina e aproxima-se da linguagem humana (quase sempre em inglês). O programador não precisa conhecer registradores nem o instruction set. Uma linha de alto nível vira várias instruções de hardware. Exemplos citados na aula: ASP, C, C++, C#, Pascal, Delphi, Java, JavaScript, Lua, MATLAB, PHP, Ruby, entre outras.

### Médio nível e “altíssimo” nível

Alguns autores colocam **C** e **C++** no médio nível: sintaxe legível, mas com acesso direto a memória e registradores. A linguagem C nasceu para desenvolver o UNIX, antes escrito em Assembly.

Há quem chame Python, Ruby e Elixir de altíssimo nível: muita biblioteca pronta e curva mais suave para iniciantes. Isso é classificação informal, não uma regra única da indústria.

## Gerações das linguagens

| Geração | Nome na aula | Ideia |
| --- | --- | --- |
| 1ª | Máquina | Só binário; máxima eficiência; máxima dificuldade |
| 2ª | Assembly | Mnemônicos + assembler |
| 3ª | Procedurais / alto nível | Variáveis, if, loop, funções; Fortran, BASIC, COBOL, C, Pascal… |
| 4ª | Aplicativas | Dizer o *quê*, não o *como*; SQL, PostScript, MATLAB |
| 5ª | Declarativas | Lisp, Prolog; IA, voz, machine learning |
| 6ª (alguns autores) | Evolução da 5ª | Ênfase em redes neurais |

### 3ª geração — propriedades em comum (aula)

- Tipos simples e estruturados
- Alocação dinâmica (ponteiros)
- Controle sequencial, condicional, repetição e (historicamente) desvio
- Programação modular com parâmetros
- Operadores relacionais, lógicos e aritméticos
- Ênfase em simplicidade e eficiência

### 3ª × 4ª geração

- 3ª: procedural — você descreve o passo a passo.
- 4ª: não procedural — você declara o resultado desejado. SQL é o melhor exemplo da aula: `SELECT ... FROM ... WHERE ...` diz o que buscar, não o algoritmo interno do SGBD.

## Arquitetura de Von Neumann

É o modelo clássico de computador em que **programa e dados compartilham a mesma memória**, e a CPU busca instruções e dados por um caminho comum (o “gargalo” de Von Neumann). Em oposição a arquiteturas que separam de forma rígida memória de instruções e de dados.

Por que aparece nesta aula: linguagens de baixo nível e Assembly trabalham perto desse modelo — registradores, endereços de memória, sequências de instruções que a CPU busca e executa uma após a outra.

## Paradigmas

Paradigma é o estilo dominante de organização do programa.

### Estruturado

Fortes nas décadas de 1970 e 1980. Evitar `goto` (desvio incondicional). Desenvolver por refinamentos sucessivos. Usar sequência, condição e repetição. Alinha-se à 3ª geração procedural.

### Orientado a objetos (OO)

Organiza o software em objetos com **atributos** (dados) e **métodos** (comportamentos). Usa **encapsulamento** (esconder detalhes internos), **herança** (reaproveitar e especializar) e **polimorfismo** (a mesma mensagem, comportamentos diferentes).

No exemplo da aula, `Animal` tem `emitir_som`. `Gato` e `Cachorro` herdam e sobrescrevem o método: “miau” e “au au”. Todo animal “nasce” e “emite som”, mas cada espécie realiza o som à sua maneira — ideia do método polimórfico.

Aula: OO favorece desenvolvimento mais rápido e confiável pelo uso amplo de abstrações.

### Declarativo: funcional e lógico

- **Funcional:** o programa é composição de funções. O retorno da função é a solução. Funções chamam funções; o resultado de uma pode ser argumento de outra. Uso intenso de **recursão** (a função chama a si mesma).
- **Lógico:** base de conhecimento + regras; o motor faz **inferência** e dedução. Exemplo clássico: Prolog. Relacionado, na aula, à base de funcionamento de sistemas de IA simbólica.

### Python: multiparadigma

Python permite programar de forma procedural/estruturada, orientada a objetos e com trechos funcionais. Por isso a aula o chama de multiparadigma: não força um único estilo.

## Tradução, compilação e interpretação

### Tradução (sentido amplo)

Converter o programa de uma linguagem (em geral de alto nível) para uma forma que a máquina execute — tipicamente linguagem de máquina ou um código intermediário.

### Compilação (pipeline da aula)

Caminho clássico até o executável:

1. Código de alto nível
2. Compilador → gera assembly (ou código intermediário)
3. Montador (assembler) → código objeto
4. Carregador → decide onde alocar na memória (objeto relocável)
5. Ligador (linker) → junta partes e bibliotecas
6. Código executável (`.exe` no Windows)

O programa é traduzido **antes** de rodar. Depois, o sistema só carrega e executa o binário.

### Interpretador

Programa que lê o código-fonte (ou um bytecode) e **executa sob demanda**, instrução a instrução ou trecho a trecho, sem gerar necessariamente um `.exe` completo no início. Exemplos típicos: interpretador Python, motores de JavaScript em muitos contextos.

### Compilação × interpretação × tradução

| Ideia | Quando vira máquina | Exemplo mental |
| --- | --- | --- |
| Tradução | Termo guarda-chuva para qualquer conversão | Compilar ou interpretar são formas de traduzir |
| Compilação | Antes da execução; gera artefato (objeto/executável) | C → `.exe` |
| Interpretação | Durante a execução; o interpretador “conduz” o código | `python script.py` |

Na prática moderna há híbridos: Java e Python podem compilar para bytecode e depois interpretar ou compilar sob demanda (JIT). A aula fixa a distinção clássica.

### AWS CLI é um interpretador?

**Não no sentido da aula.** AWS CLI é uma ferramenta de linha de comando: lê seus comandos, chama APIs da Amazon e devolve respostas. Ela não é o interpretador de uma linguagem de programação como Python ou Prolog. Pode até ser escrita em uma linguagem interpretada, mas o papel dela é cliente de nuvem, não “tradutor/executor de programa-fonte” no sentido de geração de linguagens.

## Erro comum

Achar que alto nível é “lento demais para valer” ou que baixo nível é sempre melhor. Baixo nível dá controle e eficiência potencial; alto nível dá produtividade e portabilidade. Achar que SQL é procedural como C: SQL é 4ª geração — declara o resultado. Achar que AWS CLI = interpretador de linguagem.

## Lacunas

A anotação não traz o professor nem as imagens do material online. O exemplo OO incompleto (“cada ra…”) foi fechado com o padrão Animal/Gato/Cachorro da própria aula. A 6ª geração aparece só como menção de alguns autores.
