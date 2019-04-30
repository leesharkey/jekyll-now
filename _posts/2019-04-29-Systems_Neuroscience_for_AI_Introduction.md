---

layout: post

title: Systems Neuroscience for AI&#58; An Introductory Guide to the Literature

---

#### Guide contents
* [Introduction]() (This page)
* [Motivation: why should we pay attention to the brain for AI?]()
* [Overviews: What, broadly speaking, is the brain computing?]()
* [The Cerebral Cortex: A Very Tangled Web]()
* [The Thalamus: More than just Central Station]()
* [The Hippocampus: A Less Tangled Web]()
* [Cortico-hippocampal interactions]()
* [Reinforcement Learning with the Basal Ganglia and prefrontal cortex]()
* [The Telencephalon: Or, How I Learned Concepts in the Cortico-thalamo-basal ganglia-hippocampal system]()
* [The ‘Little Brain’, often forgotten: the Cerebellum]()
* [The Cerebello-basal ganglia-thalamo-cortical system]()
* [Conclusions]()

> “The brain is arguably still the only example that we have of something that approximates the kind of intelligence we’re trying to build, and so it seems like a good idea to pay some attention to how it works.”  
> Matt Botvinick, Director of Neuroscience Research, DeepMind

_**TL;DR**: This guide aims to give AI researchers a skeleton-frame introduction to modern systems neuroscience and contextualise specific recent AI research with respect to those systems. It focuses on views of neuroscientific systems that are deemed most likely to be useful for AI research in the near term. Despite efforts to remove personal biases and omissions, some will remain in any concise guide with such a broad scope. Some articles are behind paywalls. Sci-hub exists._

General intelligence is ostensibly the central goal of the field of AI. Yet, with a few notable exceptions, few in AI research pay much attention to the only known example of general intelligence: the human brain. Although some early AI took inspiration from neuroscience, the two fields gradually grew more distant while statistical-theoretical and computational constraints caught up with the neuroscientific theory. Today, the time is ripe for an academic rapprochement between the two fields, and it’s happening. But finding good, modern sources for getting up to speed on biological intelligence takes a lot of time; it’s costly even to figure out what areas of neuroscience to prioritise. And when thousands upon thousands of new AI papers come out every year, keeping abreast in both fields is a near impossible challenge. 

To help make the challenge a little less difficult, I present this guided reading list of modern neuroscience literature. It’s aimed at AI researchers (and will also be useful to early-stage computational neuroscience students) who already have the equivalent of a basic undergraduate-level course in systems neuroscience. Its goals are twofold: 

1. To convince the reader that, although we are still ignorant of many crucial details in systems neuroscience, our knowledge as it stands provides a rational framework to organise our thinking on intelligence, and
2. To give the reader a sound, skeleton-frame mental model of our current theories of how general intelligence is implemented by the brain.

**Importantly, the guide relegates classic literature in favour of recent articles**. This was partly motivated by laziness, but it is mostly by design, since most articles present ample introductions to the historical literature. The guide presents an assortment of consensus views and emerging perspectives. The list is also populated by links to recent video lectures by the authors of some of the reviews. In addition to the neuroscience reviews, readers from either neuroscience or AI will be able to build their mental models of intelligence ‘in both directions’ thanks contextualising discussions of a selection of recent AI literature that has clear links to the respective neuroscientific systems.

## Why a _guided_ reading list?
The scope of this resource has such an extensive breadth and depth that it would be impossible to do a service to the ideas presented by review authors by recapitulating their arguments in an extremely long review or textbook. Therefore the reading list is guided, as opposed to simply being a list of reviews, in order to strike a middle ground between 
1. permitting readers to benefit from motivating explanations of the review content from people with more time to devote to the field of cognitive, computational & systems neuroscience, and
2. maintaining the authority, recency, and accuracy of the content.

