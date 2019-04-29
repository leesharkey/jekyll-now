---

layout: post

title: Systems Neuroscience for AI: An introductory guide to the literature

---

<ol>
<li>Introduction</li>
<li>Motivation: why should we pay attention to the brain for AI?</li>
<li>Overviews: What, broadly speaking, is the brain computing?</li>
<li>The Cerebral Cortex: A Very Tangled Web</li>
<li>The Thalamus: More than just Central Station</li>
<li>The Hippocampus: A Less Tangled Web</li>
<li>Cortico-hippocampal interactions</li>
<li>Reinforcement Learning with the Basal Ganglia and prefrontal cortex</li>
<li>The Telencephalon: Or, How I Learned Concepts in the Cortico-thalamo-basal ganglia-hippocampal system.</li>
<li>The ‘Little Brain’, often forgotten: the Cerebellum</li>
<li>The Cerebello-basal ganglia-thalamo-cortical system</li>
<li>Conclusions</li>

<blockquote>“The brain is arguably still the only example that we have of something that approximates the kind of intelligence we’re trying to build, and so it seems like a good idea to pay some attention to how it works.”</blockquote> 
Matt Botvinick, Director of Neuroscience Research, DeepMind

<em><b>TL;DR</b>: This guide aims to give AI researchers a skeleton-frame introduction to modern systems neuroscience and contextualise specific recent AI research with respect to those systems. It focuses on views of neuroscientific systems that are deemed most likely to be useful for AI research in the near term. Despite efforts to remove personal biases and omissions, some will remain in any concise guide with such a broad scope. Some articles are behind paywalls; Sci-hub exists. 
</em>

General intelligence is ostensibly the central goal of the field of AI. Yet, with a few notable exceptions, few in AI research pay much attention to the only known example of general intelligence: the human brain. Although some early AI took inspiration from neuroscience, the two fields gradually grew more distant while statistical-theoretical and computational constraints caught up with the neuroscientific theory. Today, the time is ripe for an academic rapprochement between the two fields, and it’s happening. But finding good, modern sources for getting up to speed on biological intelligence takes a lot of time; it’s costly even to figure out what areas of neuroscience to prioritise. And when thousands upon thousands of new AI papers come out every year, keeping abreast in both fields is a near impossible challenge. 

To help make the challenge a little less difficult, I present this guided reading list of modern neuroscience literature. It’s aimed at AI researchers (and will also be useful to early-stage computational neuroscience students) who already have the equivalent of a basic undergraduate-level course in systems neuroscience. Its goals are twofold: 
<ol>
  <li>To convince the reader that, although we are still ignorant of many crucial details in systems neuroscience, our knowledge as it stands provides a rational framework to organise our thinking on intelligence, and </li>
  <li>To give the reader a sound, skeleton-frame mental model of our current theories of how general intelligence is implemented by the brain. </li>
</ol>

<b>Importantly, the guide relegates classic literature in favour of recent articles</b>. This was partly motivated by laziness, but it is mostly by design, since most articles present ample introductions to the historical literature. The guide presents an assortment of consensus views and emerging perspectives. The list is also populated by links to recent video lectures by the authors of some of the reviews. In addition to the neuroscience reviews, readers from either neuroscience or AI will be able to build their mental models of intelligence ‘in both directions’ thanks contextualising discussions of a selection of recent AI literature that has clear links to the respective neuroscientific systems.

<h1>Why a <em>guided</em> reading list?</h1>
The scope of this resource has such an extensive breadth and depth that it would be impossible to do a service to the ideas presented by review authors by recapitulating their arguments in an extremely long review or textbook. Therefore the reading list is guided, as opposed to simply being a list of reviews, in order to strike a middle ground between 
<ol type="I">
  <li>permitting readers to benefit from motivating explanations of the review content from people with more time to devote to the field of cognitive, computational & systems neuroscience, and</li>
  <li>maintaining the authority, recency, and accuracy of the content.</li>
</ol>

Although the reading list is guided, readers can begin in any section and read sections in any order with one exception: if the reader would like very quickly to brush up on undergraduate-level neuroscience prerequisites, they should first read Chapter 15 “Neuroscience” of Reinforcement Learning: An Introduction (Sutton and Barto 2018).

Despite my best efforts, the guide omits several important research areas. Although I have sought and received review recommendation beyond my own initial readings, it is impossible to stamp out all idiosyncrasies in the views presented here, especially while keeping the guide moderately concise; the selections and omissions therefore contain personal biases toward a particular view of what topics in neuroscience are important for AI. To highlight and possibly counterbalance these biases, I will do my best briefly to be explicit about where the emphases lie. In order to do that, it will be helpful to introduce Marr’s three level of analysis. Readers familiar with Marr’s levels of analysis should feel free to skip the following interlude. 
<h1>Interlude: What would an explanation of the brain even look like?</h1>
This question keeps neuroscientists of all stripes awake at night. To break the question into more manageable parts, neuroscientists often find it useful to invoke David Marr’s three ‘levels of analysis’ (see list below), which, by analogy to a computer, describe the <b>computational level</b>, which is specified on the <b>algorithmic/representation level</b>, which in turn is implemented on the <b>implementation level</b>. It is important to recognise that these levels have overlapping boundaries due to the curse of reductionism: In order to completely understand a system on one level, you must understand it on the level below. Despite these dependencies, they serve as a useful aid for setting a manageable scope for many neuroscientific questions. Additionally, while the levels help frame questions of neuroscientific description (“What is…?” or “How does…?”), the levels of analysis can also be applied to questions of artificial intelligence design (“How should…?”).




