---
name: cozy-flat-illustration
description: Transform a user-supplied photo into a finished warm, densely populated, hand-painted scene illustration — the storybook / jigsaw-puzzle look: soft digital gouache, cheerful color, fine scattered texture, tiny figures, and lots of small things to find. Generate the image directly, with an optional postage-stamp perforated border. Use when the user uploads or points to a photo and asks for illustration style, storybook style, puzzle-style art, painted illustration, a postal-stamp treatment, or asks to turn a photo into an illustration.
---

# Cozy Illustrated Scene — Image Generator

## What this skill does

Read the photo → analyse it → **generate the finished illustration directly with the image-generation tool**.
Do not make the user copy a prompt into another image app unless they explicitly ask for a prompt-only
version. Include the uploaded photo as the image reference and preserve its essential subject and
composition.

Default to the finished **postage-stamp presentation**: a hand-painted illustration inside a warm ivory
perforated edge. The frame should feel designed as part of the artwork, not pasted on as a generic sticker.
Use a different edge color only when the user specifies one; do not default every landscape to green.
Use the included local framing tool only when the user requests pixel-perfect, repeatable framing across a
batch, or when image generation renders the edge poorly.

Write the short explanation in whatever language the user is writing in. Build the generation instruction in
English internally; only show it when the user asks to see or reuse the prompt.

## The target style

This is **hand-painted scene illustration**, not flat vector art. Six defining traits:

1. **Digital gouache** — visible brush texture, slightly soft edges, a real painted feel. **Not** crisp flat vector shapes.
2. **Fine painted texture is where the quality lives** — drifting snow flecks, thousands of small leaf dabs,
   scattered stars. This dense small-mark texture is the foundation of the style, not a flaw to remove.
3. **Cheerful color** — either soft pastels (dusty lilac, powder blue, mint) or warm saturated tones
   (marigold, coral, teal, magenta). **Never a greyed-out muted vintage palette.**
4. **Flattened perspective from a slightly elevated viewpoint** — every element legible, nothing lost to blur.
5. **Figures are tiny and numerous** — around 1/20 of the frame height, simple painted shapes with
   no facial features, dozens of them scattered through the scene.
6. **Small things to find everywhere** — birds, squirrels, dogs, pumpkins, wreaths, taxis, bicycles.
   This is the puzzle logic: the picture rewards looking.

Two more: **delicate dark linework** (bare branches, iron railings, lamp posts) is a signature element,
and **soft glows are allowed** (moonlight, lamps, warm windows).

**Never name a brand, company or living illustrator in the prompt. Describe visual traits instead.**

## Reference images beat description

Words hit a low ceiling when describing a visual style. **Every time, remind the user to upload two or
three reference illustrations alongside the photo.** One reference image is worth two hundred adjectives.
If they have none, suggest saving a few finished pieces they like.

## Photo selection (say this proactively)

This style paints **scenes**, not people.

- **Best fit**: busy streets, parks, shopfronts, holiday scenes, visitor centres, cluttered interiors —
  small figures, dense content, slightly elevated viewpoint.
- **Poor fit**: single half-body portraits, head-and-shoulders close-ups, empty seascapes and skies.
  No amount of prompt tuning makes these look like the reference style.
- When the user brings a poor-fit photo, **say so plainly** and offer two choices: pull the framing back
  and invent an environment around the subject, or pick a different photo.

## Steps

### 1. Look at the photo
Actually read the image; never infer content from a filename. If the photo lives in a connected folder on
the user's machine, stage it into the workspace first. Handle multiple photos one at a time.

### 2. Analysis checklist (internal)
- **Does this photo fit the style?** (see above)
- **Subject and composition**; **3–6 identifying elements to keep**; **what to discard**
- **Dominant colors** → map to a cheerful palette, not a muted one
- **What small things could be added** — birds, cats and dogs, bicycles, lamp posts, planters, boats
- **Which all-over texture layer** — snow flecks / falling leaves / stars / petals / rain. Pick one.
- **What makes this photo good?** If the answer is backlight, silhouette or strong tonal contrast,
  use the light-and-shade rule below.

### 3. Subject modules

**City / street / architecture** (the best fit)
Frontal or slightly elevated viewpoint, buildings side by side; windows as warm yellow squares; add street
trees, lamp posts, awnings, steps, wreaths, planters, bicycles, taxis, dozens of tiny figures, cats, dogs,
birds. Do not worry about it being too full. Night scenes: deep navy ground, warm yellow windows, stars.

