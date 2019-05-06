---

layout: post

title: Motivation&#58; why should we pay attention to the brain for AI? 

---

_This post is part of a series "Systems Neuroscience for AI: An Introductory Guide to the Literature"._

#### Guide contents
* [Introduction]({{ site.baseurl }}/Systems_Neuroscience_for_AI_Introduction/) 
* [Motivation: why should we pay attention to the brain for AI?]({{ site.baseurl }}/Systems_Neuroscience_for_AI_Motivation/) (This page)
* [Overviews: What, broadly speaking, is the brain computing?]({{ site.baseurl }}/Systems_Neuroscience_for_AI_Overviews/)
* [The Cerebral Cortex: A Very Tangled Web]({{ site.baseurl }}/Systems_Neuroscience_for_AI_Cerebral_Cortex/)
* [The Thalamus: More than just Central Station]({{ site.baseurl }}/Systems_Neuroscience_for_AI_Thalamus/)
* [The Hippocampus: A Less Tangled Web]({{ site.baseurl }}/Systems_Neuroscience_for_AI_Hippocampus/)
* [Cortico-hippocampal interactions]({{ site.baseurl }}/Systems_Neuroscience_for_AI_Cortico-hippocampal_interactions/)
* [Reinforcement Learning with the Basal Ganglia and prefrontal cortex]({{ site.baseurl }}/Systems_Neuroscience_for_AI_RL_with_BG_and_PFC/)
* [The Forebrain: Or, How I Learned Concepts in the Cortico-thalamo-basal ganglia-hippocampal system]({{ site.baseurl }}/Systems_Neuroscience_for_AI_Forebrain/)
* [The ‘Little Brain’, often forgotten: the Cerebellum]({{ site.baseurl }}/Systems_Neuroscience_for_AI_Cerebellum/)
* [The Cerebello-basal ganglia-thalamo-cortical system]({{ site.baseurl }}/Systems_Neuroscience_for_AI_CB_BG_Th_Ctx/)
* [Conclusions]({{ site.baseurl }}/Systems_Neuroscience_for_AI_Conclusions/)
<br>
<p markdown='1' style="text-align:center">---</p>
<br>

It is common to hear in some quarters that, nowadays, an alleged link between neuroscience and artificial intelligence is spurious. Informed accounts such as Hassabis et al. (2017) and this excellent post by Surya Ganguli at Stanford (both linked below) show that the link between neuroscience and artificial intelligence has always - and continues - to run deep. 

<h3 markdown='1' style="color:#515A5A">
[Neuroscience-Inspired Artificial Intelligence](https://doi.org/10.1016/j.neuron.2017.06.011)
</h3>

<p markdown='1' style="color:#515A5A">
<img align="right" width="250" height="235" src="../images/sysneuroai_images/Hassabis2017.png">
Neuron. Volume 95, Issue 2, p245-258, 19 July 2017<br>
Demis Hassabis, Dharshan Kumaran, Christopher Summerfield, Matthew Botvinick<br>
https://doi.org/10.1016/j.neuron.2017.06.011 <br>

<br>
**Abstract**<br>
_The fields of neuroscience and artificial intelligence (AI) have a long and intertwined history. In more recent times, however, communication and collaboration between the two fields has become less commonplace. In this article, we argue that better understanding biological brains could play a vital role in building intelligent machines. We survey historical interactions between the AI and neuroscience fields and emphasize current advances in AI that have been inspired by the study of neural computation in humans and other animals. We conclude by highlighting shared themes that may be key for advancing future research in both fields._<br>
<br>

Associated talks: https://www.youtube.com/watch?v=Qgd3OK5DZWI
</p>


<h3 markdown='1' style="color:#515A5A">
[The intertwined quest for understanding biological intelligence and creating artificial intelligence](https://hai.stanford.edu/news/intertwined-quest-understanding-biological-intelligence-and-creating-artificial-intelligence)
<img align="right" width="250" height="235" src="../images/sysneuroai_images/Gangulipost.png">

</h3>
<p markdown='1' style="color:#515A5A">
Surya Ganguli, 2018
<br>
<br>
_No abstract available_
<br>
<br>
<br>
<br>
<br>
<br>
</p>

<br>
<p markdown='1' style="text-align:center">---</p>
<br>
Even though we do not currently have a complete functional picture of intelligence, one benefit of studying the brain is to enable a top-down attempt to break intelligence into component functions. First, we might study what we think are the prerequisite functions (“start-up software”) needed for general intelligence. We can then examine functions of general intelligence that build on the start-up software, such as world-model-building, understanding causality, or compositionality. This top-down approach is supported in the following review by Lake et al. (2015). Readers are particularly encouraged to read the the Behavioral and Brain Sciences version of the article (as opposed to the version on Arxiv) since it includes lively responses from other prominent voices in the field that, while in agreement, tend to counterbalance Lake et al. with arguments for the bottom-up approach. Of particular mention for [our purposes]({{ site.baseurl }}/Systems_Neuroscience_for_AI_Introduction/) are the responses by:
* Botvinick et al.: Building machines that learn and think for themselves
* Marblestone et al.: Understand the cogs to understand cognition
* Dileep George: What can the brain teach us about building artificial intelligence?


<h3 markdown='1' style="color:#515A5A">[Building machines that learn and think like people](https://doi.org/10.1017/S0140525X16001837)</h3>
<p markdown='1' style="color:#515A5A">
Behavioral and Brain Sciences. Volume 40 2017 , e253<br>
Brenden M. Lake, Tomer D. Ullman, Joshua B. Tenenbaum and Samuel J. Gershman<br>
https://doi.org/10.1017/S0140525X16001837<br>

<br>
**Abstract**<br>
<img align="right" width="250" height="235" src="../images/sysneuroai_images/lake.png">
_Recent progress in artificial intelligence has renewed interest in building systems that learn and think like people. Many advances have come from using deep neural networks trained end-to-end in tasks such as object recognition, video games, and board games, achieving performance that equals or even beats that of humans in some respects. Despite their biological inspiration and performance achievements, these systems differ from human intelligence in crucial ways. We review progress in cognitive science suggesting that truly human-like learning and thinking machines will have to reach beyond current engineering trends in both what they learn and how they learn it. Specifically, we argue that these machines should (1) build causal models of the world that support explanation and understanding, rather than merely solving pattern recognition problems; (2) ground learning in intuitive theories of physics and psychology to support and enrich the knowledge that is learned; and (3) harness compositionality and learning-to-learn to rapidly acquire and generalize knowledge to new tasks and situations. We suggest concrete challenges and promising routes toward these goals that can combine the strengths of recent neural network advances with more structured cognitive models._<br>
<br>
<img align="right" src="../images/sysneuroai_images/lake_pic.png"><br>
Associated talks: https://www.youtube.com/watch?v=7ROelYvo8f0 
</p>

<p markdown='1' style="text-align:right">_Next post_: [Overviews: What, broadly speaking, is the brain computing?]({{ site.baseurl }}/Systems_Neuroscience_for_AI_Overviews/)</p>
