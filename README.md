# Calculadora (Adição,Subtração,Multiplicação,Divisão) - 4 bits
![image](https://github.com/user-attachments/assets/e41a2606-78df-4fc6-a334-f73d0dbc2afa)

O usuário poderá colocar dois números para ser efetuado a operação, deverá acionar as portas correspodente ao número que ele queira.
<a>00 - Soma</a>
<a>01 - Subtração</a>
<a>10 - Multiplicação</a>
<a>11 - Divisão</a>

![image](https://github.com/user-attachments/assets/2dc76358-ec69-49b8-95ce-f9bd3652a286)

# Decode
Será enviado 8 pinos para o decode, e ele irá retornar 4 saída, que será o número hexadecimal, e será mostrado no visor, e encaminhado para o circuito "Calculator"

![image](https://github.com/user-attachments/assets/91a45de9-f1fa-4ba6-b74e-e3d0492c4511)

O Decoder irá analisar quais determinados pinos formam o número desejado em hexadecimal, conforme a tabela verdade a seguir.

![image](https://github.com/user-attachments/assets/efde795e-7c4e-4384-89d8-d860ebfb3f71)

# Calculator

![image](https://github.com/user-attachments/assets/6ea9f192-0fa9-4ad2-9182-48bc69006a4e)

O calculator irá receber 10 entradas, sendo elas 4 bits de um número, 4 bits de outro número, e 2 entradas para determinar qual operação será feita ( Adição, subtração, multiplicação ou divisão ) essa escolha é feita por meio de multiplexador, que irá receber o resultado das 4 operações, e irá decidir qual resultado deve ser enviado como resposta.

# Multiplexador 4 entradas

![image](https://github.com/user-attachments/assets/c33449dc-f6fe-4346-947a-91d41fced4fb)

O multiplexador de 6 entradas é composto por 3 multiplexadores, ele recebe como entrada 4 número hexadecimais de 4bits, que são os resultados das operações ditas anteriormentes, e por meio de 2 portas lógicas e 4 combinações possiveis, ele irá determinar qual operação deve ser enviada como saída.

# Multiplexador
![image](https://github.com/user-attachments/assets/dcca5004-0ee4-4dc0-8df8-b445152bfcd5)

O multiplexador tem 3 entradas, sendo elas 2 números hexadecimais de 4 bits, e 1 entrada que serve para determinar qual dos dois números hexadecimais deve ser apresentado como saída.

# Somador / Subtração

![image](https://github.com/user-attachments/assets/96891e46-eabd-40bf-9845-1308a190d6cd)

![image](https://github.com/user-attachments/assets/7487ce22-ee61-4649-b255-8b2d9b50a829)

O somador e a subtração é composto por 8 entradas, sendo elas 4 entradas de cada número, e tem 4 saída, que é o resultado da operação.
Ambos tem 4 somabit ou subtraibit, que são circuitos que somam/subtraem bit por bit e dão o resultado.

# Soma bit
![image](https://github.com/user-attachments/assets/ed7fce32-6642-4a29-b9d6-649478feb6af)

O soma bit irá somar dois bits, e caso o resultado seja maior que 1 bit, ele irá mandar um para a próxima soma, pelo carry out, e na próxima soma ele irá receber esse bit por meio do carry in

# Subtrai bit

![image](https://github.com/user-attachments/assets/4161c5a8-fc8d-41ec-acba-01685687314b)

O subtrai bit irá subtrair dois bits, caso o resultado seja "negativo", irá emprestar um bit para a proxima operação, e irá ter a entrada de "emprest".

# Multiplicação

![image](https://github.com/user-attachments/assets/6a495739-c196-421f-9727-57aae15ef777)

A multiplicação irá ter a entrada de 2 números hexadecimais e funcionará com 4 multiplexadores e 3 circuitos de soma.
Inicialmente se a entrada tiver quatro "0", ele irá retornar 0 inicialmente, caso contrário irá multiplicar bit a bit por meio do multiplexador, e irá somar os resultados.

# Incrementador

![image](https://github.com/user-attachments/assets/4cc299b6-ee7a-4b15-aa1e-a41a619e7782)

O incrementador serve para somar "um" ao número atual, e temos o controle de incrementar ou não por meio do pino "perm"

# Mag

![image](https://github.com/user-attachments/assets/8563f144-5f4c-4554-aa2a-518bfa121a47)

O incrementador tem duas entradas, que são os dois números que serão comparados, e irá retornar se o primeiro número é maior, menor ou igual.

# Soma_perm

![image](https://github.com/user-attachments/assets/33742008-78e5-4fe8-a474-e3e863f1d8b7)

O circuito soma perm irá somar dois números se tiver a permissão, esse circuito serve para auxiliar a divisão.

# Divisão

![image](https://github.com/user-attachments/assets/e0489b3d-d7a0-40f8-82d2-a170375d7572)


O circuito de divisão funciona por meio da junção dos circuitos de incrementador, multiplicação, comparador de números e a permissão de soma.
Ele irá multiplicar o divisor por "1" e irá incrementar até o valor ser igual o valor do dividendo, assim ele irá somar no resultado final, e bloquear a soma para os próximos resultados.