<h1>What this guide focuses on and what it ignores</h1>
We currently do not have a good enough understanding of any single level of analysis in neuroscience to know with certainty what topics are safe to ignore. As such, this guide introduces neuroscience reviews from all three levels but places greater emphasis on the computational and algorithmic/representational levels than on the implementation level. This is not to say that excluded topics won’t be useful for building general intelligence - it just reflects my view of what systems-neuroscientific concepts AI researchers are likely to find useful in the short to medium term. This is consistent with the emphasis placed by Hassabis, who has said for a long time that many approaches to building general intelligence focus on parts of neuroscience that are too high- or low-level to be immediately useful for building intelligence. The guide therefore focuses on: 
<ul>
  <li>The functions that particular brain areas are believed to perform and, where possible, how they are believed to perform them.</li>
  <li>The high-level algorithms the brain is believed to be implementing and what we know about how they are performed</li>
  <li>Relations between the discussed brain parts and systems</li>
  <li>Links from the neuroscience to modern AI algorithms and architectures.</li>
</ul>

The guide does not emphasise:
<ul>
  <li> Electrochemical dynamics of single nerve cells or ion channels</li>
  <li>Mechanisms of synaptic plasticity, long term potentiation or depression</li>
  <li>Neural oscillations</li>
  <li>Dynamics of small scale neural assemblies</li>
  <li>Neuromorphic hardware or its inspirations</li>
  <li>Models of consciousness (even when they are computationally-informed)</li>
  <li>Neuropathology</li>
  <li><u>Detailed</u> anatomy.</li>

A further caveat to make explicit is that there is a mostly unintentional bias toward research from staff associated with DeepMind. I only mildly apologise for this - it just happens that there is an awful lot of AI-relevant neuroscience research emerging from the company, as well as a lot of AI research that is strongly linked to systems neuroscience. That said, it is far from a lone actor in the AI-neuroscience intersection. Just bear this bias in mind throughout. 

<h1>How this guide is structured</h1>

The guide starts with a section that motivates the relevance of neuroscience to AI. 

The subsequent section contains some reviews that give broad overviews of the systems likely to be at play in the brain. Such reviews represent the ‘computational’ level of analysis and aim to give an overview of what systems are likely to act in the brain; this should help contextualise more detailed reviews about particular brain parts and their functions.

The main guide follows, which primarily tackles the algorithmic/representational level of analysis, though other levels are addressed too. I take a mixed approach to divide the literature in a way that makes sense: a combination of divisions by system and by anatomy. It sometimes makes sense to look at a particular part of the brain in isolation, then later look at how particular pairs of these components interact, then finally integrating the component into the systems in which it plays a role. Though a mostly sensible structure, no part of the brain (and certainly no system within it) works in isolation, hence some reviews will demand knowledge only touched on in later sections and in some unavoidable cases, will demand knowledge that is not included anywhere in the reading list; this is to be expected when only a small subset of the literature can be selected for inclusion. 

For each paper, I provide a small, contextualising introduction. After each system has been introduced, I discuss a few of the specific, recent AI architectures that I’m aware of that draw on or inform the neuroscience. 

Not everyone will want (or need) to read every paper. In order to help readers identify which papers they’d like to prioritise, each selected review has a pie-chart that estimates the amount that it focuses on a particular level of analysis. A review that focuses equally on all levels of analysis for both AI and neuroscience would look like this:


![Template pie chart](/images/sysneuroai_images/template.png)


Before the real content, a practical note: the depressing closedness of biology literature might come as a surprise to those only familiar with the quantitative sciences. Biomedicine has long been in the grips of a publishing house kabal, though there are encouraging signs for the open science campaign. Until the field improves its publishing norms, you’ll probably need an institutional subscription. I’m not making a public recommendation for or against its use here, but be aware that Sci-hub exists. Also be aware that it may break laws in your country, even though your country might want it to be legal. 

Finally, I emphasise once again that this guided reading list cannot possibly include everything, and the vast majority of important literature had to be excluded. The reading list aims therefore only to serve as an exceedingly general overview, a springboard from which to jump deeper into the areas of neuroscience that each reader finds most exciting and relevant to their respective interests. So don’t be afraid to deviate from the list if you find more specialised reviews on topics that interest you! 

