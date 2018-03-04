# Programmers Are The Worst Readers

Apologies for such a title. The purpose is not to offend you but to draw some attention with a low trick. All I can hope is that this attention just drawn will be put to good use.

Why would such an attention needed ? Because I think the problem I will adress here is one of the most fundamental our indstry is facing today. And if I had to sum the root cause of that problem up, it would be that we are too comfortable in our habits. (familiar with our comfort zone)

Beacuse we are used to read bad written code, used to decypher other's thoughts through low level terse description, we do not make effort to make our own writing better.

But before I dive in those habits and try to highlight them, we need to agree that this extra work is worth the while.

## Writing understandable code is important

### Cost of maintenance

Frequently Forgotten Fundamental Facts about Software Engineering" by Robert L. Glass, (an article in IEEE Software May/June 2001)
=> 60/60 rule

10% increase in essential complexity => 100% increase complexity in solution (software) complexity

https://scholar.google.fr/scholar?q=software+%22cost+of+maintenance%22&hl=fr&as_sdt=0&as_vis=1&oi=scholart&sa=X&ved=0ahUKEwjc0ue0wMHZAhXoDMAKHcjpAaoQgQMIJjAA

maintenance typically consumes 40 to 80% (60% average) of software costs, and then that enhancement is responsible for roughly 60% of software maintenance costs, while error correction is about 17%

3 factors : long living technologies (COBOL / java) + long living businesses + growing technological stack

paradox : language let us write less and less code while we use more and more tech layers.

### We must read a lot of code

* knowledge transfert
* error correction
* business evolution

### consider easing the load

* express business logic
* write something you want/expect to read
* don't mix level of abstraction (https://codurance.com/2015/01/27/balanced-abstraction-principle/)
* craft convention helps : good naming + little functions

## We must fight bad habits
