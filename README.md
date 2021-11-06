# Alinhamento de sequências

Alinhamento de sequências é o jeito mais eficiente e simples de estabelecer relações funcionais, estruturais e evolutivas entre sequências. Existe o alinhamento local e global. Nesse caso, estamos interessados no algoritmo de Needleman Wunsch que faz o alinhamento global.

## Alinhamento global

Faz o alinhamento da sequência inteira

Adequado para sequências intimamente relacionadas

## Needleman Wunsch

É um método computacional para gerar alinhamentos ótimos entre duas sequências.

Ele compara cada posição das duas sequências e gera um alinhamento.

### Componentes do alinhamento de sequências

- Match - acontece quando os elementos das duas sequências na mesma posição são iguais
- Mismatch - acontece quando os elementos das duas sequências na mesma posição não são iguais
- Gap - acontece quando o tamanho da sequência atual é menor do que o tamanho da outra sequência

### Score

Reflete a qualidade do alinhamento. O score final é a soma das penalidades e recompensas durante a execução.

- Penalidades são aplicadas caso aconteça um mismatch ou um gap durante o alinhamento.
    
    Mismatch -1
    
    Gap -2
    
- Recompensas são atribuídas caso aconteça um match entre as sequências.
    
    Match +1
    

## Programação Dinâmica

Consiste em pegar um problema, dividi-lo em pequenas partes e resolver esses sub-problemas. Utilizaremos este método no desenvolvimento do algoritmo.

## Pseudo-código

1. Inicializar uma matriz N+1 x M+1, onde N é o tamanho da primeira sequência e M é o tamanho da segunda sequência.
    1. M[0,0] = 0
2. Preencher a matriz da direta pra esquerda e de cima pra baixo usando o esquema de score de forma recursiva.
3. Fazer o traceback.