# Maven: Build do zero a web

## Conteúdo Detalhado

### 1. O build: do zero a relatórios
	`Bem vindo
	O problema da linha de comando
	O maven: compilando, testando e além
	Relatório com surefire, e o package
	Maven no Eclipse
	Repositórios remoto, central e local`

### 2. O ciclo de vida
	`O ciclo de vida de um build e as fases
	Relatorio de qualidade e alterando fases do build
	Relatorio de cobertura com jacoco
	Dois goals em uma fase
	Todo o maven dentro do eclipse`

### 3. Web
	`Projeto web
	Rodando o jetty
	Plugins de servidor
	Mudando a versão das servlets
	Criando uma servlet
	O hot swap`

### 4. Empacotamento
	`Gerando nosso war
	Instalando um projeto
	Interdependências entre projetos
	Instalando o projeto local
	O problema de testes locais
	Controlando escopos com runtime, provided, test e compile
	Controlando escopos com override e exclusoes
	Resumindo`

#### Primeiros passos:

1° Passo: [Download do Maven](https://maven.apache.org/download.cgi)

2° Passo: Configurar path(variaveis de ambiente) do maven para ser utilizado via terminal: 
1. No windows digite no menu iniciar "Editar às variáveis de ambiente do sistema". 
2. Depois vá em "variáveis de ambiente". 
3. Variáveis de usuário > Path > Editar > Novo e depois cole o endereço da pasta bin do maven, no meu caso > C:\apache-maven-3.6.3\bin

	
- Para gerar um projeto quickStart no maven

`$ mvn archetype:generate -DartifactId=produtos -DgroupId=br.com.alura.maven -DinteractiveMode=false -DarchetypeArtifactId=maven-archetype-quickstart`

- Para compilar o projeto

`$ mvn compile`

- Não verifica atualizaçoes na internet(offline)

`$ mvn -o <comando>`

- Para testar e baixar possiveis bibliotecas usadas no teste

`$ mvn test`

- Para testar e não verificar na internet atualizações da dependencia

`$ mvn -o test`

- Para limpar o projeto(exclui a pasta target)

`$ mvn clean`

- Para gerar um relatorio de testes em uma pagina html

`$ mvn surefire-report:report`

- Para empacotar(criar um jar)

`$ mvn package`

- Para empacotar(criar um jar) e pular os testes

`$ mvn -DskipTests=true package`

- Para rodar o jar empacotado com a classe main App.java

`$ java -cp produtos-1.0-SNAPSHOT.jar br.com.alura.maven.App`

- Para gerar um relatorio que analisa o codigo fonte e verifica possiveis margens de bug no codigo

`$ mvn pmd:pmd`

- Falha na compilação se houver alguma violação do PMD no código-fonte

`$ mvn pmd:check`

- Para receber uma lista completa de metas e parâmetros disponíveis(plugin do jacoco)

`$ mvn jacoco:help`

