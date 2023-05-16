# Caixeiro viajante
Solução Para problema do caixeiro viajante baseada em algoritmos genéticos

## Resumo
Este repositório contém uma implementação em Java de um algoritmo genético para o problema do caixeiro viajante. O algoritmo genético é implementado na classe **CVPopulacao**. A classe **CVCromosso** representa um cromossomo no algoritmo genético. A classe **CVGene** representa um gene no algoritmo genético.

O algoritmo genético funciona criando iterativamente novos cromossomos através de cruzamento e mutação em cromossomos existentes. Os cromossomos são então avaliados por sua aptidão, que é a distância total percorrida pelo cromossomo. Os cromossomos com maior aptidão são selecionados para criar a próxima geração de cromossomos.

O algoritmo genético é encerrado após um certo número de gerações ou quando a aptidão dos cromossomos atinge um determinado limite.

Para executar o algoritmo genético, basta compilar o código-fonte Java.

## Mundo

- A classe **Mundo** permite que o programa exiba os resultados do algoritmo em uma janela gráfica.

- O construtor da classe inicializa a população(*pop*) de cromossomos e o temporizador(*tick*). O temporizador é usado para atualizar a população de cromossomos em intervalos.

- O método **paintComponent** desenha os resultados do algoritmo na tela. O número de geração, o tamanho da população, o melhor caminho e os cromossomos em si.

- O método **drawBestChromosome** desenha o melhor cromossomo na tela e desenha as cidades como círculos e as conexões entre as cidades como linhas.

- O **JFrame**  adiciona o painel Mundo ao quadro. O quadro é então exibido para o usuário. 

## Mundo
