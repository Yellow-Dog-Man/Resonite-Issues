# Resonite Issues
Issue repository for Resonite. Please log any bug reports, or feature requests here using the appropriate template:

- [🐞 Report a bug](https://github.com/Yellow-Dog-Man/Resonite-Issues/issues/new?template=1-bug-report.yml)
- [💡 Request a feature](https://github.com/Yellow-Dog-Man/Resonite-Issues/issues/new?template=2-feature-request.yml)
- [📝 Report issue with official in-game content](https://github.com/Yellow-Dog-Man/Resonite-Issues/issues/new?template=3-content-issue.yml)
- [:lock: To Report a Security issue please open a ticket](https://support.resonite.com/)

## High level feedback
If you'd like to provide us with higher level feedback without focusing too much on technical details, we recommend creating a feedback issue! You can [learn more about these here](OBSERVATION_ISSUES.md)

- [🌟 Share Positive Observation / Feature Showcase](https://github.com/Yellow-Dog-Man/Resonite-Issues/issues/new?template=5-friction-point-observation.yml)
- [🧱 Share Friction Point Observation](https://github.com/Yellow-Dog-Man/Resonite-Issues/issues/new?template=6-positive-observation.yml)

Note that this is not a replacement for bug reports! To fix specific bugs we will still need a proper technical report with logs and everything.

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

# Why do we always need logs?
For bug reports, we always request log files to be included with the initial report. If the logs are not included, the issue will automatically labeled as Needing More Information, meaning we'll pay a lot less attention to it than issues that have everything in order. We **strongly** recommend making sure you have everything together when posting the issue to maximize likelyhood of it being prioritized.

It is important to include logs, even if you feel they are unecessary. There is a number of reasons for this:
- In most cases when people assume they are not necessary, they actually are.
   - Logs aren't just for errors, they contain a number of other diagnostic information that we might be looking for, that you're not aware of
   - E.g. we can determine sequence of certain events during reproduction
   - Sometimes we can also be looking for things *NOT* being in the log
   - They also tell us which modules, systems, drivers and other systems were initialized, which can help us resolve issues quicker
- They serve as "sanity check" before we start working on issues
   - We can be sure of what Resonite version and HW you're using (for example we've had cases where bugs were reported for really old versions of Resonite without the user realizing)
- Needing back & forth to get logs from the user wastes our time and mental focus
   - This is even worse when getting logs becomes an argument - the time we spend explaining why exactly we need particular log is time we spend not fixing issues
   - Our time is very limited - we are a small team and all we're asking of you is to make our job as smooth as possible, so we can address as many issues as we can
 
**It's better for issue to have a log and not need it, than need it and not have it.** It saves us a lot of the time. And we use the logs as "starting point" to work on issues a lot more than you'd think!
 
## What if I **REALLY** feel there's issues that don't need logs?
If even given above information you feel there's types of issues that do not require logs (or can't have any), we recommend following:
- If you're reporting undesirable behavior that isn't exactly bug, you can open a "Friction Point" issue
- For problems with external systems, create "External service" issue
- If you feel there's no category for the issue type you want to make, create "Friction Point" issue about this and we can add additional issue templates
   - E.g. "locale/typo" issue template
   - This will keep these focused on particular problems that do not involve logs

**Thank you for your reports, and feedback.**

# Github Posting Guidelines

We have a few guidelines to keep in mind when submitting new issues:


- Keep discussion relevant to the issue. 

- Please follow the direction of the developers in closing or resolving issues. Do not harass or otherwise attack developers if you disagree with the closing or direction provided concerning an issue.

- Keep discussion civil. Arguments and personal disagreements should be brought to private messages, and  be respectful of the work of other users and other platforms. Entering into the repository with the intention to start arguments will lead to your removal.

- All posts must be compliant with Github’s rules on appropriate content. 

- Adult, Hateful or Obscene Content is not allowed in this Github. Please keep posts in the Github compliant with the broader Resonite Usage Guidelines.

- Respect the identity of others. Use the names and pronouns that others request. If you make an honest mistake, simply correct yourself and move on. When in doubt, use neutral terms such as "They" or "Them". Debates on or rhetoric against trans identities, rights, or existence will not be tolerated here. We believe these conversations to be harmful, not political, and do not have a place here.

# Diagnosing confusing crashes
If Resonite suddenly crashes with no Unity crash log, this might be due to the OS taking the app down due to a very low level crash. Here's a good way to check those:

1) Open the Event Viewer in Windows
2) Under Windows Logs -> Application
3) Find recent Error / Application Error and open it
4) Check if the details mention Resonite. There should be basic info like this (note it might say Renderite.Host.exe instead of Resonite.exe):

<img width="1782" height="894" alt="8f095bd5-50a3-4bf9-873f-1122a32f6b05-1" src="https://github.com/user-attachments/assets/da234ce4-018e-407b-a6f4-de4fde72cb05" />

We'll need to gather crash dump to diagnose it. To do that follow these steps:
1) Enable User-Mode Dumps: https://learn.microsoft.com/en-us/windows/win32/wer/collecting-user-mode-dumps
2) Replicate the crash
3) Go to the folder configured in the step 1) and check if there's a .dmp file with corresponding timestamp.
4) Provide the .dmp file as part of your report 
