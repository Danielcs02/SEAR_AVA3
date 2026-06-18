# Classificação de Imagens com Vision Transformer (ViT) — Base vs Large

Trabalho da disciplina **Sistemas Evolutivos e Aplicados à Robótica** — Universidade Veiga de Almeida (UVA).

## Sobre

Análise comparativa entre as variantes **base** e **large** do modelo **Vision Transformer (ViT)** do Google, aplicadas à classificação de seis imagens distintas utilizando o conjunto de dados ImageNet. O estudo avalia tanto a precisão das predições quanto o tempo de inferência de cada variante.

## Resultados

| Imagem | Classe Predita (Base) | Tempo Base (s) | Classe Predita (Large) | Tempo Large (s) |
|--------|------------------------|----------------|--------------------------|------------------|
| Leão | lion, king of beasts, Panthera leo | 1,6195 | lion, king of beasts, Panthera leo | 1,9302 |
| Pato | drake | 0,4367 | drake | 1,5793 |
| Peixe-palhaço | anemone fish | 0,3955 | anemone fish | 1,6038 |
| Titanic | liner, ocean liner | 0,3963 | liner, ocean liner | 1,5306 |
| Liga da Justiça | comic book | 0,4109 | comic book | 1,5504 |
| Lata de Coca-Cola | pop bottle, soda bottle | 0,3955 | pop bottle, soda bottle | 1,5652 |

**Observações:**
- Ambas as variantes acertaram a classe principal em todas as 6 imagens
- A versão Large foi aproximadamente 4x mais lenta que a Base
- O tempo elevado da Base no Leão se deve ao carregamento inicial do modelo
- Para imagens com objetos bem definidos, a Base já entrega resultados satisfatórios

## Como executar

### Pré-requisitos

- Conta no [Google Colab](https://colab.research.google.com/)
- Acesso à internet para baixar os modelos pré-treinados via Hugging Face

### Passos

1. Abra o arquivo `notebook.ipynb` no Google Colab
2. Execute a primeira célula para instalar as dependências
3. Execute as células seguintes para realizar a classificação das imagens
4. Os resultados (classes preditas e tempos de inferência) serão exibidos no console

### Bibliotecas utilizadas

- [Transformers](https://huggingface.co/docs/transformers) — biblioteca da Hugging Face para modelos de deep learning
- [PyTorch](https://pytorch.org/) — framework de aprendizado profundo
- [Pillow (PIL)](https://pillow.readthedocs.io/) — manipulação de imagens
- [Requests](https://requests.readthedocs.io/) — download de imagens via URL

## Estrutura do projeto

```
├── notebook.ipynb    # Notebook principal com a comparação ViT Base vs Large
├── README.md         # Este arquivo
```

## Referências

- [Vision Transformer (ViT) — Documentação Oficial](https://huggingface.co/docs/transformers/model_doc/vit)
- [google/vit-base-patch16-224](https://huggingface.co/google/vit-base-patch16-224)
- [google/vit-large-patch16-224](https://huggingface.co/google/vit-large-patch16-224)
- [An Image is Worth 16x16 Words (Dosovitskiy et al., 2021)](https://arxiv.org/abs/2010.11929)
- [ImageNet](https://www.image-net.org/)
