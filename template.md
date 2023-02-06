---
documentclass: IEEEtran
classoption:
 - 10pt #9pt, 10pt, 11pt, 12p
 - draftcls #draft, draftcls, draftclsnofoot, final
 - technote #conference, journal, technote, peerreview, peerreviewca
 - letterpaper #letterpaper, a4paper, cspaper
 - oneside #oneside, twoside
 - onecolumn #twocolumn, onecolumn
numbersections: 1
date: \today
title: |
 A complete but succinct description of work using relevant important keywords 
 while being snappy when possible
author:
 - Russell Shomberg:
	 institute: University of Rhode Island Narragansett RI USA
 # Add authors as necessary
abstract: |
 Four Sentences\:
 State the problem.
 Say why it is an interesting problem.
 Say what your solution achieves, not what it is.
 Say what follows from your solutions.
---

# Introduction #
## Problem ##

### Statement ###

> What is the specific problem did you (attempt to) solve?[^1]
> Why exactly does this problem exist?
> Who specifically has this problem?
> Scientists?
> Military?
> Industry?

### Importance ###

> How important is finding a solution (be realistic)?
> What would be possible that previously was not?
> Who specifically would benefit and how?
> Scientists?
> Military?
> Industry?

### Difficulty ###

> How difficult is the problem to solve (be realistic)?
> What specifically must be overcome?
> Are specific technologies required?
> Is there knowledge required?
> Does it require organizational or institutional support/cooperation?
  
## Solution ##

### Proposed Solution ###

![Photo (or concept drawing) of your design preferably being deployed in
the field. This figure should appear on page one. Many readers will not look at
anything else. Caption is a short description and summary of system
functionality.](solution.png){#fig:solution}

> Briefly what is your solution? 
> Reference @fig:solution.[^2]

> What is different about your solution?
> How does it overcome the problem difficulty?

### Design Considerations ###

> What specific challenges does your solution face (briefly)?
> How are those challenges different from those of other solutions? 

### Success Criteria ###

> How would you evaluate a design of your concept (be specific)?
> Why is that criteria valid/important?

> Did you create a working prototype?
> Did it meet your sucess criteria?
> Are further improvements likely?
 
# Background #

> I try to avoid including this section. It lengthens and defocusses the
> paper. I try to push this information into references or appendix. I assume my
> readers are either experts or know how to look things up. If you need this,
> keep it as short as possible or attempt to fold it into the Introduction
> and/or Related Work.

> Are there any conccepts required to understand the rest of your paper that you
> would not already expect your readers to understand?[^9]

# Related Work #

> Keep this section as short as possible and try to combine with Introduction
> and/or Background.

## Standard Practice ##

> How is this (or similar) problem commonly or historically solved?[^9]
> Why is this not good enough?
> How is this different than your solution?

## State-of-the-Art ##

> How is this (or similar) problem solved by entities with greater access
> resources and the newest technology?[^9]
> Why is this not good enough?
> Why is this not more common?
> How is this different than your solution?

## Key Projects ##

> Are there any specific related projects you need to address?
> Why are they not good enough?
> Why is this not more common?
> How is this different than your solution?

# System Overview #

## Design Overview ##

> What does the system look like? 
> What are the functional subsystems?
> How do the subsytems interact?

> For each subsystem: 
> What is it? 
> How does it work? 
> How does it interact?

## System Model ##

> I prefer to start with a broad picture and then drill down into details rather
> than start with building blocks and build up into full structure. This is an
> uncommon choice, but one that I believe strongly in.

> What is the overall state model? 
> What are the state variables? 
> How are they related?

> What category of system or equation is this? (ie. harmonic oscillator)
> What kinds of results does it predict?
	
## System Elements ##

> For each term:

> What does this represent physically?
> How do you predict the term?

> What assumptions are you making?
> Are they realisitic, conservative, conditional, or stupid?

> Can it be measured?
> Does measurement match prediction?
> Under what conditions?
> What does this mean?
> Are only emperical measured values valid?

## System Dynamics ##

 > Given characterisitics of each element, how is model expected to behave?
  
## Control ##

> Is the system controllable?

> What are the control inputs?

> What are the control outputs?

> Is the system stable?

# Modeling Results #

> Why using models instead of models matched to lab results?[^3]

> Are these model results reasonable?

> What assumptions are being made?
> Why is this valid?

# Lab Results #

> What needs testing?

> For each test:
> How did you set up the tests?
> How did you isolate variables?
> How did you control inputs?
> How did you measure outputs?
> Did results match expectations?
> What do results mean?

> Do lab results generally match expectations?
> Can a system be deployed based on results?

# Field Results #

> Who? What? When? Where? How?

> Location, Depth, Duration, Distance?

> What are qualitative observations?
> Expectations vs Reality?

> What did you demonstrate?[^4]

> What were the major successes?

> What do the results mean?

# Conclusion #

## Success ##

> Did you reach your success criteria? (be realistic)

> What does that mean?

## Conclusions ##

> For each conclusion or major point:
> Restate the conclusion plainly.

## Future Work ##

> What Technology Readiness Level (TRL)[^5] is the system in?
> What is next for this project?
> What needs to be investigated further?
> What needs to be tested?

# Acknowledgments #

> For each: This project was made possible by a grant from the Foundation
> (123456)

> For each: We wish to acknowledge (person/organization) for (contribution to
> project)

> For each: We wish to acknowledge the captains and crews of the R/V Neverdock
> for their expertise and professionalism at sea.

# References # {-}

> Use multiple bib files (related.bib/background.bib/...).
> Organize within the files as well.
> Write your own abstracts into the entries.

> 10-30 refs is reasonable.
> 15-25 makes more sense.

::: {#refs} 
:::

\appendix

## Appendix ##

  * Background information required to understand new concepts.
  * Avoid using appendixes. 
  
[^1]: Getting to the point as soon as possible is very important. I do not
recommend putting any background before stating what the point of your
paper is. Sentence 1 is more important than the abstract.

[^2]: Getting an impressive figure on page one is very important. Most
people skim figures before they do anything else. Fig. 1 is more
important than sentence 1.

[^3]: Model results can fold nicely into lab tests, but some projects
    rely heavily on modeling. This is fine, but it should be justified.

[^4]: This is a big deal and very impressive. While it only amounts to
    a paragraph or two of writing, it is the thing that makes a
    paper. Real artists ship, and real engineers deploy.

[^5]: I use the precise wording from TRL without actually refering to
    it. For example, TRL4 -> "validated in lab", TRL6 -> "demonstrated
    in the deep sea environment"

[^9]: Look to reference texts books or comprehensive review papers.
