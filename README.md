
# Arrays em Java

## O que são Arrays?

Os arrays (ou matrizes) em Java fazem parte do pacote `java.util`. Eles são objetos que armazenam um número fixo de valores de um único tipo. Após sua criação, o tamanho de um array é fixo.

Cada item em um array é chamado de **elemento**, e cada elemento pode ser acessado através do seu **índice**, que sempre começa em 0.

### Exemplo: Um array de 5 elementos

```
[0] [1] [2] [3] [4]
```

---

## Declarando Arrays

Na declaração de um array, cada elemento recebe um valor padrão:

- `0` para números primitivos
- `false` para booleanos
- `null` para referências

### Exemplo de código - Declaração de Arrays

Antes de declarar e inicializar arrays, é importante entender que arrays são estruturas que armazenam múltiplos valores do mesmo tipo em posições indexadas.

No exemplo abaixo, veremos diferentes formas de declarar, inicializar e acessar arrays em Java:

```java
public class Declaracao_Array {
    public static void main(String[] args) {
        int[] a = new int[4];
        int[] b;
        b = new int[10];
        int[] r = new int[44], k = new int[23];
        int[] iniciaValores = {12, 32, 54, 6, 8, 89, 64, 64, 6};
        int[] meuArray = new int[10];
        meuArray[0] = 100;
        meuArray[1] = 85;
        meuArray[2] = 88;
        meuArray[3] = 93;
        meuArray[4] = 123;
        meuArray[5] = 952;
        meuArray[6] = 344;
        meuArray[7] = 233;
        meuArray[8] = 622;
        meuArray[9] = 8522;
        System.out.println(meuArray[9]);
        System.out.println(meuArray[2]);
    }
}
```

---

## Descobrindo o tamanho de um Array

Todo array em Java possui um atributo `length`, que retorna seu tamanho.

### Exemplo:

Você pode descobrir o tamanho de um array utilizando a propriedade `.length`. Isso é útil para fazer verificações ou percorrer o array dinamicamente.

Veja um exemplo de como verificar o tamanho de arrays e utilizá-lo em uma condição:

```java
public class TamanhoArray {
    public static void main(String[] args) {
        int[] arrayUm = {12, 3, 5, 68, 9, 6, 73, 44, 456, 65, 321};
        int[] arrayDois = {43, 42, 4, 8, 55, 21, 2, 45};

        if(arrayDois.length > 8){
            System.out.println("Tamanho do ArrayDois - Maior que 8!");
        } else {
            System.out.println("Tamanho do ArrayDois - Menor que 8!");
        }

        System.out.println("\nTamanho do ArrayUm = " + arrayUm.length);
    }
}
```

---

## Inicializando um Array

### Inicialização sem valores definidos

É possível criar um array e definir apenas seu tamanho, sem atribuir valores inicialmente. Cada elemento receberá um valor padrão conforme seu tipo.

Veja como isso é feito e como acessar os valores padrão dos elementos:

```java
public class Criando_Inicializando_Array {
    public static void main(String[] args) {
        int[] arrayBase = new int[20];

        System.out.printf("%s %10s \n", "Index", "Valores");
        for(int i = 0; i < arrayBase.length; i++)
            System.out.printf("%3d %10d \n", i, arrayBase[i]);
    }
}
```

### Inicialização com valores definidos

Também é possível inicializar um array com valores definidos no momento da declaração.

O exemplo abaixo mostra como declarar e inicializar um array ao mesmo tempo e depois exibir os elementos:

```java
public class Inicializando_Array {
    public static void main(String[] args) {
        int[] array = {10, 20, 30, 40, 50, 60, 70, 80, 90, 100, 110};

        System.out.printf("%s %12s \n", "Index", "Valores");
        for(int counter = 0; counter < array.length; counter++)
            System.out.printf("%5d %4s %4d \n", counter, "=>", array[counter]);
    }
}
```

---

## Percorrendo Arrays

### Sintaxe do `for` aprimorado (for-each)

```java
for (tipo identificador : nomeDoArray)
    instrução;
```

### Exemplo:

O laço `for` aprimorado (ou for-each) é útil para percorrer arrays de maneira mais simples e legível, quando não é necessário acessar o índice dos elementos.

Veja um exemplo onde somamos todos os elementos de um array utilizando `for-each`:

```java
public class Percorrendo_Arrays_For_Aprimorado {
    public static void main(String[] args) {
        int[] arrayNum = {87, 68, 52, 5, 49, 83, 45, 12, 64};
        int total = 0;

        for(int i : arrayNum)
            total += i;

        System.out.printf("Total de elementos arrayNum: %d\n", total);
    }
}
```
