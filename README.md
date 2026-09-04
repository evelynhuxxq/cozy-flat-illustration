# cozy-flat-illustration

An image-generation skill for turning photos into comforting, graphic, hand-painted travel and storybook scenes. It keeps the main story of the photo, gives visible people complete kind faces, and adds small details that fit the setting.

## Structure

```
SKILL.md                # the complete skill
tools/stamp-frame.html # optional browser editor for manual captions
```

The repository root is the skill package—there is no nested copy to install.

## Use

Add this repository folder to your skills directory, then attach a photo and ask for a cozy flat illustration. The skill generates the finished illustration directly and always finishes it with a warm-ivory stamp edge unless you request no border.

## Optional stamp border

The skill completes every illustration with a dedicated second image-edit pass that adds the warm-ivory perforated frame. Open `tools/stamp-frame.html` only when you want to choose a color or add captions manually.
