# Monolithic

Autor: Nino Fabrizio Tiriticco Lizardo

O estilo Monolithic feito em Lua 5.1.4.

------------------------------

Funcionamento e lógica:

O estilo segue a base de programas construídos de forma monolítica, ou seja, um bloco inteiro que faz todos os processos necessários para alcançar a finalidade. A autora não faz uso de bibliotecas que façam tarefas muito complexas, reforçando a ideia do código ser monolítico.

O programa usa uma estrutura global para guardar palavras e suas frequências. Ele começa abrindo o arquivo **stop_words.txt** e guardando seu conteúdo em uma outra estrutura.

Em seguida inicia um loop onde pega uma linha do arquivo de leitura a ser analisado a cada iteração. Dentro desse loop existe um outro loop onde se procura identificar o início e fim de palavras na respectiva linha lida, atualizando na estrutura global a frequência de cada palavra se não for stop word.

Se a palavra identificada se encontra na estrutura global, sua frequência é aumentada em 1. Se não se encontra, a palavra é simplesmente adicionada na estrutura e tem atribuída a ela o valor 1 como frequência.

O programa sempre se certifica de que a estrutura esteja em ordem decrescente de frequência, rearrumando a estrutura global quando necessário.

Depois de terminar o loop principal, o programa simplesmente mostra as 25 primeiras entradas da estrutura global.

------------------------------

Para executar:

- Abrir janela do CMD (Windows) ou Terminal (Linux)
- Posicionar a linha de comando no endereço onde se encontra o arquivo
- Digitar **lua Monolithic.lua ../pride-and-prejudice.txt**

------------------------------

Referências:

1 - https://github.com/crista/exercises-in-programming-style/tree/master/03-monolith