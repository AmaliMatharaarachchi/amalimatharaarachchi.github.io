## The Agent Is Only One Part of the System

The Navier–Stokes case provides a useful example of a broader change in how agent systems are being designed.

The relevant system is not only the underlying language model. It includes the agents built around that model, the tools available to them, their objectives, the information they receive, mechanisms for communication and synthesis, evaluation, resource allocation, and human oversight.

Agent capability can therefore be thought of as a system-level property:

<div class="flow"><span>Model</span><b>+</b><span>tools</span><b>+</b><span>context</span><b>+</b><span>orchestration</span><b>+</b><span>coordination</span><b>+</b><span>evaluation</span><b>+</b><span>human oversight</span></div>

The Anthropic experiments show that these components do not automatically work well simply because the underlying model becomes more capable. Coordination can fail. Agents can converge on the same mistake. Important information can be lost. Dependencies can break. Local objectives can conflict with system-level goals.

OpenAI's published account describes several mechanisms intended to address some of these problems: differentiated research groups, computational and information tools, communication within groups, synthesis of intermediate results, cross-pollination between research directions, dynamic allocation of resources, and an external verification stage.

That may be the most useful takeaway from the Navier–Stokes experiment.

The interesting question is not simply whether an AI model can solve a difficult problem.

It is whether models can be surrounded by the right tools, evaluators, coordination mechanisms, context-management systems, safeguards, and human oversight to operate reliably over long, open-ended tasks.

As agents become more capable, improving the model remains important. But increasingly, the difficult engineering problem may be everything around it.

## References

<div class="references">
<ol>
<li><strong>OpenAI (2026).</strong> <a href="https://openai.com/index/navier-stokes-solution/" target="_blank" rel="noopener noreferrer">On the Navier–Stokes Millennium Prize Problem</a> — OpenAI's primary announcement and description of the result and agent workflow.</li>
<li><strong>Anthropic (2026).</strong> <a href="https://www.anthropic.com/research/multiagent-systems" target="_blank" rel="noopener noreferrer">Patterns and problems in emerging multiagent systems</a> — Experiments on coordination, convergence, information sharing, and other behaviours in multi-agent systems.</li>
<li><strong>Anthropic (2026).</strong> <a href="https://www.anthropic.com/research/riemann-zeta" target="_blank" rel="noopener noreferrer">Learning more about Claude's mathematical capabilities</a> — Anthropic's report on Claude's work related to the Riemann hypothesis and the improved lower bound.</li>
<li><strong>Anthropic (2025).</strong> <a href="https://www.anthropic.com/engineering/multi-agent-research-system" target="_blank" rel="noopener noreferrer">How we built our multi-agent research system</a> — Engineering discussion of Anthropic's orchestrator-worker multi-agent architecture.</li>
<li><strong>Clay Mathematics Institute.</strong> <a href="https://www.claymath.org/millennium/navier-stokes-equation/" target="_blank" rel="noopener noreferrer">Navier–Stokes Equation</a> — Official Millennium Prize Problem page and resources.</li>
<li><strong>Clay Mathematics Institute.</strong> <a href="https://www.claymath.org/millennium-problems/rules/" target="_blank" rel="noopener noreferrer">Rules for the Millennium Prize Problems</a> — Official requirements governing consideration and recognition of proposed solutions.</li>
<li><strong>Nature (2026).</strong> <a href="https://www.nature.com/articles/d41586-026-02842-5" target="_blank" rel="noopener noreferrer">OpenAI claims huge maths breakthrough on a famed ‘Millennium Problem’</a> — Independent reporting on OpenAI's announced Navier–Stokes result and its mathematical significance.</li>
</ol>
</div>

## Disclosure

*AI tools were used to assist with drafting and editing, and to create some of the article’s explanatory visuals.*
