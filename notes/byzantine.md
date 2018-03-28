# First Pass
Reliable computer systems need to be able to handle not just outright failures/errors of certain components
but also malfunctioning components that give conflicting information to different parts of the system.
We can demonstrate this issue in terms of a group of Byzantine generals trying to decide on a battle plan.
The generals must agree on a common battle plan but can communicate with each other by messenger only.
One or more of the generals may be traitors (malfunctioning components) who will try to confuse the others.
The generals can only communicate to eachother via unforgeable. The problem is to find an algorithm
to ensure that loyal generals will reach some agreement; this problem is only solvable if more than
2/3 of generals are loyal.

Failure due to components sending conflicting information to different parts of the system are often 
overlooked. Byzantine generals are camped outside a city and can communicate only via written messages
sent via messengers. After observing the enemy the generals must decide on a common plan of action.
Some generals may be traitors trying to prevent the loyal generals from reaching an agreement (or trying 
to get them to choose a bad plan?)

The algorithm must guarantee that:

A. All loyal generals must decide upon the same plan of action

Loyal generals all do what the algorithm says they should but traitors may do whatever they want. This
condition must be guaranteed regardless of what the traitors do. The loyals should reach an agreement,
and that agreement should be a reasonable plan.

B. A small number of traitors can't cause the generals to adopt a bad plan

How the generals reach a plan:
Suppose the generals all have different viewpoints of the city, and so have different information to
tell the other generals. Let v(i) be the information by the i'th general. Note that it's not necessarily
their decision for the plan. All the generals use the same method of combining the information of 
v(i) ... v(n) that they then use to decide on the plan. To achieve condition be that method needs to 
be robust. If each v(i) is is the i'th generals vote on whether to attack or retreat, then the overall 
decision might be based on a majority vote. A small # of traitors can only affect the decision if the
information provided by the loyal generals was more or less evenly split between available decisions.
Note that here neither decision would be considered bad.

There must be a way for generals to communicate. The obvious solution is for each general to send a
message with their information to every other general, but this could violate guarantee A, since a
traitorous general could send attack to one general and retreat to another. So to satisfy Condition A
the following must be true:

1. every loyal general must obtain the same information v(1) ... v(n)

This implies that a general can't necessarily use the value of v(i) directly from general i since they
may be a traitor. Unless we have a careful solution for this then it's possible that generals use a value
for v(i) other than the value general i intended.

2. if the i'th general is loyal, then the value that they send must be used by every other loyal
general as the value of v(i)

These two conditions smell like consensus to me.

Condition 1 can be rewritten as;

1'. Any two loyal generals must use the same values of v(i)

Since both the conditions relate to the single value sent by the i'th general we can restrict the 
problem to "how does a single general send their value v(i) to other generals?". The paper uses the terms
of a commanding general sending an order to their lieutenants. This smells like leader election to me.

The Byzantine Generals Problem, a commanding general must send an order to their n-1 lieutenant generals
such that:

IC1, all loyal lieutenants obey the same order
IC2, if the commanding general is loyal, then every loyal lt. obeys the order they send.

These conditions are called interactive consistency conditions. Note that the commanding officer does
not necessarily need to be loyal. To solve the original problem, the i'th general sends their value
of v(i) by using a solution to the Byzantine Generals Problem to send the order "use v(i) as my value"
with the other generals as the lieutenants.

Questions
- how do we ensure messages are unforgeable?
- are there papers on how we determine if the plan was good or bad?
- how do we ensure generals receive the same values of v(i)
- if the commanding general is not loyal, do loyal lieutenants not obey their order? and if so, does
that break the systems 'liveness'? trigger a leader election?


to read:
- The Byzantine generals strike again Dolev, D.
- Reaching agreement in the presence of faults, same authors as this paper

the crypto papers don't seem to relevant to my interests at this point, if the answer to messages
being unforgeable is simply to use encryption and keys then that's good enough for me