# ballot-brief

A Claude skill that helps a voter research the candidates and measures on their
actual ballot, race by race, using criteria the voter defines.

## What it does

1. **Confirms the official ballot first.** It works from a pasted or
   photographed sample ballot, or the county lookup tool, and never guesses
   districts from an address, because redistricting breaks that.
2. **Interviews the voter** about the issues they care about, the candidate
   qualities they value, and whether campaign funding matters to them.
3. **Researches every contested race in parallel** with sub-agents, giving
   every serious candidate the same depth regardless of party, with cited
   sources.
4. **Handles nonpartisan items separately:** judicial retention, special
   districts, school boards and ballot measures, including the fiscal effect on
   the voter where it can be calculated.
5. **Delivers a race-by-race guide** with a criteria-based pick per race and the
   honest tradeoff behind it, plus a list of what couldn't be verified.

## Party-agnostic by design

The skill never assumes a voter's politics, and it doesn't filter by party. If
asked for "one party's candidates only", it pushes back once. It offers to turn
the party preference into explicit criteria and review everyone against them,
then respects the voter's decision. A closed primary, where the ballot is
legally single-party, is the exception.

## Install

Copy the `ballot-brief` folder (containing `SKILL.md` and `references/`) into
your skills directory, for example `~/.claude/skills/ballot-brief/` for Claude
Code, or upload it as a custom skill in Claude.

## Use

Say something like "help with my ballot", "who's on my ballot for November?",
or attach photos of your mail ballot.

## Customize

- Fill in `references/local-lore.md` with your area's jurisdictions and
  recurring local issues.
- `references/sources.md` is US-focused; add your state's election and
  campaign-finance sites.

## Notes

The skill is built for web search and parallel sub-agents. Without them it
still works, just more slowly. Campaign-finance databases are often paywalled
or blocked, so figures may come from news reports; the skill flags these.

## License

MIT
