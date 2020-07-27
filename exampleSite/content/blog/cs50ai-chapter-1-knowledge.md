+++
author = []
categories = ["Computer Science", "Artificial Intelligence"]
date = 2020-07-19T16:00:00Z
description = ""
draft = true
image = ""
tags = ["Python"]
title = "CS50AI Chapter 1: Knowledge"

+++
At the heart of every algorithm lies its logic process, which forms the core part of decision making. The tricky part is, how do we code a computer to parse logic?

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

<span class="tablewrapper" markdown="1">

| P | Q | P ˄ Q (AND) | P ˅ Q (OR) |
| --- | --- | --- | --- |
| false | false | false | false |
| false | true | false | true |
| true | false | false | true |
| true | true | true | true |

</span>

The Not connective returns the inverse of its input.

<span class="tablewrapper" markdown="1">

| P | ¬ P (NOT) |
| --- | --- |
| false | true |
| true | false |

</span>

The Implication connective is similar to an IF-THEN statement.

| P | Q | P → Q |
| --- | --- | --- |
| false | false | true |
| false | true | true |
| true | false | false |
| true | true | true |

Example:

> P: It did not rain today.
>
> Q: Harry will go for a run today.

Say we **know** P → Q, then we know that on rain-free days, Harry would surely go for a run. If it did not rain, but Harry did not go for a run, then this sentence