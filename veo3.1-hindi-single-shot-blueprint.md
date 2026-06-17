# 🎬 Veo 3.1 Prompt Blueprint — Hindi Dialogue, Single Continuous Shot

> A reusable template and complete condition reference for writing Veo 3.1 prompts that generate **one uninterrupted take**, with natural **Hindi dialogue**, no unwanted subtitles, no hidden cuts — covering text-to-video, image-to-video, first/last-frame, and multi-character reference workflows.

---

## 📑 Table of Contents

1. [Core Prompt Formula](#1-core-prompt-formula)
2. [Complete Reference — Shot Types, Angles, Movements & Conditions](#2-complete-reference)
3. [Block-by-Block Rules](#3-block-by-block-rules)
4. [Master Template](#4-master-template)
5. [Filled Example](#5-filled-example)
6. [Two-Character Dialogue Variant](#6-two-character-variant)
7. [Common Failure Modes & Fixes](#7-failure-modes)
8. [Face / Character Reference Image Conditions](#8-face-reference)
9. [Two-Character (Multi-Character) Scene Conditions](#9-multi-character)
10. [Other Conditions Worth Planning For](#10-other-conditions)
11. [Image-to-Video & First-Frame-to-Last-Frame](#11-image-to-video)
12. [Full Combined Example (Everything Together)](#12-combined-example)
13. [Negative Prompt Cheat Sheet](#13-negative-prompts)
14. [Quick Checklist Before Generating](#14-checklist)

---

<a id="1-core-prompt-formula"></a>
## 🧩 1. Core Prompt Formula

Every prompt is built from these blocks, in this order:

```
[SHOT TYPE] + [ANGLE] + [CAMERA MOVEMENT] + [LENS/FOCUS] + [SUBJECT] +
[SETTING] + [LIGHTING] + [ATMOSPHERE] + [ACTION] + [DIALOGUE] +
[TONE/DELIVERY] + [AUDIO] + [STYLE/MOOD] + [NEGATIVE PROMPT]
```

For a single continuous shot, pick **exactly ONE** option from Shot Type, Angle, and Camera Movement — never combine two ("close-up that becomes a wide shot" = a cut, which is what we're avoiding).

---

<a id="2-complete-reference"></a>
## 📚 2. Complete Reference — Shot Types, Angles, Movements & Conditions

The full menu. Mix one item per category into the template in Section 4.

<details>
<summary><strong>2.1 Shot Types (framing / distance)</strong></summary>

| Shot Type | What it shows | Veo phrasing |
|---|---|---|
| Extreme Wide Shot (EWS) | Subject tiny within a vast environment | `extreme wide shot, subject small within the landscape` |
| Wide Shot / Long Shot (LS) | Full environment, subject fully visible | `wide shot, full environment visible` |
| Full Shot (FS) | Subject head-to-toe, environment secondary | `full shot, subject visible head to toe` |
| Medium Wide / "Cowboy" Shot | Mid-thigh up | `medium wide shot, framed from mid-thigh up` |
| Medium Shot (MS) | Waist up | `medium shot, framed from the waist up` |
| Medium Close-Up (MCU) | Chest/shoulders up | `medium close-up, framed from the chest up` |
| Close-Up (CU) | Face fills most of frame | `close-up on the face` |
| Extreme Close-Up (ECU) | Eyes, mouth, or single detail | `extreme close-up on the eyes` |
| Two-Shot | Two subjects both fully in frame | `two-shot, both subjects in frame throughout` |
| Three-Shot | Three subjects in frame | `three-shot, all three subjects visible` |
| Over-the-Shoulder (OTS) | Foreground subject's shoulder, second subject beyond | `over-the-shoulder shot favoring [subject]` |
| Point of View (POV) | Camera = a character's eyes | `first-person point-of-view shot, as if seen through [character]'s eyes` |
| Insert Shot | Tight detail on an object (no face) | `insert shot, close on the [object] only` |
| Establishing Shot | Sets location before/without subject focus | `establishing wide shot of [location]` |
| Master Shot | Wide shot covering full scene/action in one take | `single master shot covering the entire scene` |

</details>

<details>
<summary><strong>2.2 Camera Angles</strong></summary>

| Angle | Feel it creates | Veo phrasing |
|---|---|---|
| Eye-Level | Neutral, natural, relatable | `eye-level angle` |
| High Angle | Subject looks smaller/vulnerable | `high angle, looking down at the subject` |
| Low Angle | Subject looks powerful/dominant | `low angle, looking up at the subject` |
| Bird's Eye View | Total overview, detached | `bird's eye view, directly overhead` |
| Worm's Eye View | Extreme upward, looming feel | `worm's eye view, extreme low angle looking straight up` |
| Dutch Angle (Tilted) | Unease, disorientation, tension | `Dutch angle, camera tilted` |
| Three-Quarter Angle | Slightly off-center, common for dialogue | `three-quarter angle on the subject's face` |
| Profile / Side Angle | Subject seen from the side | `profile shot, subject seen from the side` |

</details>

<details>
<summary><strong>2.3 Camera Movements (pick one for the whole shot)</strong></summary>

| Movement | Effect | Veo phrasing |
|---|---|---|
| Static / Locked-off | Calm, stable, observational | `static shot, camera does not move` |
| Pan (L→R or R→L) | Reveals space horizontally | `camera pans slowly from left to right` |
| Tilt (Up/Down) | Reveals space vertically | `camera tilts upward from feet to face` |
| Dolly In (Push-in) | Builds intimacy/tension | `camera slowly dollies in toward the subject` |
| Dolly Out (Pull-out) | Builds distance/isolation | `camera slowly pulls back from the subject` |
| Tracking / Trucking Shot | Follows subject laterally | `camera tracks alongside the subject as they walk` |
| Crane / Jib Shot | Smooth vertical rise or fall | `crane shot rising slowly from ground level to overhead` |
| Handheld | Raw, documentary, intimate | `handheld camera with slight natural sway` |
| Steadicam / Gimbal | Smooth but mobile, floating feel | `smooth steadicam movement following the subject` |
| Zoom In / Out | Compresses distance optically (no physical move) | `slow zoom in on the subject's face` |
| Whip Pan | Fast, jarring transition-like motion | `fast whip pan across the room` |
| Arc Shot | Circles around the subject | `camera arcs slowly around the subject` |
| Aerial / Drone Shot | Wide elevated motion over a scene | `aerial drone shot moving forward over the landscape` |
| Dolly Zoom ("Vertigo Effect") | Background warps while subject stays same size | `dolly zoom effect, background stretches as camera pulls back` |

</details>

<details>
<summary><strong>2.4 Lens & Focus Conditions</strong></summary>

| Condition | Effect | Veo phrasing |
|---|---|---|
| Shallow Depth of Field | Blurred background, subject sharp | `shallow depth of field, blurred background` |
| Deep Focus | Everything sharp, foreground to background | `deep focus, entire scene sharp` |
| Rack Focus | Focus shifts from one subject to another | `rack focus shifting from [A] to [B]` |
| Wide-Angle Lens | Expansive, slight edge distortion | `shot on a wide-angle lens` |
| Telephoto Lens | Compressed background, flattering on faces | `shot on a telephoto lens, compressed background` |
| Fisheye Lens | Heavy distortion, surreal/comedic | `fisheye lens distortion` |
| Macro | Extreme close detail (texture, droplets, insects) | `macro shot, extreme close detail on texture` |

</details>

<details>
<summary><strong>2.5 Lighting Conditions</strong></summary>

| Condition | Mood | Veo phrasing |
|---|---|---|
| Golden Hour | Warm, romantic, nostalgic | `golden hour lighting, warm low sun` |
| Blue Hour | Calm, melancholic, cool | `blue hour lighting, soft cool tones just after sunset` |
| Harsh Midday Sun | Stark, high contrast | `harsh midday sunlight, strong shadows` |
| Overcast / Diffused | Soft, even, neutral | `overcast diffused daylight, soft shadows` |
| Backlit / Silhouette | Mysterious, dramatic | `backlit, subject in silhouette` |
| Low-Key Lighting | Dark, dramatic, moody | `low-key lighting, deep shadows, single light source` |
| High-Key Lighting | Bright, cheerful, minimal shadow | `high-key lighting, bright and evenly lit` |
| Practical Lighting | Lamps, candles, neon signs in-frame | `lit by practical sources, neon signage glow` |
| Moonlight / Night | Cool, quiet, dim | `moonlit night scene, cool blue tones` |
| Studio Lighting | Controlled, polished, three-point setup | `studio three-point lighting setup` |

</details>

<details>
<summary><strong>2.6 Atmospheric / Environmental Conditions</strong></summary>

| Condition | Veo phrasing |
|---|---|
| Rain | `light rain falling, wet surfaces reflecting light` |
| Fog / Mist | `thin fog drifting through the scene` |
| Dust / Sand | `fine dust hanging in the air` |
| Smoke / Haze | `soft haze in the air, diffusing light` |
| Wind | `gentle wind moving hair and clothing` |
| Snow | `light snow falling steadily` |
| Crowded space | `busy background with people moving naturally` |
| Empty/Isolated space | `empty space, no one else around` |

</details>

<details>
<summary><strong>2.7 Composition Conditions</strong></summary>

| Condition | Veo phrasing |
|---|---|
| Rule of Thirds | `subject positioned off-center per rule of thirds` |
| Centered / Symmetrical | `subject centered, symmetrical composition` |
| Leading Lines | `leading lines drawing the eye toward the subject` |
| Foreground Framing | `framed through [doorway/window/branches] in the foreground` |
| Negative Space | `large negative space around the subject` |

</details>

<details>
<summary><strong>2.8 Time & Setting Conditions</strong></summary>

| Condition | Veo phrasing |
|---|---|
| Dawn | `early dawn light, soft pink-orange sky` |
| Day | `clear daytime lighting` |
| Dusk | `dusk lighting, fading light` |
| Night | `night setting, artificial light sources` |
| Indoor | `indoor setting` |
| Outdoor | `outdoor setting` |
| Urban | `urban street setting` |
| Rural | `rural village setting` |

</details>

---

<a id="3-block-by-block-rules"></a>
## ✍️ 3. Block-by-Block Rules

**Subject** — describe age, clothing, expression, and posture, as specific as describing someone over a phone call to a person who can't see them.
```
A middle-aged shopkeeper in a faded blue kurta, tired eyes, gentle smile
```

**Setting** — where + lighting + atmosphere (pull from Sections 2.5–2.8).

**Action** — one continuous motion or beat that fits inside a single uncut shot.
```
he wipes a glass clean while glancing toward the camera
```

**Dialogue (Hindi)** — the critical part:

| Rule | Detail |
|---|---|
| Script over transliteration | Devanagari gives the most reliable lip-sync and pronunciation; Hinglish (Roman script) works but pronunciation drifts more |
| Use a colon, never bare quotes | `शॉपकीपर कहता है: "अरे भाई..."` ✅ vs `शॉपकीपर कहता है "अरे भाई..."` ❌ (no colon = higher subtitle risk) |
| Name the speaker explicitly | Especially in multi-character scenes — prevents misattribution |
| Keep it short | 1–2 sentences per 8-second clip; long dialogue hurts lip-sync and risks an inserted "cut" to fit the speech |

**Tone / Delivery**
```
Dialogue (Hindi, warm and inviting tone, slightly playful):
```
Other tags: `weary voice`, `whispered`, `angry and clipped`, `nervous, fast-paced`, `formal and respectful`.

**Audio** — always specify what should and shouldn't be heard.
```
Audio: clinking cups, distant traffic hum, no background music, no audience sounds
```

**Negative Prompt** (always include — full list in [Section 13](#13-negative-prompts)):
```
No subtitles, no captions, no on-screen text, no scene cuts.
```

---

<a id="4-master-template"></a>
## 🧱 4. Master Template

```
Single continuous [SHOT TYPE] shot, [ANGLE], [CAMERA MOVEMENT],
[LENS/FOCUS CONDITION], no cuts, no edits.
[SUBJECT DESCRIPTION] in [SETTING], [LIGHTING CONDITION], [ATMOSPHERE].
[He/She/They] [ACTION].
[Speaker name] says: "[HINDI DIALOGUE LINE]"
Dialogue (Hindi, [TONE/DELIVERY]).
Audio: [AMBIENT SOUNDS], [MUSIC OR NO MUSIC], [explicitly exclude unwanted sounds].
Style: [MOOD/AESTHETIC], [COMPOSITION CONDITION].
No subtitles, no captions, no on-screen text.
```

---

<a id="5-filled-example"></a>
## ✅ 5. Filled Example

```
Single continuous medium shot, eye-level angle, slow dolly-in,
shallow depth of field, no cuts, no edits. A middle-aged shopkeeper in a
faded blue kurta, tired but kind eyes, stands inside a small roadside chai
stall in Mumbai, golden hour lighting, faint steam drifting through the air.
He wipes a glass clean and looks up toward the camera.
The shopkeeper says: "अरे भाई, चाय पियो, गरमागरम है।"
Dialogue (Hindi, warm and inviting tone, slightly playful).
Audio: clinking cups, distant traffic hum, faint street chatter, no
background music, no audience sounds.
Style: warm documentary-style realism, subject framed per rule of thirds.
No subtitles, no captions, no on-screen text.
```

---

<a id="6-two-character-variant"></a>
## 👥 6. Two-Character Dialogue Variant

```
Single continuous two-shot, eye-level angle, static camera, no cuts,
no scene changes. [Character A description] and [Character B description]
stand facing each other in [setting], [lighting condition]. Both remain in
frame for the entire shot.
[Character A name] says: "[Hindi line 1]"
[Character B name] replies: "[Hindi line 2]"
Dialogue (Hindi, [tone A] for [Character A], [tone B] for [Character B]).
Audio: [ambient sound], no music.
No subtitles, no captions, no cuts between speakers.
```

---

<a id="7-failure-modes"></a>
## 🛠️ 7. Common Failure Modes & Fixes

| Problem | Likely cause | Fix |
|---|---|---|
| Subtitles appear anyway | Quotes used right after "says" with no colon | Use colon before dialogue; repeat "no subtitles" twice |
| Video cuts to a new angle mid-clip | Multiple shot types/movements described together | Reduce to one shot type + one movement, reinforce "no cuts" early in prompt |
| Wrong character speaks the line | Speaker not named explicitly | Always prefix dialogue with a named/described speaker |
| Hindi pronunciation sounds off | Hinglish/Roman script used | Switch to Devanagari script for the dialogue line |
| Random laughter/applause/music appears | Audio block left vague or empty | Explicitly state ambient sound AND what to exclude |
| Dialogue feels rushed or cut short | Line too long for clip duration | Keep to 1–2 short sentences per 8-second generation |
| Camera drifts into a movement you didn't ask for | Movement left unspecified or contradictory terms used | Name exactly one movement from Section 2.3, state "camera does not move" if you want static |
| Lighting doesn't match described mood | Lighting condition too vague ("nice light") | Use a specific named condition from Section 2.5 |
| Background looks empty/wrong despite "crowded" request | Atmosphere condition stated too late in prompt | Move atmosphere/lighting conditions earlier, right after setting |

---

<a id="8-face-reference"></a>
## 🖼️ 8. Face / Character Reference Image Conditions

When you upload a reference photo (Veo 3.1's "Ingredients to Video" feature) instead of describing a character purely in words, different rules apply.

| Condition | Why it matters | Veo phrasing |
|---|---|---|
| Always name the reference explicitly | Veo won't automatically know a description maps to an uploaded image unless you say so | `Using the provided image of [character], create a...` |
| Don't contradict the photo | Conflicting text description confuses the model | Describe only what isn't already visible — clothing change, expression, action — not core facial features |
| Reinforce identity anchors every generation | Reference images reduce drift but don't eliminate it across separate clips | Repeat the same 2–3 descriptive anchor words in every prompt |
| Add an identity-consistency negative prompt | Prevents subtle face/age/wardrobe drift mid-generation | `consistent facial features and clothing throughout, no identity drift` |
| One reference image = one role | Multiple uploaded images need explicit labeling | `the man from the first reference image` / `the woman from the second reference image` |
| Real / public figures | Generating an identifiable real person without consent is restricted by Veo's content policy | Use original/fictional characters, or reference images you have rights to use |
| Object/prop/setting references work the same way | "Ingredients to video" isn't limited to faces | `Using the provided image of the chai stall as the setting...` |

---

<a id="9-multi-character"></a>
## 🧑‍🤝‍🧑 9. Two-Character (Multi-Character) Scene Conditions

| Condition | Why it matters | Veo phrasing |
|---|---|---|
| Map each reference image to a role | Prevents Veo swapping who-is-who mid-generation | `Using the provided image for the detective and the provided image for the woman, create a medium shot of...` |
| Assign spatial position explicitly | Without this, blocking can drift or characters overlap oddly | `the man stands on the left, the woman stands on the right, facing each other` |
| Specify eye-line / eye contact | Keeps the interaction feeling connected within one shot | `both maintain eye contact throughout` |
| Sequence the dialogue, don't just list it | Prevents overlapping/garbled speech since there's no cut to separate turns | `Character A speaks first, pauses briefly, then Character B replies` |
| Unify lighting across both characters | Mismatched lighting from separate reference photos looks fake | State one lighting condition (Section 2.5) for the whole scene |
| Control reactions, not just lines | Otherwise Veo may invent unscripted gestures/expressions | `Character B listens silently, slight nod, no other movement` |
| Use OTS or two-shot framing | Implies "back and forth" without actually cutting between speakers | Pick **over-the-shoulder** or **two-shot** from Section 2.1 |
| Handle background extras separately | Extras can accidentally "talk" or draw focus if unspecified | `background extras blurred, out of focus, not speaking` |
| Wardrobe/prop consistency between characters | Mismatched style reads as two unrelated stock photos stitched together | Describe both characters' wardrobe in matching detail and era/style |

---

<a id="10-other-conditions"></a>
## 🧭 10. Other Conditions Worth Planning For

| Condition | Detail | Veo phrasing / note |
|---|---|---|
| Aspect ratio / format | Vertical (Reels/Shorts), horizontal (cinematic/YouTube), square | Set in the tool's format option, and reinforce: `vertical 9:16 framing` |
| Clip duration | 4s / 6s / 8s generations | Shorter duration = shorter dialogue line |
| Resolution | 720p vs 1080p | Doesn't change wording but affects detail fidelity |
| Setting reference image | Same "Ingredients" logic as faces | `Using the provided image of the location as the setting...` |
| Chaining clips for a "longer single-shot feel" | First-frame/last-frame or "extend" workflows stitch separate generations | Technically multiple generations connected at shared frames, not one true continuous take — don't call it "single shot" if precision matters |
| Identity drift across chained clips | Same risk as Section 8, multiplied — applies to voice/accent too, not just face | Repeat the same reference image + anchor words, and the same tone/accent tag (e.g. "Mumbai street accent"), in every chained prompt |
| Hindi-English code-switching | Very natural in real Indian speech (e.g. "yaar, ye thoda complicated hai") | Write the mixed line exactly as it would be spoken |
| Regional accent/dialect | Mumbai, Delhi, Bihari, Punjabi-inflected Hindi, etc. | `Dialogue (Hindi with a Mumbai street accent, casual tone)` |
| Brand names / logos / readable text | Often renders garbled or triggers unwanted text overlays | `no readable text or logos in the background` |
| Music rights / copyrighted songs | Don't reference real copyrighted songs by name | Describe the *style* instead of naming a track |

---

<a id="11-image-to-video"></a>
## 🎞️ 11. Image-to-Video & First-Frame-to-Last-Frame

### 11.1 Image-to-Video (animating a single still image)

| Condition | Why it matters | Veo phrasing |
|---|---|---|
| Don't contradict the image | The still already fixes subject, setting, lighting | Describe only what *changes*: motion, expression shift, camera move |
| State camera movement relative to the still | The image is literally your first frame | `Starting from this image, camera slowly pushes in...` |
| Dialogue rules still apply | If the person in the image should speak | Devanagari + colon + named speaker, as in Section 3 |
| Specify off-screen action if needed | Image has no information beyond its edges | `a second person enters from the left side of frame` |
| Audio must be specified | A still image carries no inherent sound | `Audio: [ambient sound], no music` |
| Single-shot rules still apply | Can still get "cut happy" with too much described motion | One camera movement only, `no cuts, no scene changes` |

**Template:**
```
Animate the provided image. [Camera movement] begins from this frame,
[subject] [continuous action]. [Speaker] says: "[Hindi dialogue]"
Dialogue (Hindi, [tone]). Audio: [ambient sound], no music.
No subtitles, no cuts, no scene changes.
```

### 11.2 First Frame to Last Frame (start image → end image transition)

| Condition | Why it matters | Veo phrasing |
|---|---|---|
| Both images should already match in lighting/identity/setting | Contradicting frames force Veo to invent a hidden "fix," often a disguised cut/morph | Use two images from the same shoot/style/character |
| Describe the *connecting* motion, not the destination | Veo already has the end image | `camera moves forward through the doorway` not a re-description of the room |
| Best suited to continuous physical paths | Walking forward, a reveal, a push-in, a turning head | Pick one motion type from Section 2.3 |
| Keep dialogue short and tied to the motion | Model is solving for visual path *and* audio simultaneously | A single short line delivered mid-motion |
| Useful for chaining longer sequences | End frame of clip 1 becomes start frame of clip 2 | Repeat identity anchor words across each chained prompt |

**Template:**
```
Create a cinematic transition that moves smoothly from the start frame
to the end frame. [Camera/subject motion connecting them], maintaining
consistent lighting and subject identity throughout. Motion resolves
naturally into the final frame without abrupt cuts.
[Optional short dialogue tied to the motion].
Audio: [ambient sound]. No subtitles, no on-screen text.
```

### 11.3 Which Input Mode to Use

| Workflow | Input | Best for | Key condition to remember |
|---|---|---|---|
| Text-to-video | Prompt only | Full creative control from scratch | Be exhaustive in subject/setting/lighting description (Sections 1–4) |
| Image-to-video | One still image + prompt | Bringing an existing photo/illustration to life | Describe only what changes |
| First frame → last frame | Two images + prompt | Smooth transitions, reveals, walkthroughs | Describe the connecting motion; keep both images visually consistent |
| Ingredients to video (Section 8) | Reference image(s) of character/object/setting + prompt | Keeping a character/object consistent across new scenes | Name the reference explicitly every time |

---

<a id="12-combined-example"></a>
## 🏆 12. Full Combined Example (Everything Together)

Two character reference images + spatial blocking + Hindi dialogue sequencing + single continuous OTS shot + identity-consistency negative prompts — all conditions from Sections 2, 3, 8, and 9 working together in one prompt.

```
Using the provided image for Character A (a young woman in a yellow saree)
and the provided image for Character B (an elderly man in a white kurta),
create a single continuous over-the-shoulder shot favoring Character A,
eye-level angle, slow dolly-in, shallow depth of field, no cuts, no edits.

Both characters stand facing each other on a sunlit terrace, golden hour
lighting, gentle breeze moving their clothes. Character A stands on the
left, Character B stands on the right; both maintain eye contact throughout.

Character A speaks first: "दादा जी, आपसे एक बात पूछनी थी।"
She pauses briefly, then Character B replies: "हाँ बेटा, पूछो।"
Dialogue (Hindi — Character A nervous and soft-spoken; Character B warm
and reassuring).

Audio: gentle wind, distant birds, no background music, no audience sounds.
Style: warm documentary realism, consistent facial features and clothing
throughout, no identity drift.
No subtitles, no captions, no on-screen text, no cuts, no scene changes.
```

---

<a id="13-negative-prompts"></a>
## 🚫 13. Negative Prompt Cheat Sheet

A consolidated list — pull whichever lines apply and append them to the end of any prompt in this doc.

| To avoid... | Add this phrase |
|---|---|
| Subtitles / captions | `no subtitles, no captions, no on-screen text` |
| Unwanted cuts or edits | `no cuts, no edits, no scene changes` |
| Face/wardrobe drift across a clip or chained clips | `consistent facial features and clothing throughout, no identity drift` |
| Random music when you want pure ambience | `no background music` |
| Unscripted crowd reactions | `no audience sounds, no unexpected laughter or applause` |
| Garbled text/logos in the background | `no readable text or logos in the background` |
| Wrong character speaking | Name the speaker explicitly before every line — not strictly a negative prompt, but solves the same problem |
| Overlapping dialogue between two characters | `dialogue does not overlap, one speaker at a time` |
| Background extras drawing focus | `background extras blurred, out of focus, not speaking` |

---

<a id="14-checklist"></a>
## ✅ 14. Quick Checklist Before Generating

- [ ] One shot type only (Section 2.1), stated up front
- [ ] One angle only (Section 2.2)
- [ ] One camera movement only (Section 2.3)
- [ ] "No cuts, no edits" stated near the beginning
- [ ] Lighting + atmosphere condition specified (Sections 2.5–2.6)
- [ ] Hindi dialogue in Devanagari, after a colon
- [ ] Speaker explicitly named
- [ ] Tone/delivery tag included
- [ ] Audio block filled in (ambient + exclusions)
- [ ] Negative prompts added from Section 13
- [ ] Dialogue kept short enough to fit clip length (8 sec max per generation)
- [ ] If using a face/object/setting reference image, it's explicitly named in the prompt (Section 8)
- [ ] If 2+ characters, each reference image is mapped to a role and positions are spatially defined (Section 9)
- [ ] Dialogue turns are sequenced (who speaks first, then who replies) rather than just listed
- [ ] Background extras' behavior is specified if present
- [ ] Aspect ratio and clip duration match the intended platform (Section 10)
- [ ] If animating a still image, the prompt describes only what *changes* (Section 11.1)
- [ ] If using first-frame/last-frame, both images are visually consistent and the prompt describes the connecting motion only (Section 11.2)

---

> 💡 **Tip:** keep a running log of which exact shot type + angle + movement + lighting combinations produced clean (no-subtitle, no-cut) results — Hindi-language generation is newer and less consistent than English, so small wording tweaks often make the difference between a clean take and a flawed one.
