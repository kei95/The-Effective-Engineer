# Chapter 3 - Invest in Your Team’s Growth

“I traced through code littered with obscure variable names like `qqq` and questionable function names like `load2` and `load3`”

One of the biggest lessons I learned from Ooyala is - ***Investing in a positive, smooth onboarding experience is extremely valuable.***

- Investing in onboarding is just one way to invest in your team’s growth.

*The people and the team that you work with have a significant impact on your own effectiveness.*

*And you don’t have to be a manager or a senior engineer to influence your team’s direction.*

- Building a solid team is also a job for developers

***The higher you climb up the engineering ladder, the more your effectiveness will be measured not by your individual contributions but by your impact on the people around you.***

- Your career success depends largely on your company and team’s success, and the success of your company or team depends on more than just your individual contributions.

## 1. Make Hiring Everyone’s Responsibility

Core part of the problem of hiring is often that engineers simply aren’t spending enough time on hiring.

A good interview process achieves two goals.

1. it screens for the type of people likely to do well on the team
2. It gets candidates excited about the team, the mission, and the culture.
    1. Ideally, even if a candidate goes home without an offer, they still leave with a good impression of the team and refer their friends to interview with the company.
- Interviews should be fun and rigorous.

As an interviewer, your goal is to optimize for questions with high *signal-to-noise* rations

- questions that reveal a large amount of useful information(signal) about the candidate per minute spent, with little irrelevant or useless data(noise).

In order to keep the quality of interviews updated, here are a few higher-leverage strategies to keep in mind:

- Take time with your team to identify which qualities in a potential teammate you care about the most
    - programming, communication skills, culture fit, or something else... Coordinate to ensure that all the key areas get covered during an interview loop
- Design interview problems with multiple layers of difficulty that you can tailor to the candidate’s ability by adding or removing variables and constraints
- Control the interview pace to maintain a high signal-to-noise ratio. Don’t let interviewees ramble, get stumped, or get sidetracked for too long.
    - Either guide the interviewee along with hints, or wrap up and move on to a different question.
- Scan for red flags by rapidly firing short-answer questions to probe a wide surface area.
    - Questions like how parameter passing works in a programming language or how a core library works might take a qualified candidate no more than a few seconds or a minute to answer, but can surface any warning areas that you might want to further address.
- Periodically shadow or pair with another team member during interviews. These sessions help calibrate ratings across interviewers and provide opportunities to give each other feedback on improving the interview process
- Don’t be afraid to use unconventional interview approaches if they help you identify the signals that your team cares about.

As with all skills, the only way that you can become more effective in interviewing and hiring is through iteration and practice. It’s worth for the effort.

The additional output from adding a strong engineer to your team far exceeds the output of many other investments that you could have.

## 2. Design a Good Onboarding Process

Training a new engineer for an hour or two a day during her first month generates much more organizational impact than spending those some hours working on the product.

Onboarding is a win-win situation; the new hires receive valuable training, and the mentors get more things done.

Conversely, a poor onboarding experience reduces a team’s effectiveness.

Regardless of your seniority, you can contribute meaningfully to onboarding.

- If there are wikis or internal documents that you used, see if you can directly update and improve them.
- If you’re a more senior engineer, observe what new team members pick up well and what they struggle with, and use that knowledge to improve onboarding for future employees.

The author outlined four goals that he thought the process should achieve:

1. **Ramp up new engineers as quickly as possible**
    1. Onboarding does require a short-term productivity hit for those leading it. The sooner they ramp up, the earlier it pays off
2. **Impart the team’s culture and values**
    1. the onboarding process helps ensure that they learn the values that the team shares.
3. **Expose new engineers to the breadth of fundamentals need to succeed.**
    1. What are the key things that every engineer should know? What valuable tips and tricks have you learned since joining the team? A key part of a good onboarding program is ensuring that everyone starts on a consistent, solid foundation.
