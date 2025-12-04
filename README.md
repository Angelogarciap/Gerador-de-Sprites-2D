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

Imagenet:
ImageNet é um conjunto de dados de imagens amplamente utilizado na pesquisa em visão computacional e aprendizado de máquina. O ImageNet contém mais de 14 milhões de imagens anotadas à mão, organizadas em categorias que refletem conceitos do WordNet.

Link: https://image-net.org/

°Sugestão

CIFAR-100:
O CIFAR-100 é um conjunto de dados de aprendizado de máquina desenvolvido pelo Instituto Canadense de Pesquisa Avançada (CIFAR). Ele consiste em 60.000 imagens coloridas de 32x32 pixels, organizadas em 100 classes diferentes.

Link: https://www.cs.toronto.edu/~kriz/cifar.html

Bibliotecas

_Construção da Rede Neural_

Pytorch:
O PyTorch é um framework de deep learning de código aberto baseado em software, usado para construir redes neurais, combinando a biblioteca de aprendizado de máquina (ML) do Torch com uma API de alto nível baseada em Python.

_Reconhecimento do objeto_

YOLO:
YOLO, que significa You Only Look Once, é um algoritmo de detecção de objetos em tempo real. Utiliza uma rede neural convolucional para identificar e localizar objetos em imagens ou vídeos de forma rápida e precisa.

_Processamento de imagem_

OpenCV:
OpenCV é uma biblioteca de código aberto amplamente utilizada para visão computacional e processamento de imagens, permitindo o desenvolvimento de aplicações que interpretam informações visuais.

°Sugestão

Pillow:
A Pillow é uma eficiente biblioteca de manipulação, tratamento e processamento de imagens no Python. Pode ser utilizada para tarefas como compressão de imagens, redimensionamento, conversão entre formatos e aplicação de filtros.

_Estilização do Sprite em Pixel Art_

Stable Diffusion:
Stable Diffusion é um modelo de inteligência artificial generativa capaz de criar imagens realistas e únicas a partir de descrições textuais, conhecidas como prompts.

ControlNet
ControlNet é uma rede neural que pode melhorar a geração de imagens em difusão estável adicionando condições extras. Isso permite que os usuários tenham mais controle sobre as imagens geradas. ControlNet funciona adicionando condicionamento extra ao modelo de difusão com uma imagem de entrada como restrição adicional para orientar o processo de difusão

°Sugestões:

LoRA:
LoRA é uma técnica usada em aprendizado de máquina para adaptar grandes modelos pré-treinados a tarefas específicas sem precisar treinar o modelo inteiro novamente.

Pix2Pix:
Pix2Pix é uma técnica de inteligência artificial que transforma imagens de um domínio para outro. Utiliza redes adversariais generativas (GANs) para aprender a mapear uma imagem de entrada para uma imagem de saída.

CycleGAN:
CycleGAN é uma abordagem de aprendizado de máquina utilizada para tradução de imagens de um domínio para outro sem a necessidade de pares de imagens emparelhadas. Isso significa que o modelo pode ser treinado com conjuntos de imagens de diferentes domínios, como transformar fotos de cavalos em zebras ou vice-versa, sem a necessidade de imagens correspondentes.

# Pipeline

Detecção do objeto -> Recorte -> Processamento da imagem -> Pixelização -> Pós-processamento

_Detecção do objeto_:
Detecta o objeto na imagem.

_Recorte_:
Recorta o objeto da imagem original.

_Processamento da imagem_:
Etapa de ajuste na resolução da imagem, paletas, filtros, masking e recorte

_Pixelização_:
Etapa em que a imagem é estilizada em pixel art

_Pós-processamento_:
Etapa de ajuste de resolução da imagem, paleta e recorte de pixels

# Modelos

Modelos do Hugging Face de estilização em pixel art que podem ser utilizados:

°nerijs/pixel-art-medium-128-v0.1
Gera imagens em pixel art de 128×128 pixels, grid-alinhadas. Útil se você quer sprites relativamente pequenos já com estilo de pixel art.

https://huggingface.co/nerijs/pixel-art-medium-128-v0.1

°Shekswess/pixel-art-xl-neuron
Baseado em SDXL; gera imagens com estilo pixel art (isométrico ou não). Bom para cenas ou assets maiores — útil para backgrounds ou sprites detalhados.

https://huggingface.co/Shekswess/pixel-art-xl-neuron

°nerijs/pixel-art-3.5L
Versão adaptada (adapter / LoRA) para gerar pixel art “grid-aligned” a partir de base compatível com stable-diffusion. Interessante para quem quer outputs mais consistentes.

https://huggingface.co/nerijs/pixel-art-3.5L

°pixelparty/pixel-party-xl
Modelo treinado especificamente com foco em pixel art, baseado na versão XL. Indicado para criar sprites, tiles, personagens ou objetos no estilo retro/pixel.

https://huggingface.co/pixelparty/pixel-party-xl
