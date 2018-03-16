# spring5-recipe-app

App downloaded from spring initializer:
http://start.spring.io/

To run the App:
./mvnw spring-boot:run


Properties:file
    spring.h2.console.enabled=true
        this enable to go to:
            http://localhost:8080/h2-console
            --------------------------------
            the console of the embedded DB, named h2
                driver class: org.h2.Driver
                JDBC URL: jdbc:h2:mem:testdb
            clic on the connect button


CircleCi:
    Build the project from the online tool:
    https://circleci.com/gh/viktorcardona/spring5-recipe-app/2


WebJars

    http://www.webjars.org/
    We can add maven dependencies for projects like:
        bootstrap
        jquery
    Then you can make this kind of references from the view:
        th:href="@{/webjars/bootstrap/3.3.7-1/css/bootstrap.min.css}"
        th:href is a tag from thymeleaf
