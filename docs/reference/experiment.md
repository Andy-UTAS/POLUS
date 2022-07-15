# The experimental method

![](experiment/header.jpg){: .center}

The purpose of this page is not to provide a discourse on the scientific method or best-practice experimental design. Rather, a suite of support and reference materials for skills and techniques which are key to applying the scientific method in the physics context are provided.

---

## Uncertainties

Any result or measurement which is presented numerically should always be accompanied by a numerical estimate of its accuracy or reliability.  Values will normally be presented in the form $b \pm \Delta b$. The reader of the report will know that they can expect the true value of the quantity to be within $\Delta b$ of $b$ with some high degree of probability.

In physics it is common to refer to the uncertainties as the _errors_, and the value of $\Delta b$ as the _errorbar_ (named for the way the quantity appears on a graph), but this does *not* imply that the experimenter made a blunder or mistake! Every experiment carries errors with it and no quantity can be measured perfectly. The goals of experimental physics are to minimise errors as much as possible, and to understand the circumstances that produce the remaining errors.

By convention, the values of $\Delta b$ are referred to the standard deviation of a normal probability distribution because this allows them to be easily manipulated and combined according to the rules below. Under this convention, the uncertainty estimate $\Delta b$ is often referred to by the Greek letter $\sigma$ (sigma). Because of the shape of the normal distribution, the true value of $b$ is only expected to fall within the range $b \pm \sigma$ about 68\% of the time. $b$ will be found within 2$\sigma$ of the true value about 95\% of the time, and within 3$\sigma$ over 99.7\% of the time (keep in mind that real errors are rarely perfectly normally distributed, and real results seem to fall more than 3$\sigma$ away from their expectation values with discouragingly high frequency).

Standard rules exist for the estimation of $\Delta b$.  They vary according to the circumstances of the measurement, and are summarised below. For more detailed treatments, refer to the textbooks on experimental errors and on treatment of statistical data [^1][^2][^3]

### Estimating uncertainty

#### A single, direct measurement

A direct estimate of $\Delta b$ must be made. This will take account the method used and the difficulty encountered in the observation.  For example, the width of the pointer on a dial meter, parallax between the pointed and the printed scale, imprecision in the markings on a ruler, or the manufacturer's claims about the accuracy of a voltmeter. This may also include a component to allow for the judgment (good, bad, or otherwise) of the observer. Note that there is a strong human tendency at the subconscious level to underestimate the uncertainties associated with any particular measurement.

#### A derived quantity

When a quantity is determined by combining measurements of a number of directly measured quantities, the techniques of propagation of error must be employed. Let the desired result $X$ be some function of a set of measurements, $a, b, c, ...$, of different quantities. The errors in each measurement, $\Delta a$, $\Delta b$, ..., are assumed known. Then

\[
\left( \Delta X \right) ^2 = \left( \frac{\partial X}{\partial a} \Delta a \right) ^2 + \left( \frac{\partial X}{\partial b} \Delta b \right) ^2 + \left( \frac{\partial X}{\partial c} \Delta c \right) ^2 \dots
\]

The symbol $\partial$ refers to a partial derivative; ask your demonstrator for assistance if you forget how these work.  The general rule for propagation of error can be reduced to some simple arithmetic forms for a number of commonly encountered cases, for example:

##### Error in a sum or difference

!!! info "$X = a \pm b$"

    \[
    \Delta X = \sqrt{\left( \Delta a \right) ^2 + \left( \Delta b \right) ^2}
    \]

Note that the error $\Delta X$ is the same whether $a$ and $b$ are added or subtracted. However the {\it fractional}  error, $\frac{\Delta X}{X}$, will be very different. In particular, if $a$ and $b$ are nearly equal, the fractional  error in their difference may be enormous. The relation for $\Delta X$ can obviously be extended to the sum or  difference of any number of quantities. The key feature is that the uncertainty $\Delta X$ is never less than the  largest uncertainty on any of the components of $X$.

##### Error in a product or quotient

!!! info "$X = a \times b$ or $X = a/b$"

    \[
    \frac{\Delta X}{X} = \sqrt{\left( \frac{\Delta a}{a}\right) ^2 + \left( \frac{\Delta b}{b}\right) ^2}
    \]

Again this can be extended to the products and/or quotients of any number of quantities. This is very similar-looking to the relation for sums and differences, but in this case it is the {\it fractional} errors that are added in quadrature to derive the final uncertainty. The key feature here is that the fractional uncertainty on $\Delta X$ is never less than the largest fractional uncertainty among the components of $X$.

