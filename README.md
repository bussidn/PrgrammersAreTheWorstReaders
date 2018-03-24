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

## We must fight bad habits

If you've reach this part, you are convinced that the code should be clear. But maybe you think that your code is fine. Ok I don't know you personnaly but, if you were never interested in that question, I will bet that it is not. That's fine, we're here to provide some insights.
We will explore some few biases that we're all facing that prevent us from improving ourselves.

### Quick understanding should be a long living property

First bias that is quite obvious : once you're done with your code, you understand it.

It may be a temporary state, and six month later you could come back to your code scratching your head. But in the minutes that follow, you are able to explain it if need be.
The moment you are just done, you've worked for that feature for hours or even days. You had time to understand the business and all of this is still fresh.
Once the code is done, we should make sure that if someone else wants to understand the intent behind, he could do it in a lesser time magnitude than it took to write the code.
If it stil take days to understand, maintenance will cost a lot of time. The problem often lies with code that rots. No effort is put in the first few feature. Codebase grows and methods tend to get fat. Features mixe together and correcting a production bug can take a few days. This is very common and is directly linked with the of discipline upon the team to assure the code can be understood in a timely manner.

=> Continuous efforts should be made to assure quick understanding

### We have learned a common language

Another bias is that alongside our peers, wa all talk a common language. Some are practicing it for years and are very familiar with it. Some are so new that there are still in the learning phase.

For those new, they are still trying to figure out how to manipulate the low level tools that are provided with the language and make a good use of them. That's not were the issue lies, it is that we don't teach them that those low level tools belong in the low abstraction level.
For those very familiar with the language, it is no longer a pain to read some low level language detail. It is something familiar. 

But if learning is just a phase and after that, we are able to read each other, there should be no issue right ? If so, why is it always so difficult to decypher another one's intention in the code ?

=> Because the bias here is thinking that our programming languages, so expressive may they be, are *actually* languages.

### we still don't manage to communicate intent

The reasons why we 
Our languages only possess a few *key words*. All the vocabulary, verbs, basically all taht matters to understand the purpose is business dependend. If the most basic grammer stay the same, we have to express totally different things with the same 20 words.

with every project, and the way to use that language is pretty much *personnal*.




  you're done with the code, you should have understood the business you've been doing for a long time. Therefore, your mind has already migrated from the question 'What to do?' to 'How to do it ?'
But remember that the main thing to explain is the **What**, not the **How**. It is hard to remember after hours or days of work on how to achieve the goal.


## Craft tools

### Early is cheaper
### consider easing the load

* express business logic
* write something you want/expect to read
* don't mix level of abstraction (https://codurance.com/2015/01/27/balanced-abstraction-principle/)
* craft convention helps : good naming + little functions


