The Navier–Stokes equations describe the motion of fluids. They are used to model phenomena ranging from airflow and turbulence to water currents and blood flow. Although the equations have been studied extensively, an important question concerning their mathematical behaviour in three dimensions has remained unresolved.

The problem can be stated informally as follows. Suppose a fluid begins in a smooth and well-defined state. As the system evolves, must the solution remain smooth, or can the equations produce a singularity in finite time? A singularity, or blowup, occurs when a quantity such as velocity becomes unbounded.

Viscosity complicates this question because it tends to smooth differences in fluid velocity. It is therefore necessary to determine whether this smoothing effect is sufficient to prevent singular behaviour under the conditions specified by the equations.

In 1934, Jean Leray established the existence of generalized, or weak, solutions to the three-dimensional Navier–Stokes equations. The question of global smoothness remained unresolved. In 2000, the Clay Mathematics Institute included the Navier–Stokes existence and smoothness problem among its seven Millennium Prize Problems.

<div class="hero-note"><strong>September 8, 2026.</strong> OpenAI reported that an internal AI system had produced a solution addressing the problem.</div>

{% include article1/figure1.html %}

The proposed construction begins with a fluid at rest and introduces a smooth external force. According to OpenAI, the resulting solution develops finite-time blowup while maintaining bounded kinetic energy. OpenAI states that this construction establishes alternatives C and D in the official formulation of the Millennium Prize Problem.

The result has been published together with a mathematical paper and a formalization in Lean. Formal verification, however, is distinct from broader mathematical and institutional acceptance. The result must still be examined by the mathematical community, and the Clay Mathematics Institute has its own requirements for recognizing a solution.

The case is therefore of interest for two related reasons. The first is the mathematical claim itself. The second is the research process through which the candidate solution was generated.

## From Language Models to Multi-Agent Research Systems

A conventional language-model interaction can be represented as a relatively simple process:

<div class="flow"><span>Prompt</span><b>→</b><span>Model</span><b>→</b><span>Response</span></div>

An AI agent extends this process by allowing the model to interact repeatedly with an environment. An agent can select an action, use a tool, observe the result, update its working context, and continue until an objective or stopping condition is reached.

For example, a software-development agent may inspect source code, propose a modification, run tests, observe an error, and revise the implementation. The output is therefore produced through an iterative sequence of model decisions and environmental feedback rather than through a single model response.

{% include article1/figure2.html %}

A multi-agent system extends this structure by assigning work to multiple agents. Individual agents or groups can investigate different parts of a problem, use tools independently, exchange intermediate findings, and contribute to a shared result.

OpenAI's Navier–Stokes experiment used this form of organization. According to OpenAI's published description, the agents were powered by an unreleased internal model. They were provided with code execution and access to a cached version of the internet. Agents were divided into groups, and communication was permitted within those groups.

Different groups were also assigned different formulations of the mathematical problem. Some were directed toward proving regularity, while others investigated possible counterexamples. OpenAI reports that the group associated with the final Navier–Stokes result involved on the order of 10,000 concurrent agents.
