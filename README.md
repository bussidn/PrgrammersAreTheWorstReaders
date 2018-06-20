# Programmers Are The Worst Readers

Apologies for such a title. The purpose is not to offend you but to draw some attention with a low trick. All I can hope is that this attention just drawn will be put to good use.

Why would such an attention needed ? Because I think the problem I will adress here is one of the most fundamental our industry is facing today. And if I had to sum the root cause of that problem up, it would be that we are too comfortable in our habits. (~familiar with our comfort zone)

Beacuse we are used to read bad written code, used to decypher other's thoughts through low level terse description, we do not make effort to make our own writing better.

But before I dive in those habits and try to highlight them, we need to agree that this extra work is worth the while.

## Why Writing understandable code is important

### Maintenance costs

The big decision factor today in any industry is the money. Wether it is about adopting a new technology, frameword or internal organization, the idea is always to be more efficient and in the end, to save money. It is a bet about the future.

The topic today is no exception. We do not want to write good and understandable code because it is inherently 'good'. We want it because it saves time and money.

We can still easily find papers about the cost of maintenance that comes from the 80's and 90's worrying about the capacity of software to grow steadily. At the time, estimations were made that place the cost of maintenance between 40 and 80 percent of the total cost of the software.

From that time, the need for software developpers have increased tremendously. The turnover and use of external consultants has become the norm and the number of new technologies seems to have no end. In other words, there is little chance the cost of maintenance has reduced since then. It is common to have some very complex business running for decades on old systems and that newly arrived people have to learn both the complexity of the business and the complexity of the software.

