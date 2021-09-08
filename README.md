# programa-de-bolsas-compasso
Exercicios Programa de bolsas .Net

 # Sugestão atividade 1 Sprint 3

Requisitos funcionais e não funcionais

1 - Requisitos Funcionais:

 * O usuário deve informar o numero da mesa;
 * As opções do cardápio devem aparecer;
 * As mesas aceitas são: 1, 2, 3 e 4. Validar mesa inválida;
 * Validar código de produto valido na lista de produtos(consultar via linq);
 * Encerrar pedido ao informar código do produto 999;
 * Após encerrar pedido, imprimir a lista de itens do pedido em formato JSON( utilize a classe JavaScriptSerializer() )

2 - Requisitos não funcionais

  * C#;
  * Criar classes em arquivos .cs separados.
  * Classes:
    - Pedido
      - Valor Total
      - Lista<Produto>
    - Produto
      - Codigo
      - Descricao
      - ValorUnitario      
    - Cardapio
      - Lista<Produto>

  * Utilizar array de para armazenar lista de mesas;
  * Utilizar Lista de para armazenar lista de cardápio de produtos e preços;
  * Após encerrar pedido, imprimir a lista de itens do pedido em formato JSON( utilize a classe JavaScriptSerializer() )


- O cardápio automatizado de uma lancheria
  - Quando o usuário abrir o sistema, mostrar a seguinte informação
  - Entrada :

```
Qual o numero da mesa ?: XX
Qual  o item (Codigo) do pedido abaixo? 

- Entrada em loop :
Código  Produto                   Preço Unitário (R$)
100       Cachorro quente     R$  5,70
101       X Completo          R$ 18,30
102       X Salada            R$ 16,50
103       Hamburguer          R$ 22,40
104       Coca 2L             R$ 10,00
105       Refrigerante        R$  1,00
999       Encerra pedido

Codigo:XX
Quantidade:XX

```
- Quando o usuário digitar 999, encerrar pedido e mostrar saída

```
///Saida 1:

A mesa XXX pediu os seguintes itens:
 1 - Cachorro quebte
 2 - X Completo
Com valor total de R$: 60,6

```
/// Saída 2
// Imprimir items do pedido em json. 

```json
          
{ "ValorTotal" : 60.6,
  "Itens" : [
    { "Codigo" : 100,
      "Descricao" : "Cachorro quente"
    },
    { "Codigo" : 101,
      "Descricao" : "X Completo"
    }    
]}

```
# Exemplos

- menu Principal

```
   
        static void Main(string[] args)
        {
            bool exibeMenu = true;
            while (exibeMenu)
            {
                exibeMenu = Menu();
            }
        }

        private static bool Menu()
        {
            Console.Clear();
            Console.ForegroundColor = ConsoleColor.Red;

            Console.Write("▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒ PEDIDOS ▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒");
            Console.ForegroundColor = ConsoleColor.White;
            Console.WriteLine("╔═════════════════MENU DE OPÇÕES════════════════╗    ");
            Console.WriteLine("║ 1 EFETUAR PEDIDO                              ║    ");
            Console.WriteLine("║ 2 SAIR                                        ║    ");
            Console.WriteLine("╚═══════════════════════════════════════════════╝    ");

            Console.WriteLine(" ");
            Console.Write("DIGITE UMA OPÇÃO : ");
            var leitura = Console.ReadLine();

           switch (Console.ReadLine())
            {
                case "1":
                    Pedido();
                    return true;
                case "2":
                    return false;
                default:
                    return true;
            }
        }

        private static void Pedido()
        {
            Console.Clear();
            Console.WriteLine("Pedido");

            // TODO
 
        }        

```