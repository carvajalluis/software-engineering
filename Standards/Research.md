[[_TOC_]]

# How to Research?
We can define research into two broad categories:

1. Shallow/Light research
2. In-Depth research

# Shallow/Light research
This means, that you are already aware of the topic, and searching more just to make sure if you could find something new, which can help you improve the existing functionality and improve your understanding of the topic. This shallow research is normally done when you are aware of the topic but want to understand it better, such that it helps you implement it more robustly.
# In-Depth research
Is, researching any topic which is generally new and you want to get an in-depth understanding of all the aspects of it. With a better understanding, you can find many options which could be more specific to your use case. Researching some topics in depth is trying to see all the real-life implementations. Researching at first seems very straightforward, but with proper strategy, you can get more with the time you spent researching. Here is a strategy that can be followed.

* Understanding the topic
* Explore other organizations who have used/created/dealt with it
* Check the active open source project
* Explore bloggers
* Stack Overflow, GitHub pages, etc.
* POC: Proof of Concept

## Understanding the topic
Reading the official documentation is a good source to get a better insight into the topic. Sometimes, the documentation is not very easily understood, due to the technical vocabulary used, but reading the documentation at least the key pages is very important. There is no need for reading the entire documentation in one go. This is a long process and it makes sense to distribute it equally. Distributing means reading about the basics first, understanding till that point, then continuing the rest in patches.

## Explore other organizations
Now, once you understand the problem, then comes the step to research which organization has faced it in their projects and how they approached it. Many organizations like Netflix, Uber, etc have their blogs available in which they usually tell about what are the technologies and libraries they have used. You can read about them and know the challenges they have faced so that you don't have to face such roadblocks

## Check for active products, programs, or open source code
find projects that can be used to reference how other developers have implemented certain functionality, even a tool to integrate.

## Explore bloggers
For your savors comes the blogger who tries to help others by sharing the in-depth knowledge that they have gathered. Make sure you read those blogs, there you can get a humanized version of the actual implementation. Most of the time you will find some blogs, which will help you in understanding the entire flow. Suggestion: if you like someone's blog, share it with your team, and do give them a thanks message or simply like their blog, it is a courtesy that you respect their effort.

## Q&A platforms
Explore the other discussion platforms available for software developers like Stack Overflow, and GitHub Pages. You can find the solution to your problem which you find while implementing the code. Make sure you research the problem thoroughly before making a post on these platforms. Since there is decorum of these platforms that should be maintained and we should not spoil it by asking questions, for which answers could be found easily.

## POC: Proof of Concept
Bring everything you have learned to use to fill the gaps you think aren't answered in your theoretical research and put it into practice. POC( Proof of concept), is implementing all the concepts and making them work, just to double-check before implementing them into the final code.

All the shortcomings which you were not able to identify at the time you were researching the concept, plus some of the other features which can only be understood by implementing the module.

# Broad View of Research
Reflecting on the tension in human-computer interaction research between
* "narrow truths proved convincingly by statistically sound experiments
* broad 'truths', generally applicable, but supported only by possibly unrepresentative observations".

The former satisfies the gold standard of science but are few and narrow compared to the decisions designers make daily. The latter provides pragmatic guidance but is at risk of over-generalization.

To relieve the tension through a **certainty-shell** structure -- to recognize three nested classes of results,
* Findings: well-established scientific truths, judged by truthfulness and rigor;
* Observations: reports on actual phenomena, judged by interestingness;
* Rules of thumb: generalizations, signed by their author but perhaps incompletely supported by data, judged by usefulness
with freshness as a criterion for all three.

This tension is as real in software engineering as in human-computer interaction. Observations and rules of thumb provide valuable practice guidance when findings are not available. They also help to understand and lay the groundwork for the research that will yield findings in time.  

# Questions, Results, and Validation in Software Engineering

## Types Questions 
Research questions may be about methods for developing software, methods for analyzing software, the design, evaluation, or implementation of specific systems, generalizations over whole classes of systems, or the sheer feasibility of a task

|  Type of question | Examples |
| ----------------- | --------|
|  Method or means of development | How can we do/create (or automate doing) X? What is a better way to do/create X? How do I choose between X and Y?                                                                | 
|  Method for analysis  | How can I evaluate the quality/correctness of X? How do I choose between X and Y?|
|  Design, evaluation, or analysis of a particular instance | What is a (better) design or implementation for application X? What is property X of artifact/method Y? How does X compare to Y? What is the current state of X / practice of Y? 
|Generalization or characterization| Given X, what will Y (necessarily) be? What, exactly, do we mean by X? What are the important characteristics of X? What is a good formal/empirical model for X? What are the varieties of X, and how are they related?
| Feasibility|  Does X even exist, and if so what is it like? Is it possible to accomplish X at all? 

## Types Results
Research yields new knowledge. This knowledge is expressed in the form of a particular result. The result may be a specific procedure or technique for software development or analysis. 

| Type of result | Examples |
|--|--|
|Procedure or technique | New or better way to do some task, such as design, implementation, measurement, evaluation, and the selection from alternatives. Includes operational techniques for implementation, representation, management, and analysis, but not advice or guidelines|
| Qualitative or descriptive model | Structure or taxonomy for a problem area; architectural style, framework, or design pattern; non-formal domain analysis. Well-grounded checklists, well-argued informal generalizations, guidance for integrating other results,
| Empirical model | Empirical predictive model based on observed data|
| Analytic model | Structural model precise enough to support formal analysis or automatic manipulation.
| Notation or tool | Formal language to support technique or model (should have a calculus, semantics, or another basis for computing or inference). An implemented tool that embodies a technique|
| Specific solution | Solution to application problem that shows the use of software engineering principles – may be design, rather than implementation. Careful analysis of a system or its development. Running a system that embodies a result; may be the carrier of the result, or its implementation may illustrate a principle that can be applied elsewhere
| Answer or judgment| Result of a specific analysis, evaluation, or comparison|
| Report | Interesting observations, rules of thumb| 

# Types of Research Validations
Good research requires not only a result but also clear and convincing evidence that
the result is sound

| Type of validation | Examples|
|-|-|
|Analysis| I have analyzed my result and find it satisfactory through ...normal (analysis) … rigorous derivation and proof (empirical model) …data on controlled use(controlled) … carefully designed statistical experiment) experiment|
| Experience|  My result has been used on real examples by someone other than me, and the evidence of its correctness/usefulness/effectiveness is …qualitative model) … narrative(empirical model, … data, usually statistical, on practice (notation, tool) … comparison of this with similar results in technique) actual use |
| Example | Here’s an example of how it works on (toy example) … a toy example, perhaps motivated by reality (slice of life) …a system that I have been developing |
| Evaluation| Given the stated criteria, my result... (descriptive model) … adequately describes the phenomena of interest … (qualitative model) … accounts for the phenomena of interest… (empirical model) … can predict … because …,  or … gives results that fit real data … Includes feasibility studies, pilot projects |
|Persuasion| I thought hard about this, and I believe... (technique) … if you do it the following way, …(system) … a system constructed like this would …(model) … this model seems reasonable. Note that if the original question was about feasibility, a working system, even without analysis, can be persuasive |
| Blatant assertion| No serious attempt to evaluate result |

# Reference:
* [1] [https://medium.com/swlh/software-developer-special-how-to-research-cedfc7cefc4d](https://medium.com/swlh/software-developer-special-how-to-research-cedfc7cefc4d)
* [2]  [What Makes Good Research in Software Engineering?](https://www.cs.cmu.edu/~Compose/ftp/shaw-fin-etaps.pdf) Carnegie Mellon’s School of Computer Science