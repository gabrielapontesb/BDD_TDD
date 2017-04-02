## Padrões de projeto com BDD e TDD



Postagem referente aos exercícios:

1) [Imposto de Renda com o padrão Strategy](https://github.com/gabrielapontesb/Strategy)
2) [Ar Condicionado com o padrão Observer](https://github.com/gabrielapontesb/Observer)



Há um grande confusão entre a definição de BDD e TDD. Antes da realização desses exercícios, confesso que passei nas matérias e continuei sem entender realmente o real significado delas. Por isso, vale a pena primeiro entender o conceito de cada uma e definir onde eles se encaixam.


Ambos são técnicas para o desenvolvimento ágil. O TDD *(Test Driven Development)* se baseia em pequenos ciclos de repetições, onde para cada funcionalidade do sistema, um teste é criado antes. Ou seja, primeiramente o desenvolvedor escreve um caso de teste automatizado que define uma melhoria desejada ou uma nova funcionalidade. Então, é produzido código que possa ser validado pelo teste. O objetivo é fazer com que o teste passe com sucesso e assegurar que a funcionalidade tenha qualidade.


Já o BDD *(Behaviour Driven Development)*  visa integrar regras de negócios com linguagem de programação, focando o comportamento do software. Além disso, pode-se dizer também, que BDD é a evolução do TDD. Acontece que, embora o TDD seja uma técnica testada e aprovada por grandes desenvolvedores ágeis, muitas equipes de desenvolvimento não sabem por onde começar, o que testar e o que não testar. Quem escreve os testes são os desenvolvedores, mas quando a equipe de qualidade vai testar, ela se preocupa com o comportamento do sistema e não com os testes unitários. Desta forma, não há comunicação eficiente entre as duas equipes no nível de código. Para resolver esses problemas, no BDD primeiro se escreve o teste e somente depois que o código é implementado. 


Esses testes são escritos por meio de features e possuem uma linguagem acessível a qualquer pessoa, principalmente aquelas que não desenvolvem. Exemplo:

	Feature: Calcular imposto de renda
	
	Scenario: Calcular imposto de acordo com a categoria
		Given O meu salario eh 2000
		When Eu quero calcular o imposto de renda
		Then Eu vou pagar 150 reais de imposto
   
   
Depois de escritas, as features são transformadas em código pelos desenvolvedores. Nestes exercícios foi utilizado o Cucumber, um framework que auxilia na implementação das features. Ele gera automaticamente o cabeçalho das funções que precisam ser implementadas para rodar os testes.


**Resultado do Cucumber**

	You can implement missing steps with the snippets below:

	@Given("^O meu salario eh (\\d+)$")
	public void o_meu_salario_eh(int arg1) throws Throwable {
		// Write code here that turns the phrase above into concrete actions
		throw new PendingException();
	}


	@Then("^Eu vou pagar (\\d+) reais$")
	public void eu_vou_pagar_reais(int arg1) throws Throwable {
		// Write code here that turns the phrase above into concrete actions
		throw new PendingException();
	}


A responsabilidade de implementação agora é do desenvolvedor, que deve fazer primeiro com que o teste falhe e depois que ele passe. Isso para garantir que a implementação dos testes esteja funcionando.


Depois de resolver os exercícios e pesquisar sobre os significados, finalmente ficou entendido o passo a passo sobre BDD e TDD. Espero que esteja mais claro para você, assim como está para mim. Lembrando que é possível conferir o código nos links acima :)
