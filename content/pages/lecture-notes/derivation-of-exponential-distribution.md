---
content_type: page
description: This section includes Derivation of Exponential Distribution to support
  Lectures 5-6.
learning_resource_types:
- Lecture Notes
ocw_type: CourseSection
parent_title: Lecture Notes
parent_type: CourseSection
parent_uid: 10dbcabc-062f-5677-9628-24c6d3457998
title: Derivation of Exponential Distribution
uid: 2fdb75f6-cf8c-6b73-88a5-e3c6af8731ce
---

The graph of the exponential distribution is shown in Figure 1.

{{< resource f902926e-42b3-d35f-e8fb-7989317232c5 >}}

Figure 1: Graph of Markov Process for Exponential Distribution. (Figure by MIT OpenCourseWare.)

The transition equations are

\\\[ p(0,t + \\delta t) = \\mu \\delta tp(1,t) + p(0,t) + o(\\delta t) \\tag 1 \\\]

\\\[ p(1,t + \\delta t) = (1 - \\mu \\delta t) p (1,t) + (0)p (0,t) + o(\\delta t) \\tag 2 \\\]

or,

\\\[\\frac{dp(0,t)}{dt}= \\mu p(1,t) \\tag 3 \\\]

\\\[\\frac{dp(1,t)}{dt}= -\\mu p(1,t) \\tag 4 \\\]

Solve differential equations (3), (4) and we get

\\\[p(0,t) = 1 - e^{-\\mu t}\\tag 5\\\]

\\\[p(1,t) = e^{-\\mu t}\\tag 6\\\]

Function \\(p(0,t)\\) is actually the cumulative density function of the exponential distribution

\\\[F(t) = p(0,t)\\tag 7\\\]

Then the density function of the exponential distribution is

\\\[f(t) = \\frac{dF(t)}{dt}= \\mu e^{- \\mu t}\\tag 8\\\]