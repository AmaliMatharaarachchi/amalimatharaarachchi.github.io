## Iterative Research and Knowledge Transfer

A notable feature of OpenAI's reported Navier–Stokes workflow was the use of intermediate discoveries to modify later work.

The experiment began on September 1, after OpenAI had started training a new internal model on August 28. According to OpenAI, agents were initially assigned to several open Millennium Prize Problems as well as related problems that were expected to be more tractable.

One of these related problems concerned the Euler equations. In simplified terms, the Euler equations describe an idealized fluid without viscosity and are mathematically related to Navier–Stokes.

OpenAI reports that approximately 100 agents worked on the Euler problem for about 50 hours and obtained a result concerning finite-time singularity formation for the unforced Euler equations.

Following this result, additional computational resources were directed toward Navier–Stokes. The Euler result was also supplied as context to agents working on the Navier–Stokes problem. When a later checkpoint of the internal model became available, it was incorporated into the process.

<div class="flow"><span>Exploration</span><b>→</b><span>intermediate result</span><b>→</b><span>synthesis</span><b>→</b><span>context update</span><b>→</b><span>resource allocation</span><b>→</b><span>further exploration</span></div>

This feedback mechanism is an important property of the system. Intermediate results were not treated only as final outputs. They were incorporated into the context available to later agents and were used to determine where additional effort should be allocated.

OpenAI reports that the Navier–Stokes result was obtained on September 5, approximately 88 hours after the initial agents were launched. The Navier–Stokes effort generated approximately 2.7 million agent messages and 130 billion output tokens.

<div class="metric-grid"><div class="metric"><strong>≈10,000</strong>concurrent agents in the final-result group</div><div class="metric"><strong>2.7M</strong>agent messages</div><div class="metric"><strong>130B</strong>output tokens</div></div>

These figures indicate the scale of the experiment, but they do not by themselves explain the system. The more general architectural components are parallel exploration, differentiated objectives, tool use, synthesis of intermediate findings, redistribution of relevant context, and iterative allocation of computational resources.

## From Discovery to Evaluation

Language models can generate incorrect arguments, including errors that are difficult to identify from natural-language exposition alone. A multi-agent system does not necessarily eliminate this problem because agents based on the same or related models may reproduce correlated errors.

This is one of the central problems in agentic systems: adding more agents does not automatically make an output more reliable. If the agents share similar models, context, or reasoning patterns, one agent may confidently validate an error produced by another.

OpenAI's approach therefore separated discovery from verification.

After the candidate Navier–Stokes proof was generated, OpenAI used GPT-6 Astra to assist with its formalization in Lean. OpenAI reports that this stage required approximately 17 additional hours.

Lean is a formal proof assistant. Mathematical statements and their supporting arguments are represented in a precise formal language, and the proof checker verifies whether each inference is permitted by the underlying logical system.

This creates a useful division of functions. Language models can search a large space of possible approaches, construct candidate arguments, and revise unsuccessful attempts. A separate verification system can then check the resulting artifact against explicit rules.

{% include article1/figure4.html %}

<div class="flow"><span>Probabilistic discovery</span><b>→</b><span>formalization</span><b>→</b><span>deterministic verification</span></div>

The broader lesson is not specific to mathematics. Agent systems need evaluation mechanisms that are meaningfully independent of the agents producing the work.

For software agents, this might be tests, static analysis, or sandboxed execution. For data agents, it might be schema validation and reconciliation against source data. For other tasks, reliable evaluation may require another model, external tools, explicit rules, or human review.

Where no strong external evaluator exists, hallucination becomes much harder to control. An agent may produce a plausible output without having a reliable mechanism for determining whether that output is actually correct.
