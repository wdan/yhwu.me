---
layout: post
title: "Process and Pitfalls in Writing InfoVis Papers"
date: 2014-07-10 20:58
comments: true
categories: [Research, Visualization, Paper notes]

---

This is a paper note of 'Process and Pitfalls in Writing Information Visualization Research Papers' by [Tamara Munzner](http://www.cs.ubc.ca/~tmm). This paper categorizes different types of papers presented in the area of Information Visualization and discusses a set of common pitfalls that recurs in many rejected papers.

*A project should begin with a careful consideration of  the type of paper that is the desired outcome.*

##Paper Types

###Technique

Technique papers focus on novel algorithms and an implementation is expected.

Typical results would be algorithm complexity analysis, quantitative measurements of the implementation, and a qualitative discussion of images created by the new algorithm.

There is very little or no design justification for whether the technique is actually suitable for the proposed problem domain: there is an implicit assumption that the previous cited work makes such arguments.

<!--more-->

###Design Study

Design Study papers make a case that a new visual representation is a suitable solution for a particular domain problem.

- The target problem should be explicitly explained.

- The design requirements should be crisply stated through the task analysis part.

- The visual encoding and interaction mechanisms should be described. Also, you should justify these design choices in terms of how well they fulfill the requirements. Typical arguments would refer to perceptual principles and infovis theory.

- There should be some results that back up the claim that your approach is better than others.

The research contribution of a design study paper is not typically a new algorithm or technique, but rather a well-reasone justification of how existing techniques can be usefully combined.

### Systems

System papers focus on the architectural choices made in the design of an infrastructure, framework, or toolkit. It does not introduce a new design or algorithms, neithor introduces a new design. The research contribution of a system paper is the discussion of architectural design choices and abstractions in a framework or library.

Key aspects of a systems paper are the lessons learned from building the system, and observing its use.

### Evaluation

Evaluation papers focus on assessing how an infovis system or technique is used by some target population. They typically do not introduce new techniques or algorithms, and often use implementations described in previous work.

### Models

Model papers present formalisms and abstractions. Their purpose is to help other researchers think about their own work.

The subcategories include: Taxonomy, Formalism, Commentary.

## Type Pitfalls

*Design in Technique's Clothing*: Don't validate a new design by providing only performance measurements.

*Application Bingo versus Design Study*: Don't apply some random technique to a new problem without thoroughly thinking about what the problem is, whether the technique is suitable, and to what extent it solves the problem. A very common pitfall is that application paper submissions simply describe an instantiation of a previous technique in great detail. Many do not have an adequate description of the domain problem. Most do not have an adequate justification of why the technique is suitable for the problem. Most do not close the loop with a validation that the proposed solution is effective for the target users.

*All That Coding Means I Deserve A Systems Paper*: Many significant coding efforts do not lead to a systems paper. Specific architectural lessons are important.

*Neither Fish Nor Fowl*: Papers that try to straddle multiple categories often fail to succeed in any of them.

##Middle Pitfalls: Visual Encoding

*Unjustified Visual Encoding*: An infovis design study paper must carefully justify why the visual encoding chosen is appropriate for the problem at hand.

In many successful infovis approaches, the input data undergoes significant transformations into some derived model that is ultimately shown. Without any discussion of the design requirements, it is very hard to convince a reader that your model will solve the problem.

The foundation of information visualization is the characterization of how known facts about human perception should guide visual encoding of abstract datasets.

*Hammer In Search Of Nail*: Characterize, at least with some high-level arguments, the kinds of problems where your new technique shines as opposed to those where it performs poorly.

*2D Good, 3D Better*: The use of 3D rather than 2D for the spatial layout of an abstract dataset requires careful justification that the benefits outweigh the costs. The most serious problem with a 3D layout is occlusion. People can better compare things simultaneously visible side by side rather than a 3D layout. Also, it is hard for people to make precise length judgements because of perspective foreshortening.

*Color Cacophony*: The paper will lose its credibility when you make design decisions with blatant disregard for basic color perception facts.

- Avoid huge areas of highly saturated color

- Avoid hoping color coding will be distinguishable in tiny regions

- Avoid using a sequential scheme for diverging data

*Rainbows Just Like In The Sky*: Avoid to use a continuous rainbow colormap. Standard rainbow colormap is perceptually nonlinear. Moreover, hue does not have an implicit perceptual ordering, in contrast to other visual attributes such as greyscale or saturation. '

##Late Pitfalls: Paper Strategy, Tactics, and Results

###Strategy Pitfalls

*What I Did Over My Summer Vacation*: Do not try to squeeze too many papers out of the same project, where you parcel out some tiny increment of research contribution beyond your own previous work.

*Dense As Plutonium*: Do not try to cram many papers' worth of content and contributions into one.

*Bad Slice and Dice*: Keep care when you've done two papers' worth of work and choose to write two papers.

###Tactical Pitfalls

*Stealth Contributions*: Do not leave your contributions implicit or unsaid. The author highly recommend having a sentence near the end of the introduction that starts, "The contribution of this work is"， and of using bulleted lists if there are multiple contributions.

*I Am So Unique*: Do not ignore previous work when writing up your paper. A good previous work section is a mini-taxonomy of its own, where you decide on meaningful  categorization given your specific topic. Discuss not only work that has been done on similar problems to your own, but also work that uses similar solutions to yours that occurs in different problem domains.

*Enumeration Without Justification*: Simply citing the previous work is necessary but not sufficient. You must explain why this previous work does not itself solve your problem, and what specific limitations of that previous work your approach does address. Moreover, it's not even enough to just make the case that yours is different - yous must be *better*.

*Sweeping Assertions*: A research paper should not contain sweeping unattributed assertions. Three choices: cite the source; delete the assertion; or explicitly tag the statement as your observation, your conjecture, or an explanation of your results.

*I Am Utterly Perfect*: No work is perfect. An explicit discussion of the limitations of your work strengthens, rather than weakens, your paper.

###Result Pitfalls

*Unfettered By Time*: Do not omit time performance from your writeup.

*Fear and Loathing of Complexity*: Technique papers that focus on accelerating performance should usually include some statement of algorithm complexity.

*Straw Man Comparison*: Compare against state-of-the-art approaches rather than outdated work.

*Tiny Toy Datasets*: Avoid using only tiny toy datasets in technique papers that refine previously proposed visual encodings.

*But My Friends Liked It*: Positive informal evaluation of a new infovis system by a few of your infovis-expert labmates is not very compelling evidence that a new technique is useful for novices or scientists in other domains.

*Unjustified Tasks*: Beware of running a user study where the tasks are not justified.

##Final Pitfalls: Style and Submission

###Writing Style Pitfalls

*Deadly Detail Dump*: Do not simply dump out all the details. The details are the *how* of what you did. But you must first say *what* you did and *why* you did before the *how*.

*Story-Free Captions* Avoid using a single brusque sentence fragment as your caption text. Design your paper so that as much of the paper story as possible is understandable to somebody who flips through looking only at the figures and captions.

*My Picture Speaks For Itself*: You should talk the reader through how your visual representation exposes meaningful structure in the dataset, rather than simply assuming the superiority of your method is obvious to all readers from unassisted inspection of your result images.

*Grammer is Optional*: Grammar is not optional; you should use correct syntax and punctuation for a smooth low-level flow of words.

*Mistakes Were Made*: Avoid the passive voice as much as possible. The reader does not have enough information to determine *who* did something. I urge you to use the active voice and make such distinctions explicitly.

*Jargon Attack*: Avoid jargon as much as possible, and if you must use it then define it first.

*Nonspecific Use of Large*: Never just use the words 'large' or 'huge' to describe a dataset or the scalability.

###Submission Pitfalls

*Slimy Simultaneous Submission*: Don't simultaneously submit the same work at multiple venues.

*Resubmit Unchanged*: Don't completely ignore the reviews and resubmit your rejected paper to another venue without making any changes.

