---
name: cozy-flat-illustration
description: Transform a user-supplied photo into a direct, finished comforting puzzle and greeting-card illustration: cheerful hand-painted flat shapes, simplified people with kind faces, small scene-specific discoveries, and a default warm-ivory perforated postage-stamp edge. Use when the user asks to turn a photo into a cozy, whimsical, healing, storybook, puzzle-like, illustrated-travel, or hand-painted scene.
---

# Cozy Illustrated Scene

Turn the supplied photo into a finished image with the image-generation tool. Do not make the user copy a
prompt into another app unless they explicitly ask for a prompt-only version. Use the photo as the reference
for subject, composition and mood, but **redesign it as an illustration rather than repainting the pixels**.

Do not name artists, studios, brands or companies in a generation prompt. Describe the visual traits instead.

## Visual target

Make a bright, comforting, puzzle-like editorial illustration. It should feel like a painted paper good
enough to linger over: simple large shapes at first glance, then delightful small discoveries on a second
look.

- **Shape first, not oil paint.** Rebuild the photo as 2–5 layers of clear, simplified silhouettes and color
  blocks. Flatten perspective slightly; keep major architecture, mountains, trees and objects legible.
- **Medium.** Use opaque gouache, waxy crayon and colored-pencil-like marks on lightly textured paper:
  chalky coverage, imperfect hand-drawn contour lines, small dry-brush variations. Do not use glossy blending,
  deep realistic shading, thick impasto, cinematic lighting or painterly realism.
- **Color.** Use clean, uplifting colors with generous cream or sky-blue breathing room: powder blue, soft
  coral, tomato red, leaf green, buttery yellow, ultramarine, peach, warm white. Avoid muddy brown casts and
  an all-grey muted palette.
- **Linework.** Use a few dark navy, charcoal or deep-green hand-drawn lines to anchor windows, branches,
  railings, waves and clothing folds. Lines may wobble slightly; they must not look like computer vectors.
- **Figures.** Make people graphic and warm. A visible face always gets two small aligned eyes, soft brows, a
  nose mark and a small closed mouth in the same painted texture as the scene. Never leave a visible face
  blank, mask-like or photorealistic. Distant or back-facing figures can be simple shapes.
- **Abstraction.** Simplify detail into patterned marks: a forest becomes layered pine triangles and leaf dabs;
  water becomes broad bands with a few long strokes; a city becomes stacked façades, windows and awnings. Do
  not reproduce every photographic shadow, reflection, crease or texture.

## Add meaningful small discoveries

After preserving the photo's 3–6 defining elements, add **5–12 small, context-appropriate details**. Spread
them through foreground, middle ground and distance. They must enrich the story, never look like random filler.

| Source scene | Good additions |
| --- | --- |
| Mountain, forest, meadow | wildflowers, birds, marmots or squirrels, hikers, a trail marker, tiny backpacks, butterflies, a dog |
| Water, ferry, harbour | gulls, sailboats, a ferry, buoy, folded map, thermos, binoculars, small shoreline houses |
| Street, market, town | striped awnings, flower boxes, bicycles, fruit crates, dogs, planters, tiny passers-by, cafe chairs |
| Interior, train, ferry cabin | a book, tote bag, cup, luggage, potted plant, small reflection, a distant boat or shoreline detail |
| Winter or night | uneven snowfall, warm windows, bundled walkers, lamps, wreaths, a small animal, stars |

Choose only details that make sense for the photo. Keep recognizable objects as simple, graphic painted forms.

## Workflow

1. **Read the photo.** Identify the story, 3–6 elements that must remain, the dominant palette, and what can
   be simplified or removed. Preserve the source aspect ratio.
2. **Choose the hierarchy.** Decide the main subject, 2–3 large supporting shapes, and the discovery details.
   For people in a travel scene, preserve pose, clothing and hair silhouette; make the setting the richer part
   unless the user explicitly asks for a portrait.
3. **Build one English generation instruction** with the following order:
   - what to retain from the photo;
   - simplified scene layout and the chosen additions;
   - the visual target block below;
   - default stamp-frame block;
   - avoid list.
4. **Generate the image directly.** Return the image plus one concise explanation in the user's language and
   three short tuning options. Show the full English prompt only when the user asks for it.

### Reusable visual target block

Use this wording, adapting only the palette and scene nouns:

> Render as a cheerful, comforting hand-painted editorial illustration made from simplified flat gouache
> shapes, waxy crayon texture and small colored-pencil details on softly textured paper. Use a clear silhouette
> hierarchy, slightly flattened perspective, bright clean color blocks, warm off-white highlights and a few
> loose charcoal or deep-navy contour lines. Make it whimsical and inviting rather than realistic: readable
> objects, gentle irregular hand-drawn edges, and small delightful things to discover throughout the scene.
> Avoid oil-paint realism, airbrushed gradients, cinematic lighting, heavy shadows, glossy rendering, 3D, CGI,
> photorealism, dense brown sepia, flat computer-vector shapes, unreadable text, watermarks and signatures.

### People block

Use whenever a person with a visible face appears:

> Render every visible face as a kind, complete, stylized painted face: two small naturally aligned eyes, soft
> brows, a subtle nose mark and a small closed mouth, all made with the same opaque gouache and pencil texture
> as the rest of the image. Preserve the person's pose, hair silhouette and clothing, but do not chase
> photographic likeness. No blank faces, mask-like faces, uncanny realism, glossy anime eyes or featureless
> faces on medium or large figures.

## Postage-stamp edge: default

Finish every image with a stamp edge unless the user explicitly asks for **no border** or a plain illustration.
Keep the artwork itself more important than the frame.

> Finish as a vintage postage stamp with a clean warm ivory or parchment border about 4% of the short edge and
> small rounded perforation bites evenly aligned around every outer edge. If the user specifies a border color,
> use that exact color instead. Keep important subjects inside the edge. No text, denomination, logo, watermark
> or decorative objects in the border.

For a pixel-perfect, repeatable frame across a set, use `tools/stamp-frame.html` after image generation.

## Checks before returning

- [ ] The photo's story and major shapes are still recognizable.
- [ ] The scene reads as flat, graphic gouache and paper texture—not oil paint or a filtered photograph.
- [ ] The palette is fresh and comforting, with clear color separation.
- [ ] At least five small additions fit the scene naturally.
- [ ] Visible faces are complete, warm and simplified; distant backs may stay featureless.
- [ ] Any signage is abstracted; there is no readable generated text.
- [ ] A warm-ivory stamp edge appears, unless the user explicitly asked for no border.