This is clearly one of the paradox of our ages : as we try to reduce technological noise with languages that are more and more expressive, we also try to automate more and more things, increasing the weight of that noise.

 => Due to long living businesses and long living technologies on which are added an ever growing technological stack, the cost of maintenance is today a critical point on which every competitve company try to improve.
 
 ![Mainteance](https://github.com/bussidn/ProgrammersAreTheWorstReaders/blob/master/maintenance.png?raw=true)

### Maintenance involves reading

Now that we have realized the huge part that the cost of maintenance have these days, the only thing that remains is to be convinced that reading code is an important part of maintenance activity.

That should not be the hardest part for anyone with some experience in the field. For those who want more justification on that point, let me quickly list activities made by programmers during the mintenance phase.

The two main activities are : business evolution and error correction. Both those activities require reading the code a lot.

Error correction is the most obvious, we have to confront any error message, stack log or behavior description with the idea we have about how the code should behave by **reading the code**. Or worse, by debugging, which is just reading the code very carefully with some state display.

Business evolution also needs some reading as we expect some analysis to be done on which part of the code should evolve, become public, be refactored and so on. The relation here is more subtil as the documentation should be enough for that part, but, is it really ? If you have something like living documentation then your code is already fine enough. If not, then your truth is not your documentation, it's your code. You will need to read it in any case.

Some could argue that code knowledge is sufficient to produce a preliminary design that allows any developper to start a new feature. Even if it true, no battle plan live through the first contact with the enemy. The preliminary design is often changed during the implementation phase because, after having read the code, we remember some few changes in the acutal code that are incompatible with the idea the designer had about it..

And if you have an accurate vision of all these litlle changes, then you must have read the code a lot.

=> Reading and writing code is foremostly about knowledge transfert.


## We must fight bad habits

If you've reach this part, I hope you are convinced that the code should be clear. But maybe you think that your code is fine.
Ok I don't know you personnaly but, if you were never interested in the clean code question, I will bet that there is room for improvment.

But First, I would like to express the primary rule I try to follow when thinking in term of readability :

=> We should communicate **intent**

It may be the most non-negociable rule about readability. Yet, we often fail to comply. It may also be the hardest to follow.

We will explore some few biases that we're all facing while writing code that prevent us from improving ourselves and making our intent clear.

![Enlightened Brain-bulb](https://www.healththoroughfare.com/wp-content/uploads/2018/04/habits-damage-brain.jpg)

### We don't think long term

**Quick understanding should be a long living property of the system**

First bias that is quite simple : once you're done with your code, you understand it.

But it is often a very **temporary** state.
It's not rare to come six month later back to your code and scratch your head trying to read it again.

The moment you're done with your code, you've worked for that feature for hours or even days, you had time to understand the business, you are able to explain it if need be because everything is fresh.

This is a very **short-term** vision.

Once the code is done, we should make sure that if someone else wants to understand the intent behind, he could do it in a lesser time magnitude than it took to write the code.
If it still take days to understand, maintenance will cost a lot of time.

The problem often lies with the fact that we let the code **rot**.
No specific effort is put in the first few feature. Codebase grows and methods tend to get fat. Features mix together and correcting a production bug can take a few days.
This scenario is very common and is directly linked with the lack of discipline in the team to assure the code can be understood in a **short amount of time**.

=&gt; Continuous efforts should be made to assure quick understanding

For that make sure to express business intent at the highest level of abtraction and carefully split your codebase into small and well defined methods.

### We have learned a false language

Another bias is that alongside our peers, we all talk a common language. Some are practicing it for years and are very familiar with it. Some are so new that there are still in the learning phase.

For those new, they are still trying to figure out how to manipulate the low level tools that are provided with the language and make a good use of them. That's not generally where the issue lies.

The problem is that **we do not learn that those low level tools belong in the lower levels of the code in term of abstraction.**

For those already comfortable with the language, it is no longer a pain to read some any low level language detail. All those for loops, try/catch blocks and nested if statements are already very familiar.

But if learning is just a phase and after that, we are able to read each other, there should be no issue right ? If so, why is it always so difficult to decypher another one's intention in the code ?

There are multiple reasons for that :
* It is **hard** to keep something simple when designing everything at the lowest level.
* We always have an important part of developpers in the learning phase due to the increasing need for developpers.
* **we think our programming languages, so expressive may they be, are *actually* languages.**

There may be numerous other reasons but I will only speaking about the last one here.

Our languages only possess a few *key words*. All the vocabulary, verbs, and basically all that really **matters to understand** the intent does not exist in that language at first place. Only the most basic grammer comes from the programming language and stay the same, we have to express every thing else differently from project to project.

More, the way to use that language is often very *personnal*.

So, make sure that the business code you create is enough to replicate the business language and that your **code** is as expressive as the business is. This is why DDD and its ubiquitous language is so appriciated once you tasted it. It make the whole team agreed on the vocabulary it should learn and what is **readible**.


### We are confortable with patterns

One of the things that we learned to cherish is our preferred and usual patterns. We made ourselves familiar with abstract concepts that are meant to help us in any project.

Take the layered architecture pattern for instance. It is just a tool with flaw and benefits and if you choose to adopt it, it should bring what is promised.
But it has been so predominant that many experienced developpers I meet today are prisonners of some thinking patterns the model brings with it.
It made us so comfortable with the notion of 'service', explained what the service layer is that it is a word that I often encounter.
The architecture is not to blame, it is a tool. What is to fight is the confort zone we like to be in. All I see are ProductService going along with anemic classes. All I see is a lot of coupling, and low cohesion. That's not the architecture to blame.

It's us.

We feel so well with this abstract notion of Service that we are not bothered bringing it erverywhere although it is a blank name which reveal nothing.

That's just an example but there is many more. Each time we call a class *IAccount* or *AccountImpl*, it is a pattern that we follow that prevent us from thinking about the name we should give. Each time you call a method *applyChange*, or *fillProperties*, you're not revealing intent. You force the reader to do extra job to understand what the name implies.

**We should see our own patterns only as a toolbox in which we can pick.**


## Conclusion

I hope that you recognized yourself in this article, because I hope it can be useful. Nowing what prevent us to improving ourself is the best way to cast those bad habits aside and try to change things.

This is what I love about the software craftmanship community, it tries to come back to essentials and naming things correctly, making our code readable is one of the first things we learn as a programmer. It is also one of the first things we forget.
