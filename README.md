# Desafio: 

	Criar um CRUD de filmes :D

Descrição:

	Deverá ser construída uma aplicação usando console.
	Um filme deverá conter um id, nome, descrição, gênero, ano e diretor.
	A estrutura do projeto deverá sem dividida nos pacotes model e repository.

Dicas:

	Inicie criando um projeto maven normal, lembrando de marcar o checkbox "Create a simple project".
	Preencha os dados básicos do projeto, que são o group id e o artifact id. O group id é como um namespace, onde ficaria todos os projetos de uma equipe ou da empresa. O group id tem o formato de um endereço de site, mas ao contrário: para os projetos da Neogrid, por exemplo, poderíamos criar o group id com.neogrid. O artifact id identifica o projeto, e podemos usar letras minúsculas, números ou hífen.
	Ao criar o projeto, devemos especificar qual é a versão do Java que ele vai utilizar. Para isso, colamos o seguinte código no pom.xml, dentro da tag <project>:
	
		<properties>
			<maven.compiler.target>11</maven.compiler.target>
			<maven.compiler.source>11</maven.compiler.source>
		</properties>
	
	Para utilizar a versão 8 do Java, devemos trocar o 11 para 1.8 (e não 8!).
	Talvez fique mais fácil iniciar o código pelas classes de modelo. Você sabe o que é um "model"? Na prática, são as classes que representam as tabelas do banco de dados que a aplicação acessa (já que normalmente as aplicações acessam um banco), ou seja, representam o modelo de dados da aplicação. Também podemos chamar essas classes de "entidades".
	Sobre essa nossa aplicação, já podemos perceber uma entidade óbvia: Filme! Vamos começar criando a classe Filme, mas tenha cuidado onde vai criar as classes! As classes não devem ser colocadas no pacote "default", ou seja, deixadas sem pacote. O pacote "raiz" tem o nome do group id, mais o nome do projeto, apenas com minusculas ou letras, nada mais. Dentro do pacote raiz, criamos um pacote "model" para colocar as entidades.
	Normalmente o id é um número incrementado automaticamente pelo banco de dados, mas nessa primeira versão da nossa aplicação, nós que iremos informá-lo. Costuma ser do tipo Long.
	Lembre-se de seguir as regras do ENCAPSULAMENTO para criar a classe Filme!
	Sobrescreva o método toString() na classe Filme. Aproveite pra relembrar os conceitos de SOBRECARGA e SOBRESCRITA. Pode pesquisar também qual é a função do método TOSTRING().
	Para representar a camada de acesso a dados, criaremos um repositório. Normalmente, os repositórios têm o nome da entidade + Repository, e ficam no pacote repository.
	O repositório deverá conter a lista de filmes já inicializada. Também deverá conter os métodos para adicionar, remover, listar e alterar filmes da lista.
	No repositório, o método para alterar deve receber um id e os dados do filme. O método para remover deve receber o id do filme.
	Para rodar a aplicação, crie uma classe chamada de Principal no pacote raiz, e crie o método main.
	Como ajuda para a classe Principal:
	
		private final FilmeRepository filmeRepository = new FilmeRepository();
		
		public static void main(String[] args) {
			final Principal principal = new Principal();
			
			final Scanner in = new Scanner(System.in);
			
			String opcao = "";
			
			while (!opcao.equals("0")) {
				System.out.println("=== CRUD DE FILMES ===\n");
				System.out.println("O que você deseja fazer?");
				System.out.println("1 - Listar todos os filmes");
				System.out.println("2 - Cadastrar novo filme");
				System.out.println("3 - Alterar um filme");
				System.out.println("4 - Remover um filme");
				System.out.println("0 - Sair");
				
				opcao = in.nextLine();
				
				if ("1".equals(opcao)) {
	
				} else if ("2".equals(opcao)) {
	
				} else if ("3".equals(opcao)) {
	
				} else if ("4".equals(opcao)) {
	
				}
			}
		}
	
