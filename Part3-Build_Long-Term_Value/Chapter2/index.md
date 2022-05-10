# Chapter 2 - Minimize Operational Burden

It is tough to minimizing the tax - the cost of scaling up, bug fixes and transferring ever-growing institutional knowledge etc.

“Every single, additional [technology] you add, is guaranteed mathematically over time to go wrong, and at some point, you’ll have consumed your entire team with operations.”

In this chapter, we’ll examine strategies for minimizing operational burden.

## 2. Embrace Operational Simplicity

Effective engineers focus on simplicity. Simple solutions impose a lower operational burden because they’re easier to understand, maintain and modify.

- Do the simplest thing first. On any stuff you do.
    - e.g. - In reviewing each other’s designs, the team would ask, “Is this the simplest thing?” or, “Is the simplest thing sto create an entirely new system for this one feature you’re writing?”
    - If the answer was no, then they reconsidered their approach.

The additional complexity may be a necessary evil —— but oftentimes, it’s not.

Steve Jobs goes; *“When you first start off trying to solve a problem, the first solutions you come up with are very complex, and most people store here. But if you keep going, and live with the problem and peel more layers of the onion off, you can oftentimes arrive at some very elegant and simple solutions. Most people just don’t put in the time or energy to get there.”* 

When engineering teams don’t focus on doing the simple thing first, they either end up being less effective over time because their energy is spent on a high upkeep const, or they reach a point where the operational burden gets so high that they’re forced to simplify their architecture.

Having too complex of an architecture imposes a maintenance cost in a few ways:

- Engineering expertise gets splintered across multiple systems.
- Increased complexity introduces more potential single points of failure
- New engineers face a steeper learning curve when learning and understanding the new systems
- Effort towards improving abstractions, libraries, and tools gets diluted across the different systems

Simplicity provides high leverage. That lesson applies to a variety of scenarios:

- It’s fine to experiment with a new programming language for a prototype or toy project, but thing hard before using it in a new production system. Do other team members have experience with the language? Is it easy to pick up? Will it be hard to hire engineers fluent in it?
- Proponents of new data stores promise that their systems solve the problems in battle-tested relational database like MySQL and PostgreSQL. Before using these new storage systems in production, however, do you research. Find out if other teams have successfully used them for projects of similar scope and whether they have actually been able to maintain and scale them with lower operational burden than more standard solutions.
- When tackling a new problem, consider whether repurposing an existing abstraction or tool would be simpler than developing a custom solution. People often say, “Use the right tool for the job” —— but that can also increase the number of moving parts. Does the complexity of having more parts outweigh the benefits of simplicity through standardization?
- If you’re processing large amounts of data, consider whether the data is actually large enough such that you need a distributed cluster, or whether a single, beefy machine will suffice. Clusters are harder to manage and debug than single machines.

**Remember: do the simple thing first. Always ask, “What’s the simplest solution that can get the job done while also reducing our future operational burden?” Revisit sources of complexity, and find opportunities to trim them away.**

## 3. Build Systems to Fail Fast

Many engineers(no necessarily engineers, too) associate robustness and reliability with an absence of crashes. They spend their energy adding workarounds to automatically handle software errors so that their programs can continue to function. Workarounds may include setting misconfigured parameters to default  values, adding catch-all exception handlers to deal with unexpected issues, and swallowing unexpected return values.

These techniques cause software to *fail slowly.* The software may continue to run after an error, but this is often in exchange for less decipherable bugs further down the road.

“Fail fast” is the valuable technique for such problem. It’s a nonintuitive technique: “failing immediately and visibly” sounds like it would make your software more fragile, but it actually makes it more robust. Bugs are easier to find and fix, so fewer go into production.

Examples of failing fast include:

- Crashing at startup time when encountering configuration errors
- Validating software inputs, particularly if they won’t be consumed until much later
- Bubbling up an error from an external service that you don’t know how to handle, rather than swallowing it
- Throwing an exception as soon as possible when certain modifications to a data structure, like  a collection, would render dependent data structures, like an iterator, unusable
- Throwing an exception if key data structures have been corrupted rather than propagating that corruption further within the system
- Asserting that key invariants hold before or after complex logic flows and attaching sufficiently descriptive failure message
- Alerting engineers about any invalid or inconsistent program state as early as possible

