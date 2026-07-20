# Graph Report - .  (2026-07-20)

## Corpus Check
- Corpus is ~24,693 words - fits in a single context window. You may not need a graph.

## Summary
- 90 nodes · 124 edges · 12 communities (9 shown, 3 thin omitted)
- Extraction: 82% EXTRACTED · 18% INFERRED · 0% AMBIGUOUS · INFERRED: 22 edges (avg confidence: 0.6)
- Token cost: 145,000 input · 16,140 output

## Community Hubs (Navigation)
- Ponytail Lazy-Engineering Skill
- Graphify Skill & Reference Docs
- Ponytail Instructions Loader (JS)
- Ponytail Session Activation Hook (JS)
- Ponytail Config Store (JS)
- Ponytail Runtime State (JS)
- Beach Bliss Retreat Listing Content
- Ponytail Mode Tracker Hook (JS)
- Site Photo Lightbox (JS)
- Ponytail Statusline Script
- Site Weather Widget (JS)

## God Nodes (most connected - your core abstractions)
1. `graphify` - 11 edges
2. `getPonytailInstructions()` - 7 edges
3. `normalizeMode()` - 6 edges
4. `normalizePersistedMode()` - 5 edges
5. `getDefaultMode()` - 5 edges
6. `Ponytail` - 5 edges
7. `Beach Bliss Retreat` - 5 edges
8. `normalizeConfigMode()` - 4 edges
9. `getConfigPath()` - 4 edges
10. `Extraction Subagent Prompt Spec` - 4 edges

## Surprising Connections (you probably didn't know these)
- `graphify Project Integration` --conceptually_related_to--> `graphify Skill Trigger (Global Config)`  [INFERRED]
  CLAUDE.md → .claude/CLAUDE.md
- `Ponytail (Plugin Copy)` --semantically_similar_to--> `Ponytail`  [INFERRED] [semantically similar]
  .claude/plugins/ponytail/skills/ponytail/SKILL.md → .claude/skills/ponytail/SKILL.md
- `graphify Project Integration` --references--> `graphify`  [EXTRACTED]
  CLAUDE.md → .claude/skills/graphify/SKILL.md
- `ponytail: Comment Convention` --semantically_similar_to--> `Confidence Tagging System (EXTRACTED/INFERRED/AMBIGUOUS)`  [INFERRED] [semantically similar]
  .claude/skills/ponytail/SKILL.md → .claude/skills/graphify/SKILL.md
- `graphify Project Integration` --references--> `Query, Path, Explain Reference`  [EXTRACTED]
  CLAUDE.md → .claude/skills/graphify/references/query.md

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **Ponytail Skill Family** — claude_skills_ponytail_skill_ponytail, claude_skills_ponytail_review_skill_ponytailreview, claude_skills_ponytail_audit_skill_ponytailaudit, claude_skills_ponytail_debt_skill_ponytaildebt, claude_skills_ponytail_gain_skill_ponytailgain, claude_skills_ponytail_help_skill_ponytailhelp [INFERRED 0.85]
- **graphify SKILL.md Reference Documentation Set** — claude_skills_graphify_skill_graphify, claude_skills_graphify_references_add_watch_addwatch, claude_skills_graphify_references_exports_exports, claude_skills_graphify_references_extraction_spec_extractionspec, claude_skills_graphify_references_github_and_merge_githubmerge, claude_skills_graphify_references_hooks_hooks, claude_skills_graphify_references_query_query, claude_skills_graphify_references_transcribe_transcribe, claude_skills_graphify_references_update_update [EXTRACTED 1.00]
- **Lightbox Photo Viewer Flow** — index_openlightbox, index_closelightbox, index_lbgo [INFERRED 0.85]

## Communities (12 total, 3 thin omitted)

### Community 0 - "Ponytail Lazy-Engineering Skill"
Cohesion: 0.19
Nodes (13): Ponytail (Plugin Copy), Confidence Score Rubric (Discrete Values), Extraction Subagent Prompt Spec, Node ID Format Convention, Confidence Tagging System (EXTRACTED/INFERRED/AMBIGUOUS), Ponytail Audit, Ponytail Debt, Ponytail Gain (+5 more)

### Community 1 - "Graphify Skill & Reference Docs"
Cohesion: 0.21
Nodes (12): graphify Skill Trigger (Global Config), graphify Project Integration, Add URL & Watch Reference, Exports & Benchmark Reference, GitHub Clone & Cross-Repo Merge Reference, Commit Hook & CLAUDE.md Integration Reference, LESSONS.md Reflection Mechanism, Query, Path, Explain Reference (+4 more)

### Community 2 - "Ponytail Instructions Loader (JS)"
Cohesion: 0.27
Nodes (11): normalizeMode(), normalizePersistedMode(), RUNTIME_MODES, { DEFAULT_MODE, normalizeMode, normalizePersistedMode }, filterSkillBodyForMode(), fs, getFallbackInstructions(), getPonytailInstructions() (+3 more)

### Community 3 - "Ponytail Session Activation Hook (JS)"
Cohesion: 0.18
Nodes (10): claudeDir, {
  clearMode,
  isCodex,
  isCopilot,
  setMode,
  writeHookOutput,
}, fs, { getDefaultMode, getClaudeDir, isShellSafe }, { getPonytailInstructions }, mode, output, path (+2 more)

### Community 4 - "Ponytail Config Store (JS)"
Cohesion: 0.33
Nodes (9): fs, getConfigDir(), getConfigPath(), getDefaultMode(), normalizeConfigMode(), os, path, VALID_MODES (+1 more)

### Community 5 - "Ponytail Runtime State (JS)"
Cohesion: 0.25
Nodes (7): getClaudeDir(), fs, { getClaudeDir }, isCopilot, path, stateDir, statePath

### Community 6 - "Beach Bliss Retreat Listing Content"
Cohesion: 0.25
Nodes (8): Airbnb Listing (Room 1413996032984261454), Beach Bliss Retreat, Elizabeth (Host), FL511 Road Conditions Service, Indian Rocks Beach / Indian Shores, Florida, National Hurricane Center (NHC/NOAA), OpenStreetMap Embed, Pinellas County Evacuation Zone A

### Community 7 - "Ponytail Mode Tracker Hook (JS)"
Cohesion: 0.29
Nodes (6): isDeactivationCommand(), { clearMode, setMode, writeHookOutput }, { getDefaultMode, isDeactivationCommand }, clearMode(), setMode(), writeHookOutput()

## Knowledge Gaps
- **40 isolated node(s):** `fs`, `path`, `{ getDefaultMode, getClaudeDir, isShellSafe }`, `{ getPonytailInstructions }`, `{
  clearMode,
  isCodex,
  isCopilot,
  setMode,
  writeHookOutput,
}` (+35 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **3 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `graphify` connect `Graphify Skill & Reference Docs` to `Ponytail Lazy-Engineering Skill`?**
  _High betweenness centrality (0.048) - this node is a cross-community bridge._
- **Why does `Confidence Tagging System (EXTRACTED/INFERRED/AMBIGUOUS)` connect `Ponytail Lazy-Engineering Skill` to `Graphify Skill & Reference Docs`?**
  _High betweenness centrality (0.034) - this node is a cross-community bridge._
- **What connects `fs`, `path`, `{ getDefaultMode, getClaudeDir, isShellSafe }` to the rest of the system?**
  _40 weakly-connected nodes found - possible documentation gaps or missing edges._