**Interiors / still life / clutter**
Objects arranged in rows, each one complete; give every object a readable pattern. Vehicle interiors
(ferry cabins, train carriages, terminals) follow the same logic: ceilings as repeating slats, window frames
as a geometric rhythm, seats as repeating rounded shapes.

**Landscape / flowers / pets**
Build foliage volume from masses of small leaf dabs — this is exactly where the style lives. Canopies in two
or three layered greens; branches as fine dark lines; mountains as layered shapes with snow as clean bright
forms; pet eyes as solid dots.

**Portraits** — see below.

---

## Texture and brushwork (core — do not get this backwards)

This style **needs** fine painted texture. But it must read as **organic**, never mechanical:

- **Never write** `even` / `regular rows` / `uniform` / `evenly spaced` when describing texture — that
  produces wallpaper or fish scales. Write "uneven density, varying sizes, hand-drawn rhythm".
- **For organic forms (flower plumes, clouds, canopies, waves), define the overall silhouette first,
  then describe the interior texture.** Describing only the filling always fails — "built from small dots"
  alone yields a pile of bubble-tea pearls.
- An object's **volume** comes from massed small marks; its **structure** comes from large shapes and lines.
- The all-over unifying texture layer (snow, leaves, stars) can be applied generously. It is a signature.

## Water

Water is the surface most likely to turn into noise. The variables to control are **stroke length and
contrast**, not quantity:

- short + dense + high contrast = television static
- **long + sparse + low contrast = water**

Recipe: a few broad flat bands as a base → large irregular patches of slightly darker and lighter blue
(wind-riffled areas; these carry most of the surface) → a small number of long horizontal strokes in a blue
only marginally lighter than what they sit on.

If the photo has sun sparkle, explicitly instruct `remove the sun sparkle entirely`.

## Filling empty areas: three mechanisms

When a large monotonous region (sky, water, snowfield, wall) reads as empty, add in this order:

1. **Areas** — large irregular patches of related darker and lighter tone. Covers ground without creating noise.
2. **Objects** — small boats, gulls, walkers, birds, lamp posts. Few, small, well separated. The safest option.
3. **Lines** — long strokes, branches, railings, rooflines. These supply rhythm.

Also: **varying a silhouette** (staggered treetop heights, a jagged ridgeline) is the highest-value addition
of all. **Never fill emptiness by adding more small texture** — that is what produces the wallpaper effect.

## Light and shade

Backlit silhouettes, dark interiors against bright windows, lit windows at night — the appeal of these photos
*is* the tonal contrast, and if you do not say so the model flattens everything to a mid tone.

Separate two things: **value contrast** (dark shapes against light shapes) is a **color choice** and must be
kept; **realistic cast shadows and lens flare** must go. But remember: **soft painted glows around lamps,
windows and the moon belong in this style** — do not ban them wholesale.

> Build the image on a deliberate value contrast made with color, not with photographic lighting:
> [dark content] in deep rich tones, and [bright content] in bright luminous tones. Soft painted glows
> around lamps and windows are welcome, but no harsh cast shadows, no lens flare, no photographic gradients.

Hard-edged shadows in bright sun (railing shadows striping a deck) can be kept, but written as a **flat
graphic element**: one solid darker tone, crisp contours, no gradient.

---

## Figures

### First choice: make them small
In this style people are 1/20 to 1/10 of the frame height — a colored shape with simplified limbs and
**no facial features at all**. Use this option only when the person is genuinely distant or facing away;
never use a featureless face on a visible medium or large figure.
`Populate the scene with many tiny figures, each a simple painted shape with no facial features at all.`

### Risk ordering
tiny figures < back view / silhouette < full profile < eyes closed, or hidden by a hat brim or sunglasses
< three-quarter view < facing the viewer.

When a user is repeatedly unhappy with a face, move left along this list. Sunglasses, hats and eyeglasses
are gifts: they anchor identity *and* cover the hardest feature to draw.

### When a large face is unavoidable, spell out every item
- **Rendering consistency** (most important):
  `Render the face with exactly the same painted texture as the rest of the image — the face must not be
  smoother or more three-dimensional than the background.`
  The number one cause of an uncanny face is the model rendering the face volumetrically while the rest of
  the picture stays painterly and flat.
- **Eyes**: almond shapes, one slightly thicker dark-brown arc along the upper lid as a lash line, iris in
  deep brown rather than pure black, small, no white highlight dot.
- **Closed eyes**: two downward arcs plus a lash line plus two or three short lashes at the outer corner.
  Two bare lines look dead.
