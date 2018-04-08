# spring5-recipe-app

This app was implemeted by @Jhon Thompson through the course: 
Spring Framework 5: Beginner to Guru

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

CodeCov:

    https://codecov.io/
    
    Code Coverage Done Right
    
    To generate test coverage of the unit tests:
    Adding the plugin in the pom.xml:
        cobertura-maven-plugin
    
    Then, for the circle CI script:
        .circleci/config.yml
        Look for the line:
        - run: mvn integration-test
        And change it to run the test coverage:
        - run: mvn integration-test cobertura:cobertura
        
        Also add the following lines to .circleci/config.yml
        
         - store_test_results:
             path: target/surefire-reports
        
          - run:
              name: Send to CodeCov
              command: bash <(curl -s https://codecov.io/bash)
         
         