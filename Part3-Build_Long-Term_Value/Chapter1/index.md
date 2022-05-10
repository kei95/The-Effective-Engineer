# Chapter 1 - Balance Quality with Pragmatism

- Code quality boils down to a matter of tradeoffs, and there’s no one universal rule for how to do things.
- Rather than thinking in terms of “right or wrong”, you should think “work and doesn’t work”

## **1. Establish a Sustainable Code Review Process**

Benefits of code review are the following;

- **Catching bugs or design shortcomings early**
    - A 2008 study of software quality scross 12,500 projects from 650 companies found that  a pass of design and code reviews remove, on average, 85% of remaining bugs
- **Increasing accountability for code changes**
    - You’ll have less chance to leave dirty mess change for other developers to fix that up later
- **Positive modeling of how to write good code**
    - code reviews can provide an avenue for shareing best practices
- **Sharing working knowledge of the codebase**
    - When someone reviews your code, this ensures that  at least one other person is familiar with your work and can address high-priority bugs or other issues in your absence
- **Increasing long-term agility**
    - Higher-quality code is easier to understand, quicker to modify, and less susceptible to bugs. These all translate directly into faster iteration speed for the engineering term.

## **2. Manage Complexity through Abstraction**

 *”Pick the right ones(abstractions), and programming will be a series of nasty surprises: interfaces will become baroque and clumsy as they are forced to accommodate unanticipated interactions, and even the simplest of changes will be hard to make”*

These are example of how the right abstraction increases engineering productivity 

- **It reduces the complexity of the original problem into easier-to-understand primitives**
    - Many problems can be expressed using a sequence of Map and Reduce transformations
- **It reduces future application maintenance and makes it easier to apply future improvements**
- **It solves the hard problems once and enables the solutions to be used multiple times**
    - A simple application of the DRY principle, a good abstraction consolidates all of the shared and oftentimes-complex details into one place. The solution pays off with every additional use

The right abstraction can increase engineering productivity by an order of magnitude.

Building a generalized solution takes more time than building one specific to a given problem.

Good abstractions should be:

- easy to learn
- easy to use even without documentation
- hard to misuse
- sufficiently powerful to satisfy requirements
- easy to extend
- appropriate to the audience

## **3. Automate Testing**

- The rate of error spikes whenever you make new features and it decreases over time.
    - To gain a confident of the bug fix, write test that covers the bug so that after the change gets merged into main branch, you are confident that the issue won’t reproduce ever again

Automated tests mitigate against a culture in which people are fearful of modifying and improving a piece of code just because it might break. So they make it easier to do future code transformations.

Without automated test, a problem takes longer to be discovered and often gets misrouted to whoever owns the feature that broke rather than whoever authored the change.

- Automation tests are favoured to be written by the author of the code, rather than the person who’s trying to modify the code in months or years later

**When you wanna start form scratch on a project that doesn’t have tests, start from the most valuable tests, and go from there.**

## **4. Repay Technical Debt**

**Technical debt refers to all the deferred work that’s necessary to improve the health and quality of the codebase and that would slow us down if left unaddressed.**

Technical debt doesn’t accumulate when we make quick and dirty workarounds. Whenever we write software without fully understanding the problem space, our first version will likely end up being less cleanly designed than we’d like - technical debt

- technical debt often is hard to quantify

Not all technical debt is worth repaying. Rather than blindly repaying technical debt wherever they find it, effective engineers spend their finite time repaying the debt with the highest leverage - code in highly trafficked parts of the codebase that takes the least time to fix up. These improvements generate the highest impact for your effort.

### Key Takeaways

- **Establish a culture of reviewing code**
    - Code reviews facilitate positive modeling of good coding practices.
- **Invest in good software abstractions to simplify difficult problems**
    - Good abstractions solve a hard problem once and for all, and significantly increase the productivity of those who use it
- **Scale code quality with automated testing**
    - A suite of unit and integration tests can help alleviate the fear of modifying what might otherwise be brittle code. Focus on ones that save the most time first
- **Manage your technical debt**
    - If you spend all your resources paying off interest on your debt, you won’t have enough time left to work on new things. Focus on the debt that incurs the most interest.