## From Known Answers to Open-Ended Tasks

Many AI evaluations use problems for which a correct answer is already available.

Examples include examinations, benchmark datasets, mathematical competitions, and programming problems with testable outputs. Performance can be measured by comparing a model's response with a known solution or evaluation criterion.

Open-ended agent tasks are different because the correct result, sequence of actions, or even the appropriate stopping point may not be known in advance.

An agent working in this setting must decide what to investigate, which tools to use, when to abandon an approach, what information to retain, whether another agent's output is trustworthy, and when the task is complete.

This changes the evaluation problem.

It is relatively straightforward to evaluate a model when an answer key exists. It is considerably harder to evaluate an autonomous system operating over hundreds or thousands of actions when failures can occur anywhere in the trajectory.

The OpenAI and Anthropic experiments provide useful examples of this problem at unusually large scale. They show that agent capability depends not only on the intelligence of the underlying model, but also on the infrastructure surrounding it.

## Takeaways for Building Agent Systems

The Navier–Stokes experiment highlights several issues that extend well beyond mathematics.

The first is **coordination**.

OpenAI did not simply run many identical agents against the same prompt. Different groups were assigned different objectives, intermediate findings were consolidated, and useful results were redistributed into later work.

Anthropic's experiments show why this matters. Increasing the number of agents does not ensure effective collaboration. Agents can duplicate work, converge prematurely on the same approach, fail to communicate important information, or create dependencies that other agents cannot resolve.

The second issue is **correlated reasoning**.

Multiple instances of the same underlying model are not equivalent to independent thinkers. If they share similar training, prompts, context, and reasoning tendencies, they may reproduce the same assumptions and the same errors.

This creates an important design question for multi-agent systems: how should genuine diversity be introduced?

OpenAI's experiment provides one possible answer. Different groups were deliberately assigned different formulations of the problem and encouraged to pursue different approaches. Diversity was introduced through the architecture rather than assumed to emerge automatically from scale.

The third issue is **evaluation**.

Agents need mechanisms for determining whether their work is actually succeeding. In the Navier–Stokes case, Lean provided an unusually strong verification layer. Most agent applications will not have an equivalent.

That makes the design of evaluators, tests, constraints, and feedback loops a central part of agent engineering rather than something that can be added after the system has been built.

Human oversight remains important for the same reason.

Humans in agent systems do not necessarily need to approve every individual action. At sufficiently large scale that would defeat much of the purpose of automation. Instead, human involvement can move to higher-leverage points: defining objectives, setting constraints, reviewing unusual behaviour, deciding when evidence is sufficient, resolving ambiguity, and determining whether an output should be trusted or acted upon.

The fourth issue is **context management**.

OpenAI's system did not merely generate intermediate results. Useful discoveries were incorporated into later prompts, allowing subsequent agents to build on work produced earlier in the run.

This creates another engineering problem: deciding what information should enter an agent's context.

Too little information and agents repeatedly rediscover the same things. Too much information and context becomes noisy, expensive, and potentially misleading. Multi-agent systems therefore need mechanisms for selecting, compressing, ranking, and distributing useful intermediate knowledge.

The fifth issue is **resource allocation**.

OpenAI redirected resources toward Navier–Stokes after progress on the related Euler problem made that direction appear more promising. The system therefore changed how computation was allocated based on evidence generated during the run.

This suggests that orchestration is not simply about assigning tasks at the beginning. A capable agent system may need to continually decide which branches deserve more computation, which should be terminated, and where new agents should be created.

Finally, there is **misalignment**.

As agents become more autonomous, failures do not have to take the form of an obviously malicious action. An agent can faithfully optimize the wrong interpretation of an objective, continue pursuing a strategy after it has stopped being useful, communicate misleading information to another agent, or satisfy a local objective while undermining the broader system.

In a multi-agent environment these problems can compound. One agent's incorrect assumption can become another agent's context, and eventually a system-level conclusion.

The problem is therefore not simply whether individual agents are aligned with an instruction. It is whether the behaviour that emerges from their interaction remains aligned with the objective of the system.
