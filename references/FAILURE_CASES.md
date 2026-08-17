# FAILURE CASES — Middle-balance gate

The Skill must reject both ends: portrait drift and generic-icon drift.

## A. Too portrait-like

Reject when:

- the exact gaze, worried/happy expression or facial coordinates survive;
- the owner would praise accurate resemblance before the series style;
- source-specific coat flow, muzzle construction, stance or weight distribution is reconstructed;
- realistic eyes, eyelids, catchlights, nostrils, fur or anatomy appear;
- the drawing reads as a pet commission, caricature portrait or observational likeness.

Repair by keeping only 2–4 Light-Likeness hints, neutralizing expression, using the series face and stance, and flattening coat into broad decorative blocks.

## B. Too generic or too childlike

Reject when:

- fewer than two source hints remain;
- every pet uses the same ears, face shape, coat, torso and proportions;
- the result is a puppy sticker, breed icon, preschool dog or nursery mascot;
- the dog could be swapped with another without changing any visible cue;
- thick lines become a smooth die-cut sticker border.

Repair by restoring exactly one high-value ear, coat, face, body or memorable cue. Do not add realism.

## C. Series inconsistency

Reject when:

- outline hierarchy, eye/nose language, body construction or accent grammar changes between pets;
- one card becomes a portrait while another becomes a flat icon;
- backgrounds become scenes or compositions become elaborate;
- decorations use unrelated icon packs, polished typography or copied slogans.

## D. Pose failures

Reject when:

- a running, lying, standing, curled, peeking or held pet is converted into the default sitting pose;
- a still source is made to run or jump without a user request;
- the broad body direction, lifted paw, tucked legs, curled tail or other defining gesture disappears;
- exact anatomical tracing makes the result portrait-like;
- extra legs, merged paws or impossible limb counts make the action unreadable.

Repair by restoring the source pose family and one defining gesture, then simplifying the joints and paws inside the series grammar.

## E. Decorative failures

Reject thin delicate outlines, uniform vector strokes, excessive accents, symmetrical icon borders, garbled text, polished lettering, logos, watermarks, signatures, copied slogans, frames and room mockups.

Also reject decoration when:

- the background is too close to the coat color and the silhouette disappears;
- “free color” becomes a gradient, photographic scene, floor, room or busy texture;
- every output repeats the same default background even when variation is wanted;
- waves, ticks and icons are unrelated stock filler rather than an echo of an ear, beard, fluff, marking, body or accessory cue;
- accents are evenly distributed like a border, exceed eight marks, obscure the dog or consume most negative space;
- mirrored decoration makes the card feel mechanically symmetrical.
- surrounding text is too sparse and leaves large accidental empty zones;
- text uses dark letters on a dark ground or pale letters on a pale ground;
- phrases overlap the pet, form a rigid text box or become more dominant than the dog;
- lettering looks typeset, commercially polished or calligraphic instead of casually handwritten;
- any word is misspelled, garbled, duplicated accidentally or copied from a reference slogan;
- too many icons compete with the text-rich layout.

Repair by selecting one contrasting flat paper color, switching text to the opposite value, arranging one headline plus 2–4 short side phrases, identifying one visible pet cue, and limiting remaining symbols to 2–5 marks.

## F. Wrong messiness level

Reject when the drawing is too clean: one confident contour, perfectly closed shapes, fully registered color and identical accent strokes.

Also reject when it is too chaotic: facial features obscured, silhouette broken into many fragments, uncontrolled scribble everywhere, accidental stains dominating the pet, or more than roughly 20% disorder.

The pass zone is localized repair and misregistration: 5–8 contour corrections, 2–4 gaps/overshoots and 3–6 imperfect color areas.

## Complete hard negative list

```text
photorealistic, photo filter, realistic fur, detailed fur, strand-by-strand hair,
pet portrait, specific pet likeness, observational portrait, exact facial resemblance,
individual portrait rendering, accurate gaze, realistic expression,
invented pose, default sitting pose replacing source action, unreadable action silhouette,
professional pet commission, polished storybook illustration, editorial character art,
realistic iris, eye socket, eyelid modeling, catchlight, wet eyes, nose shine,
perfect anatomy, weight distribution study, realistic stance, detailed muzzle structure,
digital painting, smooth shading, gradient, cast shadow, 3D volume, cinematic lighting,
clean vector, delicate line art, thin contour, uniform stroke, smooth sticker border,
perfectly closed contour, perfectly registered color, pristine digital fill,
kindergarten drawing, toddler crayon drawing, preschool cartoon, nursery mascot,
chaotic scribble, fully broken silhouette, excessive stray lines, dirty accidental stains,
ultra-simple dog icon, generic puppy sticker, generic breed cartoon,
universal identical dog template, interchangeable pet, empty low-information face,
excessive decorations, unrelated stock accents, more than five graphic marks when text is present,
symmetrical icon border, low-contrast coat and background, gradient background,
photographic background, room scene, polished typography, low-contrast text,
sparse accidental text layout, garbled or misspelled text, copied reference slogan,
signature, watermark, logo, copied slogan, physical frame, room mockup
```

## Retry ceiling

- Attempt 1: normal series translation.
- Attempt 2: remove portrait evidence or restore one missing hint.
- Attempt 3: rebuild from the fixed Series Blueprint plus a new 2–4-hint card.

After attempt 3, report `portrait drift remains`, `generic drift remains`, `series inconsistency remains`, or a combination.

## Final reaction gate

- “这只狗画得真像。” → **FAIL: too portrait-like**
- “就是一只通用卡通狗。” → **FAIL: too generic**
- “同系列里的一只，能看出参考了它，但不是肖像。” → **PASS**
- “姿势跟照片是同一种，但画法被简化了。” → **POSE PASS**
