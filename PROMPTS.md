# Video editing prompts and skills for Claude Code and Codex

A reusable collection of editing prompts, with a cinematic motion graphics prompt adapted from a contributor-supplied brief. These templates are not claimed to be published prompts from the linked projects.

## How to use this library

Use the shared brief, then paste a task prompt. Replace bracketed inputs. Claude Code or Codex needs access to the media and an actual editing tool, renderer, script bridge, or editor connection to execute an edit. A prompt alone does not provide tracking, segmentation, transcription, or native editor access.

Choose a timeline policy explicitly:

- **Locked source:** preserve dialogue, order, lip sync, pacing, and duration. Graphics can animate independently. No silence removal, speech retiming, repeated dialogue, or inserted holds.
- **Editorial cut:** trims and rearrangement are permitted within the task brief. Preserve factual meaning and maintain audio/video synchronization.

## Shared production brief

```text
This is an editing task using existing footage.

Source: [file or folder]
Editor or rendering stack: [installed tool, or inspect available tools]
Audience and purpose: [brief]
Output: [aspect ratio, resolution, frame rate, delivery format]
Timeline policy: [locked source / editorial cut]
Brand: [fonts, colors, logo, references]
Permitted additional assets: [none / supplied assets / specified licensed sources]
Deliverables: [render, editable project or source, captions if needed]

Inspect source metadata and available tools before choosing an implementation.
Use the original footage and voice. Do not regenerate the person, clone the
voice, invent dialogue, or add unsupported factual claims.
Transcribe only when the task needs speech timing. Mark uncertain words for
review instead of guessing. Keep an original-media backup and edit a copy.

Match the output timeline policy. Prefer source cadence unless conversion is
explicitly requested. Keep overlay text legible at phone size and clear of
faces and the target platform's interface areas.

Create the requested edit, inspect representative frames and transitions,
and check the final render for sync, missing media, text overflow, clipping,
unexpected black frames, and correct delivery settings. Report any checks
that could not be performed. Deliver the render and editable source when
the tool supports it.
```

## Prompt library

### Cinematic editorial motion graphics

Adapted from a contributor-supplied brief, with its preservation rules made explicit.

```text
THIS IS AN EDITING TASK, NOT A VIDEO GENERATION TASK.

Use [source video] as the original source footage. Create a premium 9:16
editorial edit using locked-source timing. Preserve the person, appearance,
expressions, clothing, environment, dialogue, voice, lip sync, pacing, and
total duration. Apply graphics and compositing to the existing footage.

Transcribe the speech and create a timestamped emphasis map. All visible
wording must be exact excerpts from the dialogue, with accurate spelling.
Highlight selected words and ideas instead of running continuous captions.

Build a coherent visual system with strong typography, a restrained palette,
clean spacing, and recurring motion rules. Choose treatments that reinforce
meaning: oversized kinetic type, highlight bars, geometric reveals, tracked
callouts, editorial panels, and typography behind the subject when a clean
matte is available. Do not add unrelated decoration or invented data.

Use smooth punch-ins, reframing, and graphic transitions for emphasis.
Treat 3 to 7 seconds as a pacing reference, not an effects quota. Alternate
energetic moments with clean footage. Keep the face visible.

Use controlled acceleration, weight, overshoot, settling, and appropriate
motion blur. Match the movement to the message. Avoid repetitive bounces,
excessive glitch effects, generic presets, and futuristic interface clutter.

Locked-source timing takes priority over stylistic effects. Do not insert
freeze-frame holds, trim dialogue, reorder speech, or speed-ramp the speaker.
If a freeze-frame treatment is useful, confine it to a graphic layer while
the synchronized source continues. Full-screen type may briefly cover the
image while the unaltered source continues underneath.

Use subject-depth effects only if stable segmentation or rotoscoping is
available. Inspect hair, hands, motion blur, and occlusions. Use a clean
side-panel alternative wherever the mask fails.

Preserve the original voice. Add subtle supplied or permitted effects only
when they improve an emphasis beat. Deliver an MP4, editable source, and a
short timestamped list of the principal treatments.
```

### Dialogue-led kinetic typography

```text
Edit [source] with typography driven by the actual spoken emphasis.
Use locked-source timing. Extract a timestamped word transcript and select
only the phrases that carry the argument. All visible wording must be exact
dialogue excerpts. Build three related treatments for hierarchy: a quiet
phrase reveal, an emphasized word, and a major statement.
Animate in semantic groups rather than moving every word independently.
Let text settle long enough to read. Use deliberate entrances and exits,
clear alignment, and restrained overshoot. Keep faces and gestures clear.
Deliver the edit, editable text layers or source, and the emphasis map.
```

