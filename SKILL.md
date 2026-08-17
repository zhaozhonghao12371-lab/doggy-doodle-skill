---
name: doggy-doodle
description: "Turn a user-supplied pet photo into a unified decorative pet-series doodle with light likeness and controlled messiness while preserving the photo's broad pose or action family—sitting, standing, lying, running, jumping, curled, peeking or another visible gesture. Supports text-rich, no-text and paired outputs with bold repaired outlines, simple round eyes, graphic noses, imperfect handmade color, pet-responsive accents and contrast-aware handwritten English. Use for $doggy-doodle, 狗狗乱画, 宠物丑萌涂鸦, 系列宠物插画, 宠物装饰画, stylized pet doodle, decorative pet illustration, or lightly recognizable pet art that is neither a portrait nor a generic puppy icon."
---

# 宠物丑萌涂鸦 · Doggy Doodle

> **Keep some pet-specific hints, but let the series style dominate.**
> **The result should feel like a unified decorative pet series, not a portrait and not a generic cartoon icon.**

Create a stylized pet doodle with light likeness. Target roughly **45%–60% resemblance**: the source is noticeable, but the result is decorative series art rather than a pet portrait.

## Required references

- Read [references/STYLE_GUIDE.md](references/STYLE_GUIDE.md) before every generation.
- Read [references/GOOD_EXAMPLES.md](references/GOOD_EXAMPLES.md) when selecting hints.
- Read [references/FAILURE_CASES.md](references/FAILURE_CASES.md) before evaluation or retry.

## Workflow

1. Inspect each supplied photo with `view_image`. Use it as a source of limited visual hints, not as an edit target unless requested.
2. If an iPhone `.JPG` is rejected as MPO, convert a temporary PNG with `sips`; never alter the original.
3. Lock the **Series Blueprint** and a **Pose Card** before reading fine pet detail:
   - classify the source as sitting, standing, lying, running/leaping, curled/sleeping, peeking/close-up or another clear pose family;
   - preserve that broad pose, body direction and one defining gesture; never force a default sitting pose;
   - square card; pet about 52%–70% depending on pose and lettering space;
   - blunt black outer contour 2–3 times heavier than interior marks;
   - simple small-to-medium round/dot eyes, large graphic nose, minimal mouth;
   - slightly oversized head, fluffy block body, chunky front paws, anatomy suppressed;
   - one flat paper-color background selected for coat contrast, surrounding hand lettering and 2–5 rough accent marks;
   - scrappy marker/crayon fill with no lighting or volume.
4. Build a **Light-Likeness Card** and retain only 2–4 appearance hints. The Pose Card is structural and does not consume an appearance-hint slot:
   - coat color or major marking family;
   - ear family: upright, folded, hanging, buried or mismatched;
   - broad face tendency: round, long, square or tapered;
   - fluff level or broad body tendency: long/short, round/slim;
   - at most one memorable cue such as beard, brows, blaze or one uneven ear.
5. Discard portrait evidence: exact gaze, precise facial coordinates, real expression layers, detailed coat flow, exact joint geometry, weight distribution and minor markings. Keep the broad pose family and gesture silhouette.
6. Translate the Pose Card and selected appearance hints into the Series Blueprint. Series features should account for about 60%–70% of visual decisions; source pose plus pet hints about 30%–40%.
7. Select the output mode:
   - **Text-rich:** use the lettering plan below and 2–5 graphic marks.
   - **No-text:** omit all letters and use 4–8 pet-responsive graphic marks.
   - **Paired:** generate the no-text pose master first, then derive a text-rich version that preserves the same dog, action, palette and line language.
8. Select the background, lettering and accents:
   - honor a user-requested color; otherwise choose one flat paper color from the rotating palette for clear coat contrast;
   - vary background hues across a set instead of repeating one default color;
   - place one large headline, 2–4 short side phrases and optionally one small footer around the pet;
   - use exact user copy when supplied; otherwise select 3–5 short phrases totaling 12–22 words;
   - use light lettering on dark backgrounds and dark lettering on light backgrounds;
   - derive 2–5 remaining accent marks from one visible pet cue; lettering replaces most icons.
