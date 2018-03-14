# Programmers Are The Worst Readers

Apologies for such a title. The purpose is not to offend you but to draw some attention with a low trick. All I can hope is that this attention just drawn will be put to good use.

Why would such an attention needed ? Because I think the problem I will adress here is one of the most fundamental our industry is facing today. And if I had to sum the root cause of that problem up, it would be that we are too comfortable in our habits. (~familiar with our comfort zone)

Beacuse we are used to read bad written code, used to decypher other's thoughts through low level terse description, we do not make effort to make our own writing better.

But before I dive in those habits and try to highlight them, we need to agree that this extra work is worth the while.

## Why Writing understandable code is important

### Cost of maintenance

The big decision factor today in any industry is the money. Wether it is about adopting a new technology, frameword or internal organization, the idea is always to be more efficient and in the end, to save money. It is a bet about the future.

The topic today is no exception. We do not want to write good and understandable code because it is inherently 'good'. We want it because it saves time and money.

We can still easily find papers about the cost of maintenance that comes from the 80's and 90's worrying about the capacity of software to grow steadily. At the time, estimations were made that place the cost of maintenance between 40 and 80 percent of the total cost of the software.

From that time, the need for software developpers have increased tremendously. The turnover and use of external consultants has become the norm and the number of new technologies seems to have no end. In other words, there is little chance the cost of maintenance has reduced since then. It is common to have some very complex business running for decades on old systems and that newly arrived people have to learn both the complexity of the business and the complexity of the software.

This is clearly one of the paradox of our ages : as we try to reduce technological noise with languages that are more and more expressive, we also try to automate more and more things, increasing the weight of that noise.

 => Due to long living businesses and long living technologies on which are added an ever growing technological stack, the cost of maintenance is today a critical point on which every competitve company try to improve.

### We must read a lot of code

Now that we have realized the huge part that the cost of maintenance have these days, the only thing that remains is to be convinced that reading code is an important part of maintenance activity.

That should not be the hardest part for anyone with some experience in the field. For those who want more justification on that point, let me quickly list activities made by programmers during the mintenance phase.

The two main activities are : business evolution and error correction. Both those activities require reading the code a lot.

Error correction is the most obvious, we have to connect any error message, stack log or behavior description with the idea we have about how the code should behave by reading the code. Or worse, by debugging, which is just reading the code very carefully with some state display.

Business evolution also needs some reading as we expect some analysis to be done on which part of the code should evolve, become public, be refactored and so on. The relation here is more subtil as the documentation should be enough for that part, but, is it really ? If you have something like living documentation then your code is already fine enough and you don't even have to read this article much longer. If not, then your truth is not your documentation, it's your code. You will need to read it in any case.

Some could argue that code knowledge is sufficient to produce a preliminary design that allows any developper to start a new feature. Even if it true, no battle plan live through the first contact with the enemy, and if you have knowledge enough, it is because you already have read the code.

=> The key point here is that reading the code is knowledge transfert.

## 

If 

### We must fight bad habits / We have learned a common language
### we still don't manage to communicate intent
### consider easing the load

* express business logic
* write something you want/expect to read
* don't mix level of abstraction (https://codurance.com/2015/01/27/balanced-abstraction-principle/)
* craft convention helps : good naming + little functions


