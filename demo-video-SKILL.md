---
name: "demo-video"
description: "Use when creating or revising a narrated demo video, screen recording, or executive walkthrough of an application, including voice-over narration, burned-in captions, or a pointer synchronized to the narration. Also use for requests ending in -automode, which build the video end to end without approval stops."
---

# Demo Video With Synchronized Narration

Produce or revise a genuine screen recording of an application, with generated narration, captions, and a pointer synchronized to the spoken words.

Works for any product. Never carry over a customer, URL, path, port, credential, or expected result from another project. If asked only for a script or prompt, do not record.

## What the user can change
Apply these when given, without re-asking. Report the values used on delivery.

| Setting | Default | Notes |
| --- | --- | --- |
| Pace | 150 words per minute | One locked rate for the entire video; any requested pace replaces it everywhere |
| Voice | `en-US-Andrew:DragonHDLatestNeural` | Female alternative: `en-US-Ava:DragonHDLatestNeural` |
| Burned-in captions | On | Off leaves the selectable track only |
| Pointer | On | Can be turned off |
| Chapters | On | Can be turned off |
| Runtime | 5-7 minutes executive, 8-12 minutes detailed | Fit by changing scope, never by retiming speech |
| Audience framing | Executive | Can be technical, training, or product overview |
| Approval gates | On | Append `-automode` to the request to build end to end without stopping |
| Motion | On | Camera moves, overlays, and chapter transitions. Can be reduced to plain capture |
| Frame rate | 60 fps | Lower only when capture cannot sustain it; say so on delivery |

Deliver the features that are enabled. If captions, pointer, or chapters are turned off, leave them out.

These settings are adjustable. The rules on authorization, privacy, preserving the user's environment, and representing only what actually happened are not adjustable and no request overrides them.

When a requested change is vague, such as "a bit faster" or "the other voice," state the specific value you intend to use and proceed.

## Conflicting requests
When requested runtime, depth, and coverage cannot all hold, say so plainly and propose the trade-off before building. Honor a hard runtime limit by reducing scope. Never change the speaking rate, speed up rendered audio, or pad with silence to fit.

## Order of work
1. **Inspect.** Learn the application, its real workflows, and its current state. Check capture, narration, motion, and encoding tooling. Ask only about blockers.
2. **Rehearse and capture outcomes.** Run the workflows and record what actually happens, including failures. Do this before writing any narration that describes a result.
3. **Agree the storyline.** Propose the key messages and the one or two memorable takeaways, and get the user's confirmation before writing a line of script. See "Storyline approval."
4. **Propose the script** built from the approved storyline, checked against those observed outcomes and the pronunciation list, and get the user's confirmation before rendering anything.
5. **Render narration**, calibrate pace, and collect word timings.
6. **Record the final visual take**, driven by the narration timings.
7. **Assemble, then validate** cues against the finished video.

Steps 3 and 4 are approval gates. Do not render audio, record a final take, or encode anything until both are confirmed. The only exceptions are rehearsal capture in step 2 and short calibration samples, which cost nothing to discard.

## Automode
When the request ends in `-automode`, run the whole job end to end without stopping for approval. Use this when the user wants a finished video rather than a conversation.

Automode changes only the two approval gates. Everything else in this skill still applies without exception.

What it does:
- Still do the storyline and script work, and still write them down. Decide them yourself instead of asking, and choose the reading best supported by what you observed in rehearsal.
- Make a decision on every open question rather than pausing. When evidence is thin, pick the more conservative claim.
- Resolve vague settings by stating the value you are using and proceeding.
- Deliver the storyline and the final script alongside the video, so the user can see what was decided and ask for a rebuild.
- In the delivery note, list every judgment call you made on the user's behalf, anything you could not demonstrate, and anything a reviewer would most likely want changed.

What it never does:
- Skip rehearsal. Narration still describes only observed outcomes.
- Invent a result, a number, a baseline, or a completed workflow to avoid asking a question.
- Bypass authorization, privacy, or sensitivity rules, share anything externally, create a paid resource, or use an unapproved service.
- Modify, reset, or deploy the user's application, or leave its data changed.
- Relax the pace, pause, truthfulness, or validation requirements. Every validation check still runs and still gets reported.

When a genuine blocker stops the build, such as an application that will not start or missing authorization, stop and say so. Automode removes approval steps, not judgment.

## Storyline approval
Before writing the script, work out what the video is actually for and put it in front of the user as a short, skimmable proposal. Base it on what you observed in rehearsal, not on what the product claims.

