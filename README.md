# The Three-Kill Skill

The first explanation can be coherent, plausible, and wrong. The Three-Kill Skill is a small forcing function for the moment a conclusion is about to turn into a ticket, a decision, a diagnosis, a dispatch, or a plan.

Before a claim enters a durable record, name three rival explanations and test each with the cheapest discriminating evidence available now.

If the evidence supports a rival over the original claim, revise the finding. Leave unresolved alternatives open.

## The rule

1. State the current finding as one falsifiable sentence.
2. Name three rivals:
   - a boring mechanical explanation;
   - an instrument explanation, where the query, measurement, or source is wrong;
   - the worst-case explanation.
3. Give each rival one cheap discriminating check.
4. Run the checks now when they take minutes. Record what remains open.
5. Revise the claim when the evidence supports a rival over it. Hold the conclusion if the evidence still cannot distinguish between explanations.

The point is not to make every decision slow. The point is to add a brief check at the exact moment a plausible answer begins to gather momentum.

## Start here

- Read the full [protocol](THREE_KILL.md).
- Copy the [differential template](skills/three-kill/templates/three-kill-differential.md) into a ticket, decision record, incident note, or agent instruction.
- See a [sanitized worked example](examples/payment-report-investigation.md).
- Install the shared skill below, or use the [manual integration guide](integrations/AGENTS.md) for other agents and team workflows.

## Install in Codex or Claude Code

Both clients use the same [skill folder](skills/three-kill), including its template. Run these commands in a terminal (macOS, Linux, or WSL):

```sh
git clone --depth 1 https://github.com/Inflect-ai/three-kill-skill.git
cd three-kill-skill
```

Then run the block for your client from the checkout. You can run both blocks to install in both. The commands stop if that client already has a `three-kill` folder.

### Codex

```sh
skill_dir="$HOME/.agents/skills/three-kill"
mkdir -p "$(dirname "$skill_dir")" &&
  mkdir "$skill_dir" &&
  cp -R skills/three-kill/. "$skill_dir/"
```

In Codex, type `$three-kill` or select `three-kill` from `/skills`. If it does not appear, restart Codex.

### Claude Code

```sh
skill_dir="$HOME/.claude/skills/three-kill"
mkdir -p "$(dirname "$skill_dir")" &&
  mkdir "$skill_dir" &&
  cp -R skills/three-kill/. "$skill_dir/"
```

Start a new local Claude Code session and type `/three-kill` followed by the claim to check.

For example, ask either client to check: "The weekly payment report is low because the processor is dropping transactions."

## Reuse and contributions

InflectAI, Inc. licenses the original documentation, templates, examples, and agent-integration instructions in this repository under [Creative Commons Attribution 4.0 International](LICENSE). You may share and adapt them, including commercially, with attribution. The license does not cover the separately published founder essay, linked or cited third-party works, InflectAI names or trademarks, or software that may be added later. No endorsement is implied.

See [Contributing](CONTRIBUTING.md) for how to submit corrections or examples.

## Lineage

The protocol is informed by diagnostic-reasoning research, including [Graber, Franklin, and Gordon's 2005 study of diagnostic error in internal medicine](https://pubmed.ncbi.nlm.nih.gov/16009864/). It is an operational practice, not medical advice or a substitute for domain expertise.

## Citation

If this protocol helps your team, cite it as:

> InflectAI, Inc., *The Three-Kill Skill* (2026), https://github.com/Inflect-ai/three-kill-skill, licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

For adaptations, say that you adapted the work and note that changes were made. Attribution can go in the workflow documentation or a linked credits page.
