Classe `Main.java`:
```java
public class Main {
    public static void main(String[] args) {
        Aluno aluno = new Aluno();
        aluno.nome = "Michel Leal";
        aluno.idade = 29;
        aluno.exibeInformacoes();
    }
}
```

Classe `Pessoa.java`:
```java
public class Pessoa {
    void olaMundo(){
        System.out.println("Olá, Mundo!");
    }
}
```

Classe `Calculadora.java`:
```java
public class Calculadora {
    double dobraNumero(double numero){
        return numero * 2;
    }
}
```

Classe `Musica.java`:
```java
public class Musica {
    String titulo;
    String artista;
    int anoLancamento;
    double avaliacao = 0;
    double mediaAvaliacao = 0;
    int totalAvaliacao = 0;

    void exibeFichaTecnica(){
        System.out.println("Título da música: " + titulo);
        System.out.println("Artista: " + artista);
        System.out.println("Ano de lançamento: " + anoLancamento);
        System.out.println("Avaliações: " + mediaAvaliacao);
        System.out.println("Total de avaliações: " + totalAvaliacao);
    }

    void avaliaMusica(double nota){
        avaliacao += nota;
        totalAvaliacao ++;
    }

    double mediaAvaliacao(){
        mediaAvaliacao = avaliacao / totalAvaliacao;
        return mediaAvaliacao;
    }
}
```

Classe `Carro.java`:
```java
import java.util.Calendar;

public class Carro {
    String modelo;
    int ano;
    String cor;
    void exibeFicha(){
        System.out.println("Modelo do carro: " + modelo);
        System.out.println("Ano: " + ano);
        System.out.println("Cor: " + cor);
    }
    void idadeCarro(Calendar calendario){
        int idade = calendario.get(Calendar.YEAR) - ano;
        System.out.println("Idade do carro: " + idade + " anos");
    }
}
```

Classe `Aluno.java`:
```java
public class Aluno {
    String nome;
    int idade;
    void exibeInformacoes(){
        System.out.println("Nome do aluno: " + nome);
        System.out.println("Idade: " + idade);
    }
}
```
