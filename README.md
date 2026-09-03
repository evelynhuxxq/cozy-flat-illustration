# cozy-flat-illustration

A [Claude](https://claude.ai) skill that turns a photograph into a copy-paste image prompt for
warm, hand-painted scene illustration — the storybook / jigsaw-puzzle look.

It does not generate images. It reads your photo, analyses it, and writes the prompt you paste into
ChatGPT, Gemini or any other chat-style image tool.

## The style

Hand-painted scene illustration, of the kind found on illustrated puzzles, greeting cards and picture books:

- Digital gouache — visible brush texture, slightly soft edges
- Cheerful color, never a greyed-out muted palette
- Fine painted texture across the whole image (snow flecks, leaf dabs, stars)
- Flattened perspective from a slightly elevated viewpoint; everything legible
- Tiny, numerous figures and small objects everywhere — the picture rewards looking

## Install

```bash
git clone https://github.com/<you>/<repo>.git
cp -r <repo>/cozy-flat-illustration ~/.claude/skills/
```

Or paste the contents of `cozy-flat-illustration/SKILL.md` into a new skill in Claude's Skills settings.

## Use

Drop a photo into Claude and ask for illustration style. You get back:

1. What was read from the photo, and whether the photo suits this style
2. The English prompt, in a code block
3. A short explanation of what is unusual about this particular prompt
4. Three tuning suggestions

**Strongly recommended:** upload two or three reference illustrations along with your photo.
Words hit a low ceiling describing a visual style; one reference image is worth two hundred adjectives.

## Choosing photos

This style paints **scenes**, not people.

| Works | Doesn't |
|---|---|
| Streets, parks, shopfronts, visitor centres | Half-body portraits, close-ups |
| Cluttered interiors, ferry cabins, carriages | Empty seascapes and skies |
| Anything with paths, railings, window frames | Portraits with a fully blurred background |

Close-up portraits are not impossible, but no amount of tuning makes them look like the reference style.
That charm comes from dense small content, and a single portrait has none.

## What was learned the hard way

These came out of repeated failures and are worth more than the style description itself.

**Never use `even`, `regular` or `uniform` to describe texture.** You get wallpaper or fish scales.
Write "uneven density, varying sizes, hand-drawn rhythm" instead.

**For organic forms — flower plumes, clouds, canopies, waves — define the silhouette first,
then the interior texture.** Describing only the filling always fails. "Built from small dots" alone
produced a pile of bubble-tea pearls.

**For water, control stroke length and contrast, not quantity.**
Short + dense + high contrast = television static. Long + sparse + low contrast = water.

**Fill empty areas in the order areas → objects → lines. Never by adding more texture.**
Areas are large irregular patches of related tone; objects are boats, birds and walkers; lines are long
strokes, branches and railings. Adding texture is what caused the failures above.

**An uncanny face is almost always a rendering mismatch** — the model paints the background flat but gives
the face volumetric shading. The prompt must state that the face uses exactly the same technique as
everything else.

**Pose risk, low to high:** tiny figures < back view < full profile < eyes closed or hidden by a hat brim
or sunglasses < three-quarter view < facing the viewer. Sunglasses, hats and glasses are gifts — they anchor
identity and cover the hardest feature to draw.

**Keep prompts to roughly 250–400 words.** The denser the constraints, the more mechanically the model
follows each clause. Every failure listed above came from a prompt that was too detailed, not too vague.

## Framing finished images

`tools/stamp-frame.html` adds a postage-stamp frame. Open it in a browser, drop in an image, fill in the
place and date, export a PNG. **Output dimensions match the source exactly**, so a framed version pairs
cleanly with the original side by side. The accent color is sampled from the artwork.

The matching layout rules live in the "Finished framing" section of `SKILL.md`. The important one:
never let the image model draw the frame — it comes out skewed and any text is garbled. Add it afterwards.

## License

MIT