Propose, in under one page:
- **Audience and what they should do next.** Who is watching, what decision or action sits on the other side of the video.
- **The problem.** What is hard today, stated in the audience's own terms.
- **Three to five key messages.** Each one a full sentence making a single point, ordered the way the video will make them. Name the workflow or screen that proves each message, so nothing rests on assertion.
- **One or two memorable takeaways.** The lines you want someone to repeat in a meeting a week later, if they remember nothing else. Keep them concrete and specific to this product and this evidence. Two at most; one is usually stronger.
- **What is deliberately left out**, and why, so scope is visible before it becomes a runtime problem.
- **Proposed chapters and rough runtime**, and the framing, voice, and pace that will be used.
- **Anything you could not demonstrate**, including workflows that failed or that you could not reach, and how the storyline handles that honestly.

Takeaways follow the narration style rules. They are plain declarative sentences that survive being said out loud. No slogans, no contrast templates, no numbers you did not observe.

Ask for confirmation, offering the user the choice to approve as written, change the takeaways, or reorder or drop messages. If the user changes the storyline, restate it and confirm again before moving on.

## Script approval
Write the script only from the approved storyline. Every section must serve a named key message, and the takeaways must be spoken somewhere they land naturally, usually once where the evidence appears and once in the close.

Present the script with its chapter structure, the key message each section carries, the approximate word count and the resulting runtime at the locked pace, and any place where the observed behavior forced a change to what the storyline promised. Flag anything you had to soften because the demo could not prove it.

Get explicit confirmation on the script text before rendering. When the user edits the script, apply the changes, recompute the runtime, and show the revision rather than assuming approval carries over.

If a script edit breaks a key message or a takeaway, say so and confirm the storyline change rather than quietly dropping it.

## Capture and preservation
Record only the application and only what the user is authorized to show. Keep the desktop, notifications, credentials, and unrelated windows out of frame.

Choose a capture method that suits the product: browser automation, desktop capture, emulator, or device. Prefer an isolated instance with its own data. When using headless capture, confirm the rendering matches what a normal user sees.

Never reset the user's application, copy production data into a rehearsal, deploy, send anything externally, or modify the product to force a better take. Leave the original environment as you found it.

## Narration style
Use simple English and complete, connected sentences. Explain what is happening, why it matters, and what follows. Sound like someone explaining their work to a colleague.

Do not use punchy statements, slogans, dramatic fragments, promotional language, manufactured urgency, or rhetorical questions. Do not use contrast templates such as "not X, but Y" or "this is not X; it is Y" — state the fact directly.

Avoid business jargon, reading labels aloud, unexplained acronyms, and repeated "as you can see." Explain necessary technical terms in plain words.

Apply this style to narration, chapter titles, captions, and any on-screen text. Review the whole script for these patterns before rendering.

## Story
The approved storyline governs the video. Open with 20-30 seconds on the problem, why it matters, and what the demo will show. Cover one or two workflows in depth rather than touring every screen. Give each chapter one clear point drawn from an approved key message, and explain why something matters before showing how it works.

Separate what was demonstrated from what is possible and what is planned. Never invent results, savings, baselines, integrations, or completed work.

Close with a plain summary that restates the memorable takeaways in the words the user approved, and the next step that fits the request. Propose pilot governance such as owners, data, measures, and a review date only when a pilot is genuinely in scope.

Where the demo runs on sample data, a local copy, or role-play rather than real authority, say so at the start and again where it affects a decision. Do not describe a real authorized environment as synthetic.

## Truthful capture
Map every spoken phrase to the element it describes, the action taken, and the state actually visible.

When the application produces an unexpected result, change the narration to match it. Keep meaningful failures and retries, or explain why a path could not be shown. Never present an unexecuted path as completed, and never narrate a finished action over a screen that still shows it pending. Label any shortened waiting period.

## Narration rendering
Prefer a neural speech service the user already has approved, because it gives natural delivery, explicit rate control, and word timings. Check for an existing approved resource before proposing a new one. Never create a paid resource or use an unapproved service without explicit approval; report the option and its cost instead.

Local operating-system voices are a fallback. They sound clearly synthetic and generally do not provide word timings, so pointer and caption sync must come from separate alignment and will be less precise. Tell the user when you have fallen back and what that costs.

Verify the current authentication method, exact voice identifiers, regional availability, and pricing at the time of use rather than assuming. Never print keys, tokens, or secrets.

Practical notes:
- Calibrate the speaking rate on a short sample, repeating until measured output lands within about five words per minute of target. A rate setting alone does not tell you the actual pace.
- Lock the voice and rate, then render each section once. High-definition voices vary between renders, so re-rendering one section can leave an audible seam.
- Measure pace on speech only, excluding leading, trailing, and inserted silence. Never let added silence disguise the speaking rate.
- Wait for each audio file to finish writing before encoding it.
- Build a pronunciation list for product names, acronyms, units, and customer names. Check them on a short sample and correct them before the full render.
- Keep pauses short and deliberate; follow the pause budget below rather than adding silence by feel.

