# Apresentação: Programação Orientada a Eventos e C# ⚡️🛠️

## Descrição
Esta apresentação aborda os principais tópicos relacionados ao paradigma de programação orientada a eventos e à linguagem C#. O conteúdo é dividido da seguinte forma:

## Paradigma Orientado a Eventos 💡

- **Conceitos**: Explicação sobre o que é um paradigma e como ele se aplica à programação orientada a eventos. Definições sobre eventos, *listeners* e *handlers* são apresentadas.
- **Vantagens e Desvantagens**: O paradigma permite a criação de aplicações mais dinâmicas e modulares, mas também aumenta a complexidade devido à natureza assíncrona.
- **Casos de Uso**: Exemplos incluem interfaces gráficas, jogos e sistemas de tempo real.
- **Linha do Tempo**: Evolução do paradigma, de sistemas como Whirlwind até a aplicação moderna em IoT. ⏳

## Linguagem C# ⚛️

- **História**: Criada em 2000, C# foi projetada como uma linguagem moderna para o .NET, buscando competir com Java.
- **Criador**: Anders Hejlsberg liderou o desenvolvimento da linguagem, com suporte de colaboradores como Scott Wiltamuth e Peter Golde.
- **Uso no Mercado**: Aplicações incluem ASP.NET, desenvolvimento de jogos com Unity 🎮, e aplicações móveis com Xamarin 📱.
- **Ano de Pico e Logotipo**: A linguagem teve seu auge em popularidade entre 2010-2015, com um logotipo que reflete a robustez e a identidade visual da Microsoft.

## Sintaxe e Semântica do C# 📝

- São discutidas as principais características da linguagem, como namespaces, classes, estruturas de controle, LINQ e expressões lambda.

## Referências 📚