- **Sunglasses**: one solid clean dark shape, no eyes drawn behind them, no lens reflections.
- **Brows**: thin soft arcs close to the hair color. **Nose**: one small stroke or omitted entirely.
  **Mouth**: one small closed stroke in muted rose; never an open mouth, never teeth.
- **Proportions**: features small and set slightly low, with a full forehead above. Soft face shape, no
  pointed chin.
- **Do not chase likeness**: identity comes from hair silhouette, clothing color and cut, posture, and
  carried objects.

### Clothing texture
Sherpa fleece, quilted down, knitwear: suggest them with **silhouette variation** and **a few lines**
(a scalloped edge, a few quilting seams). Never fill the interior with fuzzy texture.

### Figure negatives (always add when a face is visible)
`no uncanny or unsettling face, no realistic skin shading or airbrushed rendering on the face, no large
glossy anime eyes, no pure-black eyes without a lash line, no heavy eyeliner, no asymmetric or misaligned
eyes, no sharp pointed chin, no teeth.`
When every figure is tiny or seen from behind, use instead: `no facial features on any figure, no uncanny face.`

---

## Text and signage

Image models garble text nine times out of ten. Write signs as color blocks, geometric shapes and abstract
letterforms, and add `no readable words anywhere in the image`.

Tell the user: if those particular words matter, overlay them afterwards in Canva, Keynote or Photoshop.
A very short word (five or six letters) is worth a gamble, but flag the risk first.

---

## Direct image-generation workflow

1. Actually inspect the supplied photo. Use it as the reference image in the image-generation call.
2. Build one English generation instruction using the structure below, then generate the image directly.
3. Include this framing clause by default:

   > Finish the artwork as a charming vintage postage stamp: a clean, even warm ivory or parchment border
   > about 4% of the
   > short edge, with small rounded perforation bites along all four outer edges. Keep the scallops evenly
   > spaced and aligned, retain the original aspect ratio, and keep important subjects safely inside the
   > frame. If the user specifies a border color, use that exact color instead. No text, denomination, logo,
   > watermark, signature, or unrelated decorative objects in the border.

4. Keep the border only when it supports the request. If the user explicitly asks for an unframed image,
   omit the clause. If a precise matching frame matters more than the generated frame, generate the artwork
   without a frame and use `tools/stamp-frame.html` afterwards.
5. When a source photo includes a person, default to a small, simplified painted figure whose face is not a
   focal point. Preserve clothing, pose, hair silhouette and placement; let the landscape carry the detail.
   If the face is visible, render a complete, kind, stylized face with small aligned eyes, soft brows, a
   subtle nose stroke and a closed mouth, all in the same painted texture as the scene. Never leave a visible
   face blank or featureless. Use no facial features only for a genuinely tiny distant figure or a back view.
   Render a large, detailed face only when the user explicitly asks for a portrait.
6. Return the generated image, one short sentence about the treatment, and three concise tuning options.
   Do not output the long prompt by default.

## Assembling the generation instruction

Write it as **one continuous natural-language paragraph**, medium length (roughly 250–400 words).
**Over-specifying backfires** — the denser the constraints, the more mechanically the model follows each
clause. That is exactly what produces wallpaper water and bubble-tea flowers.

1. Instruction: `Redraw this photograph as a hand-painted storybook illustration in soft digital gouache — the warm, densely detailed look of an illustrated jigsaw puzzle.`
2. **Keep list**: name the identifying elements specifically.
3. **Remove list**: blur, grain, flare, sun sparkle.
4. **Add list** (specific to this style — do not skip it): tiny figures, birds, pets, lamp posts, boats, planters.
5. **Light-and-shade paragraph** if applicable, placed before the subject rules.
6. **Subject module rules**; add the facial spec if there is a large face.
7. **Text handling** if the scene contains signage.
8. **Style lock block** (reuse verbatim; swap only the palette and the texture layer):

> Painted in soft digital gouache with visible brush texture and slightly soft edges — hand-painted, never
> crisp vector shapes. Flattened perspective from a slightly elevated viewpoint; every element clearly
> legible, nothing lost to blur or depth of field. Cheerful color: [4–8 color names]. A fine scattering of
> [snow flecks / falling leaves / stars / petals] drifts across the whole image as a unifying layer.
> Delicate dark linework for branches, railings, lamp posts and wires. Soft warm glows around lamps,
> windows and lights are welcome. Densely populated with many tiny figures and small objects — each a simple
> painted shape with no facial features — so the eye can wander and keep finding things. Composition fills
> the frame edge to edge, no vignette, no readable text. Add the postage-stamp framing clause above unless
> the user asks for an unframed image or a separately applied precise frame.

