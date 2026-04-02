# Relatório - Coelinhos da Páscoa

> [!CAUTION]
> - Lembre-se que você <ins>**não pode utilizar ferramentas de IA para
>   escrever este relatório**</ins>

## Dados do aluno

- **Cartão UFRGS**: <mark>`00597915`</mark>
- **Nome**: <mark>`Guilherme Martins Mulazzani`</mark>

## Passos que eu segui para resolver o problema especificado (em formato de *"prompt"*)

> [!IMPORTANT]
> - Coloque aqui todas as informações necessárias para que alguém
>   (pessoa ou ferramenta de IA) possa reproduzir os seus passos para
>   solucionar o problema
> - Escreva em formato imperativo, como se fosse um *prompt* com as
>   instruções a serem seguidas na solução do problema
> - Seja objetivo e conciso: quanto *menos palavras* você utilizar,
>   melhor
> - Seja técnico e use terminologia adequada: assuma que quem irá ler
>   os seus passos possui conhecimento de Ciência da Computação e
>   Computação Gráfica
> - Caso você queira incluir informações "longas" (como algum *prompt*
>   grande usado com alguma ferramenta de IA), crie arquivos à parte e
>   adicione links no texto (por exemplo, crie o arquivo `PROMPTS.md`
>   e adicione um link markdown `[os prompts detalhados estão
>   aqui](PROMPTS.md)`)
> - Novamente, lembre-se que você *não pode utilizar ferramentas
>   de IA para escrever este relatório*

<mark>` Comece utilizando de glfGetTime() para obter um tempo contínuo na aplicação, então faça um laço de repetição que adicione um valor i de 0 a 11 (Para criar os 12 coelhos). Faça então o calculo do angulo estatico deste i com angulo_base = i * (2 * PI / 12), com este calculo em mãos, faça uma rotação que pegue todos eles com angulo_carrossel = angulo_base - tempo * vel_carrossel. As coordenadas de translação, X e Z, devem ser computadas com coordenadas polarem de raio fixo.`</mark>


 <mark>` Na coordenada Y, utilize da função seno dependendo do tempo. Alinhe o forward vector da malha à tangente da trajetória pelo calculo angulo_olhar = angulo_carrossel + PI / 2. Deve também criar a matriz model_base utilizando de Matrix_Translate * Matrix_Rotate_Y.`</mark>


<mark>` Para fazer a situação com os coelhos, faça uma cópia do model_base, valide a condição if (i % 4 == 3), se for verdade, multiplique a matriz atual por uma rotação local no eixo X para um mortal para frente contínuo, com Matrix_Rotate_X(-tempo * vel_cambalhota).`</mark>


 <mark>` Para fazer os ovos em torno do coelho, copie novamente a model_base para cada ovo, aplique uma cadeia de multipilicações de matrizes, com Matrix_Scale (Deixar no formato de ovo), Matrix_Translate (eixo Z, raio da orbita), Matrix_Rotate_X (tempo * vel_orbita), que gera a órbita, Matrix_Translate (eixo Y, desloca origem para o centro do coelho que esta associado). Para construir o ovo dois, utilize dos mesmos calculos e adicione uma desafagem de fase de pi ao ângulo da função Matrix_Rotate_X.`</mark>


## Principais dificuldades encontradas durante o desenvolvimento (formato livre)

<mark>`Com certeza a coisa mais difícil foi fazer o coelho dar sua cambalhota para frente, pois antes de implementar no if, ao mexer nele, eu fazia com que todos os coelhos ficassem rotacionando enquanto o carrossel se movia, o que não era o desejado. Outra questão foi de eu ficar muito tempo girando ele de lado, como se estivesse rolando no ar. A ultima dificuldade que tive foi fazer os ovos não passarem por dentro do coelho e seguirem eles, mas depois de fazer cada um ter um ponto origem, ficou mais fácil.`</mark>

## Você acha que conseguiu resolver o problema de forma adequada?

<mark>`Sim, foi de forma adequada, pois ele segue o resultado esperado, com uma estrutura completa e organizada, com algumas coisas diferentes apenas, como os ovos mais afastados do coelho. `</mark>

## Se você quiser compartilhar mais alguma coisa, coloque aqui:

<mark>`Achei muito bom colocar na prática o que vimos na aula, muito interessante.`</mark>

## Se você possui alguma sugestão para o professor sobre esta atividade, coloque aqui:

<mark>`Não há sugestões sobre esta atividade.`</mark>
