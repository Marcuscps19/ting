# Trybe Is Not Google

Este projeto foi desenvolvido durante o curso de desenvolvimento web da [Trybe](https://www.betrybe.com/).

### Descrição:
Aplicação em Python que simula o algoritmo de indexação de documentos similar ao do Google. Ou seja, um programa que permita anexar arquivos de texto e posteriormente opere funções de busca sobre tais arquivos. A aplicação possui dois módulos:
- Modo de gerenciamento de arquivos;
- Modo de buscas.

### Principais tecnologias utilizadas:
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

### Habilidades Desenvolvidas: 

- Manipular pilhas;
- Manipular deque;
- Manipular nó e listas ligadas;
- Manipular listas duplamente ligadas;

### Como rodar a aplicação:



```bash
# Clone o repositório:
git clone git@github.com:Marcuscps19/ting.git

# Entre no diretório
cd ting

# Crie o ambiente virtual para o projeto
python3 -m venv .venv && source .venv/bin/activate

# Instale as dependências
python3 -m pip install -r dev-requirements.txt
```

#### Funcionalidades:

##### Função txt_importer

Essa função recebe um caminho de um arquivo de texto do tipo '.txt' e retorna uma lista contendo as linhas desse arquivo, se o caminho não existir ou o tipo do arquivo for diferente de '.txt' será retornado uma mensagem de erro.

##### Função process

Essa função lê o arquivo e efetua o pré-processamento do conteúdo, deve receber como parâmetro uma instância da fila da classe Queue e o caminho do arquivo.
Exemplo de retorno da função:
```python
  {
    "nome_do_arquivo": "arquivo_teste.txt", # Nome do arquivo recém adicionado
    "qtd_linhas": 3,                        # Quantidade de linhas existentes no arquivo
    "linhas_do_arquivo": [...]              # linhas retornadas pela função do requisito 2
  }
```

##### Função remove
Essa função recebe a instância da fila e remove um elemento. Se não houver elementos, aparecerá uma mensagem de aviso, se houver apareça a mensagem que o item foi removido com sucesso.

##### Função file_metadata
Essa função receberá a instância da fila e uma posição, exibirá o elemento da fila que está naquela posição, se não existir a posição, será exibida uma mensagem de erro.

##### Função exists_word
Essa função válida a existência de uma palavra recebida por parâmetro dentro de todos os arquivos processados, para cada palavra encontrada dentro da instância recebida como parâmetro, deve-se listar sua linha conforme abaixo:
Essa busca é case insensitive.

  ```python
  [{
  "palavra": "de",
  "arquivo": "arquivo_teste.txt",
  "ocorrencias": [
    {
      "linha": 1
    },
    {
      "linha": 2
    }
  ]
}]
```
Se a palavra não for encontrada, a função retorna uma lista vazia.
##### Função search_by_word
Essa função é parecida com a exists_word, mas deverá trazer também o conteúdo do arquivo:
Essa busca é case insensitive.
```python
[{
  "palavra": "de",
  "arquivo": "arquivo_teste.txt",
  "ocorrencias": [
    {
      "linha": 1
    },
    {
      "linha": 2
    }
  ]
}]
```
Se a palavra não for encontrada, a função retorna uma lista vazia.

Link do PR: https://github.com/tryber/sd-010-a-project-ting/pull/29