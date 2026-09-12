The relevant architectural feature is not simply the number of agents. Multi-agent systems introduce a coordination problem: increasing the number of model instances does not necessarily increase the quality or diversity of the resulting research.

## Coordination in Multi-Agent Systems

Recent experiments by Anthropic provide useful evidence of this limitation.

In one set of experiments, agents were assigned software-vulnerability research tasks. Forty-five agents were placed in separate virtual machines and given access to a shared communication forum. Agents could develop tools, specialize in different tasks, share findings, and review the work of other agents. A separate arbiter evaluated submitted vulnerabilities.

This setting supported parallelization because many candidate vulnerabilities could be investigated independently.

Other experiments produced less effective coordination. When groups of agents were asked to jointly develop a software project, dependencies between the work of individual agents created integration problems. Anthropic also observed cases in which agents based on the same underlying model independently converged on similar approaches.

This creates a distinction between **parallelism** and **coordination**.

**Parallelism** allows several independent searches to occur at the same time. **Coordination** requires useful information from those searches to be selected, communicated, integrated, and used to modify subsequent work.

Anthropic also identified difficulties involving distributed information. In some experiments, information held by a minority of agents was not incorporated effectively after the broader group had converged on another conclusion. These results indicate that increasing individual model capability does not, by itself, resolve collective decision-making problems.

<div class="quote">“Coordination doesn't naturally emerge from stronger intelligence.”</div>

This issue is particularly relevant to open-ended research. If many agents are generated from the same model and given similar contexts, they may reproduce similar assumptions or search similar regions of the solution space. Diversity of research therefore cannot necessarily be assumed to emerge from the number of agents alone.

OpenAI's published description indicates that its research process introduced some diversity through task design. Different groups were assigned different formulations and approaches. Intermediate results were subsequently consolidated using Codex and incorporated into later prompts, a process OpenAI describes as cross-pollination.

This suggests an architecture based not only on parallel exploration, but on repeatedly collecting useful findings and using them to redirect subsequent research.

{% include article1/figure3.html %}

The architecture can be summarized as an iterative process:

<div class="flow"><span>Research problem</span><b>→</b><span>parallel exploration</span><b>→</b><span>intermediate results</span><b>→</b><span>synthesis</span><b>→</b><span>updated context</span><b>→</b><span>further exploration</span></div>

This differs from independent parallel sampling because intermediate findings can influence subsequent stages of the research process.

## An Earlier Example of AI-Assisted Mathematical Research

A related experiment was reported by Anthropic in August 2026.

An unreleased research version of Claude was assigned work related to the Riemann hypothesis, another Millennium Prize Problem. The system did not solve the Riemann hypothesis. Instead, it obtained an improved result concerning the proportion of zeros of the Riemann zeta function known to satisfy the hypothesis.

According to Anthropic, the resulting lower bound was increased from 41.6 percent to 67.2 percent. The result was subsequently examined by mathematicians at Anthropic and formalized in Lean.

The experiment used approximately 60 subagents with different functions. Anthropic reports that two agents developed the central mathematical ideas, 13 contributed ideas to those agents, 30 attempted alternative approaches without obtaining the final result, 13 performed validation work, and two assisted with preparation of the initial paper.

This distribution illustrates one possible organization for agent-based research. Different agents were used for exploration, development, validation, and writing rather than assigning every agent the same task.

The unsuccessful branches are also relevant to the architecture. Open research generally requires exploration of approaches that do not lead to a useful result. Parallel agents allow several such branches to be investigated concurrently, while promising branches can receive additional attention.

The system also used computational tools. Anthropic reports the use of shell commands, Python programs, numerical checks, literature retrieval, counterexample searches, and independent attempts to reproduce the result.

The mathematical work was not independent of existing human research. The agents operated using existing literature and mathematical results as part of their context. The experiment is therefore more accurately described as an AI system extending and recombining an existing body of mathematical knowledge than as mathematics generated without prior intellectual inputs.

This distinction is also relevant to the OpenAI result.
