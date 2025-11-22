# Gerador-de-Sprites-2D

O projeto baseia-se na criação de uma IA generativa que fotografa e interpreta um objeto, transformando-o em um sprite 2D. Ideal para acelerar o desenvolvimento de jogos por estúdios indie.

# Ambiente Virtual

Ao trabalhar neste projeto, é recomendado a criação de um ambiente virtual. Criar um ambiente virtual é importante pois mantém pacotes e extensões isolados somente na pasta do projeto, impedindo seu impacto em demais aplicações.

Para criar um ambiente em um projeto Python, insira o seguinte comando no seu terminal:

python -m venv venv

O venv estará disposto no .gitignore, impedindo que os arquivos do ambiente não sejam versionados.

O ambiente do projeto estará criado, mas ainda não ativo. Para ativá-lo, é necessário digitar este comando no terminal:

venv\Scripts\activate

Com o ambiente virtual criado, já é possível instalar os pacotes do projeto. Para listá-los, escreva o seguinte comando:

pip freeze

Para adicionar bibliotecas no requirements.txt, é necessário executar o seguinte comando.

pip freeze > requirements.txt

A instalação das bibliotecas na sua máquina ocorrerá quando o comando abaixo for executado no terminal.
pip install -r requirements.txt

# Ferramentas para o projeto

Dataset

ImageNet é um banco de dados de imagens organizado de acordo com a hierarquia WordNet, no qual cada nó da hierarquia é representado por centenas e milhares de imagens.

Bibliotecas

OpenCv
Pytorch
Tensorflow
