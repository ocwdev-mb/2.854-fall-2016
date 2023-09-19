---
content_type: page
description: This section includes Notes on Covariance to support Lectures 3-4.
learning_resource_types:
- Lecture Notes
ocw_type: CourseSection
parent_title: Lecture Notes
parent_type: CourseSection
parent_uid: 10dbcabc-062f-5677-9628-24c6d3457998
title: Notes on Covariance
uid: 22d7a154-2d29-e700-d030-d20a501926ce
---

\\\[X,Y\\,independent \\rightarrow cov(X,Y) = 0\\\]

Assume random variables \\(X\\) and \\(Y\\) are _discrete_. That is, assume that there is a finite or denumerable sample space which is a set of \\(w\_i\\) and a set of quantities \\(x\_i\\) and \\(y\_i\\) defined.

**Definition** \\(X\\) and \\(Y\\) are _independent_ if

\\\[prob((X = x)\\,and\\,(Y = y)) = prob(X = x)prob(Y = y)\\\]

in which \\(x\\) is some \\(x\_i\\) and \\(y\\) is some \\(y\_j\\).

Then if \\(X\\) and \\(Y\\) are independent,

\\\[E(XY) = E(X)E(Y)\\\]

_Proof:_

\\\[E(XY) = \\sum \_{i,j} \\ x\_iy\_jprob(XY = x\_iy\_j)\\\]

\\\[= \\sum \_{i,j} \\ x\_iy\_jprob((X = x\_i)\\,and\\,(Y = y\_j))\\\]

\\\[= \\sum \_{i,j} \\ x\_iy\_jprob(X = x\_i)prob(Y = y\_j)\\\]

\\\[= \\sum \_{i} \\ x\_iprob(X = x\_i)\\sum \_{j} \\ y\_jprob(Y = y\_j) = E(X)E(Y)\\\]

Then if \\(X\\) and \\(Y\\) are independent,

\\\[cov(X,Y) = E\[(X - E(X))(Y - E(Y))\]\\\]

\\\[=E\[XY - XE(Y) - YE(X)+E(X)E(Y)\]\\\]

\\\[=E\[XY\] - E(X)E(Y) - E(Y)E(X) + E(X)E(Y) = 0\\\]