### Subject masking and depth compositing

```text
Add selective depth graphics to [source] without replacing its footage.
Use locked-source timing. Identify a few moments suited to text or shapes
behind the subject. Create temporally stable mattes using available tools.
Match edge softness, motion blur, color spill, and occlusion to the source.
Check hair, hands, glasses, and fast movement at full resolution.
Use only spoken text. Keep the face unobstructed. If an interval cannot be
masked cleanly, redesign it with a side label or foreground-free treatment.
Deliver the composite and editable matte/graphic assets where supported.
```

### Documentary explainer treatment

```text
Edit [source] into an editorial explainer using [timeline policy].
Map each claim to the exact dialogue and supplied supporting assets.
Use restrained labels, diagrams, crops, and visual comparisons to clarify
the argument. Display only dialogue excerpts unless the brief explicitly
permits additional labels. Never infer chart values or fabricate statistics.
Build a consistent type, color, spacing, and transition system.
Use external footage only from the permitted asset set. Preserve the
speaker's meaning and distinguish illustrative visuals from evidence.
Deliver the edit and a timestamped asset and claim reference list.
```

### Social cutdowns from a long recording

```text
Use editorial-cut timing to make [number] self-contained clips of
[duration range] from [recording]. Find moments with a clear opening,
useful development, and a natural ending. Keep necessary qualifications.
Do not splice words into statements the speaker did not make.
Reframe for [aspect ratio], preserving relevant gestures and screen content.
Add [caption style / no captions]. Use spoken text for emphasis graphics.
Deliver each clip, a source-timecode selection list, and editable timelines
or a supported interchange format. State any interchange limitations.
```

### Podcast and multicamera editing

```text
Edit [camera and audio files] into [target format] using editorial-cut timing.
Synchronize using available timecode or waveform evidence and verify drift
near the beginning and end. Prefer the cleanest isolated dialogue tracks.
Cut for speaker intent and useful reactions, avoiding mechanical switching.
Preserve meaningful pauses and complete thoughts. Use J-cuts or L-cuts only
where they preserve context. Flag uncertain sync or missing coverage.
Deliver the edit, synchronized project, and a short unresolved-issues list.
```

### Product demonstration and screen recording

```text
Edit [screen recording and optional presenter footage] into a clear demo.
Use [timeline policy]. Emphasize actual clicks, input, and resulting states.
Use deliberate crops, cursor emphasis, and brief holds only if timing allows.
Keep text legible and avoid inventing interface states, features, or results.
Use exact spoken wording for overlays unless additional labels are permitted.
Preserve enough context to explain where each action occurs.
Deliver the edit and reusable zoom/callout settings or components.
```

### Captions and accessibility

```text
Create accurate captions for [source] in [language]. Preserve source timing.
Verify names, technical terms, punctuation, and speaker changes against audio.
Use readable phrase groups, avoid awkward line breaks, and prevent captions
from covering faces or essential screen content. Mark uncertain transcription.
Use emphasis sparingly without changing wording. Deliver an SRT or VTT file
and, if requested, a captioned render with editable styling. Distinguish a
verbatim transcript from accessibility captions containing sound cues.
```

### Audio cleanup and editorial sound design

```text
Improve [source audio] while preserving the original voice and performance.
Use locked-source timing. Reduce steady noise, rumble, harsh sibilance,
and distracting level variation without metallic artifacts or clipped words.
Do not synthesize replacement speech. Keep breaths and room tone natural.
Use only supplied or permitted music and effects. Duck them around dialogue.
Measure loudness and true peak against [delivery specification], and report
the actual measurements. Deliver the mix and separate stems if supported.
```

### Color correction and shot matching

```text
Correct [footage] for a coherent [reference/look]. Inspect source color
metadata before choosing transforms. Match exposure, white balance, contrast,
and skin tone across shots before applying a creative grade.
Preserve identity and natural texture. Avoid crushed shadows, clipped
highlights, excessive sharpening, and unintended HDR/SDR shifts.
Deliver the graded edit and editable grade settings where supported.
Do not substitute a LUT for shot-level correction.
```

### Reference-based motion direction

```text
Analyze [reference video] for typography, hierarchy, spacing, composition,
motion curves, transition logic, pacing, and sound relationships.
Describe transferable principles, then apply them to [source and brand].
Create original graphics with permitted fonts and assets. Preserve source
identity and [timeline policy]. Produce three representative style frames
and a short motion test, then develop the strongest coherent direction.
Deliver the edit and a compact reusable motion specification.
```

### Motion graphics system for a series

