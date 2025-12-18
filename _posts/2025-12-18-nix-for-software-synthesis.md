As I've been coding more with agents, I've realised that high level specs have higher value - PRD > RFC > HLD. And tests of-course, lots and lots of them. The scarce a resource, the higher its value.

Low level specs have very little value if you're doing greenfield work. Some if its brownfield.

The code itself has almost zero value. If the specs are good, an agent can churn code like crazy.

This is so counterintuitive to everything I've learned over the years or what was taught to us in SE courses.

We treat code so dearly. Have proper linters, formatters, sanity checkers. Commit it. The git history should be clean etc etc. 

We don't commit our binaries to repos though. Why? Because they’re an artefact. We know that code when passed through a compiler can get us this artefact again.

What if we're headed to a place where code could be that artefact? This bends my mind a little and I almost don't want to accept it.

People are experimenting with keeping just their prompts in commits messages and ignoring everything else. No “code” reviews happen.

Reviewers only review the prompt! Akin to how we don't worry about the byte code of a python script when reviewing it.

What if prompts when passed through an LLM created the right artefact. I know we're definitely not there today. LLMs are fallible - stochasticity / non determinism and all that. 

But then: was GCC bug free on day one? Is it bug free today? It's early days for this tech. And boy are these exciting days.

An analogy to end this LinkedIn-esque post:

“Agentic coding” is to Software Engineering what C++ was to punch cards. Fundamentally disrupting the nature of work. For the better.