9. **Negatives**: `Avoid: photorealism, 3D render, CGI, lens blur, bokeh, depth of field, HDR, glossy highlights, harsh photographic shadows, flat vector or clip-art look, muted desaturated grey palette, watermarks, signatures, readable text.` Append the figure negatives when a face is visible.
10. **Aspect ratio**: follow the source photo by default, to protect the original composition.

---

## Finished framing: postage stamp

The chosen presentation format. Use direct image generation by default; use the local tool only for the
precise fallback. Four hard rules:

1. **For a direct frame, request rounded postal perforations, not triangular saw teeth.** Ask for an even,
   aligned warm ivory or parchment edge with no text by default. Use another color only when the user asks
   for it. If the edge is visibly skewed, uneven or distracting,
   regenerate once without it and use the local tool.
2. **Output dimensions must match the source ratio** — the stamp fills the entire canvas, the perforations
   bite into the outermost edge, and the inner artwork is cropped to fit. Users pair the framed version with
   the original side by side, so the ratio has to match.
3. **Default to warm ivory or parchment**, not black or dark green. Use a stated color exactly; gentle
   choices such as dusty blue, pale pink, butter yellow, or lavender are welcome when requested.
4. **Proportions**: margins about 4% of the short edge on all sides; the caption band at the bottom about
   twice the margin. Deeper at the bottom than the top is what makes it read as designed rather than default.

**Caption format** (all three short, never sentences):
- bottom left, large: place name, serif, generous letter-spacing (`PUGET SOUND`)
- below it, small: region and year (`WASHINGTON · 2025`)
- bottom right: a denomination number

`tools/stamp-frame.html` is the exact-frame fallback. Open it in a browser, choose the finished illustration,
optionally enter the three caption fields, and download the transparent PNG. It keeps the source canvas
dimensions and uses small round perforations (postal-stamp teeth), rather than harsh triangular zigzags.

**A consistent format across the whole batch matters more than any single frame.** The same frame on
fifteen images makes them a body of work; without it they are fifteen loose pictures.

---

## Output format

1. Generate and return the finished image.
2. One sentence on what you read in the photo, whether it suits this style, and whether the stamp frame was
   applied directly or should be added with the precise local tool.
3. A short explanation **in the user's language**, covering only what is **new or unusual about this
   particular image**. Do not restate the fixed skeleton every time.
4. A reminder to upload reference images alongside the photo when useful.
5. Three tuning suggestions, each a sentence for the next generation. When a face is visible, one of
   them is always the face escape hatch (pull back, turn to profile, or go to silhouette).
6. Only when the user asks for a prompt-only result, return the English generation instruction in a code
   block instead of generating an image.

## Fidelity

Default to the middle: composition and subject faithful, details decorative, small content added in
moderation. If the user asks for "closer to the photo" or "take liberties", swap only those two sentences —
never touch the style lock block.

## Hard rules

- The style lock block and the negatives appear in full every time.
- **Never name a brand, company or living illustrator.** Describe visual traits.
- **Do not drift toward flat vector, muted, or minimal.** This is the most common failure. The style is
  hand-painted, cheerful and dense.
- Generate the illustration directly by default; only provide a copy-paste prompt when the user asks for one.
- Use the postage-stamp framing clause by default, unless the user asks for no frame or needs the precise
  local framing fallback.
- Keep the prompt medium length. Do not pile on dozens of clauses.
- Give one good version plus tuning notes, not several versions to choose between.

## Verification

- [ ] Actually read the image; every element in the keep list exists in the photo
- [ ] Prompt contains: painted gouache texture, visible brushwork, cheerful color, all-over texture layer,
      tiny figures and small objects, delicate dark linework
- [ ] Prompt does **not** contain: flat vector / muted / desaturated / crisp flat shapes
- [ ] No `even` / `regular` / `uniform` in any texture description
- [ ] Large face present → rendering-consistency line, full facial spec (or "no facial features"), and
      figure negatives are all included
- [ ] Signage present → written as abstract letterforms, with the overlay-afterwards tip given
- [ ] Direct image generated using the supplied photo as the reference image
- [ ] Framing requested → prompt has rounded, aligned postage-stamp perforations and source aspect ratio
- [ ] Precise frame requested → used or directed the user to the local framing fallback
- [ ] Reminded the user to upload reference images
- [ ] Said so plainly if the photo is a poor fit for this style
