<div align=center>
  <img src="brasaooficialcolorido.png">
</div>

#### <p style="text-align: center;">Universidade Federal de Goiás</p>
#### <p style="text-align: center;">Instituto de Informática</p>
#### <p style="text-align: center;">Bacharelado em Engenharia de Software</p>
#### <p style="text-align: center;">Teste de Software - 2021/2</p>
#### <p style="text-align: center;">Gilmar Ferreira Arantes</p>
####  <p style="text-align: center;"> Prova P1 - 16/02/2022</p>

Matrícula:201703755
Nome:Gustavo Marques Reis

<p><font color=green>Nota: 6,8.</font></p>

1. Quanto ao objetivo do Teste de Software, responda as duas questões seguintes:
   1. (**0,5 ponto**) Qual o objetivo primário da atividade de teste de software? <font color=green>Certo.</font>
    O objetivo primário do teste de software é revelar a presença de defeitos.
   2. (**0,5 ponto**) O que acontece, quando não se atinge este objetivo primário?
    O software será entregue ao cliente podendo conter defeitos. <font color=red>Errado.</font>


2. (**1,0 ponto**) Explique o que é o teste exaustivo e porque sua execução não é possível.
Teste exaustivo é testar um software usando todas as combinações de entrada possíveis, e é impossível fazer sua execução pois como é testada cada possibilidade de entrada serão criadas milhares ou até milhões de casos de teste que em sua grande maioria não serão significativos, gastando uma grande quantidade de tempo que poderia ser usado para realizar outras atividades. <font color=green>Certo.</font>

3. (**1,0 ponto**) Cite pelo menos duas limitações da Técnica de Teste Funcional e duas da Técnica de Teste Estrutural.
  -Teste Funcional: (1) Não é possível garantir que partes críticas ou essenciais do software sejam executadas. (2) Para encontrar todos os defeitos é necessário o teste exaustivo. <font color=orange>Parcialmente correto. Nota 0,25.</font>
  -Teste Estrutural: (1) Defeitos podem existir mesmo com o fluxo de controle correto. (2) Um módulo pode executar corretamente para diversos casos de teste e falhas para alguns. <font color=green>Certo.</font>

4. (**1,0 ponto**) Descreva pelo menos um dos quatro níveis de teste constantes da literatura especializada.
Teste de Carga - O objetivo é testar o comportamento do sistema submetendo-o ao processamento de um grande volume de dados. <font color=red>Errado.</font>

5. (**1.0 ponto**)Descreva qual o propósito do critério de teste funcional Particionamento por Classes de Equivalência.
O objetivo principal é a redução da quantidade de casos de teste necessários. <font color=orange>Parcialmente correto. Nota 0,5.</font>

6. (**1.00 ponto**) Existe algum tipo de hierarquia em relação aos critérios de teste estrutural, todos os nós, todos os arcos e todos os caminhos? Se sim, explique-a, considerando a perspectiva dos níveis de cobertura desejados.
Sim, existe um tipo de hierarquia em relação aos critérios de teste estrutural. Esta hierarquia, considerando os níveis de cobertura, pode ser descrita como quanto maior o nível de cobertura, maior o rigor do critério de teste, ou seja, mais casos de teste ele exige para ser satisfeito. Por exemplo, no nível 0 (o menor) o critério é: qualquer valor de cobertura inferior a 100% da cobertura de todos os comandos. Já no nível 7 (o maior) o critério é: 100% de cobertura de caminhos, também conhecido como critério todos-caminhos. <font color=green>Certo.</font>

7. Considere a especificação, a seguir, de um hipotético programa que objetiva a classificação de um triângulo, a partir dos valores informados para os seus três lados.

   a) Dado um triângulo cujos segmentos medem A, B e C, que são números inteiros positivos na faixa de 0 a 100. Esse triângulo somente existirá se: (A + B < C) ou (A + C < B) ou (B + C < A).
   b) Quanto às medidas dos seus lados o triângulo, poderá ser classificado em:
         • Isósceles = quando possui dois lados com a mesma medida;
         • Escaleno = quando todos os seus lados têm medidas diferentes;
         • Equilátero = quando todos os lados tem a mesma medida;
         • Acutângulo = quando o quadrado de um dos seus lados é menor que a soma do quadrado dois outros dois. (A<sup>2</sup> < B<sup>2</sup> + C<sup>2</sup>).
         • Retângulo: quando o quadrado de um dos seus lados é igual à soma do quadrado dois outros dois. (A<sup>2</sup> = B<sup>2</sup> + C<sup>2</sup>).
         • Obtusângulo: quando o quadrado de um dos seus lados é maior que a soma do quadrado dois outros dois. A<sup>2</sup> > B<sup>2</sup> + C<sup>2</sup>.

7.1 (**2.0 pontos**) Definir uma tabela de decisão para o teste tanto da existência do triângulo, quanto para a definição do seu tipo. Consulte exemplo de tabela de decisão na tarefa 005.

||**Regras->**|R1|R2|R3|R4|R5|R6|R7|R8|R9|R10|R11|R12|R13|R14|R15|R16|R17|R18|R19|R20|R21|R22|R23|R24|R25|R26|R27|R28|R29|R30|R31|R32|R33|R34|R35|R36|R37|R38|R39|R40|R41|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**Causas**  | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
||Segmento A|= B|= B|= B|= C|= C|< B|< B|< B|< B|< B|< B|< B|< B|< B|> B|> B|> B|> B|> B|> B|> B|> B|> B|< C|< C|< C|< C|< C|< C|< C|< C|< C|> C|> C|> C|> C|> C|> C|> C|> C|> C|
||Segmento B|= C|= A|= A|< A|> A|> A|> A|> A|> A|< C|< C|> C|> C|> C|< A|< A|< A|< A|< C|< C|< C|> C|> C|< A|< C|> A|> C|> C|> C|< A|< C|> A|< A|< C|> A|> C|< A|> A|> C|< A|< C|
||Segmento C|= B|< A|> A|= A|= A|< A|< B|> A|> B|> A|> B|< A|< B|> A|< A|< B|> A|> B|< A|> A|> B|< A|< B|> A|> A|> A|> A|< B|< B|> B|> B|> B|< A|< A|< A|< A|< B|< B|< B|> B|> B|
|**Efeitos** | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
||Isósceles  |X|X|X|X|X| |X|X| | | | |X| |X| | |X| | |X| | | |X|X| | | | |X| |X| | |X| | |X| | |
||Escaleno   | | | | | |X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|
||Equilátero |X| | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
||Acutângulo |X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|
||Retângulo  | | | | | |X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|
||Obtusângulo| | |X| |X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|X|

<font color=Orange>Parcialmente correto. Nota 1,5.</font>

7.2 (**2.0 pontos**) Criar os conjunto de casos de teste necessários para a cobertura das combinações constantes da tabela de decisão, seguindo o seguinte padrão:

|CT|Lado A|Lado B|Lado C|Resultado|
|---|---|---|---|---|
|CT01|60|60|100|Isósceles|
|CT02|30|45|60|Escaleno|
|CT03|10|10|10|Equilátero|
|CT04|15|30|30|Acutângulo|
|CT05|30|40|50|Retângulo|
|CT06|25|55|75|Obtusângulo|


<font color=Orange>Parcialmente correto. Nota 1,5.</font>
