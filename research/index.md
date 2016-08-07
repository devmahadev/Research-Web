---
layout: page
title: Testing Distributed Systems
excerpt: "Testing of Distributed Systems."
modified: 2014-08-08T19:44:38.564948-04:00
search_omit: true
image:
  feature: so-simple-sample-image-1.jpg
  credit:  deepak
  creditlink: http://research-deepak.com/home/
---
When testing a system that has multiple physically distributed interfaces (ports) we place a tester at each port of the system under test N. When applying a test sequence to N the use of multiple testers introduces the possibility of coordination problems amongst remote testers. These potential additional problems are known as controllability and observability problems. They occur if a tester cannot determine either when to apply a particular input to N, or whether a particular output from N is generated in response to a specific input, respectively. Consider a distributed architecture where there are remote testers at ports p(1), ..., p(m).[^plugins]

![Testing Distributed Architecture]({{ site.url }}/images/realWorld.png)

1. The controllability (synchronisation) problem occurs when the tester at a port p(i) is expected to send an input to N after N responds to an input from the tester at some other port p(j), without sending an output to p(i). The problem here is that the tester at p(i) is unable to determine whether N has received that input and so cannot know when to send its input.
2. The observability problem occurs when the tester at some port p(i) is expected to receive an output from N in response to a given input at some port other than p(i) and is unable to determine when to start and stop waiting. Such observability problems make it harder to determine which input led to a particular output and can introduce fault masking.

[^plugins]: http://people.brunel.ac.uk/~csstrmh/research/distributed_testing.html

--- 
**References:** 
{: .notice}

