# Introduction
Artificial intelligence covers a wide variety of types of techniques

Examples of AI
1. like recognizing someone's face in a photo
2. being able to play a game better than people can
3. being able to understand human language when we talk to our phones



1. Search
    * AI to be able to search for solutions to some kind of problem
    * get driving directions from point A to point B
    * trying to figure out how to play a game e.g. tic-tac-toe
2. Knowledge
    * AI to be able to know information
    * To be able to represent that information
    * use the information it knows and draw additional conclusions
3. Uncertainty
    * what happens if a computer isn't sure about a fact
    * we'll talk about some of the ideas behind probability
    * how computers can begin to deal with uncertain events
4. Optimization
    * Problems of when the computer is trying to optimize for some sort of goal
    * situation where there might multiple ways that a computer might solve a problem
5. Learning
    * computers can be programmed to be quite intelligent by learning from data
    e.g. Email Inbox somehow knows which are Good emails, spam emails
6. Neural Networks
    * how computers are able to draw inspiration looking at the structure of the human brain
7. Language
    * human languages that we speak every day And taking a look at the challenges that come computer tries to understand natural language


## Search

1. Sliding Window

![alt text](Assets/image.png)

2. Maze Problem

![alt text](image.png)

Analogy - Google Map

* Agent - Entity that perveives its environment and acts upon that environment
e.g. a car
* state - A state is just some configuration of the agent in its environment.


![alt text](image-1.png)

* initial state - The initial state is just the state where the agent begins.
* actions - Actions are just choices that we can make in any given state.
Actions(s) returns the set of actions that can be executed in state s

![alt text](image-2.png)

* transition model - a transition model, which will be a description of what state we get after we perform some available action in some other state.


* state space - the set of all of the states we can get from the initial state via any sequence of actions, by taking zero or one or two or more

![alt text](image-3.png)

![alt text](image-4.png)

* goal test - way to determine whether a given state is a goal state

* path cost - numerical cost associated with a given path

![alt text](image-5.png)

* Search Problems
    * initial state
    * actions
    * transition model
    * goal test
    * path cost

* Solution - 

* Optimal solution - a solution that has lowest path cost among all solutions

* node
    * a data structure that keeps track of 
        * a state
        * a parent(node that generated this node)
        * an action (action applied to parent to get node)
        * a path cost(from initial state to node)

* Approach
    * Start with a frontier that contains the initial state
    * Repeat:
        * If the frontier is empty, then no solution.
        * Remove a node from the frontier.
        * If node contains goal state, return the solution.
        * Expand node, add resulting nodes to the frontier.

![alt text](image-6.png)

What could go wrong?
e.g. if we have two way path

![alt text](image-7.png)

what is the solution to above problem?

By somewhat keeping a track of what is explored

* Revised Approach
    * Start with a frontier that contains the initial state.
    * Start with an empty explored set.
    * Repeat:
        * If the frontier is empty, then no solution.
        * Remove a node from the frontier.
        * If node contains goal state, return the solution.
        * Add the node to the explored set.


> Stack last-in first-out data type


![alt text](image-9.png)

We need to get a visual sense to understand this alogorithm

* It is called Depth-first search
    * search algorithm that always expands the deepeset node in the frontier