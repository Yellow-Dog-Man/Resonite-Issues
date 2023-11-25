Creating and prioritizing issues can be a complicated process. Many issues can take a fair bit of time to be looked at, in part due to the sheer volume and limited time on the development team. Out of the issues that do get looked at, not all of them will end up being worked on, for various reasons.

When we look at the issues submitted by the community, there’s a variety of factors - signals, that we look at when deciding which issues to look at to triage and evaluate and which ones we work on.

Whether a particular issue gets picked up or not is a complex combination of these factors. We want to help you understand what those individual factors are, so you can write your issues and interact with the existing issues in a way to maximize the chance that an issue will get picked up and worked on.

# Signals that we use to prioritize issues

Here follows a quick summary of the different signals and factors that are used when prioritizing issues. We recommend reading the sections below that expand on each and provide some examples to better understand them.

- **Descriptive title** - precise title that describes core of the issue helps issue get prioritized, vague or misleading titles hurt its changes to get picked up
- **Quality and clarity** - use precise language and to the point to increase chance of issue to get picked up, make sure to provide all necessary information
- **Impact on software, community and team** - security issues generally get higher priority. Similarly issues affecting legal, business, development, content, moderation or accessibility can be prioritized over others
- **Recency & regressions** - issues relating to recent changes and additions will get higher priority
- **Complexity of the work** - simple issues are more likely to be picked up and worked through, while issues requiring more work get weighed and selected more heavily
- **Maintenance & refactoring burden** - even if the issue needs a simple change, its priority can be lowered if the change would increase technical debt and cause more issues or work in the future
- **Prerequisites & alignment with roadmap** - we might prioritize some issues over others, if they will save significant amount of development time on other issues, even if those other issues are more popular
- **Votes & activity** - more active or upvotes issues have higher chance of getting picked up, but other factors are still considered - top voted issues do not automatically mean they’ll get picked up. However, do not “bump” issues - it doesn’t help their priority
- **Polite and neutral language** - emotionally charged issues can be harder for the team to deal with, lowering their chances of being resolved faster
- **Existing community solutions** - some issues can have lower priority if there are good in-game solutions with existing functionality. Conversely some issues can get prioritized if they would help unify a lot of fragmented community solutions to a problem.
- **Diversity** - we will avoid working on same types of issues for too long and will prioritize issues that change the pace and address needs of different users and communities on the platform
- **Developer interest** - some issues get prioritized based on particular developer’s interest in the issue and the challenge it poses
- **Mental state/capacity** - when we are mentally drained and/or busy dealing with other things, we will tend to pick up simpler and more straightforward issues
- **Chance / Human Error** - there is always an element of chance and oversights. We try to eliminate these, but they do happen

## Descriptive title
When we browse issues to be triaged or worked on, we only see their titles. Because of this, writing a good descriptive title is a key factor to increase the likelihood we’ll look at the issue more in depth.

A good title can be the difference between “I don’t know what this is, I’ll have to look at it later” to “Oh, I know what might be causing that bug, that’s 5 minute change” or “Oh, that’s a good idea / bad problem, I should look further”.

Generally you will want to avoid vague titles, such as “Problems with some components” and instead describe the core of your issue in the title, like “Grabbable component deletes itself when it’s driven and then grabbed”.

The descriptiveness of the title doesn't just matter for the initial triage, but also when deciding which triaged issues we’ll work on - we’ll often scan the list and try to identify good issues from the titles.

## Quality and clarity of the issue
Once we actually click and open your issue, the quality of the content will matter a lot to the prioritization. Issues that are well written, concise, provide all the necessary information, are more likely to get prioritized.

