## Tarefa 004 - 19/01/2022 - Análise do Valor Limte - Definição de casos de testes.

**DEFINIÇÃO**:
1. Considerando o conjunto de classes de equivalência que você definiu em atendimento à **Tarefa 003 - 21/12/2021 - Definição de Classes de Equivalência**.
2. Considerando as explicações a respeito do critério de teste funcional **Análise do Valor Limite** disponíveis em:
   1. [Análise do Valor Limite 1](https://viniciuspessoni.com/2020/03/15/analise-do-valor-limite/).
   2. [Análise do Valor Limite 2](https://www.youtube.com/watch?v=EQU5ODvmwzs).
   3. [Análise do Valor Limite 3](https://www.youtube.com/watch?v=jX7uyaTAn-k).
3. Pede-se a definição do conjunto de casos de testes necessários para o teste do mesmo cenário descrito na tarefa 003. Estes casos de teste deverão ser criadas a partir das diretrizes definidas pelo critério funcional "Análise do Valor Limte".
4. O Conjunto de casos de testes derivado deve seguir o seguinte padrão:

|CT|Valor de Entrada|Resultado Esperado|Classe Equivalência|
|--|--|--|--|
|CT01|-0.01          |Valor Inválido     |CE01|
|CT02|0.00           |Valor Válido       |CE02|
|CT03|0.01           |Valor Válido       |CE02|
|CT04|10.01          |Valor Inválido     |CE03|
|CT05|-0.01          |Valor Inválido     |CE04|
|CT06|0.00           |Valor Válido       |CE05|
|CT07|0.01           |Valor Válido       |CE05|
|CT08|10.01          |Valor Inválido     |CE06|
|CT09|-1             |Valor Inválido     |CE07|
|CT10|0              |Valor Inválido     |CE07|
|CT11|1              |Valor Válido       |CE08|
|CT12|-1             |Valor Inválido     |CE09|
|CT13|0              |Valor Inválido     |CE09|
|CT14|1              |Valor Válido       |CE10|
|CT15|17;64          |Reprovado por Falta|CE11|
|CT16|16;64;2.99;3.00|Reprovado por Média|CE12|
|CT17|16;64;3.00;2.99|Reprovado por Média|CE12|
|CT18|16;64;3.00;3.00|Recuperação        |CE13|
|CT19|16;64;5.99;6.00|Recuperação        |CE13|
|CT20|16;64;6.00;5.99|Recuperação        |CE13|
|CT21|16;64;6.00;6.00|Aprovado           |CE14|

Onde:
**CT** = Caso de Teste, seguido de um valor sequencial;
**Valor de entrada** é o valor informado para a variável;
**Resultado esperado** é o resultado que se espera da execução da função;
**Classe de Equivalência** é a identificação de qual classe de equivalência está sendo exercitada pelo caso de teste.
