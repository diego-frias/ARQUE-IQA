# 🚀 ARQUE App: Ferramenta de Inferência (Plug & Play)

Este diretório contém a aplicação final do projeto ARQUE, pronta para avaliar a qualidade estrutural de qualquer conjunto de imagens do mundo real utilizando a nossa métrica unificada: o **AQI (ARQUE Quality Index)**, que varia de 0 (Péssimo) a 100 (Perfeito).

## 📂 Estrutura do Diretório

* **`models/`**: Contém os "cérebros" da IA. São os modelos especialistas de *Random Forest* e *SVR* treinados nos datasets LIVE, CSIQ e TID2013. Eles foram exportados com compressão máxima (`.joblib`) para garantir inferência rápida e baixo uso de armazenamento.
* **`test_images/`**: Um lote com 20 imagens de amostra contendo diversas distorções reais (Blur, Ruído Gaussiano, Compressão JPEG/JP2K, etc.). Serve para testar o aplicativo imediatamente após o download.
* **`arque_cli_github.ipynb`**: O motor principal da aplicação. Um Jupyter Notebook interativo configurado com caminhos relativos. Ele varre diretórios, extrai as características geométricas via aceleração de hardware (Numba/CuPy) e faz a inferência.
* **`relatorio_qualidade.csv`**: O arquivo de saída gerado pelo aplicativo. Contém um detalhamento cirúrgico de cada imagem, incluindo o diagnóstico do tipo de ruído, a confiança da rede e o AQI final.

## 🧠 A Lógica de Consenso (Fault-Tolerant)

A maior inovação desta ferramenta de linha de comando é o seu sistema de **Média de Consenso ("2 de 3")**. 
Em vez de depender cegamente de uma única base de dados, a ferramenta avalia a imagem nos três modelos independentes. O algoritmo calcula a distância entre as predições, identifica os dois modelos que mais concordam entre si e descarta sumariamente o terceiro caso ele seja um *outlier* (comportamento comum em cenários *cross-dataset*). Isso garante avaliações extremamente robustas e imunes a falhas isoladas.

## 💻 Como Usar

O aplicativo foi desenhado para rodar "direto da caixa".

1. Clone o repositório e certifique-se de ter as dependências instaladas (`numpy`, `pandas`, `opencv-python`, `scikit-learn`, `numba`, `joblib`).
2. Abra o arquivo `arque_cli_github.ipynb` em seu ambiente Jupyter.
3. Simplesmente **execute todas as células**.

Por padrão, o script identificará automaticamente a pasta `./test_images/` e gerará o arquivo `relatorio_qualidade.csv` listando os resultados da amostra. 

Para avaliar suas próprias imagens, basta alterar o caminho do `--input` na última célula do notebook apontando para o seu diretório pessoal.
