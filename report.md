# Measuring Engineering : A Report
___

## Table of Contents:

1. Introduction
- What is software engineering?
- History of software engineering

2. Measuring Software Engineering
- Measurable data
- How does it help?

3. Computational Platforms & Algorithmic Approaches
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

Software engineering is of enormous importance in the modern world as, although software itself is intangible, it is embedded in the hardware of the machines used in various industries and its malfunction can have tangible effects, from inconsequential to loss of personal and financial information or even loss of life. Thus the discipline of software engineering is hugely important in ensuring that systems are functional before they lead to costly or disastrous consequences.

### History of software engineering

The person accredited with having first coined the term *software engineering* in the 1960s is Margaret Hamilton, a mathematician and computer science pioneer, and CEO of Hamilton Technologies. According to her, she "fought to bring the software legitimacy so that it - and those building it - would be given due respect and thus [she] began to use the term 'software engineering' to distinguish it from hardware and other types of engineering, yet treat each type of engineering as part of the overall systems engineering process."[2]

The early days of software engineering was like navigating a wilderness. No one really knew what they were doing and there was no 'knowledge-base' to refer to, but rather information was passed down from person to person. Its importance didn't become apparent until Hamilton joined the Apollo program in 1965.

Software development in the Apollo program was very structured, but very reliable, "Not only did the software itself have to be ultra-reliable, it needed to be able to perform error detection and recovery in real time."[2] Software was programmed on IBM punch cards, which had 80 columns and were 'assembled' to instruction binary on mainframes, which could take hours, thus during missions, most of the software couldn't be changed, as it was encoded into the hardware like ROM. Some engineers would even "[guess] and make up minor changes to the software to work around [hypothetical] failures that were thrown at the flight control team during simulations."[3]

The NASA engineers of the Apollo program made extraordinary accomplishments with the relatively primitive hardware and software available to them, and thanks to the rigorous design methods set out by Hamilton, they knew each line of code so well that they were able to read out binary settings to the astronauts by radio. This was essential when, during the Apollo 11 mission, several warning lights and computer overload alarms came on as the craft was descending onto the moon's surface. John Garman's pre-flight simulation experience as an engineer told him that the alarms were not critical and the landing could continue. If not for him the mission would have been aborted and the astronauts would have remained in orbit around the moon.

Over the following two decades a number of problems and disasters lead to the period being referred to as the 'Software Crisis'. Much of the emphasis during this time was placed on productivity rather than quality, causing budget and schedule overruns. An example of this is recounted in the book, *The Mythical Man-Month* by Fred Brooks, where he attributes a multimillion-dollar mistake to not having developed a coherent architecture before starting development. His observations that "adding manpower to a late software project makes it later"[4] and that "a programming product costs at least three times as much as a debugged program with the same function"[4] come from his experiences at IBM while managing the development of OS/360, where he decided to add more programmers to a project that was falling behind schedule, which counter-intuitively worsened the situation. Other disasters from this period include poor software security, which allowed hackers to steal identites, costing time, money, and reputations, and some embedded systems used in radiotherapy machines failed, causing lethal doses of radiation to be administered to patients. The most famous of such incidents was the *Therac-25* incident, which resulted in the deaths of three people.

The major changes in the software engineering process since then have been the introduction of version control and collaboration, and the rise of the open-source movement due to the internet. The open-source movements impact on software engineering productivity has been immense, with a significant number of the languages, tools, and frameworks used by developers daily stemming from it. Furthermore the features provided by tools such as git have hugely facilitated engineers working on large-scale collaborative projects, meaning that disasters such as the OS/360 are more easily avoided.

These tools can also prove useful in measuring the software engineering process. In the following sections I will discuss thoroughly the measurable data, the computational platforms and algorithmic approaches available to someone who would want to measure this data, and in my opinion the possible ethical concerns which one should consider in measuring the data.

___

## Measuring Software Engineering

### Measurable data

There are many metrics to consider in the software engineering process, and not all of them are necessarily good metrics. Consider lines of code: to an outside observer, if an engineer is producing a larger volume of code, it may seem like he is more productive, however any decent developer knows that reducing line count is often better than increasing it, especially regarding efficiency. So I have chosen three different metrics that I think provide meaningful insight into the software engineering process:

- Code quality
- Code churn
- Refactoring and reviewing

The three are highly interconnected and I will be taking a look at how they affect each other and what they can reveal when considered.

#### Code quality

To look at the productivity of engineers, you must also look at the quality of the work they are producing, after all, high productivity and low quality is far from helpful. Things to look for in measuring code quality include correctness, maintainability, readability, and test coverage. Correctness is clearly at the top of the list as, at the end of the day, it's the most important. It is also relatively easy to measure by asking one simple question: *does the code do what it's supposed to do*?

Maintainability is important when considering the collaborative nature of software engineering, as a programmer builds code intended to be usead by another programmer. If code is not maintainable it becomes a huge waste of time further down the line if it needs to be refactored to integrate it with newer components. This ties into readability because code that is not readable is even more difficult to modify.

Finally test coverage gives an idea of how thorough engineers are being when considering how their code works and what issues could arise when it is actually being used. Code which has covered all possible eventualities is a lot less likely to cause bugs and is also easier to fix if bugs present themselves.