##### Errors in quantities raised to powers

!!! info "$X = a^n$"

    \[
    \frac{\Delta X}{X} = n \left( \frac{\Delta a}{a}\right)
    \]

This can be calculated from the basic rule using partial derivatives, but it is a particularly useful relation to have in mind when analysing your data. For example, if the fractional error on a measured velocity is 5\%, then the fractional error on the associated kinetic energy ($\frac{1}{2}mv^2$) is 10\%, because the velocity is squared in the energy calculation.

##### Errors in evaluations of functions

If $X = f(a)$, then the basic rule for propagation of error from the sum of squares of the partial derivative of X with respect to a must be followed.

!!! example "Example: $X = a \sin(b)$"
    According to the partial derivative rule, $\left(\Delta X\right)^2$ = $\left( \Delta a \sin b\right)^2 + \left( a\Delta b \cos b\right)^2$.  This can result in some apparently strange behaviour: in this example, $\Delta X$ is insensitive to errors in $a$ when $b \approx 0$ or $\approx \pi$, but will be insensitive to errors in $b$ when $b \approx \pm \frac{\pi}{2}$ or $a \approx 0$.

#### A quantity measured many times

A reasonable way of improving the precision of a measurement is to make a number of independent estimates of the quantity if possible.  The best estimate of the true value of the quantity is then the mean of the individual results ($\bar{b}$), and we can try to disentangle two different contributions to the total uncertainty: a statistical component arising from random, uncorrelated measurement errors, and a systematic component that affects all of the measurements (for example, an incorrectly calibrated thermometer, or something that depends on a consistent delay in your reaction time). The random component can be reduced by repeat measurements, but the systematic component cannot-- so note that if the systematic component is large it is futile to attempt to reduce the total uncertainty by repeating the measurements multiple times.

In order to find the random component of the uncertainty in a measurement, we need to calculate the standard deviation of the sample, $s$.  The quantity $s$ represents the degree of scatter in the data, and if the uncertainties are truly random then $s$ should be normally distributed.  The relationship between the error in a single measurement and the error in the mean of $N$ independent measurements is simply given by $\Delta \bar{b}$ = $\frac{s}{\sqrt{N}}$.  Note that in the ideal case, the uncertainty on each measurement $\Delta b$ is the same, and $s$ = $\Delta b$.

#### Significance of the result

The number of significant figures in the result should be consistent with the stated accuracy. For example,
$ 3.9 \pm 0.0798234$ and $3.93765 \pm0.08$ are both incorrect, while $3.94 \pm 0.08$ would be acceptable. Since the standard error is only an estimate of where you believe the 68\% probability limits lie, experimenters sometimes drop the last digit of precision if they feel the rounded off value more accurately represents the state of knowledge about the measured quantity. Always bear in mind that systematic errors often dominate the total uncertainty, and these may be both large and difficult to quantify.

#### Least-squares fit to a straight line

Given a set of points  ($x_i$, $y_i$), we often need to find  $m$, $b$ such that the line  $y = mx + b$  gives the best straight line fit to the data in the "least squares" sense.  That is, the required line is such that the sum of the squares of the discrepancies of each point from the closest point on the line is a minimum.

This is best done by using a computer (or some graphics calculators). Statistics programs will estimate the most likely slope $m$ and intercept $b$ from the data supplied.  They will also estimate the standard errors $\sigma_m$  and  $\sigma_b$ of $m$ and $b$ respectively.  With these four numbers, one can say that, if there really is a linear relation between  x  and  y , then the slope of that relation has a 68\% chance of lying within  $\pm \sigma_m$ of  $m$  and the intercept has a 68\% chance of lying within  $\pm \sigma_b$ of $b$.  The theory underlying the method, and the procedure for computing linear least-squares fits by hand is given in the texts referred to in the Introduction above, and many other places.

### Warnings

