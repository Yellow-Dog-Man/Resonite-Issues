# Resonite Issues
Issue repository for Resonite. Please log any bug reports, or feature requests here using the appropriate template:

- [:bug: To Report a Bug Click Here](https://github.com/Yellow-Dog-Man/Resonite-Issues/issues/new?assignees=shiftyscales&labels=bug&projects=&template=bug-report.yml)
- [:computer: To Request a Feature Click Here](https://github.com/Yellow-Dog-Man/Resonite-Issues/issues/new?assignees=shiftyscales&labels=enhancement&projects=&template=feature-request.yml)
- [:paintbrush: To Report an Issue with Content such as the Cloud Home Click Here](https://github.com/Yellow-Dog-Man/Resonite-Issues/issues/new?assignees=shiftyscales%2C+AegisTheWolf%2C+RyuviTheViali%2C+RueShejn&labels=content&projects=&template=content-issue.yml)
- [:lock: To Report a Security issue please open a ticket](https://support.resonite.com/)

# Reporting Requirements
**Please ensure the following requirements are met** for anything submitted.

**FAILING TO FOLLOW THESE REQUIREMENTS MAY RESULT IN YOUR ISSUE GOING UNADDRESSED/BEING CLOSED**

- **Use the most recent version of Resonite** when replicating your issues.
  - This helps ensure that issues are still relevant and replicable
- **Try to search for existing issues** describing your problem before creating a new one
  - If an issue already exists for what you wish to report, please add any additional information to the existing issue instead.
- **Focus on the high-level issue first, not a specific solution**, as this lets us approach the problem most efficiently.
    - For example, it's better to say "I have this problem", rather than "Add a component that when this and this happens, it does this".
    - Problems can have many solutions and if your issue describes a very specific solution, you're more likely to get a lot of questions.
    - In Computing, this issue is commonly referred to as the [XY Problem](https://xyproblem.info/)
- **Do not request overhauls of systems**, focus on the bugs or features you want.
    - Overhauling a particular system is solely a Resonite engineering team decision.
    - If you want us to consider several issues for a single subsystem without specific solutions, you can [start a discussion](https://github.com/Yellow-Dog-Man/Resonite-Issues/discussions)
- **Make separate issues for each unrelated feature/bug** - in other words, don't ask for multiple separate features/bugs in a single issue. This makes them much more difficult to process and a lot less likely to be prioritized, because it means we'll have to implement all of them at once, rather than piece-wise. We might also say yes to some features/fixes and no to others - but if you group them into single issue, than if we say "no" to just one of them, we have to say "no" to the whole.
- **Do not hijack issues for another feature/bug**, Make another issue instead.
    - Issues should never have comments similar to "While you're at it, can you also do this?", it will not be considered and will get lost.
- **Try to troubleshoot** and isolate the problem first before reporting it.
    - For example, if it is a complex ProtoFlux creation try to identify the specific node/node group that is at fault. Then remove as much as possible from the item/world while still producing the bug.
- **Ensure that the issue happens WITHOUT MODS OR PLUGINS**
    - Sometimes mods or plugins can be the source of an issue, so before you submit, make sure it occurs without them.
- **Provide a clean [log file](https://wiki.resonite.com/Log_Files)** from replicating the issue
  - Except for [Diagnostic ones](#using-diagnostic-modsplugins), **Do not** use mods or plugins.
  - Launch the client, Load the replication item/world, Replicate the issue, Exit
  - If it's not possible to cleanly replicate the issue or it only occured once, you can provide whatever log you have (however still without mods!) - however note that this makes fixing the issue harder, so finding clean replication case can improve item's priority
  - For replication items, please provide the full item - the more steps it requires to assemble/replicate, the less priority we'll give the issue
- **Use objective, and respectful language** for anything submitted.
  - Follow our [Code of Conduct](CODE_OF_CONDUCT.md) 
- **Use a short, but descriptive title**, as vague titles
  - For example use instead of "System breaks when used with Other system", instead of "System Issue".
- **Be succinct and to the point**, because we tackle a lot of issues.
  - Imagine you have just 30 seconds to explain to us what is wrong.
  - If we need to read long paragraphs or watch long videos to understand an issue, then we are less likely to prioritize it.
- **Be specific** when possible, because vague statements can be hard to interpret.
  - For example instead of "It took a long time to finish", say "It took about 30 minutes to finish".
  - For some users, a minute is a long time, and for others, an hour is a short time.
  - Provide **exact** replication steps. Any vague steps can make replication difficult, because we won't know what exactly you did.
- **Provide accurate updates** if something changes with the issue.
  - If occurs more frequently, has additional, or changed replication steps then update us with a comment on the issue.
- **When asked for additional info, try to provide exactly what was asked**.
  - There are a variety of technical reasons why we need precisely what we ask for and missing the information may prevent us from progressing on an issue.
-   For example, if we ask to provide a screenshot of something, don't provide a video instead - this makes it harder for us to parse and look through.
- **Fill out all the information you have at the time** - in other words, do not create "blank" or "placeholder" issues to fill out later. Once you submit an issue, it pops a notification and we might check it right away, only to find that it's not ready. The issue should be fully ready for us to tackle at the at the time of submission.
- **Do not refer to projects we worked on in the past** we're unable to use materials or issues from past projects.

# Reporting crashes
For hard crashes - when Resonite locks up entirely and/or shuts down we will typically need crash logs & crash dumps as well.

How to find crash logs: https://wiki.resonite.com/Log_Files

# How we prioritize issues
We use several factors when prioritizing issues. If you'd like to learn more and help increase the likelihood that your issue gets addressed, [read our HOW_WE_PRIORITIZE document here](HOW_WE_PRIORITIZE.md).

# Using Diagnostic mods/plugins
We will accept additional diagnostic data produced by mods specifically made to diagnose a given issue and provide more helpful context and information. In some cases, these might be necessary to demonstrate certain issues, as they might not be visible directly or show in the log or can provide helpful information to help us narrow down the issue faster.

If you want to create and use such a mod/plugin for a report, please ensure the following:
- The issue must still occur without any mods present - in other words, ensure that the issue is a problem with the vanilla client
- Please provide the diagnostic data in the issue itself - we will typically not run third party mods or plugins ourselves
- Providing the source of the mod can be helpful as well to provide more context, even when we don't run it

**Thank you for your reports, and feedback.**

# Github Posting Guidelines

We have a few guidelines to keep in mind when submitting new issues:


- Keep discussion relevant to the issue. 

- Please follow the direction of the developers in closing or resolving issues. Do not harass or otherwise attack developers if you disagree with the closing or direction provided concerning an issue.

- Keep discussion civil. Arguments and personal disagreements should be brought to private messages, and  be respectful of the work of other users and other platforms. Entering into the repository with the intention to start arguments will lead to your removal.

- All posts must be compliant with Github’s rules on appropriate content. 

- Adult, Hateful or Obscene Content is not allowed in this Github. Please keep posts in the Github compliant with the broader Resonite Usage Guidelines.

- Respect the identity of others. Use the names and pronouns that others request. If you make an honest mistake, simply correct yourself and move on. When in doubt, use neutral terms such as "They" or "Them". Debates on or rhetoric against trans identities, rights, or existence will not be tolerated here. We believe these conversations to be harmful, not political, and do not have a place here.
