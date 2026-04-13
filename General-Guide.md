# Etapas:
1. Parse config file
2. MazeGenerator class (O que gera o labirinto) 
3. Validação das regras estruturais do labirinto 
4. Gerar o Output file output_maze.txt 
5. Printar no terminal representação visual 
6. Disponibilizar o mazegen como pacote reutilizável 

## Pontos importantes a se considerar desde o começo:
- MazeGenerator class, uma única classe que gera o labirinto, precisa 
fazer parte de um módulo standalone, que pode vir a ser importado em 
projetos futuros. 

- O módulo da MazeGenerator tem que estar disponível em um 
único arquivo apto a ser instalado posteriormente pelo pip. 
Esse pacote precisa estar localizado no root do repositorio 
git, junto com todos os elementos necessários para builda-lo. 

- O labirinto precisa ser gerado randomicamente, mas 
precisa funcionar com seed para reproduzir o mesmo labirinto 
varias vezes.

- Com o algorítmo Recursive Backtracker teremos que testar os limites
de height e width que sao gerados sem stackoverflow e entao tratar o erro nos casos em que geraria overflow.

- O código precisa passar no mypy e flake8 sem erros, e ter 
docstrings nas funções e classes seguindo a PEP 257, 
no estilo NumPy. 

- Precisamos entender como usar o pytest, unittest ou 
outra framework usada para testes unitários. É muito 
mais testar o código aos poucos a medida que vai sendo 
desenvolvido do que rodar testes no final e ter que  
refatorar tudo. 

## Arquivos que PRECISAM existir:
- Arquivo default de configuração, com um config pré 
setada padrão pronta. 
- Makefile (vai gerar o executavel a_maze_ing.py) 
-  .gitignore (file to exclude Python artifacts) 
- output_maze.txt, output do programa 
- README.md 

## Ferramentas:
- Poetry (virtual environment + instalar dependencies
- MiniLibX(MLX) - Opcional para gerar o visual 
- Unittest ou Pytest (precisamos escolher) 
- Flake8 
- MyPy 

## Ideias
- Algorítmos de geração de labirinto citados no subject: algoritmos de geração de labirinto citados no subject: 'Prim's', 
'Kruskal's' e 'recursive backtracker'. 

- Ao implementar sistema de seeds, podemos guardar seeds de labirintos uteis 
na demonstração, como o menor possível, o maior, e outros casos interessantes, 
no próprio código com um sistema de reconhecimento do filename do config.txt. 
Se o arquivo de configuração passado tiver X nome, então a seed usada sera X. 
if filename == "key.txt": seed = seed.value 

## Links úteis
https://numpy.org/doc/2.1/reference/random/generator.html 