4. **Socially integrate new engineers onto the team**
    1. This means creating opportunities for them to meet and develop working relationships with other teammates. The sooner that new engineers become full-fledged parts of the team rather than isolated silos, the more effective they will be.
    - Feedback cycle is really important.
    
    What’s important is understanding what you want to achieve so that you can focus your efforts appropriately. Using these goals, he developed the four main pillars for onboarding program:
    
    1. **Codelabs**
        1. A codelab is a document that explains why a core abstraction was designed and how it’s used, walks through relevant parts of its code internals, and supplies programming exercises to validate understanding.
    2. **Onboarding talks**
        1. they organized a series of ten onboarding talks to be delivered during a new hire’s first three weeks. These talks, given by senior engineers on the team, introduced the codebase and site architecture, explained and demoed different development tools, covered engineering expectations and values around topics like unit testing, and introduced key focus areas.
    3. **Mentorship**
        1. onboarding programs can’t be one-size-fits-all. For the new hire’s first new month, each of them pair up with a mentor for personalized training. Responsibilities included everything from reviewing code, discussing design tradeoffs, and planning work priorities, to introducing new hires to the right people on the team and helping them acclimate to the fast pace of a startup.
        2. As a team, build a shared understanding that it is acceptable - and in fact, strongly encouraged - for mentors to spend time away from their regular work to train new employees.
    4. **Starter tasks**
        1. Mentors were responsible for identifying starter tasks of increasing complexity for their mentees. The author generally advices to pick a project that would take them a day to finish, so that even if ramping up took longer than expected and the project slipped, there would still be a high probability that new hire could ship it in the first week.
        2. they aim for each of new hires to complete a starter task - whether it be deploying a bug fix, a small new feature, or a new  experiment - by the end of the first week.
    
    ## 3. Share Ownership of Code
    
    There’s a common misconception that being the sole engineer responsible for a project increases your value.
    
    Sharing code ownership benefits not only yourself but your entire reams as well.
    
    When you’re the only one with complete knowledge of a working system and it goes down, you find yourself as the first or ONLY line of defence.
    
    - Identifying others on your team who can relieve some of those demands gives you more freedom to focus on other high-leverage activities.
        - That’s a key reason why investing in your team, particularly by teaching and mentoring, helps you in the long run
    
    It’s harder for engineers on the team to be *fungible* 
    
    ***“any one thing can be done by multiple people, and that allows you more degrees of freedom, more flexibility in development, and fewer constraints for on-call and support”***
    
    To increase shared ownership, reduce the friction that other team members might encounter while browsing, understanding, and modifying code that you write or tools that you build. Here are some strategies:
    
    - Avoid one-person teams
    - Review each other’s code and software designs
    - Rotate different types of tasks and responsibilities across the team
    - Keep code readable and code quality high
    - Present tech talks on software decisions and architecture
    - Document your software, either through high-level design documents or in code-level comments
    - Document the complex workflows or non-obvious workarounds necessary for you to get things done
    - Invest time in teaching and mentoring other team members

## 4. Build Collective Wisdom through Post-Mortems

Developing the habit of regular prioritization provides one opportunity for retrospection.

After a site outage, a high-priority bug, or some other infrastructure issue, effective teams meet and conduct a detailed *post-mortem.*

- They discuss and analyze the event, and they wire up what happened, how and why it happened, and what they can do to prevent it from happening in the future.
- The goal of the post-mortem is not to assign blame, which can be counterproductive to the discussion, but to work together to identify better solutions.

Toyota’s 5 why methodology - by the time you dig the problem by asking why 5 times, you should be able to reach the root cause.

The more you learn from each experience, the more you’ll take with you into your next project, and the more you’ll succeed. Optimize for collective learning.

## 5. Building a Great Engineering Culture

Engineering culture consists of the set of values and habits shared by people on the team, and a great culture provides a number of benefits. Engineers feel empowered to get things done, which makes them happier and more productive. Happy and productive engineers in turn translate to higher employee retention.

Great engineering cultures are;

1. Optimize for iteration speed
2. Push relentlessly towards automation
3. Build the right software abstractions
4. Focus on high code quality by using code reviews
5. Maintain a respectful work environment
6. Build shared ownership of code
7. Invest in automated testing
8. Allot experimentation time, either through 20% time or hackathons
9. Foster a culture of learning and continuous improvement
10. Hire the best

A great engineering culture isn’t build in a day; nor is it already in place when a company first starts. It begins with the values of the initial team members, and it’s continual work-in-progress that every engineer helps to shape.

When we focus on high-leverage activities, we not only become more effective engineers, we also lay the groundwork for a more effective engineering culture.

## Key Takeaways

- **Help the people around you be successful**
    - The high rungs of an engineering ladder are reserved for those who make their co-workers more effective. Moreover, the success of those around you will also carry you along
- **Make hiring a priority**
    - Keep a high hiring bar and play an active role in growing your team
- **Invest in onboarding and mentoring**
    - The more quickly you can rump up your new team members, the more effective your team will be.
    - The more effective your team, the more freedom you have  to tackle different projects
- **Build shared ownership of code**
    - Increase your ***Bus factor*** to be greater than one so that you’re not a bottleneck for development, this will give you the flexibility to focus on other high-leverage activities.
- **Debrief and document collective wisdom**
    - Reflect on projects with team members, learn what worked and what didn’t work, and document and share the lessons so that valuable wisdom doesn’t get lost.
- **Create a great engineering culture**
    - This will help you be more productive, streamline decisions, and recruit other strong engineers. You build  a great culture by fostering the same habits you need to effectively deliver impact.