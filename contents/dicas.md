## Tópicos importantes

### check grad
1. O gradiente numérico de dois lados aproxima os gradientes analíticos mais de perto que a forma do lado direito.

2. Como a verificação do gradiente é muito lenta:
	- Aplique-o em um ou alguns exemplos de treinamento.
	- Desative-o ao treinar rede neural após verificar se a implementação da retropropagação está correta.

3. A verificação de gradiente não funciona ao aplicar o método de abandono. Use keep-prob = 1 para verificar a verificação de gradiente e altere-a ao treinar rede neural.

4. Epsilon = 10e-7 é um valor comum usado para a diferença entre gradiente analítico e gradiente numérico. Se a diferença for menor que 10e-7, a implementação da retropropagação está correta.

5. Graças às estruturas de Deep Learning , como Tensorflow e Pytorch, podemos nos encontrar raramente implementando a retropropagação, porque essas estruturas calculam isso para nós; no entanto, é uma boa prática entender o que acontece sob o capô para se tornar um bom praticante de Aprendizado Profundo.

### Evitar Overfitting

* Reduza a capacidade da rede removendo camadas ou reduzindo o número de elementos nas camadas ocultas
* Aplique regularização, que se resume a adicionar um custo à função de perda para grandes pesos
* Use as camadas do Dropout , que removerão aleatoriamente determinados recursos, definindo-os como zero
