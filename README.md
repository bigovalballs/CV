# Caixeiro viajante
Solução Para problema do caixeiro viajante baseada em algoritmos genéticos

## Resumo
Este repositório contém uma implementação em Java de um algoritmo genético para o problema do caixeiro viajante. O algoritmo genético é implementado na classe **CVPopulacao**. A classe **CVCromosso** representa um cromossomo no algoritmo genético. A classe **CVGene** representa um gene no algoritmo genético.

O algoritmo genético funciona criando iterativamente novos cromossomos através de cruzamento e mutação em cromossomos existentes. Os cromossomos são então avaliados por sua aptidão, que é a distância total percorrida pelo cromossomo. Os cromossomos com maior aptidão são selecionados para criar a próxima geração de cromossomos.

O algoritmo genético é encerrado após um certo número de gerações ou quando a aptidão dos cromossomos atinge um determinado limite.

Para executar o algoritmo genético, basta compilar o código-fonte Java.

https://github.com/bigovalballs/CV/assets/109481745/29cea702-c7b2-4ac1-a3ed-55181f6e24f5

## Mundo

- A classe **Mundo** permite que o programa exiba os resultados do algoritmo em uma janela gráfica.
- O construtor da classe inicializa a população(*pop*) de cromossomos e o temporizador(*tick*). O temporizador é usado para atualizar a população de cromossomos em intervalos.
- O método **paintComponent** desenha os resultados do algoritmo na tela. O número de geração, o tamanho da população, o melhor caminho e os cromossomos em si.
- O método **drawBestChromosome** desenha o melhor cromossomo na tela e desenha as cidades como círculos e as conexões entre as cidades como linhas.
- O **JFrame**  adiciona o painel Mundo ao quadro. O quadro é então exibido para o usuário. 

## CVUtils

- Essa classe contém vários métodos utilitários que são usados para resolver o problema do caixeiro viajante.
- A classe **CVUtils** possui os seguintes métodos:
  - **getNumCidades()**: Solicita ao usuário que insira o número de cidades e retorna o número. 
  - **generateData()**: Gera um conjunto aleatório de cidades e retorna as cidades como um array.
  - **randomIndex()**: Retorna um índice aleatório de um intervalo especificado.
  - **split()**: Divide uma lista em duas listas com base em um índice aleatório.

## CVPopulacao

- Essa classe representa uma população de cromossomos, onde cada cromossomo representa uma possível solução para o problema do caixeiro viajante.
- A classe **CVPopulacao** possui os seguintes métodos:
  - **CVPopulacao**: Este construtor cria uma nova população de cromossomos com o tamanho especificado. Os cromossomos são gerados aleatoriamente.
  - **getPopulacao**: Este método retorna a população de cromossomos.
  - **getAlpha**: Este método retorna o melhor cromossomo da população. O melhor cromossomo é o cromossomo com o caminho mais curto.
  - **init**: Este método inicializa a população de cromossomos aleatorios.
  - **update**: Este método atualiza a população de cromossomos. O método de atualização funciona seguindo as etapas a seguir:
    - **Crossover**: Seleciona aleatoriamente dois cromossomos e trocar genes entre eles. Isso ajuda a criar novos cromossomos que são diferentes dos cromossomos existentes.
    - **Mutacao**: Altera aleatoriamente os genes de um cromossomo. Isso ajuda a introduzir novas variações na população.
    - **Spawn**: Cria novos cromossomos aleatoriamente. Isso ajuda a manter o tamanho da população constante.
    - **Selecao**: Seleciona os cromossomos mais aptos da população. Os cromossomos mais aptos são aqueles com os caminhos mais curtos. Os cromossomos selecionados são então usados para criar a próxima geração de cromossomos.

## CVGene

- Essa classe representa um gene, que é uma cidade no problema do caixeiro viajante. 
- A classe **CVGene** possui os seguintes métodos:
  - **CVGene**: Este construtor cria um novo gene com as cordenadas.
    - **x**: A coordenada *x* da cidade.
    - **y**: A coordenada *y* da cidade.
  - **toString**: Retorna uma representação em string do gene.
  - **getX**: Retorna a coordenada *x* do gene.
  - **getY**: Retorna a coordenada *y* do gene.
  - **distancia**: Retorna a distância entre o gene e o gene especificado. A distância é calculada usando o teorema de Pitágoras.
  - **equals**: Retorna true se o objeto especificado for igual ao gene. Dois genes são iguais se tiverem a mesma coordenada x e coordenada y.
  - **hashCode**: Retorna um código hash para o gene. O código hash é calculado usando a coordenada x e coordenada y do gene.

## CVCromosso

- Essa classe representa um cromossomo, que é uma possível solução para o problema do caixeiro viajante.
- A classe CVCromosso possui os seguintes métodos:
  - **getDistancia**: Retorna a distância total do cromossomo.
  - **CVCromosso**: Este construtor cria um novo cromossomo com a lista especificada de cidades(*genes*).
  - **getCromossomo**: Retorna a lista de cidades(*genes*) no cromossomo.
  - **calcularDistancia**: Calcula a distância total do cromossomo. A distância é calculada somando as distâncias entre cada par de cidades(*genes*) consecutivas.
  - **crossover**: Realiza uma operação de *crossover* no cromossomo e no cromossomo especificado. A operação de *crossover* envolve a troca de *genes* entre os dois cromossomos.
  - **mutar**: Realiza uma operação de *mutação* no cromossomo. A operação de *mutação* envolve a troca aleatória de dois *genes* no cromossomo.
