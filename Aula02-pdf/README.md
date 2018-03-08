Essa classe se encontra no pacote org.junit e os seus métodos são estáticos, desta forma, eles podem ser invocados
diretamente a partir da classe:
Assert.assertEquals( “abc”, “abc”);
Porém recomenda-se fazer uma importação estática:
import static org.junit.Assert.*;
e chamar o método diretamente sem a classe:
assertEquals( “abc”, “abc”);
pois fica mais fácil a leitura do código pelo programador.
A classe Assert possui os seguintes métodos que são úteis para escrever testes. Esses métodos são usados para verificar
falhas, ou seja, eles não lançam a exceção AssertionError quando o resultado do teste está correto:
* fail(String message) e fail(): estes métodos são usados criar uma falha, ou seja, ao colocar ele no corpo de um
método de @Test ele irá acusar a falha. Veja como exemplo a Figura 8 e Figura 9. Para fazer esse teste programe o
Passo 4 da seção Exemplo Aula2;
-> assertEquals: este método é usado para testar se o resultado da operação confere com o valor esperado. Por ele
estar sobrecarregado ele possui várias formas de ser chamado. Veja como exemplo a Figura 10. Para fazer esse teste
programe o Passo 5 da seção Exemplo Aula2;
-> assertTrue e assertFalse: estes métodos são usados para conferir se uma condição é true e false, respectivamente.
Para fazer esse teste programe o Passo 6 da seção Exemplo Aula2;
-> assertNull e assertNotNull: estes métodos são usados para conferir se um objeto é nulo. Para fazer esse teste
programe o Passo 7 da seção Exemplo Aula2;
-> assertSame e assertNotSame: estes métodos são usados para conferir se dois objetos referenciam o mesmo objeto.
Para fazer esse teste programe o Passo 8 da seção Exemplo Aula2;
-> assertArrayEquals: este método é usado para conferir se dois arrays possuem o mesmo conteúdo. Para fazer esse
teste programe o Passo 9 da seção Exemplo Aula2.
O JUnit prove ainda as seguintes opções para tratar condições de teste. Para fazer esse teste programe o Passo 10 da seção
Exemplo Aula2:
-> @Test(timeout=1000): o teste irá falhar caso ele dure mais de 1 segundo;
-> @Test(expected=Exception): o teste irá falhar caso ele não lance a exceção esperada ou um subtipo dela.