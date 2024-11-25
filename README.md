
# Sistema de Gerenciamento de Jogos 🎮
Este projeto implementa um sistema para gerenciar uma coleção de jogos, permitindo adicionar jogos, buscar por preço, faixa de preço e gênero. O sistema utiliza uma árvore binária de busca para organizar os jogos por preço e uma tabela hash para organizar os jogos por gênero.

## Estrutura do Código 🛠
### Classes Principais
#### Jogo
Representa um jogo com as seguintes propriedades:
- *jogoId* (ID único do jogo)
- *titulo* (Título do jogo)
- *desenvolvedor* (Desenvolvedor do jogo)
- *preco* (Preço do jogo)
- *generos* (Lista de gêneros associados ao jogo)

#### Código Exemplo:
``` python
class Jogo:
    def __init__(self, jogoId, titulo, desenvolvedor, preco, generos):
        self.jogoId = jogoId
        self.titulo = titulo
        self.desenvolvedor = desenvolvedor
        self.preco = preco
        self.generos = generos
```
#### Código Exemplo:
``` python
class NoJogo:
        def __init__ (self, jogo):
        self.jogo = jogo
        self.esquerda = None
        self.direita = None
```
#### Código Exemplo:
``` python
class NoJogo:
    def __init__(self, jogo):
        self.jogo = jogo
        self.esquerda = None
        self.direita = None

```
#### ArvoreJogos
Gerencia uma árvore binária de busca de jogos, ordenando-os por preço.
- *Métodos principais*:
  - inserir(jogo) - Insere um novo jogo na árvore.
  - buscar_por_preco(preco) - Busca jogos por preço exato.
  - buscar_por_faixa_de_preco(precoMinimo, precoMaximo) - Busca jogos dentro de uma faixa de preço.

#### Código Exemplo:
``` python
class ArvoreJogos:
    def __init__(self):
        self.raiz = None
    # Métodos para inserir e buscar jogos
```

#### HashGeneros
Gerencia uma tabela hash (dicionário) que mapeia gêneros para jogos, permitindo buscar todos os jogos relacionados a um gênero específico.
- *Métodos principais*:
  - adicionar_jogo(jogo) - Adiciona um jogo aos gêneros correspondentes.
  - obter_jogos(genero) - Retorna todos os jogos de um gênero específico.

#### Código Exemplo:
``` python
class HashGeneros:
    def __init__(self):
        self.generoParaJogos = {}
    # Métodos para adicionar jogos e buscar por gênero

```
### Função menu
A função principal do programa oferece um menu interativo para o usuário realizar as seguintes operações:
- Adicionar um novo jogo.
- Buscar jogos por preço exato.
- Buscar jogos dentro de uma faixa de preço.
- Buscar jogos por gênero.

#### Exemplo de Menu:
``` python
--- Menu de Operações ---
1. Adicionar Jogo
2. Buscar Jogo por preço
3. Buscar Jogo por faixa de preço
4. Buscar Jogo por gênero
0. Sair

```
### Detalhamento das Funcionalidades 📝
#### Adicionar Jogo ➕
O sistema permite adicionar jogos com os seguintes dados:
- ID único
- Título
- Nome do desenvolvedor
- Preço
- Gêneros (que podem ser múltiplos)

#### Buscar Jogo por Preço 💰
O usuário pode buscar jogos por um preço exato, e o sistema irá retornar os jogos que correspondem ao preço informado.

#### Buscar Jogo por Faixa de Preço 💸
A busca pode ser feita dentro de uma faixa de preço, onde o usuário fornece um preço mínimo e máximo.

#### Buscar Jogo por Gênero 🎯
Os jogos também podem ser buscados por gênero. O sistema retorna todos os jogos que pertencem ao gênero informado.

### Considerações Finais 🤖
Este sistema utiliza a estrutura de dados árvore binária de busca para organizar os jogos por preço, o que permite buscas rápidas por preço exato ou faixa de preço. Além disso, a tabela hash é utilizada para buscar jogos por gênero de forma eficiente.
