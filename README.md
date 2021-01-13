# 97 things Every Programmer Should Know - Book Notes
Published by [O'Reilly Media](https://www.oreilly.com/library/view/97-things-every/9780596809515/)
| Edited by Kevlin Henney

Notes by [Martin Suja](https://github.com/Mart17)

___

## Ask, "What Would the User Do?"
- We all tend to assume that other people think like us. But they don't.
Psychologists call this the false consensus bias. Users don't think like programmers.
- Ask a user to complete a task
using a similar piece of software to what you're developing. Avoid tasks that are too specific.
Don't interrupt. Don't try to help. Keep asking yourself, "Why is he doing that?" and "Why is
she not doing that?" When users get stuck, they narrow their focus. It becomes harder for
them to see solutions elsewhere on the screen. It's one reason why help text is a poor
solution to poor user interface design. If you must have instructions or help text, make sure
to locate it right next to your problem areas. A user's narrow focus of attention is why tool
tips are more useful than help menus. It's better to provide one really obvious way of doing
things than two or three shortcuts.
- Spending an hour watching users is more informative than spending a day guessing what
they want.

## Automate Your Coding Standard
- Use static code analysis tools.
- Coding standard should be dynamic rather than static.

## Beauty Is in Simplicity
- If you haven't spent time studying other people's code, find some open source code to
study.
- No matter how complex the total application or system is, the individual parts have to be
kept simple: simple objects with a single responsibility containing similarly simple, focused
methods with descriptive names.
- Beauty is born of and found in simplicity.

## Before You Refactor
- The best approach for restructuring starts by taking stock of the existing codebase and the
tests written against that code. This will help you understand the strengths and weaknesses
of the code as it currently stands, so you can ensure that you retain the strong points while
avoiding the mistakes. We all think we can do better than the existing system...until we end
up with something no better—or even worse—than the previous incarnation because we
failed to learn from the existing system's mistakes.
- Avoid the temptation to rewrite everything. It is best to reuse as much code as possible.
- Throwing away the old code means that you are throwing away months (or years) of tested
code that may have had certain workarounds and bug fixes you aren't aware of.
- Many incremental changes are better than one massive change. It is no fun to see a
hundred test failures after you make a change. This can lead to frustration and pressure that
can in turn result in bad decisions.
- On the surface, some of these tests may not appear to be applicable to your new design,
but it would be well worth the effort to dig deep down into the reasons why this particular
test was added.
- If something isn't broken, why fix it? That the style or the structure of the code does not
meet your personal preference is not a valid reason for restructuring.
- Unless a cost-benefit analysis shows that a new language or framework will result in
significant improvements in functionality, maintainability, or productivity, it is best to leave it
as it is.

## Check Your Code First Before Looking to Blame Others
- Given how rare compiler bugs are, you are far better putting your time and energy into
finding the error in your code than into proving that the compiler is wrong.
- Once you eliminate the impossible, whatever remains, no matter how improbable, must be
the truth.

## Choose Your Tools with Care
- Software production and maintenance is human-intensive work, so buying may be cheaper
than building.
- The configurational complexity will make the application difficult to maintain and to extend.
- Start small by using only the tools that are absolutely necessary, then add more if needed.

## Code Is Design
- As predictable tasks shrink toward zero, the less predictable design time starts to dominate.
Results are produced more quickly, but reliable timelines slip away.
- Code is design—a creative process rather than a mechanical one.

## Code Layout Matters
- Observe conventions about how to lay out the parts of a class within a compilation unit:
constants, fields, public methods, private methods.
- Line breaks and groupings reflect the intention of the code, not just the syntax of the
language.
- The more I can get on a screen, the more I can see without breaking context by scrolling or
switching files, which means I can keep less state in my head.
- Everything in the text has a purpose, and that it's there to help me understand the idea.

## Code Reviews
- Instead of looking for errors, you should review the code by trying to learn and understand
it.

## Coding with Reason
- Avoid using modifiable global variables, as they make all sections that use them dependent.
- Make your functions short and focused on a single task. The old 24-line limit still applies.
- Functions should have few parameters (four is a good upper bound). This does not restrict
the data communicated to functions: grouping related parameters into a single object
localizes object invariants, which simplifies reasoning.
- More generally, each unit of code, from a block to a library, should have a narrow interface.
Less communication reduces the reasoning required. This means that getters that return
internal state are a liability—don't ask an object for information to work with. Instead, ask
the object to do the work with the information it already has.

## A Comment on Comments
- My code should explain itself to the next programmer coming behind me.
- Inside your code should be explanations about what the code is supposed to be doing.
- Your header comments should give any programmer enough information to use your code
without having to read it, while your inline comments should assist the next developer in
fixing or extending it.

## Comment Only What the Code Cannot Say
- Comments that parrot the code offer nothing extra to the reader—stating something once
in code and again in natural language does not make it any truer or more real.
- A prevalence of noisy comments and incorrect comments in a codebase encourages
programmers to ignore all comments.
- Comments should be treated as though they were code. Each comment should add some
value for the reader, otherwise it is waste that should be removed or rewritten.
- Comments should say something code does not and cannot say.

## Continuous Learning
- You need to keep learning to stay marketable.
- To play it safe, you need to take responsibility for your own education.
- Always try to work with a mentor, as being the top guy can hinder your education. Although
you can learn something from anybody, you can learn a whole lot more from someone
smarter or more experienced than you. If you can't find a mentor, consider moving on.
- Use virtual mentors. Find authors and developers on the Web who you really like and read
everything they write. Subscribe to their blogs.
- Knowing how something works makes you know how to use it better.
- Whenever you make a mistake, fix a bug, or run into a problem, try to really understand
what happened.
- A good way to learn something is to teach or speak about it. When people are going to
listen to you and ask you questions, you'll be highly motivated to learn.
- Learning how to be more productive—how to work better.

## Deploy Early and Often
- By not ensuring that the deployment sets up the application correctly, you'll raise questions
with your customers before they get to use your software thoroughly.
- Putting deployment last means that the deployment process may need to be more
complicated to work around assumptions in the code. What seemed a great idea in an IDE,
where you have full control over an environment, might make for a much more complicated
deployment process. It is better to know all the trade-offs sooner rather than later.
- If a deployment process is that it is trivial, then do it anyway since it is low cost. If it's too
complicated, or if there are too many uncertainties, do what you would do with application
code: experiment, evaluate, and refactor the deployment process as you go.

## Do Lots of Deliberate Practice
- "Why am I performing this task?" and your answer is, "To complete the task," then you're
not doing deliberate practice. You do deliberate practice to improve your ability to perform a
task. It's about skill and technique. Deliberate practice means repetition.
- You do deliberate practice to master the task, not to complete the task.
- Research over the last two decades has shown that the main factor in acquiring expertise is
time spent doing deliberate practice.
- There is little point to deliberately practicing something you are already an expert at.
Deliberate practice means practicing something you are not good at.

## Domain-Specific Languages
- (DSLs) are about: a specific domain has a specialized vocabulary to describe the things that
are particular to that domain. In the world of software, DSLs are about executable
expressions in a language specific to a domain, employing a limited vocabulary and grammar
that is readable, understandable, and—hopefully—writable by domain experts.

## Don't Be Afraid to Break Things
- The reason that making changes is so nerve-racking is because the system is sick.
- You already know what is wrong with your system, but you are afraid of breaking the eggs
to make your omelet. A skilled surgeon knows that cuts have to be made in order to operate,
but she also knows that the cuts are temporary and will heal.
- Don't be afraid of your code. Who cares if something gets temporarily broken while you
move things around? A paralyzing fear of change is what got your project into this state to
begin with. Investing the time to refactor will pay for itself several times over the lifecycle of
your project.
- Working on a system you hate is not how anybody should have to spend his time
- Slowly transition the old structure into the new one, testing along the way. Trying to
accomplish a large refactor in "one big shebang" will cause enough problems to make you
consider abandoning the whole effort midway through.
- Keep a "hygiene" list of tasks that the team feels are worthwhile for the general good of the
project.
- Even though these tasks may not produce visible results, they will reduce expenses and
expedite future releases. Never stop caring about the general "health" of the code.

## Don't Ignore That Error
- No matter how unlikely you think an error is in your code, you should always check for it,
and always handle it. Every time. You're not saving time if you don't; you're storing up
potential problems for the future.
- Deal with problems at the earliest opportunity.

## Don't Just Learn the Language, Understand Its Culture
- It takes more than just learning the syntax to learn a language: you need to understand its
culture.

## Don't Rely on "Magic Happens Here"
- When you aren't actively involved in things, there is an unconscious tendency to assume
that they are simple and happen "by magic."
- You don't have to understand all the magic that makes your project work, but it doesn't
hurt to understand some of it—or to appreciate someone who understands the bits you
don't. Most importantly, make sure that when the magic stops, it can be started again.

## Don't Repeat Yourself
- More opportunities for bugs and adding accidental complexity to the system.
- DRY requires that "every piece of knowledge must have a single, unambiguous,
authoritative representation within a system."
- Manual testing is slow, error-prone, and difficult to repeat, so automated test suites should
be used where possible.

## Don't Touch That Code!
- If it's broke, production is not the place to fix it.

## Fulfill Your Ambitions with Open Source
- You'll never get where you want to go developing software for systems you don't care
about.
- There are thousands of open source projects out there, many of them quite active, which
offer you any kind of software development experience you could want.
- You have to be willing to give up your free time.
- In addition, very few people make money contributing to open source projects.
- You can learn a lot by reading other people's source code.
- You'll learn something new just by working on solutions and contributing code.
- You'll meet great people with the same passion.
- You'll be able to add real-world experience in the technology that actually interests you.

## The Golden Rule of API Design
- If you are designing an API that is going to have hundreds or thousands of users, you have
to think about how you might change it in the future and whether your changes might break
client code. Beyond that, you have to think about how users of your API affect you. If one of
your API classes uses one of its own methods internally, you have to remember that a user
could subclass your class and override it, and that could be disastrous. You wouldn't be able
to change that method because some of your users have given it a different meaning. Your
future internal implementation choices are at the mercy of your users.
- The easiest way is to lock down the API.
- Golden Rule of API Design fits in: It's not enough to write tests for an API you develop; you
have to write unit tests for code that uses your API. When you follow this rule, you learn
firsthand the hurdles that your users will have to overcome when they try to test their code
independently.

## The Guru Myth
- I'm getting exception XYZ. Do you know what the problem is? ... Those asking the question
rarely bother to include stack traces, error logs, or any context leading to the problem. They
seem to think you operate on a different plane, that solutions appear to you without analysis
based on evidence. They think you are a guru.
- They expect you to give an intelligent answer without context. They expect magic.
- If someone seems like a guru, it's because of years dedicated to learning and refining
thought processes. A "guru" is simply a smart person with relentless curiosity.
- one of software's biggest obstacles is smart people who purposefully propagate the guru
myth. This might be done out of ego, or as a strategy to increase one's value as perceived by
a client or employer.

## Hard Work Does Not Pay Off
- By working less, you might achieve more—sometimes much more. If you are trying to be
focused and "productive" for more than 30 hours a week, you are probably working too
hard. You should consider reducing your workload to become more effective and get more
done.
- To avoid wasted work, you must allow time to observe the effects of what you are doing,
reflect on the things that you see, and change your behavior accordingly.
- Most software projects are more like a long orienteering marathon. In the dark. With only a
sketchy map as guidance. If you just set off in one direction, running as fast as you can, you
might impress some, but you are not likely to succeed. You need to keep a sustainable pace,
and you need to adjust the course when you learn more about where you are and where you
are heading. In addition, you always need to learn more about software development in
general and programming techniques in particular.
- You need to spend evenings, weekends, and holidays educating yourself; therefore, you
cannot spend your evenings, weekends, and holidays working overtime on your current
project.
- Act like a professional: prepare, effect, observe, reflect, and change.

## Improve Code by Removing It
- So why did the unnecessary code end up there in the first place?
- Someone thought that it might be needed in the future. If you don't need it right now, don't
write it right now.
- it was easier to implement it rather than go back to the customer to see whether it was
really required. (Hint: It always takes longer to write and to maintain extra code. And the
customer is actually quite approachable.
- The programmer invented extra requirements that were neither documented nor discussed.

## Interprocess Communication Affects Application Response Time
- We feel as if the software is wasting our time and affecting our productivity.
- When performance is a problem in such applications, my experience has been that
examining data structures and algorithms isn't the right place to look for improvements.
- While there can be other local bottlenecks, the number of remote interprocess
communications usually dominates.
- A prime example is ripple loading in an application using object-relational mapping. Ripple
loading describes the sequential execution of many database calls to select the data needed
for building a graph of objects.
- Even if each database call takes only 10 milliseconds, a page requiring 1,000 calls (which is
not uncommon) will exhibit at least a 10-second response time. Other examples include web-
service invocation, HTTP requests from a web browser, distributed object invocation,
request–reply messaging, and data-grid interaction over custom network protocols.
- One strategy is to apply the principle of parsimony, optimizing the interface between
processes so that exactly the right data for the purpose at hand is exchanged with the
minimum amount interaction. Another strategy is to parallelize the interprocess
communications where possible, so that the overall response time becomes driven mainly by
the longest-latency IPC. A third strategy is to cache the results of previous IPCs, so that future
IPCs may be avoided by hitting local cache instead. When you're designing an application, be
mindful of the number of interprocess communications in response to each stimulus. When
analyzing applications that suffer from poor performance, I have often found IPC-to-stimulus
ratios of thousands-to-one. Reducing this ratio, whether by caching or parallelizing or some
other technique, will pay off much more than changing data structure choice or tweaking a
sorting algorithm.
- When the system contains too many interim solutions, its entropy or internal complexity
grows and its maintainability decreases.

## Keep the Build Clean
- When I start a new project from scratch, there are no warnings, no clutter, no problems.
But as the codebase grows, if I don't pay attention, the clutter, the cruft, the warnings, and
the problems can start piling up. When there's a lot of noise, it's much harder to find the
warning that I really want to read among the hundreds of warnings I don't care about. To
make warnings useful again, I try to use a zero-tolerance policy for warnings from the build.
Even if the warning isn't important, I deal with it. If it's not critical but still relevant, I fix it.
- If it's something I really don't care about and that really doesn't matter, I ask the team if we
can change our warning policy. For example, I find that documenting the parameters and
return value of a method in many cases doesn't add any value, so it shouldn't be a warning if
they are missing.
- Having a set of warnings that are out of step with reality does not serve anyone. By making
sure that the build is always clean, I will not have to decide that a warning is irrelevant every
time I encounter it. Ignoring things is mental work, and I need to get rid of all the
unnecessary mental work I can. Having a clean build also makes it easier for someone else to
take over my work. If I leave the warnings, someone else will have to wade through what is
relevant and what is not. Or more likely, that person will just ignore all the warnings,
including the significant ones.
- Don't wait for a big cleanup.
- warnings are also an important and critical part of code hygiene.

## Know How to Use Command-Line Tools
- By working with command-line build tools, you will learn a lot more about what the tools
are doing when your project is being built.

## Know Well More Than Two Programming Languages
- A one-language programmer is constrained in her thinking by that language. A programmer
who learns a second language will be challenged, especially if that language has a different
computational model than the first.

## Know Your IDE
- Let's spend a bit of time to study how to become more effective with our IDE.

## Know Your Limits
- So you have to respect the limits of your resources. How to respect those limits? Know
yourself, know your people, know your budgets, and know your stuff.
- Your job is to create an optimal marriage of software and systems.

## Know Your Next Commit
- Do speculative experimentation whenever needed, but do not let yourself slip into
speculative mode without noticing. Do not commit guesswork into your repository.

## Learn to Estimate
- Have a reasonably accurate idea of the time, costs, technology, and other resources.
- We need three definitions: estimate, target, and commitment.
- An estimate is an approximate calculation or judgment; hopes and wishes must be ignored;
being approximate, an estimate cannot be precise.
- A target is a statement of a desirable business objective, e.g., "The system must support at
least 400 concurrent users."
- A commitment is a promise to deliver specified functionality at a certain level of quality by a
certain date or event.; "functionality will be available in the next release of the product.“

## Make Interfaces Easy to Use Correctly and Hard to Use Incorrectly
- If you do it well, your interfaces will be a pleasure to use and will boost others' productivity.
If you do it poorly, your interfaces will be a source of frustration and errors.
- Good interfaces anticipate mistakes people might make, and make them difficult—ideally,
impossible—to commit.

## Make the Invisible More Visible
- If you're 90% done and endlessly stuck trying to debug your way through the last 10%, then
you're not 90% done, are you? Fixing bugs is not making progress. You aren't paid to debug.
Debugging is waste. It's good to make waste more visible so you can see it for what it is and
start thinking about trying not to create it in the first place.
- Lack of visible progress is synonymous with lack of progress.
- Using bulletin boards and cards makes progress visible and concrete. Tasks can be seen as
Not Started, In Progress, or Done without reference to a hidden project management tool
and without having to chase programmers for fictional status reports.
- It's best to develop software with plenty of regular visible evidence. Visibility gives
confidence that progress is genuine and not an illusion, deliberate and not unintentional,
repeatable and not accidental.

## Testers Are Your Friends
- They're too picky" and "They want everything perfect" are common complaints. Sound
familiar?
- Now, none of these is a big deal, but as the errors add up, you begin to wonder about the
programmers. If they can't get the simple things right.
- And now you're questioning the competency of the programmers. So, as strange as it may
sound, those testers who seem determined to expose every little bug in your code really are
your friends.

## Only the Code Tells the Truth
- When you look at the source code, the meaning of the program should be apparent. To
know what a program does, the source is ultimately all you can be sure of looking at. Even
the most accurate requirements document does not tell the whole truth: it does not contain
the detailed story of what the program is actually doing, only the high-level intentions of the
requirements analyst.
- You might say, "Oh, my comments will tell you everything you need to know." But keep in
mind that comments are not running code. They can be just as wrong as other forms of
documentation. There has been a tradition of saying that comments are unconditionally a
good thing, so some programmers unquestioningly write more and more comments, even
restating and explaining trivia already obvious in the code. This is the wrong way to clarify
your code. If your code needs comments, consider refactoring it so it doesn't.
- What can you do to actually make your code tell the truth as clearly as possible? Strive for
good names.
- Make your code as simple as possible to read and understand.
- Craft what you express carefully, so that it does what it should and communicates as
directly as possible what it is doing; so that it still communicates your intention when you are
no longer around.
- As a team member, be patient with developers less experienced than you. Confront your
fears about being intimidated by more skilled developers. Realize that people are different,
and value it. Be aware of your own strengths and weaknesses, as well as those of other team
members. You may be surprised by how much you can learn from your colleagues.
- If you are pair programming and you run into a challenging problem, you always have
someone to discuss it with. Such dialog is more likely to open up possibilities than if you are
stuck by yourself.

## The Professional Programmer
- The single most important trait of a professional programmer is personal responsibility.
Professional programmers take responsibility for their career, their estimates, their schedule
commitments, their mistakes, and their workmanship. A professional programmer does not
pass that responsibility off on other.

## Put Everything Under Version Control
- You can make bold code changes without fear—no more commented-out code just in case
you need it in the future, because the old version lives safely in the repository. You can (and
should) tag a software release with a symbolic name so that you can easily revisit in the
future the exact version of the software your customer runs.
- Most projects have an active development branch and one or more maintenance branches
for released versions that are actively supported.
- Commit each logical change in a separate operation. Lumping many changes together in a
single commit will make it difficult to disentangle them in the feature. This is especially
important when you make project-wide refactoring or style changes, which can easily
obscure other modifications.
- Accompany each commit with an explanatory message. At a minimum, describe succinctly
what you've changed, but if you also want to record the change's rationale, this is the best
place to store it.
- Finally, avoid committing code that will break a project's build, otherwise you'll become
unpopular with the project's other developers.

## Put the Mouse Down and Step Away from the Keyboard
- You've been focused for hours on some gnarly problem, then the answer suddenly becomes
obvious.
- The trick is that while you're coding, the logical part of your brain is active and the creative
side is shut out. It can't present anything to you until the logical side takes a break.
- The point of this story is not that I eventually replaced over 30 lines of code with just one.
The point is that until I got away from the computer, I thought my first attempt was the best
solution to the problem.
- Once you really understand the problem, go do something involving the creative side of
your brain—sketch out the problem, listen to some music, or just take a walk outside.

## Read Code
- Reading someone else's code could improve your own.
- Try to learn from other people's mistakes, so that your code won't contain the same ones.

## Read the Humanities
- People work with people. In all but the most abstracted field of research, people write
software for people to support them in some goal of theirs. People write software with
people for people. It's a people business. Unfortunately, what is taught to programmers too
often equips them very poorly to deal with people they work for and with.
- Wittgenstein also shows that our ability to understand one another at all does not arise
from shared definitions, it arises from a shared experience, from a form of life.
- Martin Heidegger studied closely the ways that people experience tools. Programmers build
and use tools, we think about and create and modify and recreate tools. Tools are objects of
interest to us. But for its users, as Heiddeger shows in Being and Time (Harper Perennial), a
tool becomes an invisible thing understood only in use. For users, tools only become objects
of interest when they don't work. This difference in emphasis is worth bearing in mind
whenever usability is under discussion.
- That just isn't how people in general understand the world. They understand it in ways that
are based on examples.

## Reinvent the Wheel Often
- Reinventing the wheel is not just an exercise in where to place code constructs: it is about
how to get an intimate knowledge of the inner workings of various components that already
exist.
- Most developers simply have never created these types of core software implementations
themselves and therefore do not have an intimate knowledge of how they work. The
consequence is that all these kinds of software are viewed as mysterious black boxes that
just work. Understanding only the surface of the water is not enough to reveal the hidden
dangers beneath. Not knowing the deeper things in software development will limit your
ability to create stellar work.
- Reinventing the wheel and getting it wrong is more valuable than nailing it first time. There
are lessons learned from trial and error that have an emotional component to them that
reading a technical book alone just cannot deliver!
- Learned facts and book smarts are crucial, but becoming a great programmer is as much
about acquiring experience as it is about collecting facts. Reinventing the wheel is as
important to a developer's education and skill as weightlifting is to a body builder.

## Simplicity Comes from Reduction
- The best approach to fixing bad code is to flip into a mode where the code is mercilessly
refactored, shifted around, or deleted.
- The code should be simple. There should be a minimal number of variables, functions,
declarations, and other syntactic language necessities.

## The Single Responsibility Principle
- In short, it says that a subsystem, module, class, or even a function, should not have more
than one reason to change.
- Good system design means that we separate the system into components that can be
independently deployed. Independent deployment means that if we change one component,
we do not have to redeploy any of the others. However, if Employee is used heavily by many
other classes in other components, then every change to Employee is likely to cause the
other components to be redeployed, thus negating a major benefit of component design.

## Start from Yes
- When someone says to you, "Hey, this app would really be the bee's knees if we made all
the windows round and translucent!", you could reject it as ridiculous. But it's frequently
better to start with "Why?" instead. Often, there is some actual and compelling reason why
that person is asking for round, translucent windows in the first place.
- You'll find that when you know the context of the request, new possibilities open up.
- Sometimes the other person will simply have an idea that you find incompatible with your
view of the product. I find it's usually helpful to turn that "Why?" on yourself.

## Test for Required Behavior, Not Incidental Behavior
- Align tested behavior with required behavior
- So who should you be writing the tests for? For the person trying to understand your code.
- The person trying to understand your code should be able to look at a few tests, and by
comparing these three parts of the tests in question, be able to see what causes the software
to behave differently.

## Thinking in States
- In most real-world situations, people's relaxed attitude toward state is not an issue.
Unfortunately, however, many programmers are quite vague about state, too—and that is a
problem.
- These states are important, and you need to check that you're in the expected state before
doing operations, and that you only move to a legal state from where you are.
- Extracting expressions to meaningful methods is a very good start, but it is just a start.
- Study the State pattern. When you feel comfortable, read up on Design by Contract. It helps
you ensure a valid state by validating incoming data and the object itself on entry and exit of
each public method.

## Use the Right Algorithm and Data Structure
- Programmers should not reinvent the wheel, and should use existing libraries where
possible. But to be able to avoid problems like the bank's, they should also be educated
about algorithms and how they scale.

## Write Code As If You Had to Support It for the Rest of Your Life
- ↑↑↑

## Your Customers Do Not Mean What They Say
- I've never met a customer yet that wasn't all too happy to tell me what they wanted—
usually in great detail. The problem is that customers don't always tell you the whole truth.
They generally don't lie, but they speak in customer speak, not developer speak. They use
their terms and their contexts. They leave out significant details. They make assumptions
that you've been at their company for 20 years, just like they have. This is compounded by
the fact that many customers don't actually know what they want in the first place! Some
may have a grasp of the "big picture," but they are rarely able to communicate the details of
their vision effectively. Others might be a little lighter on the complete vision, but they know
what they don't want. So, how can you possibly deliver a software project to someone who
isn't telling you the whole truth about what they want? It's fairly simple. Just interact with
them more. Challenge your customers early, and challenge them often.
- It is generally known that using visual aids during a conversation helps lengthen our
attention span and increases the retention rate of the information.
