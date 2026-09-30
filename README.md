Dicionário de Sobrevivência: POO em C#

Use este guia para traduzir o que o código está dizendo. Se o professor mudar o tema da prova, a lógica abaixo continua 100% igual.

1. Organização do Sistema

namespace NomeQualquer

O que é: Uma gaveta ou pasta organizadora.

Como funciona: Serve para agrupar arquivos que fazem parte do mesmo assunto. Se você coloca uma classe dentro de uma gaveta chamada Senac.Cadastro, ninguém de fora consegue ver essa classe a menos que abra a gaveta.

using NomeQualquer;

O que é: A chave que abre a gaveta.

Como funciona: Fica sempre no topo do arquivo. É você dizendo ao programa: "Por favor, traga as ferramentas que estão guardadas na gaveta NomeQualquer para eu usar aqui".

2. Criando os Moldes (Classes)

public class NomeDaClasse

O que é: A planta de um projeto, o molde de gesso.

Como funciona: Uma classe não é um dado real, é apenas um desenho. Se o professor pedir um sistema de biblioteca, você cria a public class Livro.

public string Nome { get; set; } (Propriedades)

O que é: As características que o seu molde vai ter.

Como funciona: O get significa "permitir ler" e o set significa "permitir gravar". Se o professor pedir um Produto, você faria public double Preco { get; set; }.

O Construtor public NomeDaClasse(...)

O que é: A porta de entrada obrigatória, o "pedágio".

Como funciona: Tem exatamente o mesmo nome da classe e nenhum tipo de retorno (nem void). Serve para obrigar o programador a fornecer dados na hora de criar o objeto.

Exemplo: public Produto(string nome) significa "Ninguém consegue criar um Produto no sistema sem fornecer um nome".

3. Conectando as Peças (Herança)

O símbolo de dois pontos :

O que é: A Herança ("é um(a)").

Como funciona: class Carro : Veiculo significa que Carro herda tudo que Veiculo tem. Você não precisa digitar as variáveis de Veiculo de novo dentro de Carro.

A palavra : base(...)

O que é: O entregador do Sedex.

Como funciona: Fica colado no construtor da classe filha. Ele pega os dados que a classe filha recebeu e despacha (entrega) direto para a classe pai (a fundação) resolver.

4. O Motor (Programa Principal)

List<Tipo> nomeDaLista = new List<Tipo>();

O que é: O seu banco de dados temporário, a sua caixa de armazenamento.

Como funciona: O que está entre < > dita a regra da caixa. List<Carro> significa que nessa caixa SÓ entram carros. Se tentar colocar um Usuario ali, o programa quebra.

A palavra new

O que é: A fábrica de materialização. Isso é o que mais cai em prova!

Como funciona: Você não pode simplesmente jogar o texto "João" dentro da lista. Você tem que usar o new para pegar o molde, preencher com "João" e gerar o objeto físico na memória do computador.

Exemplo: lista.Add(new Produto("Caneta", 2.50));

O loop foreach (Tipo apelido in lista)

O que é: O inspetor de qualidade da esteira.

Como funciona: Ele vai na sua lista, pega o primeiro item, dá um apelido para ele (ex: p), e roda o código de baixo. Depois pega o segundo item, chama de p de novo, e roda o código.

Como ler na mente: "Para cada Produto (que vou chamar de p) dentro da minha listaProdutos, faça isso..."
