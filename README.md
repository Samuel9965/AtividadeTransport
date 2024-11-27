Sistema de Aluguel de Meios de Transporte

Este projeto implementa um sistema para gerenciar o aluguel de meios de transporte individuais utilizando o padrão de projeto Abstract Factory. O objetivo do sistema é permitir a criação de diferentes meios de transporte classificados em duas categorias: movidos a bateria e movidos pelo esforço humano.
Objetivo

    Criar um sistema de transporte utilizando o padrão de projeto Abstract Factory.
    Gerenciar meios de transporte individuais como bicicletas, patinetes, patins e skates.
    Diferenciar os meios de transporte em duas categorias:
        Movidos a Bateria: Patinetes elétricos, bicicletas elétricas.
        Movidos pelo Esforço Humano: Bicicletas convencionais, patins, skates.

Estrutura do Projeto

O projeto foi estruturado com base no padrão de design Abstract Factory, com o intuito de criar transportes de diferentes categorias, dependendo da sua propulsão.
Estrutura de Pastas

meuProjeto/
├── src/
│   └── com/
│       └── example/
│           └── transport/
│               ├── Transport.java
│               ├── ElectricScooter.java
│               ├── ElectricBike.java
│               ├── Bicycle.java
│               ├── RollerSkates.java
│               ├── Skateboard.java
│               ├── TransportFactory.java
│               ├── ElectricTransportFactory.java
│               ├── HumanPoweredTransportFactory.java
│               └── Main.java

Arquivos

    Transport.java
    Interface que define o contrato para os meios de transporte com o método ride().

    Classes Concretas
        ElectricScooter.java: Representa um patinete elétrico.
        ElectricBike.java: Representa uma bicicleta elétrica.
        Bicycle.java: Representa uma bicicleta convencional.
        RollerSkates.java: Representa patins.
        Skateboard.java: Representa um skate.

    Fábricas
        TransportFactory.java: Fábrica abstrata que declara os métodos para criar os transportes.
        ElectricTransportFactory.java: Fábrica concreta que cria transportes movidos a bateria (patinete elétrico e bicicleta elétrica).
        HumanPoweredTransportFactory.java: Fábrica concreta que cria transportes movidos pelo esforço humano (bicicleta convencional, patins e skate).

    Main.java
    Classe principal que demonstra o uso das fábricas para criar os transportes e exibir mensagens de uso (via método ride()).

Como Rodar o Projeto
Pré-requisitos

    Java JDK (Versão 8 ou superior)
    Ambiente de Desenvolvimento: Você pode usar qualquer editor de texto ou IDE, como Visual Studio Code, IntelliJ, ou Eclipse.

Passos para Executar

    Clone o repositório ou baixe o projeto.

    Abra o terminal no diretório do projeto e compile os arquivos .java usando o comando javac:

javac src/com/example/transport/*.java

Após a compilação, execute a classe Main para visualizar o funcionamento do sistema:

    java com.example.transport.Main

    O sistema exibirá mensagens no console indicando os meios de transporte sendo utilizados.

Exemplo de Saída

Riding an electric scooter.
Riding an electric bike.
Riding a bicycle.
Riding roller skates.
Riding a skateboard.

Descrição do Código

O código foi estruturado para simular o aluguel e o uso de diferentes meios de transporte, divididos entre aqueles movidos por bateria e os movidos por esforço humano.
Padrão Abstract Factory

A aplicação segue o padrão de projeto Abstract Factory, que é utilizado para fornecer uma interface para criar famílias de objetos relacionados sem especificar suas classes concretas.
TransportFactory (Fábrica Abstrata)

A interface TransportFactory declara métodos para criar objetos de transporte, como createScooter() e createBike(). As classes concretas que implementam essa interface fornecem a lógica para a criação dos objetos específicos.
Fábricas Concretas

    ElectricTransportFactory: Cria transportes movidos a bateria (como patinetes e bicicletas elétricas).
    HumanPoweredTransportFactory: Cria transportes movidos por esforço humano (como bicicletas convencionais, patins e skates).

Classes de Transporte

Cada tipo de transporte implementa a interface Transport e o método ride(), que exibe uma mensagem no console indicando que o transporte está sendo utilizado. As classes de transporte são:

    ElectricScooter (Patinete Elétrico)
    ElectricBike (Bicicleta Elétrica)
    Bicycle (Bicicleta Convencional)
    RollerSkates (Patins)
    Skateboard (Skate)

Fluxo de Execução

    No Main.java, o sistema cria uma fábrica para os transportes movidos a bateria (ElectricTransportFactory) e outra para os transportes movidos pelo esforço humano (HumanPoweredTransportFactory).
    Em seguida, os transportes são criados usando as fábricas, e o método ride() é chamado para simular o uso do meio de transporte.
    O sistema exibe no console mensagens informando o tipo de
transporte sendo utilizado.

Conclusão

Este sistema é um exemplo de como aplicar o padrão de projeto Abstract Factory para criar objetos de diferentes famílias (tipos de transportes) e usá-los de maneira consistente. Ele pode ser expandido facilmente para incluir novos tipos de transporte e novas fábricas, tornando-o uma solução flexível para sistemas de aluguel de meios de transporte.

Esse é o resultado expresso no terminal:  
 ![Captura de tela de 2024-11-27 15-29-38](https://github.com/user-attachments/assets/0d62056b-2d65-456a-99c3-64386e4882e0)

Esse README.md cobre a descrição da atividade, o funcionamento do código, como rodar o projeto e detalhes importantes sobre a implementação. Se houver mais informações ou ajustes que você gostaria de incluir, sinta-se à vontade para personalizar ainda mais o arquivo.
