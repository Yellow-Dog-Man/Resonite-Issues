# Resonite Issues
Issue repository for Resonite. Please log any bug reports, or feature requests here using the appropriate template:

- [:bug: To Report a Bug Click Here](https://github.com/Yellow-Dog-Man/Resonite-Issues/issues/new?assignees=shiftyscales&labels=bug&projects=&template=bug-report.yml)
- [:computer: To Request a Feature Click Here](https://github.com/Yellow-Dog-Man/Resonite-Issues/issues/new?assignees=shiftyscales&labels=enhancement&projects=&template=feature-request.yml)
- [:paintbrush: To Report an Issue with Content such as the Cloud Home Click Here](https://github.com/Yellow-Dog-Man/Resonite-Issues/issues/new?assignees=shiftyscales%2C+AegisTheWolf%2C+RyuviTheViali%2C+RueShejn&labels=content&projects=&template=content-issue.yml)
- [:lock: To Report a Security issue please open a ticket](https://support.resonite.com/)

# Reporting Requirements
**Please ensure the following requirements are met** for anything submitted.

**FAILING TO FOLLOW THESE REQUIREMENTS MAY RESULT IN YOUR ISSUE GOING UNADDRESSED/BEING CLOSED**

- **Use the most recent version of Resonite** when replicating your issues (this helps ensure that issues are still relevant and replicable)
- **Try to search for existing issues** describing your problem before creating a new one (if an issue already exists for what you wish to report, please add to the existing issue instead)
- **Focus on the high-level issue first, not a specific solution** as this lets us approach the problem most efficiently. E.g. it's better to create an issue saying "I can't do X", rather than "Add a component that when this and this it does this". Often there are many different solutions to a problem and if you ask us to implement a very specific solution, instead of asking the problem you're trying to solve, you're more likely to get a lot of questions and possibly no. To learn more, check this page about the XY Problem: https://xyproblem.info/
- **Do not request overhauls of systems**, focus on the bugs or features you want. Whether or not to overhaul a particular system is something that the engineering team decides with the knowledge of the codebase, other issues and long-term plans. If you specifically request a problem to be solved by overhauling the entire system, you're much more likely to receive pushback on this. If you want to consider several issues for a single subsystem without specific solutions, you can [start a discussion](https://github.com/Yellow-Dog-Man/Resonite-Issues/discussions)
- **Do not hijack issues for another feature/bug**, make another issue instead. Issues should never have comments of similar to "While you're at it, can you also do this?", it will not be considered and will get lost when the original problem in the issue gets solved.
- **Try to troubleshoot** and isolate the problem first before reporting it (e.g. if it is a complex ProtoFlux creation try to identify the specific node/node group that is not behaving as expected- strip down as much as possible from the item/world while still producing the bug)
- **Ensure that the issue happens WITHOUT MODS OR PLUGINS** - sometimes mods or plugins can be the source of an issue, so before you submit, make sure it occurs without them.
- **Provide a clean [log file](https://wiki.resonite.com/Log_Files)** from replicating the issue (do not use mods or plugins except for diagnostic ones (see below), launch the client, load the replication item/world, replicate the issue, and exit)
- **Use objective, and respectful language** for any posts/comments submitted (negativity, hateful/angry issues/comments are liable to be edited or removed)
- **Use a short, but descriptive title**, as vague titles (e.g. "Issue with system" instead of "System breaks when I grab thing") are much more likely to get overlooked and skimmed over
- **Be succinct, but to the point**, because we tackle a lot of issues. Imagine you have just 30 seconds to sell us on why something is a good idea to put our time towards. If we need to read long paragraphs or watch a long video to understand, we are much less likely to prioritize a given issue
- **Be specific** when possible, because vague statements can be hard to interpret. For example instead of "It took a long time to finish", say "It took about 30 minutes to finish". "Long" can mean different amounts in different contexts - for some things a minute is a long time,  for others an hour is a short time.
- **Provide accurate updates** if something changes with the issue, which makes the original sample or reproduction steps work, but the issue still persists with other cases, make sure to include the information with your updates.
- **When asked for additional info, try to provide exactly what was asked**. We understand you want to be helpful and provide what you think might be even better than what we asked for in clarifications, but this is not always the case. We usually have very specific technical reasons when we request additional information and providing something else, even if it seems similar, might be missing some crucial components or make things more difficult. E.g. if we ask to provide a screenshot of something, don't provide a video instead - this makes it harder for us to parse and look through.
- **Do not refer to projects we worked on in the past** we're unable to use materials or issues from past projects.

# How we prioritize issues
We use a number of factors when prioritizing issues. If you'd like to learn more and help increase the likelihood that your issue gets addressed, [read our HOW_WE_PRIORITIZE document here](HOW_WE_PRIORITIZE.md).

# Using Diagnostic mods/plugins
We will accept additional diagnostic data produced by mods specifically made to diagnose given issue and provide more helpful context and information. In some cases these might be necessary to demonstrate certain issues, as they might not be visible directly or show in the log or can provide helpful information to help us narrow down the issue faster.

If you want to create and use such a mod/plugin for report, please ensure the following:
- The issue must still occur without any mods present - in other words, ensure that the issue is a problem with the vanilla client
- Please provide the diagnostic data in the issue itself - we will typically not run third party mods or plugins ourselves
- Providing the source of the mod can be helpful as well to provide more context, even when we don't run it

**Thank you for your reports, and feedback.**
