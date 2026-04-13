Antes de ler, mantenha em mente que sempre que me referir a "célula" me refiro a um "quadrado" do grid/labirinto, mas também a um OBJETO da classe Cell, que será usada para representar cada célula do labirinto.
A classe Cell é importante para essa implementação e guarda atributos como: sua posição no grid/labirinto, se foi visitada ou não, e paredes para todas as direções marcadas como abertas ou fechadas.

## Etapas
1. Escolher a célula inicial.
2. Marca-la como visitada.
3. Colocar na stack.
4. While loop: Enquanto stack não estiver vazia:
   1. célula_atual = topo da stack.
   2. Pegar células NÃO VISITADAS vizinhas a atual.
   3. Se existir alguma vizinha:
      1. Escolher uma vizinha aleatoriamente.
      2. Remover paredes entre atual e vizinha.
      3. Marcar vizinha como visitada.
      4. Empilhar vizinha. Adicione-a a stack.
   4. Se não existir nenhuma vizinha:
      1. Desempilhar. Remova o último item da stack.

### Observação
É preciso tomar cuidado com a posição de x e y. Nessa implementação, optamos por seguir com o modelo (x, y) em tudo, mas sempre que precisamos acessar a posição x e y NO GRID, é preciso passar grid[y][x].
Aqui grid é uma matriz, e por isso y vem antes do x. Caso não entenda o motivo, por favor pesquise a respeito antes de continuar.