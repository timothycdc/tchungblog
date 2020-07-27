+++
author = ["Timothy Chung"]
categories = ["Computer Science", "Artificial Intelligence"]
date = 2020-07-19T16:00:00Z
description = ""
image = ""
tags = ["Python"]
title = "CS50AI Chapter 1: Knowledge"

+++
At the heart of every algorithm lies its logic process, which forms the core part of decision making. The tricky part is, how do we program a computer to parse logic? In this explanation, we would want to give an algorithm a set of rules, and give it and a new rule. The algorithm has to tell us whether the new rule fits in with the old rules.

### Prepositional Logic Basics

Let's try and emulate a human's thinking process. Take these three statements:

> 1. If it didn't rain, Harry visited Hagrid today.
> 2. Harry visited Hagrid or Dumbledore today, but not both.
> 3. It rained today.

Who did Harry visit? Well, we can infer some statements by combining several together. Take statements 1 and 3: It rained today, which means Harry did not visit Hagrid today.

Let's apply that to statement 2, so Harry must have visited either Hagrid or Dumbledore. Since he did not visit Hagrid, so he should have visited Dumbledore.

Now, it's time to bring computers in, using the form of **prepositional logic.** The system of prepositional logic involves **symbols**, **sentences**, and **connectives**.

Symbols are simply items that are assigned logic values. They are linked to each other via connectives to form sentences.

The statements numbered 1-3 are examples of **sentences.**

Here are some examples of connectives – first, we have the common And, Or, and Not connectives.

The And connective means both symbols have to be True to return True, and Or needs at least one True input to do the same.

<span class="tablewrappermini" markdown="1">

| P | Q | P ˄ Q (AND) | P ˅ Q (OR) |
| --- | --- | --- | --- |
| false | false | false | false |
| false | true | false | true |
| true | false | false | true |
| true | true | true | true |

</span>

The Not connective returns the inverse of its input.

<span class="tablewrappermini" markdown="1">

| P | ¬ P (NOT) |
| --- | --- |
| false | true |
| true | false |

</span>

The Implication connective is similar to an IF-THEN statement. If conditions P are met, then outcome Q will occur.

<span class="tablewrappermini" markdown="1">
| P | Q | P → Q |
| --- | --- | --- |
| false | false | true |
| false | true | true |
| true | false | false |
| true | true | true |
</span>

Example:

> P: It did not rain today.
>
> Q: Harry will go for a run today.

Say we also **know** that P → Q, then we know that on rain-free days, Harry would surely go for a run. If it did not rain, but Harry did not go for a run, then the sentence  P → Q is false, because the conditions met for P did not affect the outcome Q.

On days where it rained (P is false), it does not matter whether Harry went for a run or not, the sentence  P → Q . This is the interesting part – because there is no **contradiction** between P and Q, True can be returned.

Pay attention to the bolded term as I'll come to that later.

A close relative is the Biconditional connective. It can be understood as an  IF-THEN (AND ONLY IF) statement, meaning that one symbol implicates the other and **vice versa.** A logical equivalent would be  (P → Q)^(Q → P).

<span class="tablewrappermini" markdown="1">

| P | Q | P ⇔ Q |
| --- | --- | --- |
| false | false | true |
| false | true | false |
| true | false | false |
| true | true | true |

</span>

Let's look back at the previous example.

> P: It did not rain today.
>
> Q: Harry will go for a run today.

Say we also **know** that P ⇔ Q, then we know that on rain-free days, Harry would surely go for a run, and whichever day Harry runs, we are 100% sure it did not rain.  In the case of P → Q, Harry could have gone for a run in the rain. This means that the rain is not the sole factor for Harry running.

For biconditionals, all True instances of (Q) can only result when the condition (P) being met.

### Dealing with Logic

The next step is understanding the definition of a model.

A **model** is an assignment of a truth value to every prepositional symbol. An example:

> P: It is raining
>
> Q: It is a Tuesday

The possible models are:

{P = false, Q = false} A rain-free day that's not a Tuesday

{P = true, Q = false} A rainy day that that's not a Tuesday

{P = false, Q = true} A rain-free Tuesday

{P = true, Q = true} A rainy Tuesday

A **knowledge base** is a set of sentences that are known to be true for all models.

> P: It is raining
>
> Q: It is a Tuesday
>
> R: Harry will go for a run.

Example of a knowledge base:

(Q ^ ¬ P ) → R

If it is a Tuesday and it is not raining, Harry will go for a run.

### Entailment

a ⊨ b

Entailment means, in every model where sentence a is true, sentence b is also true. This is useful for asking questions to an algorithm and seeing if it is true – if we feed it in (a) our knowledge base of rules, we can ask it a question in (b).

> P: It is raining
>
> Q: It is a Tuesday
>
> R: Harry will go for a run.

Knowledge base (a) : ((Q ^ ¬ P ) → R  )

If it is a Tuesday and it is not raining, Harry will go for a run.

Query (b) : (R)

Will Harry go for a run?

If (a) entails (b), this means that Harry will go for a run.

### Method 1: Model Checking

KB ⊨ q

We check through all possible models. For every model where its knowledge base (KB) is valid/true, and its query (q) is true, we know that KB ⊨ q. Otherwise, KB does not entail q. We do not need to care about models that have a false knowledge base

<span class="tablewrappermini" markdown="1">

| P | Q | R | KB | R(Query) |
| --- | --- | --- | --- | --- |
| false | false | false | false | false |
| false | false | true | false | true |
| false | true | false | false | false |
| false | true | true | false | true |
| true | false | false | false | false |
| TRUE | FALSE | TRUE | TRUE | TRUE |
| true | true | false | false | false |
| true | true | true | false | true |

</span>

In this case, the row in all caps is the only instance of KB that is true, and the