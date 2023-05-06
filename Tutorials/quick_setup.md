# Para instalar as bibliotecas necessárias via pip:

### 1- Abra o terminal ou prompt de comando do seu sistema operacional.

### 2- Certifique-se de ter o pip instalado. Você pode verificar se o pip já está instalado digitando o seguinte comando no terminal:

pip --version

Se o pip estiver instalado, você verá a versão do pip instalada. Se não estiver instalado, você pode instalar seguindo as instruções em https://pip.pypa.io/en/stable/installation/

### 3- Agora, use o seguinte comando para instalar as bibliotecas necessárias:

pip install numpy<br>
pip install torch<br>
pip install websockets<br>
pip install gym<br>
pip install stable-baselines3<br>
pip install tqdm<br>
pip install psutil<br>



# Para instalar as bibliotecas necessárias via conda:

### 1- Certifique-se de ter o conda instalado. Você pode verificar se o prompt anaconda foi instalado, seguindo os seguintes atalhos para sistemas operacionais diferentes:

- Windows: Clique em "Iniciar", pesquise por "Prompt do Anaconda" e clique para abrir.
- macOS: Use Cmd+Space para abrir a busca do Spotlight e digite "Navigator" para abrir o programa.
- Linux-CentOS: Abra "Aplicativos", vá para "Ferramentas do Sistema" e selecione "Terminal".
- Linux-Ubuntu: Abra o Dash clicando no ícone do Ubuntu e digite "terminal".

### 2- Se você não tiver o Anaconda instalado, siga estas etapas para instalá-lo:

Acesse o site oficial do Anaconda: https://www.anaconda.com/products/individual.
Selecione o download para o seu sistema operacional (Windows, macOS ou Linux).
Baixe a versão mais recente do Anaconda.
Siga as instruções de instalação para concluir a instalação do Anaconda em seu sistema.
Uma vez instalado o Anaconda, você pode criar um novo ambiente virtual e instalar as bibliotecas necessárias usando o comando conda install. Para criar um novo ambiente, use o comando conda create seguido pelo nome do ambiente e a versão do Python que você deseja usar. Por exemplo:

conda create --name meu-ambiente python=3.8

Para ativar o ambiente virtual, use o comando conda activate seguido pelo nome do ambiente:

conda activate meu-ambiente

### 3- Em seguida, você pode usar o comando conda install para instalar as bibliotecas necessárias:

conda install numpy<br>
conda install pytorch<br>
conda install -c conda-forge websockets<br>
conda install gym<br>
conda install -c conda-forge stable-baselines3<br>
conda install tqdm<br>
conda install psutil<br>

Observe que, ao instalar o PyTorch via Anaconda, você precisará escolher a versão apropriada para sua plataforma. Consulte a documentação do PyTorch para obter mais informações.

# Para instalar o CUDA e os pacotes NVIDIA:

### 1- Siga as instruções disponíveis no site da NVIDIA (https://www.nvidia.com/). 

Verifique as especificações do seu sistema e escolha a versão correta do CUDA e dos pacotes NVIDIA.

### 2- Instale o CUDA e os pacotes NVIDIA via PyTorch com suporte para GPU da seguinte forma:

pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118

Observe que, se você estiver usando uma versão diferente do CUDA, precisará substituir cu118 no comando acima pela versão correta. Recomendável olhar o site https://pytorch.org/get-started/locally/

