# The idea
Read papers in three passes, each accomplishing specific goals and builds upon the previous pass. 
Do this instead of reading all the way through from the beginning in one go and getting lost in all 
the details.

# First pass
Goal: get a bird's-eye view of the paper. With this you can decide if you need to do more passes, 
read the references, etc.
1. Title, abstract, and introduction
2. Read the section and sub-section headings, what are the highlights of the paper
3. Glance at mathematical content to determine the underlying theoretical foundations (?)
4. Read the conclusions, are they sane
5. Glance over references, ticking off the ones you've already read.

From this you should be able to answer the 5 C's
1. Category - What type of paper? Measurement, analysis of the existing system, description of research
 prototype? TODO: what are these?
2. Context - Which other papers is this one related to, which theoretical bases were used to analyze 
the problem? AKA what else do you need to know
 in order to understand this paper.
3. Correctness - do the assumptions appear to be valid
4. Contributions - what are the paper's main contributions?
5. Clarity - is the paper well written?

When writing a paper, expect that most reviewers/readers will only make one pass over it, so ensure 
the abstract and section/sub-section headings are useful.

# Second pass
Read paper with more care but still ignore details (lots of math/equations, proofs, etc.). Make notes 
of terms you don't understand or questions you would want to ask the author(s).

1. Look carefully at figures/diagrams/etc. Do graphs have axes labeled properly, are results shown with
 error bars so that conclusions are statistically significant TODO: what are error bars?

2. make not of references that you haven't read

Should take ~1h for an experienced reader. Should be able to summarize main points of the paper with
supporting evidence to another person. From here decide to: (a) stop now, hope you don't need to understand
this paper for your work, (b) keep reading the paper later, probably after reading some of the references
that you haven't read before, or (c) keep reading right away.

# Third pass
The goal is to attempt to virtually re-implement the paper; that is, making the same assumption as 
the author, attempt to re-create the work. TODO: err, what? redo the research? write programs to
run the proofs?
Try to identify and challenge all the assumptions in the paper, and think about how you would present
ideas yourself. At the end of the third pass, you should be able to reconstruct the structure of the
paper from memory, as well as identify + explain it's strong and weak points. These may include implicit
assumptions, missing citations to relevant work, and potential issues with experimental or analytical
techniques.
The third pass can take multiple hours even for experienced readers.

# Doing a literature survey
This is also known as a literature review. A [search](https://www.quora.com/What-is-a-literature-survey-in-any-project-report) returns that it is a study 
of existing material on the same (or similar) topic of the paper you're reviewing:
1. Existing theories about the topic which are accepted universally.
2. Books written on the topic, both generic and specific.
3. Research done in the field usually in the order of oldest to latest.
4. Challenges being faced and ongoing work, if available.

First, use an academic search engine to find 5 recent highly-cited papers in the area. Do the first pass
on each of these papers and read their related works/references sections. If you're lucky you'll find
a recent survey paper. If you find the survey read it and you're done. 
Otherwise, find shared citations/repeated author names in the references. Download other papers from 
these authors and set them aside to read later. Make note of where the papers were published/presented.
Next, go to the conference/publication websites and look for high-quality recent work, add relevant
papers to the ones you set aside earlier. Make two passes through all the papers. Look for citations
and references to papers you've missed.

# Related work
If you are reading a paper for a literature review you should also read Timothy Roscoe’s paper on 
[“Writing reviews for systems conferences"](http://people.inf.ethz.ch/troscoe/pubs/review-writing)
If you are planning on writing a technical paper you should refer to [Henning Schulzrinne’s comprehensive  web  site](http://www.cs.columbia.edu/∼hgs/etc/writing-style.htm) and [[George Whitesides’s excellent overview of the process](http://www.ee.ucr.edu/∼rlake/Whitesides_writing_res_paper.pdf)

See also:
- S.Peyton Jones, [“Research Skills”](http://research.microsoft.com/en-us/um/people/simonpj/papers/giving-a-talk/giving-a-talk.htm)
- I.H. McLean, [“Literature Review Matrix”](http://psychologyinc.blogspot.com)