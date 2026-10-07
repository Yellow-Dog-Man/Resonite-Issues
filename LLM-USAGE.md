# LLM Usage Policy
This is a moderation policy for how LLMs are used in all `Yellow-Dog-Man` public repositories. This policy applies to both official Yellow Dog Man Studio s.r.o. contributors and staff members, as well as any 3rd party community contributors.

The policy also applies to `Yellow-Dog-Man` private repositories with additional restrictions covered by internal team AI policy (TODO: Add link).

This policy does **NOT** apply to any content published on the Resonite platform itself, which is covered by a separate policy (TODO: Add link).

For additional information about the policy itself, including exact scope, see [the appendix](#appendix).

This policy has been adapted from the [Rust language LLM policy](https://forge.rust-lang.org/policies/llm-usage.html), available under MIT license and is under the same license.

### Why we chose to adopt Rust policy as basis
At the time of adoption, we are a small team and navigating this space if both difficult and time consuming. With the increase of open source components of Resonite and the number of community contributors with different stances on use of AI, we require a clear and comprehensive policy to address use of LLMs by some contributors.

The Rust language policy is comprehensive, well written, tested by a large community of developers and has sufficient level of caution that we want for our open source components, while not requiring significant amount of time investment from our end to enforce this policy.

It also ensures that we do not introduce any substantial AI generated code (apart from trivial auto-completion) into the Resonite project.

### Changes from original Rust policy
Below are the major changes made to this policy for our usage:

- Changed wording to cover `Yellow-Dog-Man` public repositories
- Removed/changed Rust specific references
- Removed sections relating to other Rust policies
- Removed Experimentation section
     - We do not have bandwidth to review and evaluate experimental PR's produced by LLMs, we leave this to the Rust language repository
     - It is also unecessary for our use, as experimentation does not require creation of PRs against our repositories
     - If you wish to experiment, please do so on your personal forks. Any PR's against this organization must follow this policy

## Overview

Using LLMs while working on any repositories under the `Yellow-Dog-Man` organization is conditionally allowed, when done with care.
LLMs are not a substitute for thought,
and we do not allow them to be used in ways that risk losing our shared social and technical understanding of the project,
nor in ways that hurt our goals of creating a strong community.

We are aware that many clauses in this policy are unenforceable.
Our goal is *not* to catch every violation (see [It's not your job to play detective](#its-not-your-job-to-play-detective), below).
Instead, our goal is to remove plausible deniability: to force a choice between following the policy and intentionally violating it.
See [Money laundering and AML compliance](https://www.bitsaboutmoney.com/archive/money-laundering-and-aml-compliance/) for more background about the motivation.

The policy's guidelines are roughly as follows:

> It's fine to use LLMs to answer questions, analyze, distill, refine, check, suggest, review. But not to **create**.

> LLMs work best when used as a tool to write *better*, not *faster*.

### Moderation vs guidance

This document only contains our moderation policy.

## Rules
### Legend
- ✅ Allowed.
- ❌ Banned.
- ⚠️ Allowed with caveats. Must disclose that an LLM was used.
- ℹ️ Adds additional detail to the policy. These bullets are normative.
- 🔨 Violating this clause counts as a violation of the Code of Conduct.

### Summary
- ✅ Allowed: Private use.
- ❌ Banned: LLM-created comments, docs, or diagnostics. Replacing human judgement with LLM judgement. Requiring people to use an LLM to contribute.
- ⚠️ Conditionally allowed: Trivial changes, machine translation, LLM reviews and review bots
- 🔨 Carries a moderation penalty: Lying.

### Non-exhaustive policy

This policy does not aim to be exhaustive.
If you have a use of LLMs in mind that isn't on this list, talk to people about it, and judge it in the spirit of this overview:
- Using an LLM for your own personal use is likely allowed ✅
- Showing LLM output to another human without solicitation is likely banned ❌
- Making a decision that affects others based on LLM output requires disclosure ⚠️

### ✅ Allowed
The following are allowed.
- Any use of an LLM where you are the only one who sees the output. For example:
  - Asking an LLM questions about an existing codebase.
  - Asking an LLM to summarize comments on an issue or PR.
      - ℹ️ This does not allow reposting the summary publicly. This only includes your own personal use.
  - Asking an LLM to privately review your code or prose.
      - ℹ️ This does not apply to public comments by the LLM. See "review bots" under ⚠️ below.
  - Writing dev-tools for your own personal use using an LLM.
  - Using an LLM to generate possible solutions to an issue, learning from them, and then writing something from scratch in your own style.

### ❌ Banned
The following are banned.
- Comments that are originally created by an LLM posted from a personal user account.
    - ℹ️ This also applies to issue bodies and PR descriptions.
    - ℹ️ This also applies to voice/video content originally created or scripted by an LLM.
    - ℹ️ This does not apply if the LLM content is clearly quoted and marked; you can post that.
         However, the content of the comment must stand on its own even without the LLM content; it's not a substitute for your own words.
    - ℹ️ See also "machine-translation" in ⚠️ below.
    - ℹ️ See also "Scope" in the appendix below.
- Documentation that is originally created by an LLM.
    - ℹ️ This includes non-trivial source comments, such as doc-comments, safety comments, or multiple paragraphs of non-doc-comments.
    - ℹ️ This includes compiler diagnostics.
         LLMs are conditionally allowed to assist with the *logic* surrounding a diagnostic (see "Experiment: LLM-created code changes" below),
         but they must not be used to create the message itself.
    - ℹ️ This does not include "trivial" changes (see ⚠️ below).
- Policies or processes that are written such that an LLM is required to execute them.
    - For example, you must not *only* document where tests live with an `AGENTS.md`.
      Documentation must be authored for humans primarily, and LLM documentation may only summarize it, not add new detail.
- Treating an LLM review as a sufficient condition to merge or reject a change.
  LLM reviews, if enabled, **must** be advisory-only.
  Teams can have a policy that code can be merged without review, and they can have a policy that code must be reviewed by at least one person,
  but they may not have a policy that an LLM review substitutes for a human review.
    - ℹ️ See "review bots" in ⚠️ below.
    - ℹ️ An LLM review does not substitute for self-review. Authors are expected to review their own code before posting and after each change.

### ⚠️ Allowed with caveats
These uses are allowed on a case-by-case basis, under the rules below.
If you are a new contributor, you should expect to be scrutinized more heavily than existing contributors,
since you haven't yet established trust with your reviewers.

All uses under "⚠️ Allowed with caveats" **must** disclose that an LLM was used.

- Using machine-translation (e.g. Google Translate) from your native language without posting your original message is allowed but discouraged.
  Doing so can introduce new miscommunications that weren't there originally, and prevents someone who speaks the language from providing a better translation.
    - ℹ️ Posting both your original message and the translated version is always ok, but you must still disclose that machine-translation was used.
- "Trivial" code or prose changes.
    - ℹ️ Changes are trivial if there is no other way to write them, or the other ways to write them are nearly identical. For example, the following are all trivial:
        - Typo fixes
        - Markdown links
        - Changing a word to a synonym
        - Type signatures for a interface implementation
    - For more background about concepts that inspired this policy, see
      [threshold of originality](https://fsfe.org/news/2025/news-20250515-01.en.html)
      and [the Google v Oracle ruling](https://en.wikipedia.org/wiki/Google_LLC_v._Oracle_America,_Inc.) that copying API declarations is fair use.
- Using an LLM to discover bugs, as long as you personally verify the bug.
    - ℹ️ This also includes reviewers who use LLMs to discover flaws in unmerged code.
    - ℹ️ See also "Comments \[...\] posted from a personal user account" under ❌ above.
- Using an LLM as a "review bot" for PRs.
    - ℹ️ Review bots that post without being approved by a maintainer will be banned.
         This is a one-time approval; maintainers don't need to approve individual reviews.
    - ℹ️ Review bots **must** have a separate GitHub account that clearly marks them as an LLM.
      You **must not** post (or allow a tool to post) LLM reviews verbatim on your personal account unless clearly quoted with your own personal interpretation of the bot's analysis.
    - ℹ️ Review bot accounts must be blockable by individual users via the standard GitHub user-blocking mechanism. (Note that some GitHub "app" accounts post comments that look like users but cannot be blocked.)
    - ℹ️ LLM comments **must not** be blocking; reviewers must indicate which comments they want addressed.
        - In other words, reviewers must explicitly endorse an LLM comment before blocking a PR. They are responsible for their own analysis of the LLM's comment and cannot treat it as a CI failure.
    - ℹ️ This does not apply to private use of an LLM for reviews; see ✅ above.

## Appendix
### Scope

This policy applies to all public repositories under the `Yellow-Dog-Man` organization (you can view full list here: https://github.com/Yellow-Dog-Man), both for official staff and any 3rd party contributors.

Additionaly it applies to private `Yellow-Dog-Man` repositories with additional restrictions detailed in the internal team AI policy (TODO: Add link).

The following are not in scope and are free to set their own policies:
- Forks of any `Yellow-Dog-Man` repositories
    - This only applies as long as no PR's or contributions are pushed upstream
    - Any upstream contributions must follow this policy
- 3rd party libraries, mods and any other repositories related to the Resonite project, but not under the official `Yellow-Dog-Man` account
- Upstream changes in `Yellow-Dog-Man` dependency forks
    - We do not control policies of any 3rd party projects that we might be using as dependencies
    - Any changes coming from upstream sources are not (and can not be) covered by this policy
    - Direct contributions against our forks are covered by this policy
- User content published on the Resonite platform
    - This is covered by separate policy (TODO: Add link)
- Official Resonite assets
    - These are covered by internal team AI policy (TODO: Add link)

For example, the following do not fall under the policy:
- Tracking issues for T-lang
- T-lang proposals
- T-lang stabilization reports
- Language documentation
- The style guide
- Names of compiler lints. This only applies to the names themselves; the diagnostic messages are still covered under this policy.
- Direct quotes from any of the above in documentation or diagnostics.

### Motivation and guiding principles

There is not a consensus within the Resonite community—and likely never will be—about when/how/where it is acceptable to use AI-based tools.
Many members of the Resonite project and community find value in AI;
many others feel that its negative impact on society and the climate are severe enough that no use is acceptable.
Still others are working out their opinion.

Despite these differences, there are many values we all share:

- Building a community of deep experts in our collective projects.
- Building an inclusive community where all feel welcome and respected.

And many facts we agree on:

- Many people find LLM-generated code and writing deeply unpleasant to read or review.
- Many people find LLMs to be a significant aid to learning and discovery.
- LLMs are a new technology, and we are still learning how to use, moderate, and improve them.

With those facts and values in mind, the policy is designed with the following goals:

- Build an intentionally conservative policy that lets us maintain desired standard of quality
- Limit LLM contributions to the very highest standard of quality, following Rust language's guideline of "better, not faster"
- Make the policy enforceable and easy to moderate.
- Make the policy consistent and easy to understand and summarize, even for people who haven't read it in detail.
- Avoid making LLMs a requirement to contribute, to be inclusive of contributors who choose not to use them

### Moderation policy
#### It's not your job to play detective
["The optimal amount of fraud is not zero"](https://www.bitsaboutmoney.com/archive/optimal-amount-of-fraud/).
Don't try to be the police for whether someone has used an LLM.
You are not required to "actively look" for whether an LLM was involved.

Style is not evidence, and English-as-a-second-language speakers, neurodivergent people, and over-explainers are the most likely to be accused of writing like an LLM.

If it's clear someone's broken the rules, point them to this policy;
otherwise, strongly prefer [reporting to mods](https://moderation.resonite.com) over public accusations.
Reporting to moderation is not intended to be a penalty;
the mod team is interested in seeing non-violations as well as violations.
As always, the mod team is free to exercise their own judgement and discretion.

#### Be honest
Conversely, you're expected to be honest about your use of LLMs and the extent of that use.
If you are not sure where something you would like to do falls in this policy, please talk to the engineering team (either through office hours, creating a discussion/issue on GitHub seeking clarification).
Don't try to hide it.

Deliberately misrepresenting your use of LLMs is not welcome and may result in moderation action.

#### Penalties
The policies marked with a 🔨 follow the same guidelines as the code of conduct:
Violations will first result in a warning, and repeated violations may result in a ban.
- 🔨 Violations of the "Be honest" section

Other violations are left up to the discretion of reviewers and moderators.
For minor violations we recommend telling the author that we can't review the PR until it complies with the policy, with pointers to exactly what they need to do.
For major violations or extractive PRs, we recommend closing the PR or issue.

It is **not** ok to harass a contributor for using an LLM.
All contributors must be treated with respect.
The Code of Conduct applies to *all* conversations in the `Yellow-Dog-Man` repositories and other official channels.

### Responsibility

Your contributions are your responsibility; you cannot place any blame on an LLM.
- ℹ️ This includes when asking people to address review comments originally created by an LLM. See "review bots" under ⚠️ above.

### The meaning of "originally created by an LLM"

This document uses the phrase "originally created by an LLM" to mean "text that was generated by an LLM (and then possibly edited by a human)".
No amount of editing can change how it was originally created;
the origin sets the initial style, and that style is very hard to change once it's set.

For more background about analogous reasoning, see ["What Colour are your bits?"](https://ansuz.sooke.bc.ca/entry/23).

This policy makes no distinction between LLM output that comes from a chat interface and output that comes from editor auto-completion.
In most cases the output is "trivial" (see above under ⚠️), but regardless, it is not treated specially by this policy.

### Conditions for modification or dissolution
This policy is not set in stone, and we can evolve it as we gain more experience working with LLMs.

Minor changes, such as typo fixes, only require a normal PR approval.
Major changes, such as adding a new rule or canceling an existing rule, require approval from the Yellow Dog Man Studios s.r.o. staff.

This policy can be dissolved only by a decision from Yellow Dog Man Studios s.r.o. staff that has been discussed and approved by an engineering lead.