9. Apply the **Controlled Messiness Budget**: add about 15%–20% disorder through 5–8 local contour repairs, 2–4 small open gaps/overshoots and 3–6 uneven or slightly misregistered color areas. Keep the face readable and the action silhouette coherent.
10. Compile the prompt below and call the built-in image-generation tool. Do not substitute vector or code drawing.
11. Run the **Middle-Balance Gate**. Allow at most three attempts:
   - Attempt 1: normal series translation.
   - Attempt 2: if too portrait-like, remove exact facial/posture evidence; if too generic, restore one selected hint.
   - Attempt 3: rebuild from the Series Blueprint and a fresh 2–4-hint card.
12. Save outputs outside the Skill directory. Bundle only publication-safe examples, never a user's source photo without permission.

## Series Blueprint

Keep these stable across pets:

- bold, blunt, uneven outer outline; thinner sparse inner marks;
- simple irregular round/dot eyes without realistic gaze or eye anatomy;
- large flat oval/rounded-triangle nose and nearly absent mouth;
- slightly oversized head, simplified fluffy masses and chunky paws arranged to match the source pose family;
- paper-visible marker/crayon color, flat background and no scene;
- informal square composition, unequal margins and dense-but-readable handwritten English around the pet;
- rotating high-contrast background colors and pet-responsive line motifs without changing the series drawing system.

Vary only coat palette, ear family, face tendency, fluff/body tendency and one memorable hint. Never preserve every source relationship.

## Prompt compiler

```text
Use case: stylized pet doodle with light likeness

Goal:
A unified decorative pet-series illustration with selective resemblance.
Series style dominates; retain only enough source information to suggest the pet.
Target resemblance: 45%–60%. Not a portrait and not a generic cartoon icon.

Series Blueprint — keep fixed:
square card; pet occupies 52%–70%; preserve source pose family, body direction and one defining gesture;
bold blunt black outer contour 2–3x interior line weight;
simple irregular round/dot eyes; large graphic nose; minimal mouth;
slightly oversized head; fluffy block body; chunky front paws; no realistic anatomy;
scrappy marker/crayon fill; one flat paper-color background selected for coat contrast;
handwritten English fills the surrounding negative space; only 2–5 rough graphic accents remain.

Light-Likeness Card — keep only 2–4:
1. coat color/major marking family: <hint>
2. ear family: <hint>
3. face or body tendency: <hint>
4. optional memorable cue: <one hint only>

Deliberately discard:
exact gaze, precise eye/nose coordinates, complex expression, exact coat flow,
minor markings, realistic stance, weight distribution and source-photo perspective.

Face:
simple small-to-medium irregular black round/dot eyes with mild size/spacing variation;
large flat graphic nose; mouth reduced to a tiny line or omitted;
no realistic emotion, iris, catchlight, eyelid or facial modeling.

Body:
one or two simplified fluffy masses arranged in the source pose family;
preserve sitting, standing, lying, running/leaping, curled, peeking or another visible broad gesture;
preserve only one defining action cue such as lifted paw, stretched body, tucked legs, turned head or curled tail;
use broad uneven paws and decorative proportions; no exact anatomy, weight or perspective study;
never replace a non-sitting source with the standard seated body.

Controlled messiness — target only 15%–20% more disorder:
5–8 local doubled/restarted contour sections;
2–4 small open joins or overshoots;
3–6 areas of uneven, skipped or slightly out-of-register color;
a few stray short construction marks near fur edges;
keep the eyes, nose, silhouette and accents clearly readable;
messy adult marker handling, never chaotic toddler scribble.

Background color selection:
if the user names a color, use it unless the pet would disappear into it;
otherwise choose freely from cobalt blue, turquoise, mint, coral pink, butter yellow,
warm cream, dusty lilac or pale sky blue, favoring clear contrast with the coat;
white/cream pets favor saturated cool or coral grounds;
apricot/tan pets favor cobalt, turquoise, mint or dusty lilac;
dark pets favor butter yellow, warm cream, mint, dusty pink or pale sky blue;
multicolor pets use a hue not dominant in the coat;
one flat color only, with light paper grain—no gradient, scenery or photographic floor.

Contrast-aware lettering:
use light cream, paper white or butter yellow lettering on dark backgrounds;
use charcoal black, deep navy or dark desaturated blue lettering on light backgrounds;
for medium-value backgrounds, choose whichever direction gives the strongest immediate contrast;
allow one muted accent color, but every phrase must remain legible at thumbnail size.

Text-rich layout:
use exact user-supplied wording when available;
otherwise choose 3–5 phrases totaling 12–22 words from this safe vocabulary:
HAPPY, GOOD DOGGY, ONLY YOU, SO FLUFFY, LOVE YOU, CUTEST,
WITH YOU I'M NOT AFRAID, YOU ARE MY LITTLE HAPPINESS, MY BEST GIFT;
place one large 1–2 word headline across the upper-left or top edge;
stack 1–2 short phrases down each side in uneven handwritten lines;
optionally add one small footer phrase along the bottom;
vary scale, baseline and tilt; keep letters rough, marker-drawn and clearly spelled;
fill roughly 25%–40% of the background with lettering while keeping a clear gutter around the pet;
never overlap the eyes, nose, mouth or main silhouette;
if any phrase is misspelled or garbled, retry once with fewer and shorter phrases.

Pet-responsive decoration plan:
derive the primary marks from one visible cue:
floppy/folded ears -> loose curved ripples beside the ears;
upright ears -> short radiating ticks above or beside the ears;
beard/long muzzle -> broken waves or zigzags near the cheeks;
round fluffy coat -> soft cloud loops or scalloped strokes;
long/low body -> elongated horizontal swashes;
spots/patches -> a small cluster of irregular dots or broken blobs;
mismatched ears -> intentionally different marks on the two sides;
bandana/collar -> 2–3 rough diagonal ticks or tiny triangle echoes;
curled tail -> one loose spiral or wave.
Add at most one secondary family such as a heart, speech bubble or star.
When lettering is present, keep graphic accents to 2–5 marks total, asymmetrically placed around—not over—the pet.

Accents:
one pet-derived main family plus at most one secondary motif, 2–5 marks total;
same rough marker language and series logic, irregular placement, no icon border;
lettering is the main decorative layer; symbols only fill small remaining gaps.

Success:
“same decorative series, lightly based on this pet, balanced between portrait and generic icon”

Avoid:
<complete hard negative list>
```

