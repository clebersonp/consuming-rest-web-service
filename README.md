# Descrição
Estudo do framework **_Spring Boot_** versão 2.5.3. [Spring Boot Documentation](https://docs.spring.io/spring-boot/docs/2.5.3/reference/htmlsingle/).
Aplicação de estudo **_spring boot_** para consumir um **_RESTful Web Service_**. [Aplicação Spring Boot](https://spring.io/guides/gs/consuming-rest/).

### Requerimentos
- Maven versão 3.6.1 ou superior. [Maven installation](https://maven.apache.org/install.html).
- JDK versão 11 ou superior [JDK installation](https://adoptopenjdk.net/).

### Build da aplicação exemplo via plugin maven:
Digitar `mvn clean install` no diretório raiz do projeto. Você deve ver uma saída semelhante a seguinte:
```maven
$ mvn clean install
  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/
 :: Spring Boot ::                (v2.5.3)

2021-07-31 18:58:34.831  INFO 7312 --- [           main] c.e.ConsumingRestWebServiceApplicationTests      : Starting ConsumingRestWebServiceApplicationTests using Java 15.0.1
[INFO] Results:
[INFO] 
[INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0
[INFO] 
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  8.330 s
[INFO] Finished at: 2021-07-31T18:58:38-03:00
[INFO] ------------------------------------------------------------------------
```

### Execução da aplicação exemplo a partir do `fat jar` gerado:
Digitar `java -jar target/consuming-rest-web-service-0.0.1-SNAPSHOT.jar` no diretório raiz do projeto. Você deve ver uma saída semelhante a seguinte:
```java
$ java -jar target/consuming-rest-web-service-0.0.1-SNAPSHOT.jar

  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/
 :: Spring Boot ::                (v2.5.3)

2021-07-31 19:02:55.387  INFO 7431 --- [           main] com.example.FirstSpringBootApplication   : Starting ConsumingRestWebServiceApplication v0.0.1-SNAPSHOT using Java 15.0.1
2021-07-31 19:02:57.548  INFO 7431 --- [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat started on port(s): 8080 (http) with context path ''
2021-07-31 19:02:57.563  INFO 7431 --- [           main] com.example.FirstSpringBootApplication   : Started ConsumingRestWebServiceApplication in 2.861 seconds (JVM running for 3.437)
```
> **_Nota_**: Para finalizar a execução da aplicação pressionar as seguintes teclas: `ctrl + c` .

### Execução da aplicação exemplo via `plugin maven`:
Digitar `mvn spring-boot:run` no diretório raiz do projeto. Você deve ver uma saída semelhante a seguinte:
```maven
$ mvn spring-boot:run

  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/
 :: Spring Boot ::                (v2.5.3)

2021-07-31 18:56:36.932  INFO 7157 --- [           main] com.example.ConsumingRestWebServiceApplication   : Starting ConsumingRestWebServiceApplication using Java 15.0.1
2021-07-31 18:56:38.082  INFO 7157 --- [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat started on port(s): 8080 (http) with context path ''
2021-07-31 18:56:38.091  INFO 7157 --- [           main] com.example.ConsumingRestWebServiceApplication   : Started ConsumingRestWebServiceApplication in 1.51 seconds (JVM running for 1.791)
```
Você deve ver o payload da resposta da integração no log da aplicação semelhante a saída:
```json
{
    "type": "success",
    "value": {
        "id": 4,
        "quote": "Previous to Spring Boot, I remember XML hell, confusing set up, and many hours of frustration."
    }
}
```

### API RESTful consumida
Segundo a documentação, segue [link API RESTful](https://quoters.apps.pcfone.io/api/random) que será consumida pela aplicação.

## Referências
- [Spring Boot Documentation](https://spring.io/guides/gs/consuming-rest/) - Consumindo RESTful Web Service com **_RestTemplate_**.

