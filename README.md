# RFCs

The RFC process aims to leverage the collective ideas, insights, and experience of the tech community to improve the development experience. Its primary goal is to maintain the vision and conceptual coherence of technical decisions.

# What is an RFC?

RFC is an acronym for 'Request for Comments'. It is a platform to float and polish an idea before implementation. It provides a basic description of a problem, proposed implementation with high (and sometimes low) level detail, and a roadmap for seeing the implementation move from idea to reality.

RFCs should be typically be reserved for any significant system design or team process items where the implementation path is perhaps not clear from the outset, and the problem needs to be systematically deconstructed to arrive at a viable consensus.

An RFC should not consist only of a problem statement (use a standard issue for that).

An RFC should not be used for bug reports or trivial discussions - the overhead of compiling an RFC does not justify it.

# RFC process

Before submitting an RFC, it is a good idea to discuss your aims with your team to get early feedback.

- Recruit reviewers from the project maintainers of the area for your RFC concerns.
- Submit your RFC as a pull request to `master` branch.
- Name your RFC file using the template YYYYMMDD-filename.md, where YYYYMMDD is the date of submission, and 'filename' relates to the title of your RFC. For instance, if your RFC is titled "Integrate codegen for localizable strings", you might use the filename 20200110-codegen-localization.md. If you have images or other auxiliary files, create a directory of the form YYYYMMDD-filename in which to store those files.
- At the top of the PR, identify how long the comment period is going to be active and follow the template.
- Assign label that RFC is referencing to notify dedicated channels in Slack.
- The reviewers may approve the RFC, reject it, or require changes before it can be considered again, based on a vote. Approved RFCs will be merged into community/rfcs, and rejected RFCs will have their PRs closed.
  Implementations of a successful RFC should reference it in their documentation, and work with the sponsor to successfully land the code.

While implementation code is not necessary to start the RFC process, its existence in full or part may help the design discussion.

# How to write an RFC

RFC's should be created as a separate branch from the provided template and should consist of the following key elements:

- **Title**: The title should be succinct and explanatory.

- **Introduction**: A short description of what the feature is. Try to keep it to a single-paragraph "elevator pitch" so the reader understands what problem this proposal is addressing.

- **Motivation**: Describe the problems that this proposal seeks to address. If the problem is that some typical pattern is currently hard to express, show how one can currently get a similar effect, and describe its drawbacks.

- **Proposed solution**: Describe your solution to the problem. Provide examples and describe how they work. Show how your solution is better than current workarounds: is it cleaner, safer, or more efficient?

- **Detailed design**: Describe the design of the solution in detail. If it's a new API, show the full API and its documentation comments detailing what it does. The detail in this section should be sufficient for someone who is _not_ one of the authors to be able to implement the feature reasonably.

* **Record of Votes**: In this section, the RFC convenor should record all the final votes for the RFC in the following manner:

  | Vote | Name    |
  | ---- | ------- |
  | +1   | Vlad Z. |

# Commenting on an RFC

Use the commenting tools in the Github to add comments to the RFC. The original RFC should be updated as the discussion evolves in order to always reflect the current state of the proposal.

# Approval of an RFC

A simple voting system should be used whereby interested and affected parties add a comment to the RFC according to the following scheme:

- `-1` - I strongly **disagree** with the proposal
- `0` - I am not engaged enough with the proposal to be able to provide an informed assent or dissent. This is tacit agreement to continue if there are sufficient +1 votes or to abstain if there are sufficient votes.
- `+1` - I strongly **agree** with the proposal

If sufficient requests are made (or insufficient feedback is provided), the proposer should call the upon the interested and affected parties to cast their votes, or extend the deadline.

When casting a vote of disagreement, the voter should indicate whether they are willing to entertain a revised version of the proposal, or if they reject the idea outright.

# Implementation of an RFC

Once the RFC comment period has concluded, and approval has been given, the implementation should be carried out as a series of story tickets. The individual tickets are going to break down the RFC into actionable atomic components and optionally distribute the actual implementation work between one or more developers.
