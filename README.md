//EXPLICAÇÃO DAS ESTRUTURAS BASE E FUNCIONAMENTO

// CLASSE PRINCIPAL
```
/* classe
| visibilidade | class | nome |
|    public    | class | Main | */

public class Main {

    // main é necessario para rodar o codigo mas so pode ser colocado na classe
    // principal
    public static void main(String[] args) {

    //------------------------------------------------------------------------------------------------------------------------


        /* vetor
        | tipo + [] | nome | new | tipo + [ TAMANHO ] |
        |   int[]   | veto | new | int[10] |
        não se apegue apenas ao tipo int, vetores podem armazenar qualquer tipo ate mesmo objetos */

        // aqui definimos o tamanho mas os valores não
        int[] vetor = new int[10];

        // aqui definimos os valores mas o tamanho não, e estamos armazenando objetos do TIPO PESSOA
        Pessoa[] vetor2 = {};

    //------------------------------------------------------------------------------------------------------------------------


        // criar um objeto

        // | tipo | nome | new | classe do objeto e parametros de entrada
        // | pessoa | alguem | new| pessoa ( nome da pessoa )

        Pessoa alguem = new Pessoa("claudio");
        // new quer diser que é um novo objeto


//------------------------------------------------------------------------------------------------------------------------


        /* chamar um metodo do objeto

            1. chamar o objeto ---> alguem

            isto seria a mesma coisa que entrar na classe

            2. chamr o metodo desejado separando com um ponto ---> alguem.falar()

            apos entrar na classe ai podemos chamar o metodo

            caso o metodo tenha que ser chamado dentro da classe pessoa não precisa chamar o objeto
            DENTRO ---> falar()
            FORA ---> alguem.falar()
        */

        alguem.falar();

        // este possui parametros de entrada por isso eu entrego dois valores separaddos por virgula para o metodo
        alguem.somar(1, 1);


//------------------------------------------------------------------------------------------------------------------------


        // for i

        // for ( variavel ; condição/limite ; incremento/decremento ) {}

        /* for ( int i = 0;      i < 10     ;           i++         ) { 
            SEU CODIGO SERA EXECUTADO AQUI DENTRO ENQUANTO A CONDIÇÃO FOR VERDADEIRA
            ATENÇÃO COM AS CHAVES ELAS SÃO MUITO IMPORTANTES
        } */

        for (int i = 0; i < 10; i++) {

            //enquanto o valor de i for menor que 10 o for vai ser executado
            System.out.println(i); //imprime i 10 vezes com valores de 0 a 9

            // ja que neste for o ( i ) vai de 0 a 9
            // esta simples linha percorre o vetor dos indices 0 ate o 9
            vetor[i];

            // [i] ---> referece ao indice de valor i daquele vetor

        }

    }
}
```
// CLASSE SECUNDARIA
```
class Pessoa {

    /*
     * atributos
     * | visibilidade | tipo | nome |
     * | private | int | idade |
     */

    // atributos agem como caracteristicas do objeto

    private String nome;
    private int dinheiro;
    // na classe main não precisa colocar a visibilidade

    // ------------------------------------------------------------------------------------------------------------------------

    /*
     * construtor
     * | visibilidade | nome da classe |
     * | public | Pessoa |
     * public pessoa ( PARAMETROS DE ENTRADA ) |
     */

    /*
     * os parametros de entrada são um requisito para o construtor funcionar e
     * define os valores dos atributos usando os parametros
     * mas ja que dinheiro é um atributo padrão não precisa de parametro de entrada
     * para ele o valor sera atribuido manualmente
     */

    public Pessoa(String nome) {
        // this se refere ao atributo que foi declarado no inicio da classe
        this.nome = nome;

        /*
         * como foi dito anteriormente este atributo é padrão pois recebe seu valor logo
         * de cara e não precisa de um parametro para ele
         * ele vai servir como um valor de inicio universal para aquele tipo de objeto
         * EXEMPLO: um carro por padrao tem 4 rodas ou seja | this.rodas = 4; |
         */
        this.dinheiro = 0;
    }

    // ------------------------------------------------------------------------------------------------------------------------

    /*
     * metodos
     * | visibilidade | retorno | nome |
     * | public | void | falar |
     */

    // não retorna nada
    public void falar() {
        System.out.println("ola criança!");
    }

    // assim como o construtor quando o metodo possui um parametro de entrada é
    // necessario preencer os campos para que ele funcione
    // retorna um inteiro
    public int somar(int a, int b) {

        // quando o metodo retorna algo o return entra em ação
        return a + b;
    }

}
