---
layout: page
title: Testing Distributed Systems
excerpt: "Testing of Distributed Systems."
modified: 2014-08-08T19:44:38.564948-04:00
image:
  feature: so-simple-sample-image-4.jpg
  credit:  deepak
  creditlink: http://research-deepak.com//home/
---
When testing a system that has multiple physically distributed interfaces (ports) we place a tester at each port of the system under test N. When applying a test sequence to N the use of multiple testers introduces the possibility of coordination problems amongst remote testers. These potential additional problems are known as controllability and observability problems. They occur if a tester cannot determine either when to apply a particular input to N, or whether a particular output from N is generated in response to a specific input, respectively. Consider a distributed architecture where there are remote testers at ports p(1), ..., p(m).

1. The controllability (synchronisation) problem occurs when the tester at a port p(i) is expected to send an input to N after N responds to an input from the tester at some other port p(j), without sending an output to p(i). The problem here is that the tester at p(i) is unable to determine whether N has received that input and so cannot know when to send its input.
2. The observability problem occurs when the tester at some port p(i) is expected to receive an output from N in response to a given input at some port other than p(i) and is unable to determine when to start and stop waiting. Such observability problems make it harder to determine which input led to a particular output and can introduce fault masking.

There has been much interest in constructing test sequences that cause no controllability and observability problem during their application. Given such a test sequence, a tester can determine when to apply its own inputs and whether an output observed is received in response to the correct input. An alternative is to construct a test sequence that includes external coordination messages: messages sent between the testers in order to overcome controllability and observability problems. However, there is often a cost associated with the use of such messages. This cost includes the delay introduced by the sending of each message. Thus, another problem is to produce an adequate test sequence that is cheapest to apply when including the cost of sending external coordination messages.
It has been found that we can produce test sequences that avoid controllability and observability problems, possibly through the use of coordination messages. However, if these problems will also affect users then we are in danger of giving testing too much power: testing can distinguish between an implementation and a specification in cases where users cannot. Instead, we can recognise the limitations caused by controllability and observability problems as something that affects our ability to distinguish implementations and specifications and consider an implementation to be acceptable (correct) if in use it is not possible to distinguish it from the specification. This leads to new implementation (conformance) relations that capture what we mean by correctness and these lead to new test generation algorithms.plugin[^plugins]


--- 
**References:** http://people.brunel.ac.uk/~csstrmh/research/distributed_testing.html
{: .notice}

---
