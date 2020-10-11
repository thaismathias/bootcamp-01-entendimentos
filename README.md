# Repositório de entendimentos

Sobre ser uma melhor estudante, pessoalmente, é através da repetição que memorizo algo novo. Acredito que quanto mais vezes fazemos algo, menos esforço e energia é exigido. Prefiro também partir direto para prática. Talvez, por ser inicialmente da área de exatas, tenho o costume de aprender pelo excesso de exercícios práticos.
Sobre meu entendimento do CDD (Cognitive Driven Development), tenho como uma teoria de desing que usa uma métrica de pontos para limitar a complexidade dos códigos e trazer facilidade para o próximo.
O sistema de pontuação é basicamente:

- 1 ponto: Acoplamento específico do projeto em análise, acoplamentos não transversais.
- 1 ponto: Branchs como if, else, casa, while.
- 1 ponto: Funções passadas como argumento.

A pontuação limite máxima é:

- 7 pontos para classe com atributos de dependência, como Controller, Service e outras.
- 9 pontos para classe com atributos de estado, como Entity, DTO e outras.
- 10 a 12 pontos para bibliotecas .
- 3 pontos para repositórios.

Devemos partir da ideia de que o código não é flexível e deve automatizar o desejo do cliente de forma simples. Portanto, deve-se sempre prezar por fórmulas prontas que o framework te oferece, além de não incluir detalhes sem necessidade. Por exemplo, se foi solicitado retorno de código 200, não há necessidade de retornar um 201. Ou seja, devemos apenas atender os requisitos de negócio, a não ser que seja algo muito fora do padro, nesse caso deve-se confirmar a requisição com o cliente.
O sistema de pontuação auxilia a manter o código coeso, como um guia. Onde, se a pontuação de uma classe ultrapassa seu limite máximo, significa que é necessário repensar e refatorar. Seja usando conceitos como coesão por encapsulamento, dividir o código para melhor entendimento, criar nova classe, ou melhor, redistribuir as responsabilidades nas classes já existentes.
Num geral, o objetivo é criar sistemas funcionais de qualidade, no menor tempo possível e com baixo custo. Usar as boas práticas para facilitar no caso de uma outra pessoa precisar dar continuidade no código. Para isso é legal manter o código organizado com separação em categorias e funcionalidades, com comentários e dicas, usar algumas convenções de nomenclatura, sempre testar os endpoints, não fazer classes muito longas, dentre outras coisas. Isso tudo levará a um código com qualidade e, se tudo der certo, com baixa complexidade.
Temos ainda uma questão importantíssima, a segurança. Existe uma prática de proteção das bordas do sistema. Essas bordas são as classes onde há entrada e saída de dados. É comum usarmos classes e interfaces para fazermos pontes entre as classes de domínio e os endpoints do projeto. Onde as classes de domínio não enxergam os endpoints e suas classes. O conceito de polimorfismo, um dos pilares da programação orientada ao objeto, é uma das diversas formas que temos para esse tipo de proteção.
