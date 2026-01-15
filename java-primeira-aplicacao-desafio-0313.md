Olá, pessoal! Segue abaixo minha resolução:

Arquivo `Main.java`:
```java
public class Main {
    public static void main(String[] args) {
        Fatorial fatorial = new Fatorial();
        MenuOpcoes menuOpcoes = new MenuOpcoes();
        ParImpar parImpar = new ParImpar();
        PositivoNegativo positivoNegativo = new PositivoNegativo();
        SemelhancaNumeros semelhancaNumeros = new SemelhancaNumeros();
        Tabuada tabuada = new Tabuada();

        fatorial.main();
        menuOpcoes.main();
            parImpar.main();
        positivoNegativo.main();
        semelhancaNumeros.main();
        tabuada.main();
    }
}
```

Arquivo `Fatorial.java`:
```java
import java.util.Scanner;

public class Fatorial {
    public static void main() {
        Scanner ler = new Scanner(System.in);
        int numero;
        int resultadoFatorial = 0;
        int calculaFatorial;

        System.out.println("Informe um número para calcular seu fatorial");
        numero = ler.nextInt();

        for (int i = 1; i < numero; i++) {
            if(resultadoFatorial == 0){
                resultadoFatorial = numero * (numero-i);
            }else{
                resultadoFatorial = resultadoFatorial * (numero-i);
            }
        }

        System.out.printf("O fatorial de %d é %d", numero, resultadoFatorial);
        System.out.println();
    }
}
```

Arquivo `MenuOpcoes.java`:
```java
import java.util.Scanner;

public class MenuOpcoes {
    public static void main() {
        Scanner ler = new Scanner(System.in);
        int opcaoEscolhida;
        double pi = 3.14;
        double lateralQuadrado;
        double raioCirculo;
        double areaQuadrado;
        double areaCirculo;

        System.out.printf("""
                Menu principal (digite o número da opção escolhida):
                1. Calcular a área de um quadrado.
                2. Calcular a área de um círculo.
                """);
        opcaoEscolhida = ler.nextInt();

        switch(opcaoEscolhida){
            case 1:
                System.out.println("Informe o tamanho da lateral do quadrado em centímetros.");
                lateralQuadrado = ler.nextDouble();

                areaQuadrado = lateralQuadrado*lateralQuadrado;

                System.out.printf("A área do quadrado é %.2f cm².", areaQuadrado);
                break;
            case 2:
                System.out.println("Informe o tamanho do raio do círculo em centímetros.");
                raioCirculo = ler.nextDouble();

                areaCirculo = pi*(raioCirculo*raioCirculo);

                System.out.printf("A área do círculo é %.2f cm².", areaCirculo);
                break;
            default:
                System.out.println("Opção inválida, encerrando.");
                break;
        }
        System.out.println();
    }
}
```

Arquivo `ParImpar.java`:
```java
import java.util.Scanner;

public class ParImpar {
    public static void main() {
        Scanner ler = new Scanner(System.in);
        int numero;

        System.out.println("Informe um número para verificar se é par ou ímpar.");
        numero = ler.nextInt();

        if(numero % 2 == 0){
            System.out.println("O número é par!");
        }else {
            System.out.println("O número é ímpar!");
        }

        System.out.println();
    }
}
```

Arquivo `PositivoNegativo.java`:
```java
import java.util.Scanner;

public class PositivoNegativo {
    public static void main() {
        Scanner ler = new Scanner(System.in);
        System.out.println("Informe um número inteiro, por gentileza.");
        int numero = ler.nextInt();

        if(numero > 0){
            System.out.println("O número informado é positivo.");
        }else{
            System.out.println("O número informado é negativo.");
        }
        System.out.println();
    }
}
```

Arquivo `SemelhancaNumeros.java`:
```java
import java.util.Scanner;

public class SemelhancaNumeros {
    public static void main() {
        Scanner ler = new Scanner(System.in);
        int numero1;
        int numero2;

        System.out.println("Informe o primeiro número inteiro, por gentileza.");
        numero1 = ler.nextInt();
        System.out.println("Agora o segundo número...");
        numero2 = ler.nextInt();

        if(numero1 == numero2){
            System.out.println("Os números são iguais");
        }else{
            System.out.println("Os número são diferentes");
        }

        if (numero1 > numero2){
            System.out.println("O primeiro número é maior do que o segundo");
        }else{
            System.out.println("O segundo número é maior do que o primeiro");
        }

        System.out.println();
    }
}
```

Arquivo `Tabuada.java`:
```java
import java.util.Scanner;

public class Tabuada {
    public static void main() {
        Scanner ler = new Scanner(System.in);
        int numero;
        String tabuada;
        int contador = 1;

        System.out.println("Informe um número para obter a tabuada");
        numero = ler.nextInt();

        for (int i = 0; i < 10; i++) {
            System.out.printf("""
                    %d x %d = %d
                    """, numero, contador, numero*contador);
            contador++;
        }

        System.out.println();
    }
}
```

Resultado:

<img width="650" height="795" alt="Captura de tela 2026-01-15 115114" src="https://github.com/user-attachments/assets/593f515a-af24-4073-9d98-3e87bb38f789" />
<img width="474" height="433" alt="Captura de tela 2026-01-15 115120" src="https://github.com/user-attachments/assets/26f3f5ad-56c4-452d-ac45-bfd1e3c1131f" />

