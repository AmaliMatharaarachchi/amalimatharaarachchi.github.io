## Iterative Research and Knowledge Transfer

A notable feature of OpenAI's reported Navier–Stokes workflow was the use of intermediate discoveries to modify later research.

The experiment began on September 1, after OpenAI had started training a new internal model on August 28. According to OpenAI, agents were initially assigned to several open Millennium Prize Problems as well as related problems that were expected to be more tractable.

One of these related problems concerned the Euler equations. In simplified terms, the Euler equations describe an idealized fluid without viscosity and are mathematically related to Navier–Stokes.

OpenAI reports that approximately 100 agents worked on the Euler problem for about 50 hours and obtained a result concerning finite-time singularity formation for the unforced Euler equations.

Following this result, additional computational resources were directed toward Navier–Stokes. The Euler result was also supplied as context to agents working on the Navier–Stokes problem. When a later checkpoint of the internal model became available, it was incorporated into the research process.

<div class="flow"><span>Exploration</span><b>→</b><span>intermediate result</span><b>→</b><span>synthesis</span><b>→</b><span>context update</span><b>→</b><span>resource allocation</span><b>→</b><span>further exploration</span></div>

This feedback mechanism is an important property of the system. Intermediate results were not treated only as final outputs. They were incorporated into the context available to later agents and were used to determine where additional research effort should be allocated.

OpenAI reports that the Navier–Stokes result was obtained on September 5, approximately 88 hours after the initial agents were launched. The Navier–Stokes effort generated approximately 2.7 million agent messages and 130 billion output tokens.

<div class="metric-grid"><div class="metric"><strong>≈10,000</strong>concurrent agents in the final-result group</div><div class="metric"><strong>2.7M</strong>agent messages</div><div class="metric"><strong>130B</strong>output tokens</div></div>

These figures indicate the scale of the experiment, but they do not by themselves explain the research process. The more general architectural components are parallel exploration, differentiated research objectives, tool use, synthesis of intermediate findings, redistribution of relevant context, and iterative allocation of computational resources.

These components can be applied conceptually to other open-ended research tasks even when the number of agents, models, tools, and verification methods differs.

## From Discovery to Formal Verification

Language models can generate incorrect mathematical arguments, including errors that are difficult to identify from natural-language exposition alone. A multi-agent system does not necessarily eliminate this problem because agents based on the same or related models may reproduce correlated errors.

For this reason, discovery and verification can be treated as separate stages.

After the candidate Navier–Stokes proof was generated, OpenAI used GPT-6 Astra to assist with its formalization in Lean. OpenAI reports that this stage required approximately 17 additional hours.

Lean is a formal proof assistant. Mathematical statements and their supporting arguments are represented in a precise formal language, and the proof checker verifies whether each inference is permitted by the underlying logical system.

This creates a useful division of functions. Language models can be used to search a large space of possible approaches, propose conjectures, construct candidate arguments, and revise unsuccessful attempts. Formal proof systems can then be used to check whether a formalized argument satisfies explicit logical rules.

{% include article1/figure4.html %}

<div class="flow"><span>Probabilistic discovery</span><b>→</b><span>formalization</span><b>→</b><span>deterministic verification</span></div>

Formal verification does not resolve every question concerning a mathematical result. It establishes that the formalized theorem follows from the definitions, assumptions, and logical rules represented in the proof environment. Human review remains necessary to determine whether the formal statement accurately corresponds to the intended mathematical problem and to assess the interpretation and significance of the result.

Formal verification should therefore be distinguished from acceptance by the mathematical community or recognition by the Clay Mathematics Institute.