1. [BestProg: "The history of the emergence of the C# programming language and Microsoft .NET technology"](https://www.bestprog.net/en/2022/05/22/c-the-history-of-the-emergence-of-the-c-programming-language-and-microsoft-net-technology/)
2. [DEV Community: "C#'s History, .NET Relationship, and Advantages/Disadvantages"](https://dev.to/snelson723/cs-history-net-relationship-and-advantagesdisadvantages-102b)
3. [AltexSoft: "C# Pros and Cons"](https://www.altexsoft.com/blog/c-sharp-pros-and-cons/)
4. [DEV Community: "The History and Importance of C# in the Software Industry"](https://dev.to/dogaaydinn/the-history-and-importance-of-c-in-the-software-industry-if2)
5. [DotNetCurry: "The Evolution of C#"](https://www.dotnetcurry.com/csharp/1465/csharp-evolution)
6. [CodeGuru: "C# Advantages"](https://www.codeguru.com/csharp/c-sharp-advantages/)
7. [DevMedia: "O que é C#?"](https://www.devmedia.com.br/introducao-ao-c/1696)
8. [Microsoft Docs: "Visão geral do C#"](https://learn.microsoft.com/pt-br/dotnet/csharp/)
9. [GeeksforGeeks: "What is the Event Driven Programming Paradigm"](https://www.geeksforgeeks.org/what-is-the-event-driven-programming-paradigm/)
10. [StudySmarter: "Event Driven Programming"](https://www.studysmarter.co.uk/explanations/computer-science/computer-programming/event-driven-programming/)
11. [The Architecture of Open Source Applications - Twisted](https://aosabook.org/en/v2/twisted.html)
12. Concepts of Programming Languages - Robert W. Sebesta, 2012 (PDF)
13. Programming Language Pragmatics - Michael L. Scott, 2008 (PDF)
14. Paradigmas de Desenvolvimento de Software: Comparação entre abordagens orientada a eventos e orientada a notificações - ROBSON DUARTE, 2014 (PDF)
15. [Microsoft Docs: "Compiler Errors"](https://learn.microsoft.com/pt-br/dotnet/csharp/language-reference/compiler-messages/feature-version-errors)
16. [Microsoft Docs: "Classes e Structs"](https://learn.microsoft.com/pt-br/dotnet/csharp/programming-guide/classes-and-structs/)
17. [Microsoft Docs: "If, Else If, Else Statements"](https://learn.microsoft.com/en-us/training/modules/csharp-if-elseif-else/)
18. [Microsoft Docs: "Selection Statements"](https://learn.microsoft.com/pt-br/dotnet/csharp/language-reference/statements/selection-statements)
19. [Microsoft Docs: "Events Programming Guide"](https://learn.microsoft.com/pt-br/dotnet/csharp/programming-guide/events/)
20. [Microsoft Docs: "List<T> Class"](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1?view=net-8.0)
21. [Microsoft Docs: "Iteration Statements - The For Statement"](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/statements/iteration-statements#the-for-statement)
22. [Wikipedia: "Whirlwind I"](https://en.wikipedia.org/wiki/Whirlwind_I)
23. [Wikipedia: "Semi-Automatic Ground Environment (SAGE)"](https://en.wikipedia.org/wiki/Semi-Automatic_Ground_Environment)

## TrafficLightSimulationGUI - Exemplo Prático 🚦

### Descrição
**TrafficLightSimulationGUI** é um projeto em C# que simula o funcionamento de um semáforo usando uma interface gráfica. O projeto foi desenvolvido para demonstrar conceitos de *programação orientada a eventos*, um paradigma muito utilizado em interfaces gráficas e sistemas que precisam reagir a eventos externos, como cliques de usuários e temporizadores.

### Estrutura do Projeto 📁
O projeto é composto por diferentes arquivos que desempenham papéis específicos:

- **Form1.cs**: Contém a lógica do formulário, incluindo como as luzes do semáforo mudam e a interação com o botão de pedestre. Implementa eventos que respondem às interações do usuário (como o clique do botão) e aos eventos de temporização que controlam a troca das luzes.
  
- **Form1.Designer.cs**: Arquivo gerado automaticamente que define a estrutura visual do formulário, incluindo a criação dos painéis de luz (verde, amarelo, vermelho) e do botão do pedestre.

- **Program.cs**: Ponto de entrada do aplicativo, responsável por inicializar e executar o formulário principal (Form1).

- **TrafficLightSimulationGUI.csproj**: Define as configurações do projeto, incluindo as dependências e a versão do framework .NET utilizada.

---

### Paradigma Orientado a Eventos 📈

Este projeto é um exemplo claro de *programação orientada a eventos*. Abaixo estão alguns dos principais conceitos aplicados no código:

- **Eventos**: Um evento é algo ao qual um programa deve responder, mas que ocorre em um momento imprevisível. No contexto deste projeto, temos:
  - O clique no botão de pedestre, que dispara a mudança do semáforo do verde para o amarelo.
  - A utilização de Timers que controlam quando o semáforo deve mudar de uma cor para outra.

- **Event Listener e Event Handler**:
  - *Event Listener*: No código, temos listeners como `ButtonPedestrian.Click`, que "escutam" por eventos específicos e chamam os event handlers correspondentes.
  - *Event Handler*: Métodos como `ButtonPedestrian_Click` e `OnTimedEvent` são executados em resposta a eventos. Eles tratam a lógica do que deve ser feito quando o evento é disparado, como mudar a cor do semáforo.

- **Event Loop**: A aplicação utiliza um *loop de eventos* através do Timer para manter o semáforo funcionando continuamente até que seja fechado pelo usuário.

### Como Executar ⚙️
1. **Requisitos**:
   - .NET SDK versão 8.0 ou superior.
   - Visual Studio ou qualquer outra IDE compatível com projetos .NET.

2. **Compilação e Execução**:
   - Abra o projeto em sua IDE.
   - Compile o projeto usando o comando `dotnet build`.
   - Execute o projeto usando o comando `dotnet run`.

### Funcionamento ⏳
- O semáforo começa no *verde* e permanece assim até que o botão do pedestre seja pressionado.
- Ao pressionar o botão:
  - Espera *10 segundos* e então muda para *amarelo*.
  - Após *5 segundos*, muda para *vermelho*.
  - Permanece no *vermelho* por *20 segundos* antes de voltar ao *verde*.
  
- A interface também exibe um **contador regressivo** indicando o tempo restante para a próxima mudança de luz.

### Casos de Uso 📄
Este projeto pode ser usado em diversos contextos para ensinar ou demonstrar a *programação orientada a eventos*, como:
- **Interfaces gráficas**: Como responder a cliques de botões e manter uma aplicação interativa.
- **Processos Assíncronos**: Utilizando timers para gerenciar mudanças de estado ao longo do tempo.

---

### Vantagens do Paradigma Orientado a Eventos ✅
- **Responsividade**: Permite que a aplicação responda às ações do usuário de forma eficaz, resultando em uma experiência dinâmica.
- **Processamento Assíncrono**: O uso de timers permite que o processamento ocorra de forma não bloqueante.
- **Modularidade**: Cada evento é tratado separadamente, facilitando a manutenção e a escalabilidade do código.

### Desvantagens do Paradigma Orientado a Eventos ❌
- **Complexidade de Sincronização**: Lidar com vários eventos simultâneos pode aumentar a complexidade do software, exigindo cuidado para evitar condições de corrida.
- **Efeitos em Cascata**: Uma série de eventos interconectados pode tornar difícil prever o resultado e o estado do sistema.

---

## Menti - Resultados 📊
[Mentimeter](https://www.mentimeter.com/app/presentation/n/alurvh2q1ged6gzrq4xzxahgi1v5rhi4/edit?question=xg42qoxv8rnf)

## Autores 👨‍💻
- **André** - 30003032
- **Ewerton B. Ramos** - 30189098
- **João Marcos** - 30620406
- **Miguel** - 30129061
- **Pedro Mateus** - 29988080
- **Juan Farias Vaz** - 30289955
  
