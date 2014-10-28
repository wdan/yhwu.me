---
layout: post
title: "Dynamic Graph Visualization Survey"
date: 2014-06-29 18:28
comments: true
categories: [Research, Visualization, Paper notes]

---

This is a paper note of 'The State of the Art in Visualizing Dynamic Graphs' that was published at EuroVis'14. Its online web tool can be accessed as [dynamicgraphs.fbeck.com](http://dynamicgraphs.fbeck.com).

##Data Source

The authors collected 129 papers about dynamic graph from 1992 to 2014. The journals and conferences include:

###Journals

- *Computer Graphics Forum*
- *TVCG*
- *Information Visualization*
- *Journal of Graph Algorithms and Applications*

###Conferences

- *PacificVis (APVIS)*
- *InfoVis*
- *IV (International Conference on Information Visualization)*
- *EuroVis*
- *GD (Symposium on Graph Drawing)*

<!--more-->

##Data Analysis

Different kinds of tag categories are identified to describe various aspects of a paper. Each publication was assigned to at least one tag per category.

The tag categories include:

1. Type: *application, evaluation, technique*
2. Time: *animation, timeline, generic*
3. Paradigm: *node-link, matrix, generic*
4. Evaluation: *algorithmic, case_study, expert, etc.*
5. Application: *biology, business, document, etc.*
6. Other: *3d, acyclic_graph, clustering, etc.*

##Dynamic Graph Visualization Techniques Taxonomy

Since the time dimension might be the one of the most important criteria to discern between static graph visualization and dynamic graph visualization, the first level of the taxonomy divides the approaches into *animation*, *timeline* and *hybrid* techniques.

###I. Animation

Up to now, all animated approaches are based on node-link diagrams.

In nearly all approaches, the mental map is discussed. The position of nodes is tried to be kept stable, which is called *dynamic stability*.

#### 1. General-purpose Layout

General-purpose layouts do not impose any requirements on the type of graph. They can be discerned as:

**Online approach**: the animation only considers past time steps. This approach fits the scenario that the future evolution of the graph is not yet know better.

**Offline approach**: the animation considers both past and future time steps. This approach allow for better optimizing the layout and maintaining the mental map since next changes are known.

Other approaches are quite independent but look in closer detail at the animated transition period between two consecutive layouts. Sometimes, the transition period is divided as separate phases.

#### 2. Special-purpose Layout

**Compound Graph**: not only layout stability but also cluster stability needs to be optiimzed and clusters need to be tracked across time.

###II. Timeline

Timeline-based approaches promise to provide a better overview of time. However, only little space is available for drawing each of the graphs.

#### 1. Node-link based

Node-link diagram forms:

**Juxtaposed**: node-link diagrams are positioned next to each other.

Potential problems:

- It is hard to compare the differences between subsequent time steps.
- It is difficult to trace a node over several time steps.
- The overall representation is likely cluttered even for small examples.

Sample solutions:

- Linearized
- Linearized bipartite
- Radially layered

**Superimposed**: Diagrams are stacked on top of each other (Most in 2.5D).

**Integrated**: Sequence of graphs are merged into an integrated diagram.

- Timeline edges
- Ego timeline
- Parallel Edges

#### 2. Matrix based

Advantage: staying more readable for larger and denser graphs.

**Intra-cell Timeline**: Each matrix cell contains an individual timeline to represent the edge evolution.

- Bar chart
- Gestaltlines
- Pixel-based

**Layered Matrices**: Adjacency matrices can also be juxtaposed or layered on a timeline.

- Small multiples
- Radially distributed
- Radially layered
- Stacked

###III. Hybrid

##Evaluation

Most evaluations are only case studies (86 out of 129 publications). Some papers specifically focus on evaluation.

Most evaluation approaches focus on animated node-link diagrams, only few on timeline representations; matrix visualizations are not yet evaluated in the context of dynamic graphs.

Task taxonomy:

1. By entity, property and temporal feature
	- entity: granularity such as nodes and links, groups or complete network
   - property: topology of entities and domain-specific attributes
   - temporal feature: states over time
2. By temporal tasks(when), topological tasks(where), and behavioral tasks(what).

Aesthetic criteria in dynamic graph visualization: *general aesthetic criteria*, *dynamic aesthetic criteria*, and *aesthetic scalability criteria*.

Algorithmic evaluation criteria: runtime performance, node density, cluster characteristics, preservation of the mental map, etc.

###User studies

**Mental Map**: Although several studies have been conducted so far, the role of the mental map is not yet clear. *'At least there are indications that its role might have been overestimated in the literature*.

**Animation vs. Timeline**:

Appropriate scenarios and advantages for **animation**:

- Only one or two points in time need to be studied
- Tasks related to the appearance of entities (lower error rates)
- May reveal more findings on adjacent time steps

Appropriate scenarios and advantages for **Timeline**:

- Tasks involving more than two time steps
- May foster the discovery of patterns lasting over longer periods
- May get quicker response time

**Specific Approaches**:

- Timeline-based node-link approach may work better than Hasse diagrams for visualizing the information flow between interacting software processes.
- Interactively selectable presentation speed may not have a positive effect on comprehension performance, but that always showing labels instead of retrieving labels only on demand is beneficial.
- Difference maps and staged-animation may be helpful.
