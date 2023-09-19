---
content_type: page
description: This section includes Memorylessness to support Lectures 3-4.
learning_resource_types:
- Lecture Notes
ocw_type: CourseSection
parent_title: Lecture Notes
parent_type: CourseSection
parent_uid: 10dbcabc-062f-5677-9628-24c6d3457998
title: Memorylessness in exponential and geometric random variables
uid: e7a7b880-51d3-2e09-4d40-8ab6ea8def0f
---

The memorylessness property of the exponential distribution was described in the probability lecture slides as

\\\[p(T>t + x | T>x) = p(T>t) \\tag 1\\\]

where

\\(p(T>t) = e^{-\\lambda t}\\) for \\(t\\geq0\\); \\(p(T>t) = 1\\) otherwise

1.  **To prove (1)**, note that

\\\[p(T>t+x|T>x)= \\frac{p(\\{T>t+x\\}\\bigcap\\{T>x\\})}{p(T>x)} \\tag 2\\\]

But

\\\[\\{T>t+x\\}\\bigcap\\{T>x\\} = \\{T>t+x\\}\\\]

because if \\(T > t + x\\), then \\(T>x\\). Therefore

\\\[p(\\{T > t + x\\}\\bigcap\\{T > x\\}) = p(\\{T > t + x\\})\\\]

so, from (2), assuming \\(x>0\\),

\\\[p(T > t + x | T > x) = \\frac{p(\\{T > t + x\\})}{p(T > x)} = \\frac{e^{-\\lambda(t + x)}}{e^{-\\lambda x}}\\\]

and the last fraction is just equal to \\(e^{-\\lambda t}\\), so (1) is proved.

2.  **What does (1) mean in intuitive terms?**
    
    Let random variable \\(T\\) be the time until a certain event (like the failure of a machine) occurs after time 0. That time is exponentially distributed with parameter \\(\\lambda\\). Then (1) means that if we look at the machine at time \\(x>0\\) and the failure has not yet occurred, the time until the failure does occur \\((t)\\) is distributed exponentially with parameter \\(\\lambda\\).
    
3.  **How can this possibly be true? Machines wear (at least a little) during each operation. The more operations a machine does since its last maintenance, the sooner it is likely to fail than it would immediately after maintenance.** That is, suppose that immediately after maintenance, the expected number of operations it can perform before it fails is 100. Then if it somehow does 1000 operations without failure, the exponential distribution model says that the expected number it will do before it fails is still 100 (for a total lifetime of 1,100 operations). But the expected number of operations until the failure ought to be a lot less than 100 because of all the wear that must have occurred.
    
    That's correct. But remember: Models are not exact representations of reality. As engineers, we don't judge models by how accurately they represent reality; we judge them by how accurately they make the predictions we need. The exponential distribution can be a good approximation for _some_ (but not all) purposes. For example, suppose we have to order expensive cutting tools infrequently in large batches. (You will see why that might be true in the inventory lecture.) Suppose these tools have average lifetimes of one week and suppose we can only order tools once a year. How many tools should we have on hand at the start of a year (that is, after the tools we order have arrived)?
    
    Suppose we require that the probability of running out of tools before we order the next batch is less than .01. (If we run out of tools, production stops.) The number we need depends on the variance of the time to fail. If the tool life were perfectly deterministic, then 52 tools would be plenty. The greater the variance of the tool life, the more tools would be needed. The small deviation from the exponential distribution is not important to the answer to this question.
    
    **Challenge:** Solve the problem assuming exponentially distributed life times. (Treat a year as having exactly 52 weeks.)
    
4.  Sometimes it is important to model a given non-exponential probability distribution more accurately than an exponential distribution can. This can be done, but describing it is too complicated for this note.
5.  All this applies equally to geometrically distributed discrete times.