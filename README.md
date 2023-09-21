## EvoSuite

É bem parecido com o Randoop, porém no tutorial inicial ele já mostrou como executar o comando do terminal considerando que você tenha uma estrutura de projeto como a do Eclipse. Exemplo a seguir:

```powershell
evosuite -class org.example.Trivialissimo -projectCP target/classes
```

Com o comando acima ele foi capaz de identificar a classe Trivalismo e onde estão os .class. Após isso, ele gerou as classes de teste e um CSV simples mostrando a cobertura de testes. 

Diferente do Randoop, o EvoSuite não permite colocar um quantitativo de testes que desejo. Pelo que entendi do artigo, ele vai usar inteligência artificial para determinar cenários mais propícios a erro. (Pendente melhor entendimento)

Além disso, a biblioteca vai gerando informações de log enquanto executa o processo. São informações úteis que ajuda no entendimento de como ela foi pensada e trabalha.

```
* EvoSuite 1.2.0
* Going to generate test cases for class: org.example.Trivialissimo
* Starting Client-0
* Connecting to master process on port 6017
* Analyzing classpath: 
  - target/classes
* Finished analyzing classpath
* Generating tests for class org.example.Trivialissimo
* Test criteria:
  - Line Coverage
  - Branch Coverage
  - Exception
  - Mutation testing (weak)
  - Method-Output Coverage
  - Top-Level Method Coverage
  - No-Exception Top-Level Method Coverage
  - Context Branch Coverage
[Progress:>                             0%] [Cov:>                                  0%]* Total number of test goals for DYNAMOSA: 45
* Using seed 1695287484285
* Starting evolution
* Initial Number of Goals in DynaMOSA = 36 / 45
[Progress:>                             0%] [Cov:================================>  93%]
* Search finished after 0s and 1 generations, 731 statements, best individual has fitness: 1.0
* Minimizing test suite
* Going to analyze the coverage criteria
* Coverage analysis for criterion LINE
* Coverage of criterion LINE: 100%
* Total number of goals: 3
* Number of covered goals: 3
* Coverage analysis for criterion BRANCH
* Coverage of criterion BRANCH: 100%
* Total number of goals: 3
* Number of covered goals: 3
* Coverage analysis for criterion EXCEPTION
* Coverage of criterion EXCEPTION: 100%
* Total number of goals: 1
* Number of covered goals: 1
* Coverage analysis for criterion WEAKMUTATION
* Coverage of criterion WEAKMUTATION: 100%
* Total number of goals: 24
* Number of covered goals: 24
* Coverage analysis for criterion OUTPUT
* Coverage of criterion OUTPUT: 100%
* Total number of goals: 6
* Number of covered goals: 6
* Coverage analysis for criterion METHOD
* Coverage of criterion METHOD: 100%
* Total number of goals: 3
* Number of covered goals: 3
* Coverage analysis for criterion METHODNOEXCEPTION
* Coverage of criterion METHODNOEXCEPTION: 100%
* Total number of goals: 3
* Number of covered goals: 3
* Coverage analysis for criterion CBRANCH
* Coverage of criterion CBRANCH: 100%
* Total number of goals: 3
* Number of covered goals: 3
* Generated 8 tests with total length 8
* Resulting test suite's coverage: 94% (average coverage for all fitness functions)
* Generating assertions
* Resulting test suite's mutation score: 83%
* Compiling and checking tests
* Writing tests to file
* Writing JUnit test case 'Trivialissimo_ESTest' to evosuite-tests
* Done!
```

### Limitações

Apesar de existirem extensões para IDEs, elas estão bastante defasadas e não são compatíveis com as versões atuais. Portanto, para utilizá-las seria necessário usar uma versão antiga.