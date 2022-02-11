## Tarefa 003 - 21/12/2021 - Definição de Classes de Equivalência.

**DEFINIÇÃO**:
1. Definir um conjunto de classes de Equivalência e um conjunto de casos de testes derivados, para testar a seguinte função de avaliação universitária.
2. A função avalicao, recebe como parâmtros os seguintes dados:
   2.1. **nota1** (numérico de ponto flutuante com duas casas decimais);
   2.2. **nota2**  (numérico de ponto flutuante com duas casas decimais);
   2.3. **cargaHoraria** (numérico inteiro, positivo);
   2.4. **faltas** (numérico inteiro, positivo).
3. A forma de calcular a avaliação é a seguinte:
  3.1. Se a quantidade de faltas for superior a 25% da carga horária, o aluno estará reprovado por falta. Neste caso a função retorna a seguinte mensagem "Reprovado por Falta";
  3.2. Estando o aluno reprovado por falta, não haverá a necessidade de se avaliar as notas;
  3.2. Se a média entre nota1 e nota2 for menor que 3.0, o aluno estará reprovado por média.  Neste caso a função retorna a seguinte mensagem "Reprovado por Média";
  3.3. Se a média entre nota1 e nota2 for >= 3.0 e < 6.0, o aluno estará em recuperação.  Neste caso a função retorna a seguinte mensagem "Recuperação";
  3.4 Em qualquer outra situação o aluno estará  aprovado. Então a função retornará a mensagem: "Aprovado".
4. O Conjunto de classes de Equivalência deverá ser definido seguindo o seguinte padrão:

|id|descrição|V/I|
|--|--|--|
|CE01|nota1 < 0.00                                               |I|
|CE02|nota1 >= 0.00                                              |V|
|CE03|nota1 > 10.00                                              |I|
|CE04|nota2 < 0.00                                               |I|
|CE05|nota2 >= 0.00                                              |V|
|CE06|nota2 > 10.00                                              |I|
|CE07|cargaHoraria <= 0                                          |I|
|CE08|cargaHoraria > 0                                           |V|
|CE09|faltas <= 0                                                |I|
|CE10|faltas > 0                                                 |V|
|CE11|faltas/cargaHoraria < 0.25                                 |V|
|CE12|faltas/cargaHoraria >= 0.25; (nota1+nota2)/2 < 3.00        |V|
|CE13|faltas/cargaHoraria >= 0.25; 3.00 <= (nota1+nota2)/2 < 6.00|V|
|CE14|faltas/cargaHoraria >= 0.25; (nota1+nota2)/2 >= 6.00       |V|

Onde:
**CE** = Classe de Equivalência, seguido de um número sequencial;
**Descrição** = define um cenário de teste;
**V/I** = Válida ou Inválida.

5. O Conjunto de casos de testes derivado das classes de Equivalência deve seguir o seguinte padrão:

|CT|Valor de Entrada|Resultado Esperado|Classe Equivalência|
|--|--|--|--|
|CT01|-2.00          |Valor Inválido     |CE01|
|CT02|0.00           |Valor Válido       |CE02|
|CT03|4.30           |Valor Válido       |CE02|
|CT04|11.00          |Valor Inválido     |CE03|
|CT05|-3.25          |Valor Inválido     |CE04|
|CT06|0.00           |Valor Válido       |CE05|
|CT07|6.10           |Valor Válido       |CE05|
|CT08|12.00          |Valor Inválido     |CE06|
|CT09|-5             |Valor Inválido     |CE07|
|CT10|0              |Valor Inválido     |CE07|
|CT11|64             |Valor Válido       |CE08|
|CT12|-1             |Valor Inválido     |CE09|
|CT13|0              |Valor Inválido     |CE09|
|CT14|14             |Valor Válido       |CE10|
|CT15|32;64          |Reprovado por Falta|CE11|
|CT16|16;64;1.00;4.00|Reprovado por Média|CE12|
|CT17|4;64;7.50;2.50 |Recuperação        |CE13|
|CT18|0;64;9.00;8.25 |Aprovado           |CE14|

Onde:
**CT** = Caso de Teste, seguido de um valor sequencial;
**Valor de entrada** é o valor informado para a variável;
**Resultado esperado** é o resultado que se espera da execução da função;
**Classe de Equivalência** é a identificação de qual classe de equivalência está sendo exercitada pelo caso de teste.
