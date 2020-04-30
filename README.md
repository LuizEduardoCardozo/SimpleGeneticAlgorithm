# SimpleGeneticAlgorithm
Algoritimo simples de machine learning feito em python que imita o processo da evolução

## Qual o propósito?
Eu, como estudante de CC, achei interessante esse conceito de algorímos na computação que imitam a natureza, então, decidi construir esse pequeno exemplo como um exercício.

A pesar de limitado da maneira com que está construido, com simples modificações, ele pode vir a se tornar algo util para resolver alguns tipos de problemas inversos (estimativa de coeficientes)

Basicamente, necessitariam modificações na função "do_fit", usando um algoritimo de, por exemplo, RMSE, e na função "mate", achando alguma maneira de reimplementar os cromossomos.

Qualquer ideia ou sujestão de melhoria é bem vinda! Mas lembre-se, o proposito desse algorítimo é ensinar!

## Como funciona?
Bom, é algo bem próximo da vida real: Individuos são seres constituidos de células, essas células carregam um DNA, que tem um cromossomo, que por sua vez é constituido por "genes". 

#### Individuo > DNA > Cromossomo > Gene

Fazendo uma simples modificação em um *gene* dentro de um cromossomo, pode gerar grandes mudanças nas caracteristicas fisicas daquele indivíduo.

Toda vez que acontece um "cruzamento" (eufemismos... rs) entre dois individuos, isso irá gerar um novo indivíduo. Esse terá um cromossomo, basicamente, constituido por uma "mistura" dos genes do pai e da mãe. Durante o processo, mutações aleatórias em alguns genes também podem acontecer.

### Tá, mas e o algortimo?

O principio do funcionamento é o mesmo:
Temos uma classe "individuo", com um atributo "cromossomo" e duas funções importantes: "mate", que cruza dois individuos, e "do_fit", que classifica a qualidade daquele cromossomo.

Inicialmente, geramos uma população com cromossomos compostos por genes aleatórios. Então classificamos cada um pela qualidade de seus cromossomos. Os de maior nota são mantidos, enquanto os de menor nota são descartados.

Após isso, começamos a cruzar os individuos restantes, gerando uma nova população.

O processo é repetido diversas vezes (classificar, eliminar os de menor qualidade, cruzar, classificar, eliminar...) até que surja por fim um indivíduo, cujo cromossomo bate com o critério determinado. No caso deste código, o cromossomo deve ser igual a palavra definida na varíavel WORD, declarada na segunda célula de código.