Although the reading list is guided, readers can begin in any section and read sections in any order with one exception: if the reader would like very quickly to brush up on undergraduate-level neuroscience prerequisites, they should first read Chapter 15 “Neuroscience” of [Reinforcement Learning: An Introduction (Sutton and Barto 2018)](http://incompleteideas.net/book/RLbook2018.pdf).

Despite my best efforts, the guide omits several important research areas. Although I have sought and received review recommendation beyond my own initial readings, it is impossible to stamp out all idiosyncrasies in the views presented here, especially while keeping the guide moderately concise; the selections and omissions therefore contain personal biases toward a particular view of what topics in neuroscience are important for AI. To highlight and possibly counterbalance these biases, I will do my best briefly to be explicit about where the emphases lie. In order to do that, it will be helpful to introduce Marr’s three level of analysis. Readers familiar with Marr’s levels of analysis should feel free to skip the following intermezzo. 

## Intermezzo: What would an explanation of the brain even look like?
This question keeps neuroscientists of all stripes awake at night. To break the question into more manageable parts, neuroscientists often find it useful to invoke [David Marr’s](https://en.wikipedia.org/wiki/David_Marr_(neuroscientist)) three ‘levels of analysis’ (see list below), which, by analogy to a computer, describe the **computational level**, which is specified on the **algorithmic/representation level**, which in turn is implemented on the **implementation level**. It is important to recognise that these levels have overlapping boundaries due to the curse of reductionism: In order to completely understand a system on one level, you must understand it on the level below. Despite these dependencies, they serve as a useful aid for setting a manageable scope for many neuroscientific questions. Additionally, while the levels help frame questions of neuroscientific description (“What is…?” or “How does…?”), the levels of analysis can also be applied to questions of artificial intelligence design (“How should…?”).


<style type="text/css">
  table          {border:ridge 1px grey;}
  table td       {border:inset 1px #000;}
  table tr#ROW1  {background-color:red; color:white;}
  table tr#ROW2  {background-color:white;}
  table tr#ROW3  {background-color:blue; color:white;}
</style>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<tbody>
<tr><td markdown="span"> <h4>The computational level</h4>
What generic problems are being solved? What information is abstracted and why? What do different programs do on an abstract level? 
</td></tr>
<tr><td>Neuroscience examples: 
* Is the cortex performing unsupervised learning? Prediction? Reinforcement learning? Supervised learning? Meta-learning? Is it just minimising ‘free energy’?
* Does the brain use an episodic memory buffer? Or is it just memorising sequences of activity? Are these the same thing?
</td></tr>
<tr><td>AI examples: 
* Should our system predict future inputs? Should the system compress input data or just memorise all of it?
* Should the system learn a probability distribution or a deterministic function? 
What mathematical quantity should the system optimise?
</td></tr>
<tr><td> #### The algorithmic/representation level
How exactly does the system solve the problems described on the computational level? What assumptions, computations, or representations does it use? How are the objects in the implementational level used to compute the programs on the computational level?
</td></tr>
<tr><td>Neuroscience examples:
* What representational format do cortical predictions and uncertainty take? And is the sparse coding performed by ICA, winner-takes-all, non-negative PCA, or some other algorithm? 
* Are the basal ganglia calculating the temporal difference learning equation? How are expected rewards and value functions calculated and how are state-values updated? How are states represented?
* What mathematical descriptions can be given to the seemingly chaotic dynamics of recurrent systems with many neurons?
</td></tr>
<tr><td>AI examples: 
* Should our model use deep learning or other algorithms? 
* What deep learning architecture should be used to perform prediction? LSTM? Transformer?
* How should reinforcement learning used in our system be structured? Model-based or model-free? Hierarchical or not? Distributed training or not? Should the RL algorithm incorporate MAML or not?
</td></tr>
<tr><td> #### The implementational level
What is the physical instantiation of the computational algorithms and representations? How exactly does the hardware run the programs from the computational algorithmic level?
</td></tr>
<tr><td>Neuroscience examples:
* How do cortical pyramidal neurons integrate incoming signals and decide when to fire? What proteins and other structures are involved and how do they function?
* Which neurons are connected to which other neurons (on a micro- and macroscopic scale)? 
* Do neural oscillations, such as gamma oscillations, have a functional role in neural computation or are they mere side-effects or neural activity? 
* What role do glial cells play in neural function?
</td></tr>
<tr><td>AI examples:
* What materials should we use in chip design, and how should they be arranged?
* How best to parallelise matrix computation in a GPU? 
* Can we design neuromorphic circuits and chips that make better use of the physics of the chips to perform useful computation? 
* In what framework or language should we write our architecture? Tensorflow? Theano? Python? C? Do these frameworks have the requisite functions for our algorithm? Do they perform them efficiently?
</td></tr>
</tbody>
</table>


## What this guide focuses on and what it ignores
We currently do not have a good enough understanding of any single level of analysis in neuroscience to know with certainty what topics are safe to ignore. As such, this guide introduces neuroscience reviews from all three levels but places greater emphasis on the computational and algorithmic/representational levels than on the implementation level. This is not to say that excluded topics won’t be useful for building general intelligence - it just reflects my view of what systems-neuroscientific concepts AI researchers are likely to find useful in the short to medium term. This is consistent with the emphasis placed by Hassabis, who has [said](https://www.youtube.com/watch?v=Qgd3OK5DZWI) for a long time that many approaches to building general intelligence focus on parts of neuroscience that are too high- or low-level to be immediately useful for building intelligence. 

The guide therefore focuses on: 
* The functions that particular brain areas are believed to perform and, where possible, how they are believed to perform them.
* The high-level algorithms the brain is believed to be implementing and what we know about how they are performed
* Relations between the discussed brain parts and systems
* Links from the neuroscience to modern AI algorithms and architectures.

The guide does not emphasise:
* Electrochemical dynamics of single nerve cells or ion channels
* Mechanisms of synaptic plasticity, long term potentiation or depression
* Neural oscillations
* Dynamics of small scale neural assemblies
* Neuromorphic hardware or its inspirations
* Models of consciousness (even when they are computationally-informed)
* Neuropathology
* <u>Detailed</u> anatomy.

A further caveat to make explicit is that there is a mostly unintentional bias toward research from staff associated with DeepMind. I only mildly apologise for this - it just happens that there is an awful lot of AI-relevant neuroscience research emerging from the company, as well as a lot of AI research that is strongly linked to systems neuroscience. That said, it is far from a lone actor in the AI-neuroscience intersection. Just bear this bias in mind throughout. 

## How this guide is structured

The guide starts with a section that motivates the relevance of neuroscience to AI. 

The subsequent section contains some reviews that give broad overviews of the systems likely to be at play in the brain. Such reviews represent the ‘computational’ level of analysis and aim to give an overview of what systems are likely to act in the brain; this should help contextualise more detailed reviews about particular brain parts and their functions.

The main guide follows, which primarily tackles the algorithmic/representational level of analysis, though other levels are addressed too. I take a mixed approach to divide the literature in a way that makes sense: a combination of divisions by system and by anatomy. It sometimes makes sense to look at a particular part of the brain in isolation, then later look at how particular pairs of these components interact, then finally integrating the component into the systems in which it plays a role. Though a mostly sensible structure, no part of the brain (and certainly no system within it) works in isolation, hence some reviews will demand knowledge only touched on in later sections and in some unavoidable cases, will demand knowledge that is not included anywhere in the reading list; this is to be expected when only a small subset of the literature can be selected for inclusion. 

For each paper, I provide a small, contextualising introduction. After each system has been introduced, I discuss a few of the specific, recent AI architectures that I’m aware of that draw on or inform the neuroscience. 

Not everyone will want (or need) to read every paper. In order to help readers identify which papers they’d like to prioritise, each selected review has a pie-chart that estimates the amount that it focuses on a particular level of analysis. A review that focuses equally on all levels of analysis for both AI and neuroscience would look like this:


![Template pie chart](/images/sysneuroai_images/template.png)


Before the real content, a practical note: the depressing closedness of biology literature might come as a surprise to those only familiar with the quantitative sciences. Biomedicine has long been in the grips of a [publishing house kabal](https://www.nature.com/news/open-access-the-true-cost-of-science-publishing-1.12676), though there are [encouraging signs](https://www.nature.com/articles/d41586-018-06178-7) for the open science campaign. Until the field improves its publishing norms, you’ll probably need an institutional subscription. I’m not making [a public recommendation for](https://slatestarcodex.com/2018/03/19/the-dark-rule-utilitarian-argument-for-science-piracy/) or against its use here, but be aware that [Sci-hub](https://whereisscihub.now.sh/go) exists. Also be aware that it may break laws in your country, even though your country [might](https://openscience.com/elsevier-gets-blocked-in-sweden-after-it-legally-requires-internet-providers-to-make-sci-hub-locally-inaccessible/) want it to be legal. 

Finally, I emphasise once again that this guided reading list cannot possibly include everything, and the vast majority of important literature had to be excluded. The reading list aims therefore only to serve as an exceedingly general overview, a springboard from which to jump deeper into the areas of neuroscience that each reader finds most exciting and relevant to their respective interests. So don’t be afraid to deviate from the list if you find more specialised reviews on topics that interest you! 