* [Measuring a quantity many times](#a-quantity-measured-many-times) and [performing a least-squares fit](#least-squares-fit-to-a-straight-line) will assist you in estimating the random uncertainty due to statistical effects, but will not help you in determining possible systematic errors. This will require some common sense, some physical reasoning, and some experience.  You will have to judge the systematic errors as best you can, and then combine them appropriately with your statistical uncertainty estimates.
* Never apply linear regression calculations to a set of figures unless you have plotted a graph and confirmed that the results are consistent with a linear relation!  A common occurrence is to have something go wrong in the experiment which transforms the points into a gentle curve. The experimenter may plug the data into a line-fitting routine, which always comes up with a result. If the curve is small, then the reported standard error in the slope will be small, and there may be no indication that the result is in fact meaningless. {\it Always} plot a graph of your data. Then, if the results are consistent with a straight line, use a least-squares fitting routine.  In some of the experiments in \unitname , the results take the form of a power law, which can  easily be transformed into a straight line suitable for fitting.

## Communication

### Logbooks

It is likely that in any study that you have undertaken which involves project work that you have been encouraged in to keep a log book. In many instances, these can often appear as a collection of scribbles: a date, a few measurements, maybe a table of raw data, but rarely is there a formal structure or in reality, anything that will remain useful. This is unfortunate, as in practice, logbooks are a cornerstone of rigorous and efficient work. The realisation that this is the case typically comes after some extended period of working on a complex project, where it is simply too difficult to recall minor technical details or re-tread a train of thought, which leaves you wondering "what on Earth was I thinking/doing?". It is in this context the we seek to embed the practice of careful, reasoned, and useful log-book keeping.

#### The general idea

Rather than thinking of a log as a cache of details pertinent to a given project, one should try to think of an experimental log as capturing your background research, experimental plan(s), methods and techniques, experimental data, data analysis, presentation of results, and conclusions but in a less formal and highly-educative manner. As much as you are writing to convince someone reading the log, you can use it to reason with yourself, in a way which allows the document to act as a conduit to place you back into your state of mind at the time of writing.  It can often be difficult to appreciate the need for such diligent record keeping in the abstract, but this will have to be a leap of faith. Think of it like brushing your teeth: something the you are essentially forced to do, and at a later stage you a thankful that you have a habit that really improves your life.

#### The log mantra

A log should not be constructed in a prescriptive way, although there will be many common elements incorporated in well-maintained logs. In the specific case of an experimental log for a single project, you will have some materials to point you in the direction of what you are to investigate. From here, you can write something along the lines of a background section. This would contain a broad summary what you expect that you are going to do. What might be the aim of the experiment, and what are the relevant phenomenon. It should be emphasised that we are trying to move away from right and wrong, and rather discuss things that might be important. For example, if one is going to be performing an experiment involving diffraction, it may be worthwhile to explain what underpins the phenomenon: what exactly is the origin of diffraction? What are the implications of diffraction occurring, and how might these manifest in the experiment. The scope and explicit content to cover will be dependent on the experiment, but you want to provide yourself and the reader a comprehensive discussion of the phenomenon under investigation.

With the (back)ground work laid, one basically enters the real-time cycle of writing a scientific method stream of consciousness:

* What do I want to do?
* Why do I want to do it?
* How am I going to do it?
* Why am I going to do it that way?
* What did I see?
* Why did I see it?
* What are the implications of seeing it?

Once again, the exact flavour of this will depend on the task at hand, but basically you want to be explaining what you are doing and critically, why you are doing it. The markers of a successful log often take the form:

* I want to do this, and this is what I would expect
* I see this thing completely at odds to that which I would expect. I wonder why that might be
* I just had an idea, I am going to test it by doing _____
* Okay, the results from that make sense, I know what is going on
* (proceeds to explain what is going on and implications)

You may remark that this is just like the process one would follow for problem solving or troubleshooting, and you would be correct! These processes are essentially identical, with the spice in the mix for scientific experiments, you might know what you are expecting to observe, so it can be tricky to determine if what you observe is that what you think to be – a void largely filled by theory and simulations but in all cases, careful experimentation trumps all!

#### Hints

At first, writing a log is not easy as it requires that one plan ahead, and then often demands that one slow down and parse what the world is offering up. But to be clear: with the exception of the background material, a log is to be written in real time, and consequently mistakes will be made. Mistakes are to be embraced: you can explain what was done wrong, or what was required to correct your understanding.

<p style="text-align:center; border:3px; border-style:solid; border-color:#EF5653; padding: 1em;">To emphasise: to purpose of this document is to document both what you did, but also what you learned. </p>

The presentation of a log is not the most important thing, but it should not be overlooked. It should be well laid out, easy to read, and the thread of the experimental journey should be easily followed. It is simply not possible to construct on scientific report style log, as a formal report has clearly defined sections, whereas a log exists in the moment, but the log should contain essentially all of the information that would be present in a formal report.


One of the purposes of a log is to provide a vehicle for the development of ideas, so if something strikes you, embrace it. Do you have an idea for something that could be done better? Write it down. Unsure of one particular aspect of a theory? Write it down. Can you think of a complementary way to measure the same or similar phenomenon? Write it down. Insightful comments and/or discussions which arise from a comprehensive understanding of a given topic and command over the relevant adjacent materials are the true currency of a log, and science more broadly.  

Logs are individual. Despite that physics rightly is undertaken in collaboration with others, each person should be maintaining an individual log. It is strongly recommended that logbooks be produced digitally, ideally prepared within a [Jupyter notebook](https://utasphys.cloud.edu.au/POLUS/reference/computation/#using-python). For part III labs, this in mandatory, and in Part II labs it is encouraged, but not required.

##### Model log book

An example log book is provided below as a guide for the kind of logbook that might be produced. Hopefully the text above has convinced you that there is no single _right_ way to create a log, so you should do what works for you, whilst building on the principles which undergird rigorous scientific investigation.

<figure markdown>
  [<i class="fas fa-solid fa-book fa-5x"></i>](https://github.com/Andy-UTAS/POLUS/blob/master/docs/reference/experiment/model_log/examplelog.ipynb){ .md-button .md-button--primary class="text-center" style="margin-left: 0%"}
  <figcaption>An example logbook prepared as a jupyter notebook</figcaption>
</figure>

<figure markdown>
<a href = 'https://jove2021.cloud.edu.au/user/andy/notebooks/POLUS/docs/reference/experiment/model_log/examplelog.ipynb'> <i class="fab fa-python fa-5x"></i> </a>
    <figcaption>An executable version of the example notebook above. This is one of the major advantages of using jupyter notebooks!</a>
    </figcaption>
</figure>

Additional resources to aid with the production of jupyter notebooks will be forthcoming, but in the meantime, please consult with your demonstrator should you have any questions or problems.

#### Assessment

Assessment of logs will be conducted in the same way as any other report you have done in the past, in that physical insight and good experimental technique will be rewarded.

In addition, a mandatory "reflections" section provides a pathway to improving one's logs and log-keeping technique, with the comments from the previous experimental logs to be addressed, with marks being awarded for engagement with the "reflection" process

### Reports

The purpose of a report is to concisely communicate your findings to an audience in a structured document; in science, reports are often flavoured as commissioned pieces of research (for example, a study of the feasibility of _microgrids for remote communities_) or academic research (for example, journal articles).

#### Preparing a report
Reports must be set out in the nature of a scientific paper with sections outlining the theory, experimental procedure, results and analysis, and conclusions. Each of those sections should carry the appropriate heading. All reports must have a brief abstract at the beginning and a list of references at the end. The crucial questions to ask yourself on completing a first draft of your report are

1. Could someone else read this, and duplicate the experiment to reproduce my results?
2. If someone else had written this and given it to me to read, would I believe it?

If unfamiliar with this structure, it is advisable to have a have a look at existing reports, for example, articles which appear in any of the [_Physical Review_ publications](https://journals.aps.org/) are likely to be worth emulating. Note that some of the more general-coverage publications such as _New Scientist_ or _Scientific American_ employ their own styles which are aimed at a general audience and should not be taken as examples of a research report (but may be emulated in the case of a [popular-science pitch](#popular-science-pitch)). The exact layout of a report will depend on the nature of the experiment, but a typical paper would have the following sections:

1. [Abstract](#Abstract)
2. [Introduction](#Introduction)
3. [Theory](#Theory)
4. [Experimental procedure](#experimental-procedure)
5. [Results and analysis](#results-and-analysis)
6. [Conclusion](#Conclusion)
7. [References](#References)

##### Abstract

The purpose of the abstract is to summarise the subject and findings of your work in one short paragraph. Typically, scientists will want to check several journals in a few minutes to see if any contain reports of interest to them in their field. They will check the contents page and then read the abstracts of those reports that may be of interest. Increasingly, scientists subscribe to services that email a list of abstracts in their field, a dozen or more per day. The abstract is your only chance of catching the attention of the people you want to read your report. If your abstract is not concise and to the point, then no one will read the report. It should contain a few words (normally less than about 50) outlining what has been done, what is new or interesting about the method you have used, the results and conclusions. It should include numerical results obtained where this was an aim of the experiment, and their standard error. If the results are significantly different from accepted values, this should be commented on. You are strongly advised to look at some examples in journals in the library or online (often, these are best found on [https://journals.aps.org/prl/](journal landing pages)), or flatter your demonstrator by asking to see one they’ve written.

##### Introduction

If the abstract has caught the attention of a reader, their next step will be to read the introduction. The introduction should not just repeat the contents of the abstract, but should assume the abstract has been read, and expand on it. In particular, it should give the object of the experiment and a general outline of the theory and method. It will probably include an outline of previous related measurements and attempt to show how the experiment contributes to the store of information on the subject. Appropriate comparisons may be made here with alternative methods, and the historical significance of the experiment may be commented on if this is relevant.

##### Theory

The theory underlying the experiment should be given. Where the script for the experiment describes the mathematics in detail, there is a conflict between the requirements of a bona fide original research report in which relevant theory is often skimmed over and a result given with citation to the appropriate works in the literature, and the requirements of a marked report in which your marker is looking for evidence that you have worked through the maths yourself and understood what you were doing. From the marking point of view, there is no point in copying out a slab of theory verbatim from the experiment notes. In this case you should summarise the notes in your own words, in a manner that makes it clear that you understand the process. In any case, you should refer to this handbook, giving page numbers and equation numbers where relevant, and the major steps in the theory should be written up. Where the script asks students to prove certain statements or equations, this should be done and described in the report. If the theory is descriptive and short, it may be appropriate to include it in the introduction.

##### Experimental procedure

Describe the procedure and apparatus used, with diagrams, to the extent that they are relevant to your results. Do not include detailed descriptions of equipment which cannot reasonably have affected the outcome of the experiment. Discuss difficulties encountered and methods used to overcome them.

##### Results and analysis

Final results should either be tabulated or displayed as graphs, as appropriate. If you use graphs, then the numerical results should be included in an appendix for marking purposes, referred to in the text by table or figure number. Each table and graph or diagram should have a table or figure number and brief caption describing it. Methods of analysis should be given but detailed calculations and measurements leading up to these results are not normally included in a scientific paper. It should go without saying that graphs must be clearly labelled with a legend, with clear distinction between data points and any theoretical or numerical curves or fits, and clear axis labels. Any information necessary to interpret the graph should be included in a brief caption.

Error limits should be given for all numerical results and for all intermediate quantities which make a significant contribution to the accuracy of the final result. This is especially important in the abstract and the final conclusions. The error should always be quoted to the same power of ten as the result itself, and to the same significant figure, e.g. $1.67 \times 10^{-19} \pm 2 \times 10^{-21}$ and $(1.67 \pm 0.0234) \times 10^{-19}$ should be replaced by $(1.67 \pm 0.02) \times 10^{-19}$.

Error bars should be attached to data points on graphs unless they are too small, in which case a comment should be attached to that effect. The method of calculation of errors should be indicated in the text. You should also discuss possible systematic errors, and if you can, possible ways of increasing the precision of the measurements. The goal of an experiment is to answer a question (e.g., is this theory true or false?). Without a clear discussion of the experimental uncertainties associated with a given numerical value, it is impossible to safely assign any credence to the value, or use it to answer the question.

There is often a conflict between the way a scientist would lay out his/her report in a genuine research situation, and the requirements of a marker reading a student report in order to decide whether the student has understood the work and used appropriate experimental techniques, in order to attach a mark. If the scientist is demonstrating a relation between two variables, the result will be expressed in graphical form, or as an equation if it is possible to fit a relation. The reader will not be interested in the fine details of the calculation, but will assume that they have been done with care, and will assume that the error calculations have been done correctly. Hence calculations will normally be omitted from a research report unless there is something interesting or unusual to which the author wishes to draw attention. On the other hand, your demonstrator has to mark your report and will want to both see the raw data and to know how you did the calculations. He will also want a readable report – not one that is broken up by slabs of arithmetic. How you handle this problem will depend on the experiment and the nature of your calculations, but unless the calculations are very short, they should be put in an appendix.

Every table should have a ‘table’ number, and every graph, diagram or photograph should be given a ‘figure’ number, together with a short title or description. (If a reader has read the abstract and introduction, but is still not sure whether he/she wants to read the complete report, the next step will be to glance at the graphs and diagrams. If they have no titles, they will be meaningless.) Every reference to a table or figure in the text should be through the appropriate number.

##### Conclusion

This summarises briefly what has been achieved and gives numerical results. It may include recommendations for relevant new experiments or alterations to the present one.

##### References

These should be given in detail, i.e., author, title of book or journal, page and chapter or volume number, year of publication, publisher and place of publication of a book. It is important that references are identified at the relevant point in the text. It is not sufficient to quote the book in the list of references at the end of the report without stating explicitly where it has been used. It is also important the references be accurately cited, and for a full description of citation style, refer to the [style guide for Physical Review](experiment/styleguide-pr.pdf).

#### General comments

Finally, some general comments:
* Organise your report before you start writing it. Jot down the above headings on a scrap sheet of paper and list under each heading the topics that you need to discuss or describe. Decide on the best order for the topics under each heading. Decide which items are best relegated to appendices. Your aim is to have a smooth flow of ideas and concepts from the introduction to the conclusion. Anything that breaks that flow should probably be merely mentioned in the text and relegated to an appendix.
* Be brief. Having decided what you want to say, say it clearly and concisely. Long waffly sentences and paragraphs mean your report won’t be read. A research report will normally assume that readers are competent physicists, and if the paper is in a specialised field, then the readers will already be competent in that field. In your case, we ask that you assume your report will be read by fellow students with a similar background to your own. It is up to you to explain what you did in terms that will be understood by your peers.

#### Additional resources
The article [_Scientific Writing Made Easy: A Step-by-Step Guide to Undergraduate Writing in the Biological Sciences_](https://esajournals.onlinelibrary.wiley.com/doi/full/10.1002/bes2.1258) which appeared in the [_Bulletin of the Ecological Society of America_](https://esajournals.onlinelibrary.wiley.com/journal/23276096) is a useful resource, albeit in the context of biological sciences. It can be accessed directly from the publisher, or downloaded [here](experiment/Bulletin Ecologic Soc America - 2016 - Turbek - Scientific Writing Made Easy A Step‐by‐Step Guide to Undergraduate Writing.pdf)

### Popular-science pitch

Scientific communication is difficult, and perhaps increasingly so with incessant demand for ever-smaller chunks of communicable content. However, the worst reaction to this would be to "pull the pin" and say that it can't be done. There are excellent examples of people/teams of people who create and curate highly complex and nuanced content in broadly understandable ways, and increasingly this is a viable pathway for education. It should therefore come as no surprise that this is something that you should practice!

You will select one experiment, and produce a `popular-science pitch`. This is not a pitch in the sense of stating what you want to do, but rather a pitch to others for why they should care about your work. Consequently, the content might be an interesting result from part of the work, an interesting aspect of the apparatus, or simply the context of the work, it is totally up to you. The task is deliberately broad, but the `pitch` should satisfy the following criteria:
* less than one page
* suitable to be distributed to a non-scientist

#### Example pitch

Below one can find an example of a popular science pitch for an extremely esoteric experiment: [Pound–Rebka experiment](https://en.wikipedia.org/wiki/Pound%E2%80%93Rebka_experiment). By design, this is a rigorous, technical experiment which has had the detailed barnacles stripped off, leaving just the bare physics concepts to be communicated.

<figure markdown>
[<i class="fas fa-solid fa-file-pdf fa-5x"></i>](experiment/Pop-science example.pdf){ .md-button .md-button--primary class="text-center" style="margin-left: 0%"}
<figcaption>Example pitch</figcaption>
</figure>

Moreover, countless examples of popular-science abound, from dedicated science platforms to news websites to social media, and content runs the gamut from glorious to drivel - and vaguely correlated with the listed sources. For near-guaranteed quality content, try [Scientific American](https://www.scientificamerican.com/).

### Presentations

On of the most important - and often overlooked - skills in science is the ability to communicate complex results and ideas succinctly. It is therefore of critical importance that this skill is developed and practiced.

_Presentation resources coming soon_

[^1]: G. L. Squires, _[Practical physics](https://archive.org/details/practicalphysics00squi)_, (Cambridge university press, Cambridge, 2001).
[^2]: J. R. Taylor, _[An Introduction to Error Analysis: The Study of Uncertainties in Physical Measurements](https://archive.org/details/introductiontoer00tayl)_, (University Science Books, Melville, 1997).
[^3]: P. R. Bevington and D. K. Robinson, _[Data Reduction and Error Analysis in the Physical Sciences](https://archive.org/details/datareductionerr0000bevi)_, (McGraw-Hill, Inc., New York, 1992).

--8<-- "includes/abbreviations.md"
