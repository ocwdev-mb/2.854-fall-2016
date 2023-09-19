---
content_type: page
description: "This section includes The Mysterious \u03C4 to support Lectures 12-14."
learning_resource_types:
- Lecture Notes
ocw_type: CourseSection
parent_title: Lecture Notes
parent_type: CourseSection
parent_uid: 10dbcabc-062f-5677-9628-24c6d3457998
title: "The Mysterious \u03C4"
uid: c3a7f219-65e4-2a06-2e8d-a2115ef5e35c
---

There seems to be a lot of confusion as the parameters of the production line models. I'll try to clear it up without creating too much more.

1\. Continuous Time, Continuous Material Models
-----------------------------------------------

There should be no confusion about this case. \\(r \\delta t\\) is the probability of a repair during an interval of length \\(\\delta t\\) and is therefore dimensionless. \\(p\\delta \\)t is the probability of a failure during an interval of length \\(\\delta t\\) and is also dimensionless. Since \\(\\delta t\\) is in units of time, \\(r\\) and \\(p\\) are in units of \\(\\frac{1}{time}\\). The time unit could be seconds or minutes or hours, years, or centuries, whichever is more convenient. \\(\\frac{1}{r}\\) is the MTTR of a machine and \\(\\frac{1}{p}\\) is the MTTF of a machine, and they have units of time.

\\(\\mu\\) is in units of stuff / time. ("Stuff" could be parts, it could be a weight unit, it could be a volume unit, etc.)

Just be sure that the time units are consistent for all parameters and that the stuff units of \\(\\mu \\) is the same as the stuff units for the buffer sizes \\(N\\).

2\. Discrete Time, Discrete Material (AKA Deterministic Processing Time) Models
-------------------------------------------------------------------------------

\\(τ\\) is the common operation time of all the machines in the system being studied. It is a time and is expressed in natural time units.

However, the time unit for this model is the _number of operation times_. Events only occur at integer multiples of \\(τ\\). In this model, \\(r\\) and \\(p\\) are probabilities and therefore dimensionless. \\(r\\) is the probability of a repair during an operation time; \\(p\\) is the probability of a failure during an operation time. \\(\\frac {1}{r}\\) is the MTTR of the machine _**expressed in units of** **operation times**_.

That is, MTTR is the mean number of operation times until a machine is repaired. We treat MTTR as dimensionless. Similarly, \\(\\frac{1}{p}\\) is the MTTF of the machine, also _**expressed in units of** **operation times**_.

The stuff unit is a part, and is treated as dimensionless. The buffer sizes are therefore also dimensionless.

The confusion arises when I present problems in natural time units (seconds, minutes, etc.). For example, suppose I tell you that the operation time \\(τ\\) of a machine is 15 seconds and that its MTTR is 30 minutes. In order to use this information in the deterministic processing time model, we have to express MTTR as a multiple of \\(τ\\). The relationship is

\\\[{MTTR\\,in\\,seconds} = \[MTTR\\,in\\,operation\\,times\] \\times \[the\\,number\\,of\\,seconds\\,in\\,an\\,operation\\,time\]\\\]

or

\\\[{MTTR\\,in\\,seconds} = \[MTTR\\,in\\,operation\\,times\] \\times \\,{τ \\;in \\,seconds}\\\]

so in this case,

\\\[30 \\times 60 = \[MTTR\\,in\\,operation\\,times\] \\times 15\\\]

or

\\\[\[MTTR\\,in\\,operation\\,times\] = \\frac{30 \\times 60}{15} = 120\\\]

so

\\\[r = \\frac{1}{MTTR} = 0.0083333\\\]

and similarly for MTTF and \\(p\\).