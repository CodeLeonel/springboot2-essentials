
# DevLog

## Configuração mínima

Nas primeiras aulas do curso foi ensinado como instalar o Spring Boot.
Diferente de usar o site básico para baixar um pacote pronto do Framework,
foi utilizado um conjunto de tags no POM.XML que praticamente realiza o download
de todas as dependências do Spring Boot de uma versão específica, a 2.3.4.RELEASE.
O conjunto de tags se apresenta a seguir:

```XML
 <parent>
   <artifactId>spring-boot-starter-parent</artifactId>
   <groupId>org.springframework.boot</groupId>
   <version>2.3.4.RELEASE</version>
  </parent>
```

 A única dependencia necessária para o funcionamento do Spring Boot é o Starter Web:

```XML
  <dependencies>
    <dependency>
     <groupId>org.springframework.boot</groupId>
     <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
   </dependencies>
```

Em seguida foi criado uma classe com o método main, com instrução de executar o programa.
Além de precisar utilizar a classe SpringApplication, também foi nessário a Anotação
@EnableAutoConfiguration para disponibilizar configurações mínimas para a execução do
Spring Boot.

O Domain e o Controller foram criados em seguida para operacionalizar o mínimo de uma
API REST, mas nada daquilo funcionaria corretamente se não fosse pela anotação @ComponentScan
que basicamente mapeou as classes para serem incluidas na aplicação REST.

-----------

## Lombok e melhoria da configuração

A classe de ignição da API subiu um nível acima para compor todos os elementos que estão e serão implementados. Lombok foi inserido no Maven, instalado na IDE, também foi executado comando: "mvn clean install -U" e o projeto foi limpado (Clean) para poder funcionar o "log" de Lombok.

Talvez seja importante encontrar uma forma de documentar anotações para aprendizado pessoal.

-----------

## Anotações anotadas

Feito um esquema para rememorar e especializar nas anotações Spring.

![Anotações Spring](./Spring.jpg)

------------

## Devtools

No POM foi acrescentado mais uma dependência, que é o DevTools. Com ela é possível xecutar mais rapidamente e também qualquer alteração realizada e salva faz com que o sprint Boot seja reiniciado.

```XML
	<dependency>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-devtools</artifactId>
	</dependency>
```

---------

## Spring Starter

A inevitabilidade do Spring Starter é forte pois possui uma configuração mais ampla. O que leva a inutilidade deste projeto agora depreciado, porém pode se tornar um desafio para realizar configurações manuais até chegar em níveis esperados da qualidade do Spring Starter. Para prosseguir com o curso as funcionalidades criadas nesta API e o DevLog serão preservados para a próxima API que será registrada mais adiante neste DevLog 