```text
Build an editable motion package for [series/brand] in [tool].
Include a lower third, spoken-word emphasis card, statistic layout, section
transition, and end card only where the series brief permits their wording.
Expose text, colors, typography, duration, and layout controls.
Use consistent easing and spacing. Test long text, short text, portrait and
landscape layouts, and transitions at different durations.
Deliver editable components, a rendered contact sheet or sample reel, and
usage notes explaining the controls and supported constraints.
```

### Review and repair an existing edit

```text
Review [render] against [source, transcript, brief, and editable project].
Identify concrete issues with timestamps: changed meaning, sync drift,
misquotes, illegible text, inconsistent spacing, mask chatter, awkward cuts,
uneven sound, clipped highlights, missing assets, and export mistakes.
Prioritize issues by viewer impact. Repair supported issues in a duplicate
project, render, and verify the affected intervals plus delivery metadata.
Deliver the corrected edit and a concise before/after change list.
```

## Skills and tools worth collecting

### Published skills verified in primary sources

| Resource | Best fit | What to collect |
|---|---|---|
| [Remotion Agent Skills](https://www.remotion.dev/docs/ai/skills) | React-based motion graphics and programmatic video composition | `remotion-best-practices`, `remotion-create`, `remotion-markup`, `remotion-captions`, `remotion-render`, and `remotion-studio` |
| [HyperFrames skills](https://hyperframes.heygen.com/guides/skills) | HTML/CSS motion compositions, footage overlays, and rendered video | Core `hyperframes`, `hyperframes-cli`, `hyperframes-registry`, and `media-use` |
| [Auto-Editor skill](https://github.com/wyattblue/auto-editor/blob/master/skills/auto-editor/SKILL.md) | Dialogue rough cuts, silence analysis, manual ranges, and pacing | `auto-editor`; use its preview before committing to cuts |

Remotion explicitly documents support for Claude Code and Codex. HyperFrames also documents a [Codex workflow](https://hyperframes.heygen.com/guides/with-codex). Auto-Editor's linked resource is a published SKILL.md, rather than a claim of an editor integration.

Documented installation commands, provided for reference and not executed:

```bash
npx skills add remotion-dev/skills
npx skills add heygen-com/hyperframes
```

Use the installer to choose the intended agent and scope. Start with the relevant core skills. Review third-party skill instructions before installing. Auto-Editor cuts alter timing, so its cutting workflow belongs to editorial-cut projects.

### Native editors and supporting tools

These are editing platforms or APIs, not automatically Claude/Codex skills.

| Tool | Useful agent task | Required bridge or condition |
|---|---|---|
| [Premiere Pro UXP](https://developer.adobe.com/premiere-pro/uxp/) | Project, sequence, track, clip, and marker automation | Compatible installed Premiere and a UXP plugin/integration using supported APIs |
| [After Effects API](https://developer.adobe.com/after-effects/uxp/after-effects-api/) | Compositions, layers, properties, and rendering automation | Compatible host and plugin; check API minimum-version requirements |
| [Editly](https://github.com/mifi/editly/) | Declarative clip assembly, text overlays, transitions, and audio | Node.js/FFmpeg environment matching project requirements |
| [Auto-Editor](https://github.com/WyattBlue/auto-editor/) | First-pass cuts driven by audio or other analysis | Installed CLI; review cuts to retain meaningful pauses |

For DaVinci Resolve/Fusion, inspect the scripting documentation shipped with the user's installed version before building automation. No version-specific API or edition availability was verified here.

## Reusable editor-automation prompt

```text
Work in [Premiere Pro / After Effects / Resolve / other editor].
Inspect the installed version and its supported scripting or plugin API.
Determine which actions can actually be executed with the available bridge.
Use a duplicate project. Implement [specific editing task] using supported
operations, preserving source references and organizing assets clearly.
Render a preview if the connection supports it. Otherwise provide the
executable script/plugin and exact run steps, and state that the edit has
not yet been applied. Do not claim success from code generation alone.
```

## Useful custom skills to build next

These are proposed names, not existing verified packages:

- `source-footage-editor`: enforce timeline policy, inspect media, and protect source assets.
- `dialogue-motion-designer`: convert verified speech timing into typography and emphasis beats.
- `subject-depth-compositor`: manage mattes, edge quality, occlusion, and fallback layouts.
- `editor-automation`: maintain version-specific native-editor scripts and supported operations.
- `video-delivery-qa`: inspect exports, text, synchronization, sound, and source fidelity.

A prompt states the creative task. A skill adds repeatable tool instructions, constraints, and validation. Keep those roles clear when expanding this library.

