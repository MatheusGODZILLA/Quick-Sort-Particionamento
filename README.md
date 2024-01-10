# QuickSort: Análise dos métodos de particionamento

Instituto Federal do Piauí (IFPI) - Curso superior de Análise e Desenvolvimento de Sistemas - Módulo II

Projeto de implementação e teste da execução do algoritmo Quick Sort com o uso de duas técnicas de particionamento: Hoare e Lomuto para a disciplina de Estrutura de Dados I

Equipe: Marcos Paulo e Matheus da Silva

## -> Descrição do trabalho
No Quicksort, a parte mais importante do trabalho ocorre no passo de Particionamento e, por isso, várias estratégias foram criadas e aprimoradas. 

A primeira delas é a versão do próprio criador do algoritmo, Charles Antony “Tony” Richard Hoare. Outro método importante de nota é o método de Lomuto. 

Neste trabalho os alunos em dupla deverão testar a execução do algoritmo Quick Sort com o uso destas duas técnicas de particionamento. Para isso deverá ser utilizado vetores de números inteiros de tamanhos 100, 500, 1000, 5000, 30000, 80000, 10000, 150000 e 20000. 

Deverá ser realizado uma análise (através de gráficos) da quantidade de trocas realizadas por cada método e o tempo de execução em milissegundos de cada um.

## -> Funcionamento dos Métodos: 
O objetivo de um algoritmo de particionamento é dividir um array em dois subarrays, um com todos os elementos menores ou iguais a um elemento pivô e outro com todos os elementos maiores ou iguais ao pivô.

### - Hoare
No método Hoare, escolhe-se um elemento como pivô (geralmente o primeiro elemento do array). Em seguida, iniciamos dois índices, um no início do array e outro no final do array. Movemos o índice do início para a direita até encontrar um elemento maior que o pivô e movemos o índice do final para a esquerda até encontrarmos um elemento menor que o pivô. Se os índices não se cruzarem, troca-se os elementos nos índices. Continua-se esse processo até que os índices se cruzem. O ponto de cruzamento dos índices é a posição correta do pivô.

### - Lomuto:
No método Lomuto, escolhe-se um elemento como pivô (geralmente o último elemento do array). Em seguida, inicia-se a varredura do array da esquerda para a direita. Mantem-se um índice `i` que aponta para o último elemento menor ou igual ao pivô encontrado até agora. Para cada elemento, se ele for menor ou igual ao pivô, troca-se o elemento com o elemento no próximo índice `i` e incrementa `i`. No final do array, troca o pivô com o elemento no índice `i`, colocando o pivô em sua posição correta.