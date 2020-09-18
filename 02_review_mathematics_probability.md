# Probability Space
A **probability space** is a triple composed by: a sample space ($\Omega$), a $\sigma$-algebra ($\mathfrak{M}$) and a probability measure($\mathbb{P}$).

## Sample spaces and how big they can be

A **sample space** $\Omega$ is the set of all possible outcomes of an experiment.  
An **event** is a subset of $\Omega$ (the sample space). We will use Capital letters to denote events. Most used ones are $E$ and $A$.

$\#\Omega = 1$ means that we have an experiment that allows only a possible outcome and is therefore *deterministic*.  
Usually we start thinking about sample spaces as finite ($\#\Omega \in \mathbb{N}$), however we can also have an sample space $\#\Omega = \#\mathbb{Z}$ containing infinite possible outcomes.

Remember that infinities do not behave like we expect: $\#\mathbb{Z} = \#\mathbb{N}$ even though $\mathbb{N} \subset \mathbb{Z}$.  
Informally we can write: $\frac{\#\mathbb{N}}{\#\mathbb{Z}} = 1$ to deliver the point that the set of natural numbers and integers are countable and their "infinity" is equal. Also we could informally state that $\frac{\#\mathbb{N}}{\#\mathbb{R}} = 0$ to say that the cardinality of the set of real numbers is infinitly larger than the cardinality of countable sets like the set of natural numbers.

We can also have sample spaces that are infinite and **countable** but also we can have cases where the sample space is **uncountable** $\#\Omega = \#\mathbb{R}$.
These are cases where the possible outcomes cannot be counted and in the future we will have to deal with them in a different way in respect of the countable case.

## Infinite sums and integration

We can sum countable many numbers
$
\sum^\infty_{i=1} x_i = \sum^\infty_{i\in\mathbb{N}} x_i 
$

We cannot sum all the uncountable numbers but if they satisfy a condition (being infinitly small, this is what $dx$ actually means) we can integrate them.
$
\int_{x \in \mathbb{R}}{f(x)dx}
$

The largest event in $\Omega$ is $\Omega$ itself which is called the *certain event*.  
The smallest one is the empty set $\varnothing$ which is also called the *impossible event*.

## Concepts that we need to know (review on our own)
- Intersection, union, complement, difference on sets.  
- Venn diagrams.  
- De Morgan's Laws.
- Integration.


## $\sigma$-algebra
A sigma algebra is a set of subets of $\Omega$ which satisfy these properties:
1. The sample space $\Omega$ is an element of the sigma algebra. $\Omega \in \mathfrak{M}$. If something happens that it could happen.
2. Everytime I have an event, its complement must also be in the sigma algebra. $\forall E \in \mathfrak{M}: \bar{E} \in \mathfrak{M}$.
3. The union of a series of event is part of the $\sigma$-algebra $E_1, E_2, ... \implies \bigcup E_i \in \mathfrak{M}$. Whenever I have a sequence of event I also have their union. A sequence is an "or" between events. And I can use the third axiom of probability, with some tricks, to measure its probability.

## Axioms of probability

The axioms of probability defines the properties of a probability function however we should not forget that a probability is a mathematical *MEASURE*. It is used to compare uncertainty of events.

If we have a sample space $\Omega$ with a $\sigma$-algebra $\mathfrak{M}$ probability is a function that maps the domain $\mathfrak{M}$ to the interval $[0, 1]$.  

$\mathbb{P}:\mathfrak{M} \rightarrow [0, 1]$

The axioms of probability are:

1. $\mathbb{P}(\Omega) = 1$.
2. $0 \le \mathbb{P}(E) \le 1$, this is a consequence of the codomain definition.
3. Given a countable collection of mutually exclusive events such as all the events are present in $\mathfrak{M}$ then:
$\mathbb{P}[E_1 \cup ... \cup E_n] = \sum_{i=0}^n \mathbb{P}(E_i)$.

### Terrible Errors
- If the teacher asks for a probability and you get a greater than 1 or less than 0 value that will be a Terrible Error.  
- An obvious contradiction of the axioms of probability is considered a Terrible Error.

## Consequences

* $\mathbb{P}(E) = 1 - \mathbb{P}(\bar{E})$. Once we know the probability of an event, also the probability of its *complement* is known.
* $\mathbb{P}(A \cup B) = \mathbb{P}(A) + \mathbb{P}(B) - \mathbb{P}(A \cap B)$. To properly measure the probability of an union of events we must take into consideration that summing the probabilities could count more than once for the intersection of events.
* $A \subset B \implies \mathbb{P}(A) \leq \mathbb{P}(B)$ 
    * $\mathbb{P}(A \cap B) \leq \mathbb{P}(A)$
    * $\mathbb{P}(A \cap B) \leq \mathbb{P}(B)$
    
### On calculating the probability of unions of events
$A, B \in \mathfrak{M} \quad \mathbb{P}(A \cup B) = \mathbb{P}(A) + \mathbb{P}(B) - \mathbb{P}(A \cup B)$

If $A, B$ are disjoint $\implies A \cap B = \varnothing$ so we are "safe" however if this is not the case this can get hairy.  
For example consider the union of three events $A, B, C$:
$\mathbb{P}(A\cup B \cup C) = \mathbb{P}(A) + \mathbb{P}(B) + \mathbb{P}(C) - \mathbb{P}(A \cap B) - \mathbb{P}(A \cap C) - \mathbb{P}(B \cap C) + \mathbb{P}(A \cap B \cap C)$

What happens if I have countable many sets?  
This could be a project that has to do with the Principle of inclusion/exclusion, Bonferroni Inequalities.

## Probability as a measure

Suppose that we have a rectangle of area 1 representing our sample space $\Omega$.  
We could represent events proportionally to their probability.

For a couple of events $A, B$ they could have an intersection but which intersection has 0 probability, especially for uncountable sample spaces.

## Examples of $\sigma$-algebras

The simple possible experiment in probability has 2 possible outcomes. $ \Omega = \left\{ 0, 1\right\}$ .  
The smallest $\sigma$-algebra we can come up with is: $\mathfrak{M} = \left\{ \Omega, \varnothing \right\} $

This is called a Trivial $\sigma$-algebra as it is quite possibly useless.

Another possible sigma algebra from that defined sample space could be the partition set $\mathscr{P}(\Omega)$, which adds the singletons to the trivial $\sigma$-algebra.

$\mathfrak{M} = \{\Omega, \varnothing, \{0\}, \{1\}\}$

Usually a $\sigma$-algebra is composed by what we CAN measure during our experiment.