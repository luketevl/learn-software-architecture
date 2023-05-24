# Arquiterura de Software
# AULA 1

## Sobre o assunto
> É a estrutura **lógica** e **física** de um sistema de software, incluindo os **componentes**, suas **interações** e suas **restrições de design**. *Como* deve ser *construido* e *intregrados*
> Afeta a maneira como um sistema é **criado, desenvolvido, mantido, evoluído** e como ele pode afetar a qualidade do sistema, na sua **flexibilidade, escalabilidade, desempenho e segurança**
- Fatores a serem considerados
  - Requisitos de negócio
  - Restrições de tempo e orçamento
  - Padrões de design e tecnologias
- Principais considerações
  - Separação de preocupações
  - Modularização
  - Reutilização de componentes
  - Padrões de design
- Abordagens
  - Arquitetura em camadas
  - Arquitetura em componentes
  - Arquitetura em serviços
  >  Cada abordagem possui vantagem e desvantagem, a **escolha da obordagem apropriada** depende das **necessidades do projeto** e do **contexto** em que o sistema será utilizado
> Projeto **escalável e manutenível**: Tecnologia, modelos de arquiteturas, avaliação e seleção de arquiteturas, documentação e o gerenciamento de mudanças ao longo prazo.


# Tipos de Arquitetura de Software
- Design Pattern: Soluções para problemas comuns. Ex:
  - MVC
  - Repository
  - Factory
- Microservices: Divide uma aplicação em pequenos serviços independentes que trabalham juntos para fornecer uma solução completa.
- Arquitetura de Camadas: Estrutura o software em camadas lógicas, cada uma responsável por uma funcionalidade especifica

## Design Pattern
> **Soluções estabelicidas e comprovadas** para **problemas comuns na arquitetura de software** que possui uma**abordagem padronizada e comprovada** para solucionar problemas específicos e **ajudam a melhorar a reutilização de código e a manutenção do software**
- 3 Categorias principais:
  - Criação
  - Estruturais
  - Comportamento

### Padrões de Criação
> Foco na criação de **objetos e instâncias**, aborda questões comuns como *ocultação da complexidade de criação*.
- Exemplos de padrões de criação
  - **Factory**: Fornece uma **interface** para **criar objetos** em uma **classe base** **sem especificar suas classes concretas**. Permitindo a **flexibilidade** para **adicionar novs classes sem afetar o código existente**
  - **Builder**: Separa a **construção de um objeto complexo** da sua **apresentação**, **permitindo que diferentes** repesentações sejam criadas **com o mesmo processo de criação**.
  - **Singleton**: Garante que **uma classe** tenha **APENAS UMA** **instância** e fornece um ponto de **acesso global** a ela
  - **Prototype**: Especifica *tipos de objetos** a serem criados por uma **operação de clonagem**. Isso permite que novos objetos sejam criados **rapidamente** a partir de **modelos existentes**


### Padrões Estruturais
> Foco na **organização de classes o objetos** para formas **estruturas maiores e mais complexas**. Padroes úteis para **simplificar e melhorar** a **comunicação** entre **diferentes partes do sistema**, além de **reduzir a complexidade** do código e **aumentar sua reutilização** 
- 3 Categorias principais
  - **ADAPTAÇÃO**
    - **Adapter**: Permite que **objetos com interfaces incompatíveis** trabalhem **juntos**, *convertendo a interface de um objeto em outra interface que o cliente espera*
    - **Brigde**: Separa uma **abstração** de sua **implementação**, *permitindo que ambas evoluam independentemente*
    - **Proxy**: Fornece um **objeto** representante que **controla o acesso a outro objeto**
  - **AGREGAÇÃO**
    - **Composite**: Compõe objetos em estruturas de árvore para representar hierarquias de **partes-todo**
    - **Decorator**: Anexa responsabilidade adicionais a um objeto dinamicamente
    - **Facade**: Fornece uma interface simplificada para um conjunto de interfaces complexas.
  - **COMPOSIÇÃO**
    - **Flyweight**: **Minimiza** o uso de **memória** compartilhando o **estado** entre **objetos** que são idênticos ou semelhantes.
    - **Private Class Data**: Protege a **integridade** dos dados encapsulando-os em uma classe privada.
    - **Bridge**: **Separa** uma **abstração** de sua **implementação**, permitindo que ambas evoluam independentemente

## Padrões de Comportamento
> Lidam com **algoritmos**, **comunicação** e **responsabilidade** entre **objetos**. 
> Ajuda a definir como os **objetos** **interagem** e se **comunicam** entre sí, permitindo que o **software seja mais flexível e modular**.
- 3 Categorias principais
  - **COMPORTAMENTO DE CLASSE**
    - **Template Method**: Define o **esqueleto** de **algoritmo** em uma **superclasse** e **permite** que as **subclasses** **substituam** etapas específicas do algoritmo **sem alterar sua estrutura**
    - **Strategy**: Define uma **família de algoritmos**, **encapsula** cada um deles e os torna **intercambiáveis**. Varia *independentemente dos clientes que usam*
    - **State**: Permite que um **objeto altere seu comportamento** quando seu **estado interno mudar**.
  - **COMPORTAMENTO DE OBJETO**
    - **Observer**: Define uma **dependência 1-n** entre **objetos** para que, quando um **objeto mude de estado**, **TODOS os seus dependentes** sejam **notificados e atualizados automaticamente**
    - **Chain of Responsibility**: Permite que **vários objetos** **processem** uma **solicitação em cadeia**. *Cada objeto na cadeia tem a opção de processar a solicitação* ou *passá-la para o próximo ojeto da cadeia*
    - **Command**: **Encapsula** uma solicitação como um **objeto**, permitindo que você **parametrize clientes com diferentes solicitações**, **fila** ou **registre solicitações** e *suporte as operações* **DESFAZER** e **REFAZER**
  - **COMPORTAMENTO DE INTERAÇÃO**
    - **Interpreter**: Define uma **representação gramatical** para um **idioma** e fornece um **interpretador** para interpretar sentenças dessa linguagem.
    - **Mediador**: Define um **objeto** que **encapsula** como um **conjunto de objetos se interagem**. O **mediador** romove o **ACOPLAMENTO FRACO**, *evitando que os objetos se refinam uns aos outros explicitamente* e permitindo que você *varie sua interação independentemente*.
    - **Visitor**: Permite que você **adicione novas operações** a uma **estrutura de objetos existente** **sem modificar os objetos**. 

## Arquitetura de Camadas
> Sistema divido em camadas ou níveis lógicos distintos, **cada um com sua própria responsabilidade** e funcionalidades especificas.

> Principal objetivo **separar as preocupações** em níveis distintos de abstração, permitindo que cada **camada seja implementada**, **testada** e **mantida de forma independente** das outras. *Isso facilita a escabilidade, o teste e a manutenção, melhorando modularidade e flexibilidade*
- Geralmente organzadas em **pilha** onde:
  - **Camadas mais baixas fornecem serviços para as camadas mais altas**.
  - **Camadas mais altas usam os serviços fornecidos para implementar suas funcionalidades**
- Camadas mais comuns:
  - **Apresentação ou interface do usuário:** Responsável pela **interação do usuário** com o **sistema**, *apresentando informações e recebendo comandos*
  - **Aplicação**: Contém a **lógica** de **negócios** do sistema, **implementando a funcionalidade específica** do *domínio do problema*
  - **Persistência de dados**: Gerencia a **persistência de dadosa** do sistema, incluindo **leitura e gravação** de dados em **banco de dados* ou outro *armazenamentos*


  ## OBS
  - 