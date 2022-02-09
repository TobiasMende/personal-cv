+++ 
title = "Code ownership conflicts as a signal for structural mismatch"
description = "Code ownership on a team-level can not only help to identify the team that has knowledge in a certain area, it also can serve as a signal for a mismatch between architecture and team structures."
tags = ["Practices", "Software Development"]
categories = ["Software Craft", "Organizational Design"]
series = ["Code Ownership"]
authors = ["Tobias Mende"]
featuredImage = "/images/2022-02-19-code-ownership-conflicts.jpg"
date = 2022-02-19T11:00:00+01:00
slug = "code-ownership-conflicts"
draft = false
+++
In my [last article](/blog/code-ownership/ "Code Ownership: Keeping the balance between structure and agility"), I explained why I believe that individual code ownership is bad and why weak code ownership on a cross-team level can be highly beneficial.

Today, I want to highlight another benefit of defining ownership of components on a team level, which is, that it can serve as a signal for misalignment or mismatch between team structures and software architecture.

## Imagine a system without any ownership
Imagine a system, where all teams are owning the entire system collaboratively and everybody can change anything at any time without informing others. It works well on a small scale, but with fifty or more developers working like this, it will likely end in chaos if there are no clear subsystem boundaries.

Nobody can oversee the entire system and consequences of their action, which is normal at a certain size. However, in such a scenario, nobody can oversee even smaller subsystems because they change unpredictably.

Furthermore, areas where nobody has knowledge in, remain unnoticed. 

## The relationship between team structures and software architecture
In 1967, Melvin Conway phrased a sentence which from then on became known as Conway’s *law*:

> Any organization that designs a system *(defined broadly)* will produce a design whose structure is a copy of the organization's communication structure.

Since then, this statement has proven to be true again and again. Consequently, today, we see software architecture as more than only software modules and the dependencies between them. Software architecture only focusing on the technical aspects but ignoring team structures, and thus ignoring Conway’s law, is doomed to fail.

Furthermore, people caring about software architecture can apply what is known as an *Inverse Conway Manoeuvre*: Structuring teams according to how the software architecture should (ideally) look like. This approach is able to help to enforce boundaries in the architecture. If architectural boundaries are aligned with team boundaries, they are more likely to appear and remain in the system itself.

Thus, it is apparent, that team structures and software architecture are highly interconnected matters that cannot be treated individually.

## Code ownership conflicts as a signal
Mapping the ownership of subsystems, modules, or components to teams creates transparency and can surface hidden issues like areas without owners or implicit assumptions about ownership.

Not always, the code ownership is crystal-clear and thus, discussions, why which team should own which component can help to solve these issues.

Furthermore, applying the practice not just to change code in the ownership of another team but also using this as a reason for communication may raise the fact, that team structures and architecture are not aligned well enough.

If one team frequently needs to change code owned by another team, it can mean that either the ownership is wrong or that the interface provided by another team does not fit well enough with the use cases of the dependent team. Thus, this signal can either lead to improving the structure or the ownership and hence reduce friction/dependency between teams.

## Code ownership is not a hall pass
I wrote this point already in my last article, but it cannot be stressed enough: Code ownership is not a hall pass for not caring about issues in components not owned by my team. Issues in one module can affect the *(perceived)* quality and stability of the entire system.

Thus, I would always encourage people to change code and fix bugs in code they do not own, if they feel comfortable to do so. Code ownership is merely a tool to know which team to ask if I lack knowledge about an area, or which team I should inform if I change something.

## Summary
Making code ownership visible and acting on it can serve as a signal for tensions between team structures and software architecture, and thus help to improve the overall system.

Therefore, thinking about ownership on a team level is a worthwhile and beneficial activity. However, it is important that everybody understands, that building a system is still a shared effort and defining code ownership must not lead to siloed teams.

**Have you thought about code ownership in your company? What effects are you observing? Share your experience here in the comments or via [LinkedIn](https://www.linkedin.com/in/tobiasmende/) or [Twitter](https://twitter.com/Tobias_Mende).**