![img1](https://i0.wp.com/blog.gitprime.com/wp-content/uploads/2017/07/slide-8alt.png?resize=996%2C1024&ssl=1)

#### Code churn

Code churn is defined as lines added to, modified, or deleted from a file from one version to another. For example, a developer writes a piece of code, but it doesn't work and is discarded. The developer writes the code again, but with a different approach. Unfortunately it doesn't work either and is discarded again. Finally the third time it's written yet another way and this time it works. The developer technically produced three times the amountof code, but only one part was useful. The discarded code is the churn, and it's important to keep track of this as a developer generating a lot of churn could mean anumber of things.

High churn can be expected from an engineer who is prototyping a new feature, or polishing some features in time for a release date, however it can mean bad news if it is caused by unclear requirement specification or merely can indicate that they are stuck on a difficult problem. Identifying what the causeof the churn is will help improve productivity.

#### Refactoring and reviewing

![img2](https://docs.microsoft.com/en-us/azure/devops/learn/_img/code-reviews-ranked-reasons.png)

Peer code reviews are a standard practice in software engineering. Open source workflows especially are designed to enforce a successful peer review before the merge of a change into the main codebase. Who reviews code and accepts or blocks the change from becoming a part of the codebase is crucially important. Most engineers hope for defects to be spotted or possible improvements to be suggested by code reviews.

However reviewing can cause bottlenecks if, for example, all the code produced by a team of 50 developers is being reviewed by the same two or three senior developers, because it requires heavy involvement from them. The average time from a review being requested to receiving all necessary sign-offs is about 24 hours, but can last days or weeks. Therefore I think that the amount of time spent reviewing code is an important metric in measuring software engineering.

Time spent refactoring legacy code is also of interest. Say a team is spending a lot of resources refactoring in order to get ready for a release. Someone decides to increase the manpower dedicated to refactoring to meet the deadline, but as evidenced by Fred Brooks this could lead to the project being even later. Refactoring should be done in large installments so as to avoid pressure from deadlines.

### How does it help?

As mentioned briefly, measuring and analysing this data can help give an idea of where and how developers are falling behind, and how to optimize their ability to work effectively.

___

## Computational Platforms & Algorithmic Approaches

Processing these datasets can be easy on a small scale, but larger teams mean larger datasets and this can be problematic. In the following subsections I will discuss the tools and approaches available to work around these problems

### Tools available

**git** is an immensely helpful tool when it comes to the metrics that I discussed earlier. It provides version control, which means that any changes to a codebase can be identified and viewed, which is very helpful in identifying code churn. Also the authors of the changes can be looked at, making it very simple to determine code quality. Senior developers can also review another developers code using **git**.

The company **GitPrime** offers this service. Their approach is to take in data from any **git**-based code repository - such as GitHub, GitLab, or BitBucket - and use it to optimize work patterns among engineers. They process the data and display it in a more human-readable form using libraries such as d3, to be able to identify patterns and adjust accordingly.

### Automation

As the datasets grow it becomes more difficult for humans to come up with meaningful conclusions, which is where artificial intelligence and machine learning come into play. Convolutional Neural Networks (CNNs) are replacing hand coded rules by directly building inference networks from data. This means that gathering *good* data is a new and very important discipline as your inference is only as good as your data. Equally CNNs, owing to their opacity (since humans aren't responsible for codifying the rules), can reinforce and amplify human bias.

___

## Ethical Concerns

### Privacy

### Exploitation of labour

Rockstar Games, the developer behind the 'Grand Theft Auto' and 'Red Dead Redemption' series, has recently been involved in controversy regarding their 

___

## Bibliography

1. https://en.wikipedia.org/wiki/Software_engineering
[1]: https://en.wikipedia.org/wiki/Software_engineering

2. https://publications.computer.org/software-magazine/2018/06/08/margaret-hamilton-software-engineering-pioneer-apollo-11/
[2]: https://publications.computer.org/software-magazine/2018/06/08/margaret-hamilton-software-engineering-pioneer-apollo-11/

3. https://www.linux.com/news/how-they-built-it-software-apollo-11
[3]: https://www.linux.com/news/how-they-built-it-software-apollo-11

4. https://www.rainforestqa.com/blog/2017-05-04-mythical-man-month-agile-software-testing-lessons/
[4]: https://www.rainforestqa.com/blog/2017-05-04-mythical-man-month-agile-software-testing-lessons/

5. https://www.softwareengineerinsider.com/articles/what-is-software-engineering.html
[5]: https://www.softwareengineerinsider.com/articles/what-is-software-engineering.html

6. https://blog.gitprime.com/2017-software-developer-productivity-survey/
[6]: https://blog.gitprime.com/2017-software-developer-productivity-survey/

7. https://blog.gitprime.com/6-causes-of-code-churn-and-what-you-should-do-about-them/
[7]: https://blog.gitprime.com/6-causes-of-code-churn-and-what-you-should-do-about-them/

8. https://blog.gitprime.com/why-code-churn-matters/
[8]: https://blog.gitprime.com/why-code-churn-matters/

9. http://engineering.kapost.com/2015/08/you-can-and-should-measure-software-engineering-performance/
[9]: http://engineering.kapost.com/2015/08/you-can-and-should-measure-software-engineering-performance/

10. https://docs.microsoft.com/en-us/azure/devops/learn/devops-at-microsoft/code-reviews-not-primarily-finding-bugs
[10]: https://docs.microsoft.com/en-us/azure/devops/learn/devops-at-microsoft/code-reviews-not-primarily-finding-bugs

11. http://uk.businessinsider.com/rockstar-games-controversy-explained-red-dead-redemption-2-crunch-culture-2018-10?r=US&IR=T
[11]: http://uk.businessinsider.com/rockstar-games-controversy-explained-red-dead-redemption-2-crunch-culture-2018-10?r=US&IR=T
