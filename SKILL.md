---
name: cozy-flat-illustration
description: "Transform a user-supplied photo into a direct, finished dreamy editorial illustration through abstract visual extraction and poetic recomposition—not a one-to-one painted translation. Preserve the photo's aspect ratio, use layered luminous paint shapes and designed abstract figures, add a few scene-specific discoveries, and finish with a default warm-ivory perforated postage-stamp edge when the user asks for cozy, whimsical, healing, storybook, puzzle-like, illustrated-travel, or hand-painted scenes."
---

# Cozy Illustrated Scene

Turn the supplied photo into a finished image with the image-generation tool. Do not make the user copy a
prompt into another app unless they explicitly ask for a prompt-only version. Treat the photo as a bag of story
ingredients, not a blueprint: extract its mood, visual symbols and spatial rhythm, then **recompose them into
an illustration rather than translating each pixel, object or person**.

Do not name artists, studios, brands or companies in a generation prompt. Describe the visual traits instead.

## Visual target

Make a bright, comforting, dreamy narrative illustration. It should feel like a carefully composed travel
keepsake or illustrated stationery: beautiful and cohesive from afar, then full of small story moments on a
second look. Let the scene feel gently heightened or remembered, not literal. Do not make a rough sketch, a
crude cut-paper collage, a hard-edged travel poster or a literal painted photo.

- **Designed composition first.** Preserve the source photo's exact horizontal, vertical or square aspect ratio.
  Recompose within that fixed canvas around one strong focal moment, then balance it with foreground,
  middle-ground and distance. Move, enlarge, crop, combine or remove source elements only inside the fixed
  proportion when that creates a more beautiful rhythm of large and small shapes.
- **Luminous, layered paint—not flat graphic poster art.** Build the scene from simplified painted shapes that
  overlap, soften and vary in opacity. Use soft-edged color passages, a few translucent washes and subtle shifts
  of light within a color family to create air, depth and a dreamlike feeling. Keep paper texture delicate.
  Never render every leaf, pebble, fabric weave or material surface, but do not reduce the whole picture to
  uniform flat blocks either. Avoid grit, antique patina, scratchy pencil, dense speckles, dry-brush noise or
  visibly built-up paint.
- **Color and value.** Choose a deliberately edited 4–7 color palette plus warm white. Create beauty through
  unexpected color relationships and clear light/dark grouping: powder blue, peach, coral, tomato red, leaf
  green, ultramarine, butter yellow and cream are useful starting points. Avoid muddy browns, greyed-out
  realism and a universal sepia cast.
- **Linework is an accent, not a skeleton.** Do not enclose everything with dark outlines. Prefer changes of
  color, overlapping shapes and painted edges. Use a few thin, soft broken marks only where they clarify an
  important architectural rhythm, branch, wave or fold; never use heavy navy contours, comic inking, or uniform
  linework around people and objects.
- **Figures.** Turn people into designed, warm character shapes with a clear pose, clothing silhouette and
  gesture. For a medium or large visible face, preserve feeling and direction but not photographic likeness:
  construct it from 3–6 simple painted shapes—a rounded skin plane, an expressive hair silhouette, two tiny
  unequal dark marks or a single profile eye, a small nose plane, and a quiet mouth accent with restrained
  blush. Never make symmetrical manga/anime faces, large shiny eyes, eyelashes, detailed lips, individual hair
  strands, blank faces or photorealistic faces. Convert background crowds into elegant small color groups.
- **Integrated richness.** Turn a forest into layered canopies, trunks and a few leaf motifs; water into broad
  bands, long reflections and small boats; buildings into stacked façades, roof rhythms, windows and awnings.
  Add many small motifs only where they belong to the composition—on a ledge, beside a path, inside a window,
  around a foreground object—not as isolated stickers.

## Abstract extraction, not one-to-one translation

Before composing, name only these four things:

1. **Story:** the emotional moment, such as a slow ferry ride, a mountain outing or a roadside stop.
2. **Anchors:** 3–5 motifs worth recognizing, such as the red truck, ferry window, stone stairs, hiker or tree
   line.
3. **Picture idea:** one deliberate visual move that the photo does not need to supply—an oversized window, a
   winding path, a broad sky, a patterned stone wall, a simplified close-up object or a gentler viewpoint.
4. **Omissions:** remove at least half of the remaining literal detail. Replace it with purposeful color fields,
   motifs or a small invented vignette—not an unresolved blank area.

Use the story and anchors, then invent the picture. Preserve recognizability, not photographic accuracy. For
example, turn a crowd into three walking color groups, turn engraved text into nonverbal motifs, and turn many
trees into overlapping dark-and-light green shapes.

## Add meaningful small discoveries

After preserving the story and 3–5 anchors, add **8–16 small, context-appropriate details**. Arrange them as
2–4 miniature discovery clusters—such as a flower-and-animal corner, a small resting spot, a distant activity
or a patterned foreground—plus a few repeating motifs that bind the picture together. Give every object a
place in the scene and repeat its colors or shapes elsewhere; do not sprinkle unrelated stickers across empty
space. Keep one broad quiet area, but give it a purposeful role as sky, water, wall, path or large color field.

