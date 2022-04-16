<div align=center>
  <img src="brasaooficialcolorido.png">
</div>

#### <p style="text-align: center;">Universidade Federal de Goiás</p>
#### <p style="text-align: center;">Instituto de Informática</p>
#### <p style="text-align: center;">Bacharelado em Engenharia de Software</p>
#### <p style="text-align: center;">Teste de Software - 2021/2</p>
#### <p style="text-align: center;">Gilmar Ferreira Arantes</p>
####  <p style="text-align: center;"> Prova P2 - 12/04/2022</p>

Matrícula: 201703755

Nome: Gustavo Marques Reis

<font color="red">Nota 7,93</font>

1. Quanto ao Processo de Teste de Software, responda as duas questões seguintes:
   1. (**0,5 ponto**) Defina os seguintes conceitos Processo de Teste de Software, Projeto de Teste de Software e Plano de Teste de Sofware.
      - Processo de Teste de Software: Estruturar as etapas, as atividades, os artefatos, os papéis e as responsabilidades do teste, permitindo organização e controle de todo o ciclo do teste, minimizando os riscos e agregando valor ao software.
      - Projeto de Teste de Software: Um conjunto de tarefas que devem ser realizadas para atingir um objetivo, neste caso, fazer testes de software.
      - Plano de Teste de Sofware: Artefato que descreve o escopo, abordagem, recursos e cronograma das atividades de teste. <font color="red">Nota 0,5</font>


   2. (**0,5 ponto**) Descreva o relacionamento existente entre estes conceitos.
    A relação entre estes conceitos é bem simples, ao termos um processo de teste bem definido podemos aplicar-lo gerando uma instância dele, e esta é chamada de projeto de teste. E durante a execução do projeto um artefato é criado, chamado de plano de teste. Ou seja, um processo de teste gera um projeto de teste que por sua vez cria o plano de teste. <font color="red">Nota 0,5</font>

2. (**1,0 pontos**) Descreva as vantagens para a equipe de desenvolvimento ao se adotar um processo de teste ágil.
  * Os testes são realizados com maior ênfase por meios automáticos, liberando tempo que seria usado para realizar testes manuais;
  * O processo ocorre durante o desenvolvimento em ciclos frequentes e contínuos, assim as funcionalidades são testadas mais rapidamentes.
  * Proximidade entre os stakeholders, garantindo sempre uma conformidade com os requisitos. <font color="red">Nota 1,0</font>

3. (**1,0 ponto**) Cite pelo menos três características do Teste Exploratório.
  * Resultados de teste, casos de teste e documentação de teste são geradas a medida que os testes são realizados;
  * Testadores podem interagir com a aplicação da forma como quiserem;
  * Ideais para o teste de aplicações web modernas, desenvolvida seguindo metodologias ágeis. <font color="red">Nota 1,0</font>

4. Considere os arquivos .java (Banco.java, Agencia.java, Conta.java e BankValidator.java). Nos próprios arquivos .java estão definidas as regras para cadastramento de cada um deles (Banco, Agencia e Conta). Desta forma, pede-se:
   1. (**2.0 Pontos**) Definir os cenários de teste suficientes para testar o cadastro e movimentações financeiras envolvendo bancos, agências e contas, conforme especificado. Para cada cenário definir os critérios de teste adequados à definição dos seus casos de teste.<br>
      * CONTA
      1. Número da conta com cinco digitos
      2. Número da conta válido
      3. Número da conta com sete digitos
      4. Tipo da conta inválido
      5. Tipo da conta válido
      6. Valor do limite da conta do tipo corrente
      7. Valor do limite da conta do tipo poupança
      8. Depositar valor na conta
      9. Sacar valor da conta
      10. Transferir valor entre contas
      11. Creditar Rendimentos da conta do tipo poupanca
      12. Debitar juros do cheque especial
      * BANCO
      1. Número do banco com um número negativo de três digitos
      2. Número do banco com dois digitos
      3. Número do banco válido
      4. Número do banco com quatro digitos
      5. Nome do banco com tamanho 4
      6. Nome do banco válido
      7. Nome do banco com tamanho 101
      8. Nome do banco com números
      9. Nome do banco com caracter inválido
      * AGENCIA
      1. Número da agência com 2 digitos
      2. Número da agência válido
      3. Número da agência com 6 digitos
      4. Nome da agência com tamanho 4
      5. Nome da agência válido
      6. Nome da agência com tamanho 101
      7. Nome da agência com números
      8. Nome da agência com caracter inválido
      9. Nome da cidade da agência com tamanho 4
      10. Nome da cidade da agência válido
      11. Nome da cidade da agência com tamanho 101
      12. Nome da cidade da agência com números
      13. Nome da cidade da agência com caracter inválido

      <font color="red">Nota 1,5</font>

   2. (**2.0 Pontos**) Definir os casos de teste suficientes para a cobertura do teste de cada um dos cenários definidos. Documentar os casos de teste no seguinte padrão:
   |CT|Valores de Entrada|Resultado esperado|
   |---|---|---|
   |01|12345;Corrente;agencia|Número, tipo, limite, saldo e agência vazias|
   |02|123456;Corrente;agencia|Número não vazio|
   |03|123457;Corrente;agencia|Número, tipo, limite, saldo e agência vazias|
   |04|123456;Especial;agencia|Tipo e limite vazios|
   |05|123456;Corrente;agencia|Tipo e limite não vazios|
   |06|123456;Corrente;agencia|10000.00|
   |07|123456;Poupanca;agencia|0.00|
   |08|conta;5000.00|25000.00|
   |09|conta;5000.00|15000.00|
   |10|conta;conta2;5000.00|15000.00;25000.00|
   |11|conta;5000.00|15000.00|
   |12|conta;5000.00|15000.00|
   |13|-123;BancoA|Número vazio|
   |14|12;BancoA|Número vazio|
   |15|123;BancoA|Número não vazio|
   |16|1234;BancoA|Número vazio|
   |17|123;Banc|Nome vazio|
   |18|123;BancoA|Nome não vazio|
   |19|123;BancoAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA|Nome vazio|
   |20|123;BancoA1|Nome vazio|
   |21|123;Banco#|Nome vazio|
   |22|12;AgenciaA;Goiania;banco|Número, nome, cidade e banco vazios|
   |23|1234;AgenciaA;Goiania;banco|Número não vazio|
   |24|123456;AgenciaA;Goiania;banco|Número, nome, cidade e banco vazios|
   |25|1234;Agen;Goiania;banco|Número, nome, cidade e banco vazios|
   |26|1234;AgenciaA;Goiania;banco|Nome não vazio|
   |27|1234;AgenciaAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA;Goiania;banco|Número, nome, cidade e banco vazios|
   |28|1234;AgenciaA1;Goiania;banco|Número, nome, cidade e banco vazios|
   |29|1234;Agencia#;Goiania;banco|Número, nome, cidade e banco vazios|
   |30|1234;AgenciaA;Goia;banco|Número, nome, cidade e banco vazios|
   |31|1234;AgenciaA;Goiania;banco|Cidade não vazia|
   |32|1234;AgenciaA;Goianiaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa;banco|Número, nome, cidade e banco vazios|
   |33|1234;AgenciaA;Goiania86;banco|Número, nome, cidade e banco vazios|
   |34|1234;AgenciaA;Goi#nia;banco|Número, nome, cidade e banco vazios|
   <font color="red">Nota 1,7</font>

  3. (**3.0 Pontos**) Implementar (na linguagem de programação java) as classes para o teste da criação dos objetos e das movimentações financeiras envolvendo bancos e agências e contas.
  <font color="red">Nota 1,73</font>