Conversely, **there are things that might result in the issue not getting prioritized**:
- Missing key/required information (e.g. log files, replication objects/steps) - this will require back and forth making the issue more difficult to address
- Being too vague - we might not understand or have enough details, which means we’ll have to ask questions. In some cases, it can be difficult to understand what we even need to ask in the first place
- The core issue is hidden in lots of text / fluff - we likely won’t have time to read paragraphs of text and context until we get deeper into the issue - meaning we’ll have to skim and more likely miss important bits. Adding more context and extra information is good, but the core issue should always have a brief description at the top
- Combining several problems/features into one issue - if you ask us to implement A, B, C, D and E at the same time, it makes the issue much bigger. If you ask us for each individually, we might get through them faster, or implement a few of them first and then others
- Replication steps more complicated than they need to be - if the replication requires a lot of setup and unnecessary steps, or has dependencies (e.g. downloading 3rd party software, loading complex worlds/items), it can lower the priority of the issue, due to increasing of its complexity on our end
- Missing replication item - if we have to spend 5-10 minutes (or even longer) making our own replication of this, we might push the issue for later and pick another one
- Asking for very specific solution/approach - if you ask us to implement things in a very specific way, we’re more likely to decline given issue, especially if we don’t understand motivations of such change and the proposed change doesn’t mesh well with the codebase - we recommend to read up on the [XY Problem](https://xyproblem.info/) for more context. Figuring out a way to solve a problem is our job and the more you constrain our hands/options on this by not providing necessary context or demanding a particular approach, the less likely the issue is going to be picked up.

**What’s particularly effective to get higher priority:**
- Concise and precise language - clear description of the issue and to the point. Bullet points can work pretty well for this
- Focus on the root problem & motivation / use-case for the change - if you make the issue about the core issue you want addressed, it makes it easier for us to understand motivation and come up with a good and efficient solution that can be implemented
- Clear replication steps that have been reduced to minimum - the more work you do at reducing and narrow the problem on your end, the less time we need to spend on the issue ourselves and more likely to prioritize it higher
- Easy to use replication item/world - if we can launch, press a button and have the issue occur, this helps a lot

## Impact on the software, community and team
There are specific types of issues that are more likely to be prioritized over others. For some of them, the impact alone can be sufficient to put them very high up in the priority list.

### Security
This is probably the most obvious one. Security vulnerabilities, depending on their severity, will often get picked up faster than other issues.

For particularly impactful ones - for example ones that allow remote code execution, which would allow an attacker to hijack someone’s system, we are likely to drop everything immediately and prioritize a solution that specifically addresses a given issue even if it delays other work.

In some cases, if the given vulnerability is more theoretical and it’s not clear if it can be exploited at all or if the result of exploit is more of an inconvenience, rather than security threatening scenario, they can be prioritized lower - e.g. as a part of larger rework or refactoring to address a number of issues.

### Legal / Business
As a company, we need to comply with a number of laws, regulations and agreements/contracts with other companies. Some features might get prioritized at times to ensure the smooth operation of the company and avoid legal issues.

### Blockers
Certain issues can be significant blockers to parts of our community or our team. For example some users, both casual and commercial, might have their workflows blocked by a particular issue. Depending on the severity of the impact, we might prioritize issues based on this factor.

This is also similar for issues that are affecting various teams on Resonite. Issues that the content team requires to implement new official content or issues that will benefit moderation, support and QC teams might be given higher priority, to ensure smoother workflow and better operation of the platform.

### Accessibility
Certain issues might be affecting smaller groups of users, particularly due to various disabilities or health issues. We will prioritize such issues even if there’s not as much general interest in them, as we believe that making the platform accessible to more users is important on its own.

## Recency & Regressions
If a particular issue concerns a recently added feature, tweak or bugfix, it’s much more likely to be looked at and prioritized over other issues.

Every time we make changes to the software code, there can be unintended consequences of such change that only show up once the change is used by the wider community.

After releasing updates, we will look out for issues specifically concerning the recently done changes and try to correct or mitigate problems caused by this change or use the feedback to polish the new feature some more.

Another reason why this is done immediately after the change is that the technicalities of this change are still fresh in our mind, which makes it easier and faster to pick these issues up and resolve them, compared to switching focus to other things.

## Complexity of the work
For each issue, we will try to gauge how much work is involved to make it happen. This can range anywhere from a few minutes to weeks, months and even years worth of work.

Issues that are very quick changes - typically few lines of code, often get prioritized easily, since they are easy to couple with a number of larger changes. We will often tackle a few of those issues every week even when working on bigger problems most of the time.

However even for issues that might be a small amount of work, we still consider the other factors - particularly if it introduces any technical debt, has a negative impact or would add significant maintenance & refactoring burden, so not every quick change will get prioritized.

Some issues might also seem small at first, but when we dig into them deeper, they end up being more complex than we estimated, which can shake up its priority. Because of this, you’ll see us pick up some issues, but then defer them for later. We’ll send a message when this happens, usually explaining why it got more complicated.

Conversely, issues that wake weeks, months or even more time, we cannot simply “dive into” and start working on them, but require more robust and careful planning. We also need to be a lot more careful and deliberate which ones we do pick.

Consider this - if an issue takes 5 minutes, we can ideally tackle 475 of them per day, which is 169100 per year. These are idealized numbers, but the point is, that we can tackle lots of them and don’t need to be as selective. In comparison, if an issue takes 3 months to implement, we can only do 4 of them per year.

## Maintenance & refactoring burden
When evaluating issues, we do not only look at the complexity of implementation itself, but we also consider the long term impact of given change or addition. There are a number of issues which might be easy and fast to implement, but will have a long term impact on the software and quality of the codebase.

For example, a quick implementation might become broken with unrelated changes, particularly in parts of the more messy parts of the codebase, or it might make other features and changes harder to implement in the future.

Particularly in cases where we plan to refactor/redesign parts of the system, we are less likely to take incremental changes, improvements and additional requests for that system, until the rework is done or even draw a line and stop taking changes altogether.

This is done so the priority gets put on the rework instead and results in the rework being prioritized. Doing further incremental changes not only takes pressure off the much needed rework, but makes it even a bigger task when it does get prioritized, because the changes need to be reworked and transitioned to the new system.

As a general rule, we do try to avoid “hacky” and “ad hoc” solutions to problems where possible and will prefer cleaner solutions, even when they take longer to pick and and implement.

In cases where a given change has potential to become a dependency for user made content, we will also be very cautious about adding certain features or changes or flat out refuse them, if there’s a concern that we will not be able to preserve its behavior with future changes, to ensure that user content does not get broken.

In other words, we place a high priority on not breaking user content and if there’s a concern of this happening, the issue is a lot more unlikely to be picked up.

## Prerequisites & alignment with roadmap
Certain issues cannot be easily addressed directly and will require other features or major changes to be implemented first. Because of that, the issue itself won’t likely be prioritized for a while, even if there’s significant interest in it.

This can happen for a number of reasons. In some cases, implementing certain features can simply be nearly impossible with the current state of the code. In this case it’s simply not possible to prioritize the issue, until other changes are made.

However in other cases, it might be possible to implement a given feature, but we might already be planning to make changes to the engine and its architecture, that would make implementing the requested feature much simpler or would require reimplementing it.

To give an example, consider as an example that adding rigidbody physics will take 2 months. We might also be planning to restructure how the engine handles transforms, which might take 1 month. Reworking rigidbody physics to this new system will take another 1 month.

If we implement rigidbody first, the total amount we need to spend is 2 months for rigidbody, 1 month for rework of transforms and 1 month to rework rigidbody = 4 total months of development time.

However if we shuffle things around, we get this: rework of transforms 1 month + implement rigidbody 1.5 month (because it was simpler with the reworked transforms) = 2.5 months.

Simply by shuffling the priorities around, we saved 1.5 months of development time - which is time that we can contribute to other issues instead.

These numbers are just demonstrative and will vary in practice, but hopefully they make the principle clear. In practice the chains can also be more complex - we might need to implement feature A, to make B simpler, which makes C simpler, which makes D simpler.

By being careful with how we order things, we can save a lot of development time, which can then be used to address additional issues. Because of this, we might not prioritize and start working on certain issues right away, even if there’s a popular demand, but instead chart a roadmap to maximize what we get out of our limited development time.

## Votes & activity
When evaluating issues, either for triage or for prioritization, one of the factors we do look at is how many upvotes the issue has ([learn how to upvote issues here](HOW_TO_UPVOTE.md)). This lets us know which issues affect more people than others or at least which ones are more popular.

Users chiming in with more context, information, replication information for the same issue also helps, as we see there’s more interest / activity and the additional information can help reduce the workload on our end to ensure the issue goes through.

Conversely, when we ask for additional information, context and receive no answers on the issue, we’re more likely to drop it, because we assume the user doesn’t have enough interest in the issue to stay engaged with it.

### Does this mean that top voted issues get immediately worked on?
TLDR: No.

Long answer: Votes & activity is just one factor of many, so an issue being at the top of the list does not mean it will be picked up soon - some of the more complex issues might require months of work, perhaps even pre-requisite work.

Some might not be quite aligned with our goals and plans for the project and so we might not have a way to fit them into the roadmap for the foreseeable future. We will try to communicate this when it happens.

Some we might not have enough information or resources to actually address. This can be the case with some elusive issues that are hard to diagnose and get enough information to start working on. Usually we will ask people for more information when needed.

In a number of cases we will also prioritize other issues that have very few, if any votes on them, over issues that have more votes, because the other factors outweigh the votes. For example accessibility issues or issues that open up new creative or business opportunities can get prioritized.

We do not want issues to be prioritized solely by majority rule, as this would exclude other important work on the project (e.g. issues that aren’t as exciting and voted upon, but provide strong foundations for the future) or issues that might affect minority groups (e.g. with accessibility issues).

However issues with more votes are at very least more likely to get looked at, evaluated and put into our long term planning.

### Should I bump issues?
Also no.

Generally going “bump” in the issue does not help to prioritize it, because it does not make the issue sort higher when counting the number of upvotes and adds a bit of noise to it instead.

Similarly stating that issue still exists on latest build does not help - if we haven’t released a build and stated that the issue should be addressed, it’s not necessary to write a message it’s still an issue on the latest build, as this doesn’t really give us any new information - we haven’t worked on the issue yet.

Instead, if you want to help prioritize the issue, upvote the issue instead ([see this page if you don't know how](HOW_TO_UPVOTE.md)). Writing a comment that provides more context on its impact, what workflows, actions, events it blocks or that helps narrow down the problem will also help improve the chances it gets addressed.

## Polite and neutral language
It’s important to remember that we are humans as well and that the pressures of development can be very stressful and emotionally draining.

Addressing issues and solving problems requires strong focus and a clear head, which is harder to achieve when stressed or filled with anxiety.

Because of this, it’s important to keep the issues and their languages as emotion free as possible. Issues that get heated or that are very emotionally charged can be more difficult for us to deal with and think about clearly, which is detrimental to getting the actual issue prioritized and resolved.

Remember, we are here to solve problems together, not to fight against each other. Our goal is to get as many things resolved as possible, while keeping the project and codebase stable. But as humans, we have our limits and there are only so many things we can address at the time.

By focusing on the issue in an objective and polite manner, we can get more out of our development time and get more problems resolved. 

To give an example, comments of type “It’s been a month, why wasn’t this fixed yet?!” can actually hurt the prioritization of the issue, by bringing emotional charge to it. Instead, consider a more constructive approach: Voting the issue up and adding additional context and information. For example saying “I have encountered this problem frequently over the past month and it has interrupted my work this and that way. It would improve my workflow if this was prioritized.” is much better instead.

The bottom line is - please keep emotion out of the issues. You can rant to your friends, but GitHub is the place to get issues resolved, not a place to be angry about them.

## Existing community solutions
When looking at the issues, one of the less usual factors that we can consider is whether there are existing community tools (whether it’s tools built in-game or plugins/mods) that implement a given feature or address a particular issue.

However whether this increases or decreases priority of a given issue depends heavily on a case by case basis.

### Decreases in priority 
Part of our philosophy is to provide the community with tools to solve problems and evolve the platform on their own, rather than solve every single problem ourselves. As such, we might not prioritize certain issues or address them on our own, if there is already a good community solution or way to achieve a given goal with existing features, we might not prioritize a more specific native solution.

### Increases in priority
In some cases, looking at community solutions and mods can help bump up the priority of certain features. In some cases this is when it saves us time we’d have to spend investigating the source of a given problem and possible solutions - community fix can help put us on the right path to implement it officially.

However this is not a guarantee - in some cases, community fixes and approaches can be done in a “hacky” way, which would have a significant maintenance burden or negative side effects. In such cases, we’ll have to investigate and look for a more clean solution.

In some cases, we might see various community solutions to a common set of problems, where we could introduce a generalized system that would greatly simplify the approaches used and possibly unify/standardize them into a single official system, rather than a number of fragmented solutions. In such cases the existence of these various community solutions is a good signal to us that it’s something that would actively benefit the community.

## Diversity
Another factor that comes to feature prioritization is the diversity of the issues. We can prioritize certain issues over others based on the fact that they are different from issues that have been worked on recently.

This is done mainly for two reasons:

1) When working on a particular type of problem for too long, we might become fatigued, making it harder to focus and remain engaged with the issues. Switching the gears to something else helps us remain sane and sharp
2) Our goal is to make Resonite into a versatile software and balance the needs of a diverse community. Because of this, you will see us prioritize features and bug fixes that might not be relevant or interesting to you, but that are important for other parts of the community

## Developer interest
Part of the role that can play into prioritization of issues are issues that we find interesting or challenging to work on. We pick a good amount of “chore work” issues, even if they aren’t particularly interesting, because they are important for other reasons.

In order to remain engaged and happy with our work, sometimes we will prioritize a particular issue because it’ll be fun to work. This isn’t a factor that you have that much control over - and generally we do not use it too much for that reason, but we want to acknowledge that it does play a role for some issues.

One thing you can do with certain issues (particularly feature requests and tweaks) - the more general you make your issues and the less you tie our hands with how you ask us to solve a particular problem, the more interesting it becomes. We like solving general problems, rather than doing “chore work”. If we find a way to generalize certain problems and provide a cool solution, that makes it more likely to be picked up and prioritized.

## Mental state/capacity
Some days or weeks, we can be very mentally or physically drained and we simply can’t focus on more complex issues. We might be dealing with struggles in our life, in the community or perhaps other aspects of the project and the company, whether it’s dealing with finances, challenging support or moderation issues, legal issues, making difficult decisions and so on.

As a result, we’ll more heavily prioritize issues that are simpler to do when in that state, because they can be a good way to kill time, improve mood by making some progress and gain more momentum to tackle bigger issues again.

There’s not super much you can do on your end for this prioritization factor - however if you do like a particular change we did or something helped, letting us know can help lift our mood quite a bit.

Most of the feedback and communication we receive as part of our work  is often negative in a way, because they are reports of problems, so knowing the work we did had a positive impact can help us feel more empowered and give us the strength and motivation to handle more problems.

## Chance / Human Error
With all the factors above, there is still a certain element of chance and luck as we go through the issues. Some issues might get missed or overlooked. We might evaluate some of the factors wrong. Sometimes we see the right issue at the right time and sometimes we don’t.

While this is unfortunate and our goal is to keep the impact on overall prioritization minimal, we think it’s important to acknowledge that this happens.

The issues are an ongoing process and when some issues get overlooked, other factors should help bring them back - adding votes, adding additional context, related issues help the issue to be picked up.

However, even with all this, there often are too many issues for us to work through and some might never get prioritized or looked at in detail. This is the unfortunate reality of projects like this - there is a finite amount of time we can spend on things.

We know it sucks to spend time on an issue, only for it to never be done. But hopefully with this document we’ve given you enough knowledge and tools to significantly increase the chances of your issue to be picked up!
