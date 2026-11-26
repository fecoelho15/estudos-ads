# Aula

- Data: 23/10/2026
- Disciplina: Base computacional / Linguagens de programação
- Tema: Paradigmas e classificação das linguagens
- Professor:

## Anotações

### Classificação por nível

Linguagem de máquina: conjunto de instruções nativas de um processador.

Linguagens de baixo nível: aproximam-se da linguagem de máquina; comunicam-se diretamente com hardware (processador, memória, registradores). Relacionadas à arquitetura. Cada família de processador (ex.: i3, i5, i7) tem seu conjunto de instruções (instruction set).

Instrução em binário (exemplo da aula): palavras de 16 bits — 4 bits para o código da instrução, 6 bits para cada operando.

Programar só em 0 e 1 é complexo → surge Assembly, que usa mnemônicos das instruções reais e precisa ser convertida para máquina.

Exemplo Assembly: mover 2 para AX, mover 1 para BX, somar os registradores.

Pergunta da aula: as linguagens de baixo nível estão próximas ou distantes da língua humana (escrita)? → distantes.

Linguagens de alto nível: afastam-se da máquina e aproximam-se da linguagem humana (em geral, inglês). O programador não precisa conhecer registradores. Exemplos: ASP, C, C++, C#, Pascal, Delphi, Java, JavaScript, Lua, MATLAB, PHP, Ruby…

Um comando de alto nível equivale a várias instruções de hardware. O programador escreve menos código.

C e C++: alguns autores chamam de médio nível (próximas do humano e ainda próximas da máquina). C criada para o UNIX, antes escrito em Assembly.

Algumas pessoas falam em altíssimo nível: Python, Ruby, Elixir (bibliotecas grandes; mais fáceis para iniciantes).

### Gerações

1ª: linguagem de máquina (binário).
2ª: Assembly + assembler (montador).
3ª: procedurais / alto nível (Fortran, BASIC, COBOL, C, Pascal…).
4ª: aplicativas, não procedurais (SQL, PostScript, MATLAB).
5ª: declarativas (Lisp, Prolog); IA, reconhecimento de voz, machine learning.
Alguns autores: 6ª geração ligada a redes neurais.

### Paradigmas

Estruturado (anos 1970–80): sem goto; refinamentos sucessivos; sequência, condição, repetição.

Arquitetura de Von Neumann? O que é?

Python → multiparadigma.

Orientado a objetos: abstrações, atributos e métodos, encapsulamento, herança e polimorfismo. Exemplo Animal / Gato / Cachorro com `emitir_som`.

Declarativo → funcional e lógico.
- Funcional: soluções por funções, composição, recursão.
- Lógico: inferência e dedução a partir de base de conhecimento (ex.: Prolog).

### Tradução

Código de alto nível → compilador → assembly → montador → código objeto → carregador → código objeto relocável → ligador → executável (.exe).

Definir interpretador. Diferença entre tradução × interpretação × compilação. AWS CLI seria um interpretador?