The more complex the system, the more time that fail-fast techniques can save.

Building systems to fail fast can be a very high-leverage activity. It helps reduce the time you spend maintaining and debugging software by surfacing problematic issues sooner and more directly.

## 4. Relentlessly Automate Mechanical Tasks

When deciding whether to automate, the judgement call that an engineer must make is: *will I save more time overall by manually doing  a particular task or by paying the upfront cost of automating the process?*

Engineers automate less frequently than they should, for a few reasons:

- **They don’t have enough time right now**
    - Upcoming deadlines and managerial pressure often prompt engineers to sacrifice the long-term benefits of automation for the short-term benefit of shipping a product sooner.
- **They suffer from the *tragedy of commons***
    - Which is; individuals act rationally according to their own self-interest but contrary to the group’s best long-term interests.
    - When manual work is spread across multiple engineers and teams, it reduces the incentive of any individual engineer to spend the time to automate.
- **They lack familiarity with automation tools**
    - Many types of automation rely on systems skills that non-systems engineers are not as familiar with. It takes time to learn how to quickly assemble command-line scripts, combine UNIX primitives, and hack together different services. Like most skills, however, automation gets easier with practice.
- **They underestimate the future frequency of the task**
    - It’s fairly straightforward to update  a script, but manually redoing the entire task over  and over again is time-consuming
- **They don’t internalize the time savings over a long time horizon**
    - Saving 10 seconds per task might not seem like  a big deal, even if it happens 10 times a day. But over  the course of year, thats’ almost an entire workday saved.

Every time you do something that machine can do, ask yourself whether it’s worthwhile to automate it.

Activities where automation can help in include:

- validating that  a piece of code. an interaction, or a system behaves as expected
- Extracting, transforming, and summarizing data
- Detecting spikes in the error rate
- Building and deploying software to new machines
- Capturing and restoring database snapshots
- Periodically running batch computations
- Restarting a web service
- Checking code to ensure it conforms to style guidelines
- Training  a machine learning model
- Managing user accounts or user data
- Adding or removing a server to or from a group of services

## 5. Make Batch Processes Idempotent

As you automate more operations, your time’s leverage increases — but so does the probability that some of you automation will fail. Scripts executing a sequence of actions without human intervention(also known as *batch processes*)that you schedule to run periodically, will hit network timeouts or unexpected hiccups.

You’d end up spending so much time on fixing that if you’re not careful. Therefore, minimizing that burden is a high-leverage activity.

- One technique to make batch processes easier to maintain and more resilient to failure is to make them *idempotent*
    - idempotent process produces the same results regardless of whether it’s run once  or multiple times.
    - With that, you can reduce the risk of unexpected side effects

## 6. Hone Your Ability to Respond and Recover Quickly

No matter how careful we are, unexpected failures will always occur. Therefore, how we handle failures plays  a large role in our effectiveness. At some point, it becomes higher leverage to focus our time and energy on our ability to recover quickly than preventing failures in the first place.

Some company does simulation of failure. Google does Disaster Recovery Testing events, and Dropbox simulates additional load for their production systems. Doing so enables them to artificially trigger issues sooner; It’s better to deal with such scenario rather than in production which when they can’t even turn it off.

- What if a critical bug gets deployed as part of a release? How quickly can we roll it back or respond with a fix, and can we shorten that window?
- What if a database server fails? How do we fail over to another machine and recover any lost data?
- What if our servers get overloaded? How can we scale up to handle the increased traffic or shed load so that we respond correctly to at least some of the requests?
- What if our testing or staging environments get corrupted? How would we bring up a new one?
- What if a customer reports an urgent issue? How long would it take customer support to notify engineering? How long for engineering to follow up with a fix?

## Key Takeaways

- **Do the simple thing first**
    - Simpler system are easier to understand, extend, and maintain
- **Fail fast to pinpoint the source of errors**
    - Make debugging easier by not masking your errors and by not deferring failures until later
- **Automate mechanics over decision-making**
    - Aggressively automate manual tasks to save yourself time. At the same time, think twice before trying to automate decision-making, which tends to be hard to get correct
- **Aim for idempotence and reentrancy**
    - These properties make it easier for you to retry actions in the face of failure
- **Plan and practice failure modes**
    - Building confidence in your ability to recover lets you proceed more boldly