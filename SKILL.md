---
name: cozy-flat-illustration
description: "Transform a user-supplied photo into a direct, finished comforting editorial illustration through abstract visual extraction and playful recomposition—not a one-to-one painted translation. Use bright flat shapes, graphic figures with kind faces, a few scene-specific discoveries, and a default warm-ivory perforated postage-stamp edge when the user asks for cozy, whimsical, healing, storybook, puzzle-like, illustrated-travel, or hand-painted scenes."
---

# Cozy Illustrated Scene

Turn the supplied photo into a finished image with the image-generation tool. Do not make the user copy a
prompt into another app unless they explicitly ask for a prompt-only version. Treat the photo as a bag of story
ingredients, not a blueprint: extract its mood, visual symbols and spatial rhythm, then **recompose them into
an illustration rather than translating each pixel, object or person**.

Do not name artists, studios, brands or companies in a generation prompt. Describe the visual traits instead.

## Visual target

Make a bright, comforting, graphic editorial illustration. It should feel like a charming painted paper or
travel keepsake: bold simple shapes at first glance, a handful of thoughtful discoveries on a second look.

- **Abstract first.** Recompose the scene as 3–5 broad color areas and a few memorable silhouettes. Move,
  enlarge, crop, combine or remove source elements whenever that makes a clearer, more pleasing picture. Do not
  preserve the camera framing by default.
- **Flat picture-making, not painterly rendering.** Use mostly opaque, clean, matte gouache-like color fields
  with a very light paper grain. Use only one or two simple shadow shapes per large object. Do not model volume
  with brushstrokes, realistic light, visible paint buildup, dense speckles or intricate material texture.
- **Color.** Choose a small, fresh palette of 4–7 harmonized colors plus warm white: powder blue, soft coral,
  tomato red, leaf green, buttery yellow, ultramarine and peach. Let cream or sky-blue areas breathe. Avoid
  muddy browns, greyed-out realism and a universal sepia cast.
- **Linework.** Use sparse dark-navy, charcoal or deep-green drawn lines only where they clarify a silhouette,
  window, branch, railing, wave or clothing fold. Let most forms be defined by color blocks, not outlines.
- **Figures.** Turn people into warm graphic characters with simplified bodies and clear clothing shapes. A
  visible face gets two small aligned eyes, soft brows, a nose mark and a small closed mouth. Never leave a
  visible face blank, mask-like, hyper-detailed or photorealistic. Convert background crowds into a few small
  color-and-shape groups rather than individual portraits.
- **Quiet surfaces.** Turn a forest into layered pine shapes and a few leaf dabs; water into broad bands and a
  few long marks; buildings into stacked façades and awnings. Do not reproduce every shadow, reflection, rock,
  crease, tree branch or photographic texture.

## Abstract extraction, not one-to-one translation

Before composing, name only these four things:

1. **Story:** the emotional moment, such as a slow ferry ride, a mountain outing or a roadside stop.
2. **Anchors:** 3–5 motifs worth recognizing, such as the red truck, ferry window, stone stairs, hiker or tree
   line.
3. **Picture idea:** one deliberate visual move that the photo does not need to supply—an oversized window, a
   winding path, a broad sky, a patterned stone wall, a simplified close-up object or a gentler viewpoint.
4. **Omissions:** remove at least half of the remaining literal detail. A good empty area is better than a
   faithful copy of clutter.

Use the story and anchors, then invent the picture. Preserve recognizability, not photographic accuracy. For
example, turn a crowd into three walking color groups, turn engraved text into nonverbal motifs, and turn many
trees into overlapping dark-and-light green shapes.

## Add meaningful small discoveries

After preserving the story and 3–5 anchors, add **3–7 small, context-appropriate details**. Spread them with
restraint; open sky, water, walls or ground should remain quiet. Each addition must enrich the story, never
look like random filler.

| Source scene | Good additions |
| --- | --- |
| Mountain, forest, meadow | wildflowers, birds, marmots or squirrels, hikers, a trail marker, tiny backpacks, butterflies, a dog |
| Water, ferry, harbour | gulls, sailboats, a ferry, buoy, folded map, thermos, binoculars, small shoreline houses |
| Street, market, town | striped awnings, flower boxes, bicycles, fruit crates, dogs, planters, tiny passers-by, cafe chairs |
| Interior, train, ferry cabin | a book, tote bag, cup, luggage, potted plant, small reflection, a distant boat or shoreline detail |
| Winter or night | uneven snowfall, warm windows, bundled walkers, lamps, wreaths, a small animal, stars |