## Middle-Balance Gate

Pass only when all are true:

1. **Series consistency:** would it sit naturally beside other pets using the same outline, face, body, background and accent grammar?
2. **Light pet hints:** are 2–4 chosen cues visible without reconstructing the exact face?
3. **Not too portrait-like:** are exact gaze, facial geometry, coat flow and stance absent?
4. **Not too generic:** does coat/ear/face/body variation distinguish it from the series base?
5. **Balance:** does it read as decorative series art first and this pet second?
6. **Controlled messiness:** does it feel casually repaired and hand-colored without becoming noisy or careless?
7. **Background contrast:** is the freely selected color distinct from the coat while remaining a flat paper ground?
8. **Pet-responsive decoration:** does at least one accent family echo a visible pet cue without forming a border or crowding the dog?
9. **Text coverage:** does handwritten English occupy the top, sides and optional footer without obscuring the pet?
10. **Text contrast and accuracy:** is every phrase correctly spelled and clearly lighter than a dark background or darker than a light background?
11. **Pose fidelity:** does the broad pose, body direction and defining gesture match the source without reconstructing exact anatomy?

If the first reaction is “画得真像”, reduce likeness. If it is merely “一只卡通狗”, restore one high-value hint.

## Retry rules

### Too portrait-like

- replace eyes with small flat dots/beans and neutralize the real expression;
- regularize face placement toward the series grammar;
- simplify coat into broad blocks and remove location-specific hair flow;
- replace the exact pose with the standard series stance;
- keep only the 2–4 selected hints.

### Too generic

- restore exactly one missing high-value hint: ear family, major coat block, face tendency, body tendency or memorable beard/blaze;
- vary one proportion mildly within the series grammar;
- never repair genericness with realistic eyes, exact anatomy or detailed fur.

### Wrong pose

- restore the source pose family and one defining gesture before restoring facial detail;
- simplify joints and paws, but keep the action silhouette readable;
- do not turn running, lying, standing, curled, peeking or held pets into sitters;
- do not invent running or jumping when the source is still.

## Output

Return the image and this concise Chinese test card:

- **系列感是否统一？** YES / NO
- **是否保留一点宠物特征？** YES / NO — list 2–4 hints
- **是否太像真实宠物？** YES / NO
- **是否太像通用卡通狗？** YES / NO
- **是否达到中间版平衡？** YES / NO

Only `YES / YES / NO / NO / YES` passes. Report generation mode, final prompt and saved path. Never claim physical hand-painting.
