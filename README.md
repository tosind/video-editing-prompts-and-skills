# Video Editing Prompts & Skills

Reusable prompts and a curated skill directory for editing video with Claude Code and OpenAI Codex. Covers motion design, kinetic typography, compositing, captions, audio, color, and native editor automation.

**Start here: [the prompt library](PROMPTS.md).**

## Quick start

1. Copy the shared production brief from [PROMPTS.md](PROMPTS.md#shared-production-brief).
2. Add a task prompt and replace its bracketed inputs.
3. Give your agent access to the source media and a compatible editing tool.
4. Request a rendered preview and editable source, then review the result.

Choose your timing policy before editing:

- **Locked source:** keep the original dialogue, order, pacing, and duration. Add graphics without changing the performance.
- **Editorial cut:** allow trims and rearrangement while preserving meaning and synchronization.

## What's inside

| Prompt | Use it for |
|---|---|
| Cinematic editorial motion graphics | Premium graphics over original footage |
| Dialogue-led kinetic typography | Speech-timed emphasis and text animation |
| Subject masking and depth compositing | Typography and graphics behind a subject |
| Documentary explainer treatment | Diagrams, evidence, and visual explanation |
| Social cutdowns | Short, self-contained clips from recordings |
| Podcast and multicamera editing | Sync, speaker coverage, and dialogue cuts |
| Product demonstrations | Screen recordings, crops, and callouts |
| Captions and accessibility | Accurate captions and readable timing |
| Audio cleanup and sound design | Dialogue clarity, music, and effects |
| Color correction and shot matching | Consistent exposure, color, and skin tone |
| Reference-based motion direction | Translate visual principles into original work |
| Motion systems for a series | Reusable, editable graphic components |
| Review and repair | Timestamped quality checks and fixes |

The library also includes a shared brief, an editor-automation prompt, and ideas for custom skills.

## Published skills

| Project | Best fit | Official resource |
|---|---|---|
| Remotion | React-based composition, animation, captions, and rendering | [Agent Skills](https://www.remotion.dev/docs/ai/skills) |
| HyperFrames | HTML/CSS motion graphics, overlays, and video rendering | [Skills guide](https://hyperframes.heygen.com/guides/skills) |
| Auto-Editor | Silence analysis, rough cuts, and pacing | [Published skill](https://github.com/wyattblue/auto-editor/blob/master/skills/auto-editor/SKILL.md) |

These are external resources, not bundled dependencies. No third-party skills are installed by this repository. Follow each publisher's current installation instructions and license.

## Scope

This repository contains prompts and links. It does not ship an editor, executable integration, or installable custom skill package. Executing a prompt requires the appropriate media, tools, and permissions. A text prompt alone cannot provide subject segmentation, motion tracking, or control of a native editor.

The templates emphasize editing existing footage. Generated assets can be used when a brief explicitly permits them.

## Contributing

Useful additions include tested prompts, primary-source skill links, editor workflows, and before/after examples. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

Repository content is available under the [MIT License](LICENSE). Linked tools, skills, fonts, and media retain their own licenses. This project is independent and is not affiliated with Anthropic, OpenAI, Adobe, Remotion, or HeyGen.
