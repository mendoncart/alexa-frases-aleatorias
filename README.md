# Gerador de frases aleatórias
Nó para Node-red contendo subflow que sorteia aleatóriamente uma frase, dentro de um banco de frases, para o uso com Alexa ou outro nó dentro do Node-red.

O banco de frases é separado por **categorias** (Ex: frases de boa noite, frases de boas vindas, etc), divididas em **subcategorias**, que definem características das frases, como o tipo (Ex: Normais, Engraçadas, Sarcásticas, etc) e outras características, como frases singulares ou plurais.

Este nó, permite ao usuário definir a categoria a ser usada, removendo desta se desejar, subcategorias específicas. Desta forma, é possível controlar quais as categorias e subcategorias estarão disponíveis para que o sorteio seja feito. Este nó também obriga que todas as opções exclusivas disponíveis sejam percorridas antes de permitir retornar uma resposta já usada, isso faz com que o nó sempre retorne uma resposta diferente da anterior.

## Como colaborar com suas frases?
Essa ferramenta é tão boa quanto as frases disponíveis. Para isso, nos ajude a aumentar nosso acervo.

Basta fazer um pull request, e se por acaso eu não ver, me dá um toque em [@ruytter](https://telegram.me/ruytter) no telegram!

Se não souber fazer um pull request, também pode me mandar suas sugestões de frases pelo telegram.

## Instruções de uso

* Importe [este nó](https://raw.githubusercontent.com/mendoncart/alexa-frases-aleatorias/main/node-red_subflow) em seu Node-red. ([*Como importar um nó no Node-Red?*](https://nodered.org/docs/user-guide/editor/workspace/import-export))
* Configure o nó da seguinte forma:

|  Campo |  Obrigatório? | O que preencher? | Exemplo |
| ------------ | ------------ | ------------ | ------------ |
|  Name  |  Não  | Qualquer coisa. | Frase de bom dia.
|  Categoria  | **Sim**  | Nome da [categoria](https://github.com/mendoncart/alexa-frases-aleatorias/tree/main/frases) desejada. | bomdia |
|  Remover subcategoria  | Não  | Nome da subcategoria indesejada. Se houver mais de uma separar por vírgulas. | Normais-Plural, Engraçadas-Plural, Sarcásticas-Plural |

* Após a excução do nó, este fornecerá a frase sorteada em *msg.payload*.

## Categorias e sugestões de gatilhos
Sugestões de gatilho para cada categoria, e um exemplo de frase de retorno.

|  Categoria |  Gatilho | Retorno Aleatório | 
| ------------ | ------------ | ------------ |
| despedida | "Alexa, estou saindo." | Tchauzinho |
| boasvindas | Entra em casa | Já estava com saudades! |
