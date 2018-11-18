# Measuring Engineering : A Report
___

## Table of Contents:

1. Introduction
- What is software engineering?
- History of software engineering

2. Measuring Software Engineering
- How can it be measured?
- Version control & collaboration

3. Computational Platforms & Algorithmic Approaches
- Continuous integration
- Automation

4. Ethical Concerns
- Privacy
- Exploitation of labour

5. Bibliography

___

## Introduction

### What is software engineering?

In order to explore how the software engineering process can be measured, we must first ask the question: *what is software engineering*?

The Institute of Electrical and Electronic Engineers (IEEE) defines software engineering as "the systematic application of scientific and technological knowledge, methods, and experience to the design, implementation, testing, and documentation of software."[1]

Software engineering is of enormous importance in the modern world as, although software itself is intangible, it is embedded in the hardware of the machines used in various industries and its malfunction can have tangible from, from inconsequential to loss of personal and financial information or even loss of life. Thus the discipline of software engineering is hugely important in ensuring that systems are functional before they lead to costly or disastrous consequences.

### History of software engineering

The person accredited with having first coined the term *software engineering* on the 1960s is Margaret Hamilton, a mathematician and computer science pioneer, and CEO of Hamilton Technologies. According to her, she "fought to bring the software legitimacy so that it - and those building it - would be given due respect and thus [she] began to use the term 'software engineering' to distinguish it from hardware and other types of engineering, yet treat each type of engineering as part of the overall systems engineering process."[2]

The early days of software engineering was like navigating a wilderness. No one really knew what they were doing and there was no 'knowledge-base' to refer to, but rather information was passed down from person to person. Its importance didn't become apparent until Hamilton joined the Apollo program in 1965.

Software development in the Apollo program was very structured, but very reliable, "Not only did the software itself have to be ultra-reliable, it needed to be able to perform error detection and recovery in real time."[2] Software was programmed on IBM punch cards, which had 80 columns and were 'assembled' to instruction binary on mainframes, which could take hours, thus during missions, most of the software couldn't be changed, as it was encoded into the hardware like ROM. Some engineers would even "[guess] and make up minor changes to the software to work around [hypothetical] failures that were thrown at the flight control team during simulations."[3]

The NASA engineers of the Apollo program made extraordinary accomplishments with the relatively primitive hardware and software available to them, and thanks to the rigorous design methods set out by Hamilton, they knew each line of code so well that they were able to read out binary settings to the astronauts of by radio. This was essential when, during the Apollo 11 mission, several warning lights and computer overload alarms came on as the craft was descending onto the moon's surface. John Garman's, an engineer, pre-flight simulation experience told him that the alarms were not critical and the landing could continue. If not for him the mission would have been aborted and the astronauts would have remained in orbit around the moon.

Over the following two decades a number of problems and disasters lead to the period being referred to as the 'Software Crisis'. Much of the emphasis during this time was placed on productivity rather than quality, causing budget and schedule overruns. An example of this is recounted in the book, *The Mythical Man-Month* by Fred Brooks, where he attributes a multimillion-dollar mistake to not having developed a coherent architecture before starting development. His observations that "adding manpower to a late software project makes it later"[4] and that "a programming product costs at least three times as much as a debugged program with the same function"[4] come from his experiences at IBM while managing the development of OS/360, where he decided to add more programmers to a project that was falling behind schedule, which counter-intuitively worsened the situation. Other disasters from this period include poor software security, which allowed hackers to steal identites, costing time, money, and reputations, and someembedded systems used in radiotherapy machines failed, causing lethal doses of radiation to be administered to patients. The most famous of such incidents was the *Therac-25* incident, which resulted in the deaths of three people.

The major changes in the software engineering process since then have been the introduction of version control and collaboration, and the rise of the open-source movement due to the internet. The open-source movements impact on software engineering productivity has been immense, with a significant number of the languages, tools, and frameworks used by developers daily stemming from it. Furthermore the features provided by tools such as git have hugely facilitated engineers working on large-scale collaborative projects, meaning that disasters such as the OS/360 are more easily avoided.

These tools can also prove useful in measuring the software engineering process. In the following sections I will discuss thoroughly the data and how it can be measured, the computational platforms and algorithmic approaches available to someone who would want to measure this data, and in my opinion the possible ethical concerns which one should consider in measuring the data.

___

## Measuring Software Engineering

###
