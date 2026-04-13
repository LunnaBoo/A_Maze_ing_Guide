# Etapas
1. Gerar o grid.
2. Marcar bordas e 42 central como visitadas (quando aplicável).
3. A partir disso, gerar o labirinto com o algoritmo escolhido.
4. Retornar o output com os dados do labirinto
5. Visualização em ASCII
6. Gerar o output_maze.txt

### 1. Gerar o grid
Será usado o método generate_grid da classe MazeGenerator para gerar o grid usando a classe Cell, que
representará cada célula do grid. Todas as células serão criadas com suas paredes fechadas em todas as
direções e marcadas como NÃO VISITADAs.

### 2. Marcar bordas e 42 central como visitadas
Precisamos evitar que o algoritmo de geração do labirinto saia dos limites do grid. 
Para isso, iremos adicionar uma camada externa ao labirinto e marcar todas suas células como VISITADA.
No código, será necessário se certificar de que a altura e comprimento do labirinto sejam impares.

### 3. Gerar o labirinto
Será aplicado ao grid o algoritmo de Recursive Backtracking que irá abrir caminho por ele e definir
todos os corredores do nosso labirinto. Ao final, quando todas as células dentro do grid
estiverem VISITADAs, teremos o labirinto completo.

### 4. Retorno dos dados
Retornar uma matriz bidimensional grid[x][y], na qual cada posição contém uma instância do objeto Cell, representando uma célula do labirinto.

### 5. Visualização em ASCII
Exibir uma pré-visualização do labirinto em formato ASCII no terminal.

O sistema deve incluir um menu interativo com as seguintes opções:

1. Gerar um novo labirinto
2. Exibir o caminho entre a entrada e a saída
3. Alterar a cor da visualização
4. Encerrar o programa

### 6. Gerar o output_maze.txt
Implementar um interpretador que percorra a matriz grid célula por célula, lendo as informações de paredes de cada Cell.

Esses dados devem ser:

- Convertidos para formato binário
- Posteriormente convertidos para hexadecimal
- Gravados no arquivo output_maze.txt

Após a escrita da matriz:
- Inserir três quebras de linha
- Escrever as coordenadas do ponto de entrada no formato x,y
- Escrever as coordenadas do ponto de saída no formato x,y

Em seguida:

Inserir mais uma quebra de linha
Escrever o caminho da entrada até a saída no formato de direções, por exemplo:
- NSEWNSWNSEW
  - Onde:
    - N = North (Norte)
    - S = South (Sul)
    - W = West (Oeste)
    - E = East (Leste)