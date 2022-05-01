# Gerador de frases aleatórias
Nó para Node-red contendo subflow que sorteia aleatóriamente uma frase, dentro de um banco de frases, para o uso com Alexa ou outro nó dentro do Node-red.

O banco de frases é separado por **categorias** (Ex: frases de boa noite, frases de boas vindas, etc), divididas em **sub-categorias**, que definem características das frases, como o tipo (Ex: Normais, Engraçadas, Sarcásticas, etc) e outras características, como frases singulares ou plurais.

Este nó, permite ao usuário definir a categoria a ser usada, removendo desta se desejar, sub-categorias específicas. Desta forma, é possível controlar quais as categorias e sub-categorias estarão disponíveis para que o sorteio seja feito. Este nó também obriga que todas as opções exclusivas disponíveis sejam percorridas antes de permitir retornar uma resposta já usada, isso faz com que o nó sempre retorne uma resposta diferente da anterior.

## Instruções de uso

* Importe [este nó](https://raw.githubusercontent.com/mendoncart/alexa-frases-aleatorias/main/node-red_subflow) em seu Node-red
* Configure o nó da seguinte forma:
  * Preencha a categoria, usando o nome da [categoria](https://github.com/mendoncart/alexa-frases-aleatorias/tree/main/frases) desejada.
  * Se desejar remover sub-categorias, basta preencher a sub-categoria indesejada. Se houver mais de uma separar por vírgulas.
* Após a excução do nó, este fornecerá a frase sorteada em *msg.payload*.
