# Java-Spring

Krótki pokaz tworzący bazowy projekt w Springu

POTRZEBNE ZALEŻNOŚCI w mavenie ( może jest za dużo , ale cholera wie )
```
<dependencies>
        <!-- https://mvnrepository.com/artifact/org.springframework/spring-core -->
        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-core</artifactId>
            <version>6.1.9</version>
        </dependency>
        <!-- https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-starter-test -->
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-test</artifactId>
            <version>3.3.0</version>
            <scope>test</scope>
        </dependency>
        <!-- https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-starter-web -->
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
            <version>3.3.0</version>
        </dependency>

        <!-- https://mvnrepository.com/artifact/org.springframework/spring-web -->
        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-web</artifactId>
            <version>6.1.9</version>
        </dependency>

    </dependencies>
```

WYGLAD KLASY MAIN

```
@SpringBootApplication
public class Main {
    public static void main(String[] args) {
        SpringApplication.run(Main.class,args);
    }
}
```


WYGLĄD KONTROLERA POLECEŃ 
```
@RestController
public class Controller {
    @GetMapping("/")
    public String helloWord(){
        return "Hello World";
    }
    @GetMapping("/KochamJave")
    public String kochamJave(){
        return "jaja sobie robisz";
    }
}
```

takich kontrolerów może być wiele , aby polecenia z nich mogły się wykonywać , klasa musi posiadać nagłówek "@RestController"
