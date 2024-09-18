## knowledge-based agents
agents that reason by operating on internal representations of knowledge

* If it didn't rain, Harry visited Hagrid today.
* Harry visited Hagrid or Dumbledore today, but not both
* Harry visited Dumbledore today.

=> Harry did not visit Hagrid today.
=> It rained today.

## sentence
an assertion about the world in a knowledge representation language

## Propositional logic

* Symbols - P, Q, R
* Logical Connectives
not ~
and ^
or | v
implication =>
biconditional <=>

![alt text](image-25.png)

* And ^

|P|Q|P^Q|
|-|-|-|
|false|false|false|
|false | true | false|
| true | false | false|
|true | true | true|

* Or (v)

|P|Q| PvQ|
|-|-|-|
|false|false|false|
|false|true|true|
|true|false|true|
|true|true|true|

* Implication =>
![alt text](image-26.png)
