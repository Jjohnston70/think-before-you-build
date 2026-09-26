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

## License

MIT. See `LICENSE`.

## Who built it

True North Data Strategies LLC, an operations consultancy that builds for the people who run the work. [truenorthstrategyops.com](https://truenorthstrategyops.com)
