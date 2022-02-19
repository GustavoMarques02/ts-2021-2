## Tarefa 006 - 15/02/2022 - Grafo de Fluxo de Controle

1. Considere o fragmento de código implementado na Linguagem de Programação Java.

~~~java

public class Avaliacao {


1    public String avalia(double nota1, double nota2, int faltas, int cargaHoraria) throws ValoresInvalidosException{
2        String result;
3        double percentualFaltas = (faltas*100/cargaHoraria);
4        double media = (nota1 + nota2)/2;
5        if((nota1 < 0.0 || nota1 > 10) || (nota2 < 0.0 || nota2 > 10) || (faltas < 0 || faltas > cargaHoraria) || cargaHoraria < 0){
6            throw new ValoresInvalidosException();//result = "Valores Inválidos.";
7        }else if(percentualFaltas > 25.0){
8            result = "Reprovado por Falta.";
9        }else if(media < 3.0){
10            result = "Reprovado por Média.";
11        }else if(media >= 3.0 && media < 6.0){
12            result = "Prova Extra.";
13        }else{
14            result = "Aprovado.";
15        }
16        return result;
17    }
18 }
~~~

2. Pede-se:
   1. Desenhar o **Grafo do Fluxo de Controle**. Pode-se anexar a imagem, aqui neste arquivo.
   2. Calcular a complexidade ciclomática do código. Exemplo de como calcular pode ser obtido no [link](https://www.treinaweb.com.br/blog/complexidade-ciclomatica-analise-estatica-e-refatoracao)
   3. Definir quantos caminhos de execução existem;
   4. Definir os casos de teste necessários para se percorrer todos estes caminhos. Cada caso de teste deve ter o valor correspondente para cada variável de entrada e o valor esperado.

   **Grafo do Fluxo de Controle**

   <img src="https://github.com/GustavoMarques02/ts-2021-2/blob/main/Tarefa-006/imagens/Grafo-do-Fluxo-de-Controle.png">

   **Complexidade Ciclomática (C)**

   C = arcos - nós + 2
   C = 14 - 11 + 2
   C = 5

   **Caminhos de Execução**

   Considere o GFC abaixo:
   <img src="https://github.com/GustavoMarques02/ts-2021-2/blob/main/Tarefa-006/imagens/GFC-Caminhos.png">
   Os caminhos de execução serão:
   1. ABCEGIK
   2. ABDK
   3. ABCFK
   4. ABCEHK
   5. ABCEGJK

   **Casos de Teste**

   |Caso de Teste|B|C|E|G|Resultado Esperado|
   |--|--|--|--|--|--|
   |CT1|False|False|False|False|Aprovado.           |
   |CT2|True |N/A  |N/A  |N/A  |Valores Inválidos.  |
   |CT3|False|True |N/A  |N/A  |Reprovado por Falta.|
   |CT4|False|False|True |N/A  |Reprovado por Média.|
   |CT5|False|False|False|True |Prova Extra.        |