## Pace consistency and emphasis
Uneven pace is the most common defect in generated narration and the listener hears it immediately. Treat the speaking rate as a single global constant for the whole video.

Rules:
- Calibrate once, then lock one rate value and use that exact value for every section. Do not tune the rate section by section, and do not set a different rate for an introduction, a summary, or a technical passage.
- Never slow or speed a whole section, sentence, or clause for emphasis, mood, importance, or to hit a timing target. Rate changes at that scale read as a machine shifting gears, not as a person speaking.
- Get emphasis the way a speaker actually does, at word and short-phrase scale:
  - Put the important word at the end of the sentence, where stress falls naturally.
  - Shorten the sentence around the key term so it carries more weight.
  - Use a brief break of 150-300 milliseconds immediately before a key term, and up to 400 milliseconds after a conclusion, instead of stretching the words.
  - Apply the speech service's word-level emphasis, or a small pitch or volume lift, to no more than three consecutive words.
- Any prosody adjustment must cover a short phrase, last under about one and a half seconds, and return to the locked rate immediately afterward. Adjacent phrases must not be slowed to match it.
- Never compensate for a long section by speaking faster elsewhere. Fix length by cutting words, not by changing rate.
- Never resample, time-stretch, or speed-adjust rendered audio.

Verification: measure speech-only words per minute for every section, and for every fifteen-second window inside a section. Each measurement must land within five words per minute of the target, and the slowest and fastest sections must differ by no more than eight words per minute. When one section falls outside the band, re-render that section at the locked rate rather than adjusting the others.

## Pause budget
Dead air at the opening and between sections makes a demo feel slow and unfinished. Keep silence deliberate and short.

- Trim leading and trailing silence inside every rendered audio segment to 150 milliseconds or less before assembly, since speech services often emit far more.
- The first spoken word begins within one second of the video starting. Hold the opening frame only as long as it takes to be readable.
- Between sections, leave 400-700 milliseconds. Never exceed one second unless something on screen genuinely requires the time.
- After a screen transition, allow 0.5 to 1 second for the layout to settle before narration resumes, and only when the screen actually changed. Dense screens may take slightly longer; say why in the build notes when they do.
- Let sentence-level pauses come from the voice itself. Do not insert extra silence between sentences within a section.
- Silence is never used to pad runtime, to disguise the speaking rate, or to let a slow render catch up.
- Trailing silence at the end of the video stays under one and a half seconds.

Any pause longer than one second must be intentional, tied to something visible, and labeled in the cue manifest with the reason. Treat every unlabeled gap over one second as a defect to remove.

## Motion and transitions
A recording of static screens with a pointer moving over them looks unfinished. Motion is what makes a demo read as produced. Treat it as a comprehension device that directs attention to the thing being discussed, never as decoration.

Motion is on by default. It can be turned down to plain capture on request.

### Capture settings that make motion possible
Decide these before the final take, because they cannot be added later.
- Record at 60 frames per second. This is the single largest gain in perceived quality.
- Capture at twice the output resolution so the camera layer can crop in without softening the picture.
- Let the application's own transitions finish. Never cut partway through one.
- Scroll with easing over 600-900 milliseconds rather than jumping the viewport.
- Drive real interactions at human speed and let each screen settle.

### Camera layer
Applied during assembly to real footage, using the resolution headroom.
- A slow push of three to five percent over six to ten seconds while a point is being explained.
- A punch to a cropped detail when narration turns specific, then a return to the full view when it widens again.
- A smooth pan that follows the pointer to its target.
- Keep camera moves under about eight seconds and let them come to rest before the next one starts. Never run two camera moves at once.
- Recompute pointer bounds and caption placement after every crop or pan, since both are defined against the final frame.

### Graphic layer
Composite transparent overlays over the real recording.
- Chapter and title cards with simple typographic motion.
- A highlight mask that dims everything except the region under discussion.
- Callouts, annotations, arrows, and connector lines that draw on and off rather than appearing instantly.
- Animated values, only for numbers the application actually produced and that are visible on screen.
- Lower thirds and a chapter progress indicator.

Build overlays as HTML and CSS, render them to a PNG sequence with alpha through browser automation, and composite with the encoder. Keep every overlay clear of the pointer target and the caption band.

