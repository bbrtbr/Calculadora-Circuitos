# Calculadora (Adição,Subtração,Multiplicação,Divisão) - 4 bits
![image](https://github.com/user-attachments/assets/e41a2606-78df-4fc6-a334-f73d0dbc2afa)

O usuário poderá colocar dois números para ser efetuado a operação, deverá acionar as portas correspodente ao número que ele queira.
00 - Soma
01 - Subtração
10 - Multiplicação
11 - Divisão

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

