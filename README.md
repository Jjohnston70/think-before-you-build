# Think Before You Build

Two thinking tools for operators. One pressure-tests a decision before you commit resources. The other finds the gaps in a process or system before you build or fix it.

## The two skills

| Skill | Use it when | What you get |
|---|---|---|
| The Bearing Check | "Should I do this?" A career move, an investment, a strategy you want to copy | Eight checkpoints from base rate to pre-mortem, and a final bearing with a confidence level |
| World Model Mapper | "Why isn't this working?" or "What should this system track?" | A state inventory, action map, transition model, feedback audit, a ranked gap report, and one next step |

They work in order. The Bearing Check decides whether a move is worth making. The World Model Mapper works out what the system has to capture once you make it.

## The ideas underneath

| Idea | In practice |
|---|---|
| Study the graveyard, not just the winners | Look up who tried the same thing and failed before you copy anyone |
| Base rates come with a source | Every success rate is looked up and dated in the session, never stated from memory |
| All-in is fragility, not confidence | Start small, raise the bet as evidence builds, keep a margin of safety |
| Shadows vs. reality | A status someone typed is a shadow; a timestamp a system recorded is reality |
| Every prediction needs a feedback loop | If you can't say how you would know a prediction was wrong, the loop is broken |

## What is in the plugin

| Path | What it is |
|---|---|
| `skills/bearing-check/SKILL.md` | The eight checkpoints and output format |
| `skills/bearing-check/references/` | Detailed checkpoint examples, the seven cognitive traps, red flags |
| `skills/bearing-check/USER_MANUAL.md` | How to invoke it, full vs. quick pass, attribution |
| `skills/world-model-mapper/SKILL.md` | The five-phase mapping workflow and deliverables |
| `skills/world-model-mapper/*.md` | Domain physics, feedback loop patterns, shadow vs. reality, output template, user manual |

## Install

Once it is listed in the Claude plugin directory: in Claude Code, open `/plugin` and find it under Discover; in the Claude app, add it from the directory.

## How to use it

Ask Claude "run a bearing check on [decision]" or "map this process: [process]." Both skills also trigger on everyday phrasing like "should I" or "where are the gaps in this workflow."

## Credits

The Bearing Check synthesizes established ideas from decision theory and behavioral economics; its original eight-step structure was inspired by an article in the Data Science Collective on Medium. The World Model Mapper applies Yann LeCun's case for world models to business operations.

## Example prompts

| Prompt | Skill |
|---|---|
| "Run a bearing check on quitting my job to consult full time." | The Bearing Check, full pass |
| "Quick bearing check: should I copy my competitor's free-trial offer?" | The Bearing Check, checkpoints 1, 5, 7 |
| "Map this process: how we schedule and dispatch jobs, from customer call to completed work." | World Model Mapper |
| "Our team stopped using the dashboard we built. Diagnose it." | World Model Mapper, debugging mode |

## Troubleshooting

| Problem | Fix |
|---|---|
| The skill does not kick in | Ask for it by name: "Run a bearing check on..." or "Use the world-model-mapper skill on..." Then confirm the plugin is installed and enabled (in Claude Code, run `/plugin`). |
| The wrong skill answers | Name the one you want. "Should I" questions belong to the Bearing Check; "what should this system track" belongs to the World Model Mapper. |
| A base rate appears with no source or date | Ask for the source and the date on the page. If Claude cannot search, turn on web search or supply the number yourself. The skill treats an unsourced rate as unconfirmed. |
| The mapping feels too abstract | Give one concrete case: "Walk through what happened the last time a job ran late." The framework works best on a specific event. |
| The Mermaid diagram in the output template shows as plain text | Your viewer does not render Mermaid. GitHub, VS Code with a Mermaid extension, and most Markdown tools that support Mermaid will draw it. |

## Support

| Need | Where |
|---|---|
| Bug, wrong behavior, or a question | Open an issue at https://github.com/Jjohnston70/think-before-you-build/issues |
| Security or privacy concern | Email jacob@truenorthstrategyops.com with "Security" in the subject; please do not open a public issue |

## License

MIT. See `LICENSE`.

## Who built it

True North Data Strategies LLC, an operations consultancy that builds for the people who run the work. [truenorthstrategyops.com](https://truenorthstrategyops.com)