Choose only details that make sense for the photo. Keep recognizable objects as simple, graphic painted forms.

## Workflow

1. **Read the photo.** Identify the story, 3–5 anchors, dominant palette, one new picture idea, and the
   omissions. Preserve the source aspect ratio, but not its exact camera framing.
2. **Choose the hierarchy.** Decide the main subject, 2–3 large supporting shapes, one generous quiet area and
   3–7 discovery details. For people in a travel scene, preserve a recognizable pose, clothing and hair
   silhouette; do not reproduce every person or every background object.
3. **Build one English generation instruction** with the following order:
   - what to retain from the photo;
   - simplified scene layout and the chosen additions;
   - the visual target block below;
   - default stamp-frame block;
   - avoid list.
4. **Generate the illustration directly, without asking the model to draw the border.** Do not return this
   first-pass image yet.
5. **Apply a mandatory final image-edit pass to the generated image.** The edit must preserve the illustration
   exactly and make only this addition:

   > Keep every part of the artwork unchanged. Add only a clean warm-ivory postage-stamp border about 4% of
   > the short edge, with small rounded perforation bites evenly spaced around all four outer edges. Keep the
   > artwork inside the border; do not crop, redraw, add text, change colors, alter faces, add logos, or add
   > decorations. This is the final image.

   Return only the second-pass framed image plus one concise explanation in the user's language and three short
   tuning options. Show the full English prompt only when the user asks for it. If the user requests a different
   frame color, replace “warm-ivory” with that exact color. Skip this step only when the user explicitly asks for
   no border.

### Reusable visual target block

Use this wording, adapting only the palette and scene nouns:

> Recompose the photo as a bright, comforting graphic editorial illustration, not a literal painted copy.
> Build the image from a few large opaque matte gouache-like color shapes, a small harmonious palette, slightly
> flattened perspective, warm off-white breathing room and sparse dark-navy hand-drawn lines. Use only a faint
> paper grain and simple decorative marks; keep surfaces quiet and the silhouette hierarchy obvious. Make the
> scene whimsical, spacious and inviting, with a few delightful discoveries rather than dense detail.
> Avoid oil-paint realism, painterly brush modeling, dense speckles, realistic material texture, airbrushed
> gradients, cinematic lighting, heavy shadows, glossy rendering, 3D, CGI, photorealism, muddy brown or sepia,
> hyper-detailed linework, flat computer-vector shapes, readable text, watermarks and signatures.

### People block

Use whenever a person with a visible face appears:

> Render every visible face as a kind, complete, stylized painted face: two small naturally aligned eyes, soft
> brows, a subtle nose mark and a small closed mouth, all made with the same opaque gouache and pencil texture
> as the rest of the image. Preserve the person's pose, hair silhouette and clothing, but do not chase
> photographic likeness. No blank faces, mask-like faces, uncanny realism, glossy anime eyes or featureless
> faces on medium or large figures.

## Postage-stamp edge: default

Finish every image with a stamp edge unless the user explicitly asks for **no border** or a plain illustration.
Keep the artwork itself more important than the frame. Always use the mandatory second-pass image edit in the
workflow; never return the unframed first-pass image.

> Finish as a vintage postage stamp with a clean warm ivory or parchment border about 4% of the short edge and
> small rounded perforation bites evenly aligned around every outer edge. If the user specifies a border color,
> use that exact color instead. Keep important subjects inside the edge. No text, denomination, logo, watermark
> or decorative objects in the border.

`tools/stamp-frame.html` remains available when a person wants to add an optional place name, date or
denomination manually in a browser.

## Checks before returning

- [ ] The photo's story and selected anchors are recognizable, without copying all its literal detail.
- [ ] The scene reads as abstracted, flat graphic gouache-like color fields—not oil paint or a filtered photograph.
- [ ] The palette is fresh and comforting, with clear color separation.
- [ ] The picture has a deliberate recomposition and one generous quiet area.
- [ ] Three to seven small additions fit the scene naturally.
- [ ] Visible faces are complete, warm and simplified; distant backs may stay featureless.
- [ ] Any signage is abstracted; there is no readable generated text.
- [ ] A warm-ivory stamp edge appears, unless the user explicitly asked for no border.