### Transitions
- Cross dissolve of 250-400 milliseconds between chapters.
- A brief dip through a neutral or brand color only at a major act break.
- A hard cut inside a workflow. Never dissolve across a state change; a dissolve there is indistinguishable from concealing a step.
- Do not use wipes, spins, slides, flashes, or any transition that draws attention to itself.

### Easing and restraint
Use ease-in-out for anything the eye follows, and a short ease-out for something arriving. Nothing moves at a constant speed. Keep at most one deliberate motion running at a time, so the viewer always knows where to look. When a screen is already busy, hold still.

### Honesty rules for motion
These are not adjustable.
- Never animate a value, chart, state, or interface element the application did not produce.
- Never simulate loading, progress, or a result that did not occur.
- A transition must never hide a state change, a failure, a retry, or a cut that skips work.
- A shortened waiting period stays labeled, and a transition does not substitute for that label.
- Motion never obscures the element being discussed, the pointer target, or the captions.

### Timing
Motion cues live in the same cue manifest, on the same final-video clock, driven by the same word timings as the pointer and captions. A move that supports a spoken phrase begins slightly before the phrase and settles during it. Motion never justifies extending a pause, and never changes the speaking rate. Recompute motion cues against the assembled file after any trim, join, or offset.

## Pointer and caption synchronization

Take word or phrase timestamps from the speech service, never from a percentage of a scene.

For each spoken reference: scroll the target into view, let the layout settle, measure its current bounds, then move the pointer smoothly to arrive 0.3-0.6 seconds before the words and hold through the explanation. Point beside text without covering it. On a chart, indicate the specific mark being discussed. Recalculate bounds after any scroll, resize, or crop. Hide the pointer during general narration, and use a visible pulse only for a real click.

Captions are burned into the picture by default so they show regardless of the player, with a selectable track also embedded. Plan the output canvas and the application viewport together so adding a caption band does not shrink the interface below readable size. Keep captions clear of the pointer target and the content being discussed. Show one or two lines at a time, broken at natural phrase boundaries. Caption text must match the spoken words exactly, including qualifications.

Maintain one cue manifest in final-video time. Segment offsets, inserted silence, trims, and joins all shift cues during assembly, so recompute against the assembled file rather than the source audio.

Whenever the voice, pace, or wording changes, regenerate the narration, timings, captions, and pointer cues. Reuse footage only where the sequence and the real on-screen states still match; re-record the rest. Never move replacement audio onto old timings, and never resample finished audio to change pace.

When revising an existing video, confirm what is changing before rebuilding. A wording, voice, or pace change needs only script confirmation. A change to what the video argues needs the storyline confirmed again first.

## Assemble, validate, deliver
Produce an MP4 with H.264 video and AAC audio at a resolution where the interface stays readable. Normalize narration around -16 LUFS with true peaks no higher than -1 dBTP.

Encoding and compositing use ffmpeg and ffprobe, installed on this machine. The camera layer uses `zoompan` or per-frame `crop`, chapter transitions use `xfade`, transparent overlays composite with `overlay`, and narration loudness uses `loudnorm`. Confirm the tools resolve on the current shell before starting a build, since a freshly installed path may not be present in an existing session.

Validate against the finished file:
- Each pointer cue arrives within the intended window before its spoken reference and stays through the explanation.
- Captions match the spoken words, are legible, and cover nothing important.
- Measured speaking pace is within five words per minute of target for every section and every fifteen-second window, and no two sections differ by more than eight words per minute.
- No emphasis was created by slowing a section, sentence, or clause.
- Leading silence is under one second, gaps between sections are 400-700 milliseconds, and every gap over one second is labeled with a reason.
- Transitions settle before narration resumes; screen text is readable.
- Every section carries an approved key message, and the memorable takeaways are spoken as approved.
- Narration style contains no punchy lines or contrast templates.
- Every action shown matches what is narrated.
- Every animated value corresponds to something the application actually produced.
- No transition hides a state change, a failure, or skipped work.
- Motion settles before the next move begins, and never covers the pointer target or the captions.
- Frame rate is constant and matches the capture setting.
- Media decodes fully; duration and enabled features are correct.
- The original application and its data are unchanged.

Confirm the deliverable plays correctly where it will actually be viewed, since chapter and subtitle support varies between players. Supply a sidecar caption file when the target player needs one.

Deliver a clickable link with the actual duration, the voice and measured pace, and a note that narration is synthetic. Do not share externally without confirmation. Stop only the processes you started and remove temporary copies. Keep the source media, narration segments, cue manifest, and build scripts so settings can be changed later without re-recording.

State honestly which checks you could not perform. Reviewing frames and timings is not the same as listening to the audio.

