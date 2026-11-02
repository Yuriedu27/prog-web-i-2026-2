# Observações – Block e inline (Aula 03)

| Elemento | Block ou inline? | Por quê faz sentido |
|---|---|---|
| h1, h2, h3 | **Block** | O destaque ocupa a linha inteira; títulos separam blocos de conteúdo, então precisam de uma linha própria. |
| p | **Block** | O destaque ocupa a linha inteira; cada parágrafo é uma unidade de texto separada das demais. |
| ul, ol | **Block** | O destaque ocupa toda a largura; a lista é um bloco que contém vários itens e fica separada do texto ao redor. |
| a (link no menu) | **Inline** | O destaque cobre só o texto do link; links ficam no meio do texto ou lado a lado no menu sem quebrar linha. |
| strong dentro de p | **Inline** | O destaque cobre só a palavra; serve para enfatizar um trecho sem interromper o parágrafo. |
| img | **Inline** | O destaque cobre só a área da imagem; por padrão ela se comporta como um caractere grande dentro da linha de texto. |

## Experimento: dois `strong` lado a lado vs. dois `p` lado a lado

- **Dois `strong` no mesmo parágrafo:** ficaram **na mesma linha**, um após o outro, porque são inline e só ocupam a largura do próprio conteúdo.
- **Dois `p` seguidos:** ficaram **um embaixo do outro**, porque são block: cada um ocupa a linha inteira e força quebra de linha antes e depois.

**Conclusão:** elementos block empilham na vertical; elementos inline fluem na horizontal dentro da linha.

---

# Desafio opcional

## figure e figcaption vs. `p` depois do `img`

Um `p` solto depois do `img` é só um parágrafo que, visualmente, parece uma legenda, mas o HTML não diz que os dois estão ligados. O `figure` agrupa o conteúdo que ilustra o texto e o `figcaption` declara semanticamente que aquele texto é a legenda daquela imagem. Assim, leitores de tela e buscadores entendem a relação, e o conjunto pode ser movido sem perder a legenda.

## caption na tabela vs. h3 acima da tabela

O `caption` faz parte da tabela e é o nome acessível dela. Ao chegar na tabela, o leitor de tela anuncia o título junto com a estrutura (por exemplo, número de linhas e colunas), e o usuário decide se quer entrar nela ou pular. Um `h3` só é um título solto na hierarquia da página, sem vínculo programático com a tabela.