| Source scene | Good additions |
| --- | --- |
| Mountain, forest, meadow | wildflower patches, birds, marmots or squirrels, hikers, trail markers, tiny backpacks, a picnic thermos, butterflies, a dog, a sketchbook |
| Water, ferry, harbour | gulls, sailboats, a ferry, buoy, folded map, thermos, binoculars, small shoreline houses, flowerpots, a striped blanket |
| Street, market, town | striped awnings, flower boxes, bicycles, fruit crates, dogs, planters, tiny passers-by, cafe chairs, baskets, window plants |
| Interior, train, ferry cabin | a book, tote bag, cup, luggage, potted plant, small reflection, a distant boat or shoreline detail, ticket-like motifs, a scarf |
| Winter or night | uneven snowfall, warm windows, bundled walkers, lamps, wreaths, a small animal, stars, footprints, a steaming cup |

Choose only details that make sense for the photo. Keep recognizable objects as simple, graphic painted forms.

## Workflow

0. **Separate multiple inputs.** When the user supplies multiple photos, treat each photo as an independent
   illustration request. Generate one finished, separately framed image for each input photo, using one
   generation request per output. Never combine several inputs into a collage, contact sheet, split panel,
   merged panorama or single composite story unless the user explicitly asks for that format.
1. **Read the photo.** Identify the story, 3–5 anchors, dominant palette, one new picture idea, and the
   omissions. Lock the final canvas to the source photo's exact aspect ratio before generating. Recompose
   contents within that proportion; do not turn a landscape into a portrait, a portrait into a landscape, or
   a rectangle into a square unless the user explicitly asks.
2. **Choose the hierarchy.** Decide the main subject, 2–3 large supporting shapes, one purposeful quiet area,
   and 2–4 discovery clusters containing 8–16 details. For people in a travel scene, preserve a recognizable
   pose, clothing and hair silhouette; do not reproduce every person or every background object.
3. **Build one English generation instruction** with the following order:
   - what to retain from the photo;
   - simplified scene layout and the chosen additions;
   - the visual target block below;
   - default stamp-frame block;
   - avoid list.
4. **Generate the final framed illustration directly in one pass.** Include the stamp-edge block below in the
   generation instruction and return that finished image. Do not use a separate image-edit pass. Show the full
   English prompt only when the user asks for it. If the user requests a different frame color, use that exact
   color. Skip the frame only when the user explicitly asks for no border.

### Reusable visual target block

Use this wording, adapting only the palette and scene nouns:

> Recompose the photo as a refined, comforting, slightly dreamlike narrative illustration, not a literal painted
> copy. Preserve its exact aspect ratio. Build a beautiful hierarchy of foreground, middle-ground and distance
> using layered painted shapes, softened overlaps, translucent color washes and a controlled small palette. Let
> color create depth and a luminous remembered feeling; avoid uniform flat color blocks. Use no strong enclosing
> outlines—only occasional thin soft marks as accents. Do not individually render leaves, stones, fabric texture
> or realistic materials. Create 2–4 integrated story clusters with 8–16 scene-specific discoveries, repeating
> colors and motifs to make the whole picture feel designed. Use a purposeful quiet area for breathing room, not
> emptiness.
> Avoid oil-paint realism, thick or muddy paint, travel-poster line art, heavy navy contouring, vintage/antique
> patina, scratchy sketchiness, dense speckles, all-over dry-brush noise, realistic material texture, airbrushed
> gradients, cinematic lighting, heavy shadows, glossy rendering, 3D, CGI, photorealism, sepia casts, crude
> cut-paper collage, unreadable text, watermarks and signatures.

### People block

Use whenever a person with a visible face appears:

> Render every medium or large visible face as a warm, designed abstract character portrait that captures the
> person's direction, mood, hair silhouette and gesture rather than their photographic likeness. Construct the
> face from 3–6 painted shapes: a rounded skin plane, a single hair mass, two tiny unequal dark marks or a single
> profile eye, a small nose plane, a quiet mouth accent and restrained blush. Keep it expressive but non-anime:
> no symmetrical manga face, no large or shiny eyes, eyelashes, detailed lips, individual hair strands, detailed
> skin, uncanny realism, blank faces or mask-like faces.

## Postage-stamp edge: default

Finish every image with a stamp edge unless the user explicitly asks for **no border** or a plain illustration.
Keep the artwork itself more important than the frame. Include it as part of the direct final generation; do not
use a second image-editing pass.

> Finish as a vintage postage stamp with a clean warm ivory or parchment border about 4% of the short edge,
> while preserving the source image's exact canvas aspect ratio, and
> small rounded perforation bites evenly aligned around every outer edge. If the user specifies a border color,
> use that exact color instead. Keep important subjects inside the edge. No text, denomination, logo, watermark
> or decorative objects in the border.

`tools/stamp-frame.html` remains available when a person wants to add an optional place name, date or
denomination manually in a browser.

## Checks before returning

- [ ] The photo's story and selected anchors are recognizable, without copying all its literal detail.
- [ ] The final canvas keeps the source photo's exact aspect ratio unless the user explicitly requested another ratio.
- [ ] The scene reads as an abstracted, luminous painted illustration with layered color and soft atmosphere—not
      oil paint, a filtered photograph, a hard-edged poster or a uniformly flat graphic.
- [ ] The palette is fresh and comforting, with clear color separation.
- [ ] The picture has a deliberate recomposition, one purposeful quiet area and no unresolved emptiness.
- [ ] Eight to sixteen details form two to four natural, compositionally integrated discovery clusters.
- [ ] Visible faces capture mood and gesture through designed abstract features, without anime-like eyes or
      heavy enclosing linework; distant backs may stay featureless.
- [ ] Any signage is abstracted; there is no readable generated text.
- [ ] A warm-ivory stamp edge appears, unless the user explicitly asked for no border.
- [ ] For multiple supplied photos, each photo has its own separate finished output; no collage or merged scene
      was made unless explicitly requested.
