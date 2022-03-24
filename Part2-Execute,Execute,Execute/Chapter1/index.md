# Chapter 2 - Invest in Iteration Speed

Effective engineers and teams tend to have good understanding and implement solid continuous integration schema. That would help hundreds of hours and eventually make your work focused on what really matters like coding. In this chapter, the author will go over what we can do to make more daily work automated and efficient.

## **1. Move Fast to Learn Fast**

As facebook's belief ***"Move  fast and break things“***, it’s important to move fast and making changes even though it breaks something. If you iteration speed of the development is fast, you should  be able to fix that and apply the change quickly too. Hence it’s a high-leverage decision.

In order to make faster, there’re several actions you can take, this Chapter is about actionable items you can work on.

## 2. **Invest in Time-Saving Tools**

Boddy Johnson, a former facebook Director of Infrastructure Engineering says “A very good indicator of future success was if the first thing someone did on a problem was to write a tool”

Similarly, Raffi Krikorian, former VP of Platform Engineering at Twitter keeps his teammates as following “If you have to do something manually more than twice, then write a tool for the third time.”

- Tools are multipliers that allow you to scale your impact beyond the confines of the say.
- Time-saving tools pay off large dividends

Even though your tools is objectively superior to the existing one, sometimes, switching costs discourage other engineers from actually changing their workflow and leaning your  tool.

- Start small - Find an area where a tool could save time, build it, and demonstrate its value.
- Don’t let the pressure to constantly ship new features cause the important but non-urgent task to building time-saving tools to fall by the wayside

## 3. Shorten Your Debugging and Validation Loops

When you finish implementing new feature or bug fix, it makes you feel like you are done with that, but you should spend some effort to make debugging and validation easier in the future. 

Even though you have the flow that works already, you should also doubt that there’s no any other way to make it better.

- The extra investment in setting up a minimal debugging workflow can help you fix an annoying bug sooner and with less headache.
- “Effective engineers have an obsessive ability to create tight feedback loops for what they’re testing”

**When you find yourself going through the same motions when you’re fixing a bug or iterating on a feature, pause.**

**Take a moment to think through whether you might be able to tighten that  testing loop. It could save you time in the long run**

## 4. Master Your Programming Environment

If you have some un-efficient step you take in your programming environment such as file search, try to make it more easy and less time-consuming by researching some technique or tools  or shortcut provided by the editor or the environment.

These small updates on your work might be too less impactful at glance, but considering you’ll be doing the same thing hundreds of thousands of times, it easily compounds to a big number of hours over time.

There’re some tips to gain your fundamental programming skills

- **Get proficient with your favorite text editor or IDE.**
    - Also you  can ask effective co-worker or friends if you can observe their work, they often have some secret make their work efficient.
- **Learn at least one productive, high-level programming language**
- **Get familiar with UNIX shell commands**
    - Being able to manipulate and process data with basic UNIX tools instead of writing a python or java can reduce the time to complete a task from minutes down to seconds.
    - Learn basic commands like `gerp` , `sort`, `uniq`, `wc`, `awk`, `sed`, `xargs` and `find`
- **Prefer keyboard over the mouse**
    - know shortcuts that can replace your house, it’ll save lots of time
- **Automate your manual workflows**
    - developing such skill takes time, whether they be using shell scripts, browser extensions, or something else. But the cost of mastering these skills gets smaller the more often you do it and the better you get at it
- **Test out ideas on an interactive interpreter**
    - save-and-go kind of interpreter(metro, ews etc), allows you to evaluate and test out expressions. Use them to build confidence that your program behaves as expected.
    - That will provide significant boost in iteration speed.

No one can master these in the first place. Mastery is a process, bot an event.

## 5. Don’t Ignore Your Non-Engineering Bottlenecks

The best strategy for optimizing your iteration speed is the same as for optimizing the performance of any system: identify the biggest bottlenecks, and figure out how to eliminate them. But sometimes, non-engineering constraints may also hinder your iteration speed.

### **common bottleneck #1 - dependency on other people**

- Communication is critical for making progress on people-related bottlenecks
    - Ask for updates and commitments from team members at meetings or daily stand-ups. Periodically check in with that PM to make sure what you need hasn’t gotten dropped

### **common bottleneck #2 - Time for waiting for approval from decision-maker**

- Try to obtain early feedback as possible to avoid wasting time after making changes

### **common bottleneck #3 - the review processes that accompany any project launch**

- It’s easy to get so focused on getting a feature to work that you defer these reviews to the last minute.
- As an example consequence,  the team that needs to sign off on your work hadn’t been aware of your launch plans and won’t be available until two weeks from now

Find out where the biggest bottlenecks in your iteration cycle are, whether they’re in the engineering tools, cross-team, dependencies, approvals from decision-makers, or organizational processes. Then work to optimize them.

### Key Takeaways

- **The faster you can iterate, the more you can learn**
    - Conversely, when you move too slowly trying to avoid mistakes, you lose opportunities
- **Intest in tooling**
    - Fater compile times, faster development cycles, and faster turnaroud times for development all provide time-saving benefits that compound the more you use them
- **Optimize your debugging workflow**
    - Don’t underestimate how much time gets spent validating that your code works. Invest enough time to shorten those workflows
- **Master the fundamentals of your craft**
    - Get comfortable and efficient with the development environment that you use on a daily basis. This will pay off dividends throughout your career
- **Take a holistic view of your iteration loop**
    - Don’t ignore any organizational and team-related bottlenecks that may be within your circle of influence

***Excerpt From***
The Effective Engineer: How to Leverage Your Efforts in Software Engineering to Make a Disproportionate and Meaningful Impact
Edmond Lau
This material may be protected by copyright.