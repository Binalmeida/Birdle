# Diferença de Arquiteturas: Explique qual a principal diferença entre o desenvolvimento Nativo (Android/iOS) e o Cross-Platform/Híbrido (como o Flutter).
    R: No nativo, utiliza-se apenas uma linguagem por plataforma, como por exemplo Kotlin/Java para Android ou Swift/Objective-C para iOS, fazendo com que tenha dois códigos fonte, um para cada sistema. No desenvolvimento híbrido, que é caso do Flutter, existe um único código-fonte em Dart que é compilado para código nativo em ambas as plataformas.


#Ciclo de Vida e Widgets: No Flutter, "tudo é um Widget". Explique a diferença entre um StatelessWidget e um StatefulWidget. Dê um exemplo de quando usar cada um.
    R: Um StatelessWidget é um widget "imutável", pois uma vez construído, ele não guarda nenhum dado que possa mudar sozinho ao longo do tempo. Já um StatefulWidget é composto por duas classes, o próprio Widget e um objeto State associado a ele, que é capaz de guardar dados mutáveis que podem mudar durante o tempo de vida do widget.

#Gerenciamento de Estado: O que acontece na tela do aplicativo quando chamamos o método setState() dentro de um StatefulWidget ?
    R: Quando setState() é chamado em um StatefulWidget, o Flutter executa a função passada para atualizar o estado, marca o widget para reconstrução e, no próximo frame, chama o build() novamente. Em seguida, compara a nova árvore de widgets com a atual e atualiza apenas as partes da interface que realmente mudaram, sem redesenhar toda a tela.