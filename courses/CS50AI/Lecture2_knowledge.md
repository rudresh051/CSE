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

### And ^

|P|Q|P^Q|
|-|-|-|
|false|false|false|
|false | true | false|
| true | false | false|
|true | true | true|

### Or (v)

|P|Q| PvQ|
|-|-|-|
|false|false|false|
|false|true|true|
|true|false|true|
|true|true|true|

### Implication =>

![alt text](image-26.png)

### Biconditional <=>
![alt text](image-28.png)


### Model

```
A model in AI or machine learning is a set of instructions or rules that helps a computer understand how to make predictions or decisions. It learns from past experiences (data) to figure out what will happen next. For example, if an AI model has learned from many photos of dogs, it can predict whether a new picture shows a dog.
```

## Why to assign true or false?
```
Assigning truth values to propositions is essential in logical systems and AI reasoning for several reasons, primarily to evaluate the validity of statements, derive conclusions, and simulate possible worlds or scenarios. Here's why this assignment process is important:

1. Defining Meaning and Truth
Propositions are abstract statements about the world, but their meaning depends on whether they are true or false in a specific context.
Assigning a truth value to propositions gives us a way to evaluate their truthfulness, which is necessary for logical reasoning. Without assigning truth values, it would be impossible to make any formal judgments about the propositions' correctness or applicability in a given situation.
Example:
If you have a proposition like "The sky is blue," it’s meaningless unless we know whether this statement is true or false in a given context (e.g., during the day vs. at night).
```


The model is an assignment of a truth value to every proposition.   
To reiterate, propositions are statements about the world that can be either true or false.  
However, knowledge about the world is represented in the truth values of these   propositions.   
The model is the truth-value assignment that provides information   
about the world.

For example, if P: “It is raining.” and Q: “It is Tuesday.”,   
a model could be the following truth-value assignment: {P = True, Q = False}.   
This model means that it is raining, but it is not Tuesday.   
However, there are more possible models in this situation (for example, {P = True,   
Q = True}, where it is both raining and a Tuesday).   
In fact, the number of possible models is 2 to the power of the number of propositions.   
In this case, we had 2 propositions, so 2²=4 possible models.

### Knowledge Base (KB)
```
In Artificial Intelligence (AI), a Knowledge Base (KB) is a centralized repository of 
information used to store, organize, and retrieve knowledge. It is a critical component 
of various AI systems, especially expert systems, and is designed to help these systems 
make decisions, reason, and solve complex problems by simulating human expertise. 
A knowledge base can include facts, rules, relationships, concepts, and other types 
of structured or unstructured data relevant to a particular domain.
```

The knowledge base is a set of sentences known by a knowledge-based agent.   
This is knowledge that the AI is provided about the world in the form of   
propositional logic sentences that can be used to make additional   
inferences about the world.

### Entailment (⊨)
Entailment refers to a logical relationship between two statements where one statement   
necessarily follows from another. If a statement A entails a statement B, then B must be true if A is true.



```
For example, if an AI knows that:
"All humans are mortal" (A),
"Socrates is a human" (B),
then it can logically entail that "Socrates is mortal" (C).
```

If α ⊨ β (α entails β), then in any world where α is true, β is true, too.

For example, if α: “It is a Tuesday in January” and β: “It is January,”   
then we know that α ⊨ β. If it is true that it is a Tuesday in January,   
we also know that it is January. Entailment is different from implication.   
Implication is a logical connective between two propositions.   
Entailment, on the other hand, is a relation that means that   
if all the information in α is true, then all the information in β is true.

## Inference
**Inference is the process of deriving new sentences from old ones.**

```
Logical Inference
Inference is the process of deriving new truths (conclusions) from known truths (premises). 
To infer new information, we need to know the truth values of the propositions involved.
By assigning truth values, a logical system can determine whether certain conclusions follow 
from a set of premises (this is where entailment comes in).
Example:
Consider the propositions:
P: "If it rains, the ground will be wet."
Q: "It is raining."
R: "The ground is wet."
```

For instance, in the Harry Potter example earlier, sentences 4 and 5 were inferred   
from sentences 1, 2, and 3.

There are multiple ways to infer new knowledge based on existing knowledge.   
First, we will consider the Model Checking algorithm.

To determine if KB ⊨ α (in other words, answering the question: “can we conclude that   
α is true based on our knowledge base”)  
Enumerate all possible models.
If in every model where KB is true, α is true as well, then KB entails α (KB ⊨ α).
Consider the following example:

P: It is a Tuesday.   
Q: It is raining.   
R: Harry will go for a run. 

KB: (P ∧ ¬Q) → R 
(in words, P and not Q imply R) P (P is true) ¬Q (Q is false) Query: R (We want to know whether R is true or false; Does KB ⊨ R?)

To answer the query using the Model Checking algorithm, we enumerate all possible models

# Model Checking
```
Model checking is a formal verification technique used to systematically check whether a model of a system satisfies certain specifications or properties. It is widely used in computer science, particularly in verifying the correctness of hardware and software systems. The goal of model checking is to ensure that a system behaves as intended under all possible conditions.
```

![alt text](image-29.png)

![alt text](image-30.png)







