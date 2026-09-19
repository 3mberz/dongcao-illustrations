# 生图提示词模板

每张图单独生成，不要把多张拼在一起。

生图时**把 `assets/reference/` 里的角色三视图一起附上**，模型看图比看字准得多。

## 单张生成

```text
Generate one standalone colored-pencil illustration in a warm children's-book style.

BACKGROUND — pick one before anything else:

[A] Cream paper (default, for standalone images):
    ...on cream ivory textured paper (#F5F2EC), visible paper grain.

[B] Transparent (when the image will be placed into another layout — a card,
    poster, web page, slide, print piece):
    Fully transparent background, PNG with alpha. Nothing behind the subject:
    no paper, no paper grain, no white, no off-white, no vignette, no ground
    plane except the small pencil shadow directly under the feet. Do NOT paint
    a cream background and expect it to be cut out later — output transparency
    directly. Paper texture belongs to the page this will sit on, not to the
    drawing.

MEDIUM (most important — get this right first):
Drawn with colored pencils{在此接上所选的底}. Every colored
area is built from FINE, DENSE, EVENLY-DIRECTED pencil hatching, layered in several
light passes — thin strokes close together, not coarse scribble. THE PAPER GRAIN MUST
SHOW THROUGH THE COLOR: never fully covered, never saturated flat. Colors stay muted
and settled, softened by the paper — never bright, never neon, never marker-like,
never waxy crayon. NEVER flat digital fill, never gradient, never airbrush, never
thick paint. All outlines drawn in DEEP INDIGO BLUE pencil (#152A55), never black.
Outlines show slight repeated searching strokes, gently wobbly, hand-made. Ground
shadow is only a small patch of loose pale-blue pencil scribble under the feet.
Flat even light, no drama, no highlights, no cast shadows. Warm, quiet, tactile.

INTENT (equally important):
This is a quiet moment from her ordinary day on the plateau — not an instructional
diagram. She is doing something for herself, not demonstrating it for the viewer.
Nothing in the frame addresses the viewer. No before/after comparison, no numbered
steps, no cross marks, no right/left "correct vs wrong", no signage, no held-up
placards. The picture should read as "this is her life", not "here is how to do it".

CHARACTER — 冬草, fixed, identical every time:
A young Tibetan girl, chibi proportions about 4.5 heads tall — large round head,
short body, short rounded limbs, round full cheeks.
Face: plain black oval dot eyes, no whites, no catchlights. Thin short dark brows.
A tiny upward-curved smile. Nose barely drawn. TWO round peachy-orange blush circles
below the eyes. Expression always gentle, quiet, calm — never exaggerated, never posing.
Hair: deep indigo-black, fine pencil strokes showing individual strands. Two braids
falling in front over the chest, one thick braid down the back. Small coral and
turquoise beads threaded into the braids. A few loose wisps at the forehead.

THREE SIGNATURE OBJECTS — all three must be visible:
1. A necklace of large round orange-red coral beads.
2. A silver chased belt plaque with a SNOW-MOUNTAIN motif engraved at its center
   and a coral cabochon set in it.
3. A small brown leather diary hanging at her waist on a strap — cover shows a simple
   triangular snow-mountain line drawing and the Chinese characters 冬草日记, with a
   brass clasp. This is the signature prop and must never be omitted.

CLOTHING:
Royal blue Tibetan chuba top, its damask pattern made of small GRASS-SPROUT motifs
(not flowers). A long skirt of uneven VERTICAL colored stripes. A woven zigzag sash
in red/orange/yellow across the chest. Dark brown round-toed Tibetan boots.
Secondary: long turquoise-and-coral earrings, small silver pendants at the hip.

COLOR PALETTE — use only these plus the paper:
royal blue #1D6FD0, teal #10A5A0, orange-red #E8503A, magenta #D6246E,
wine #7B1E45, cream #F0E6D2, deep indigo #152A55.

SCENE:
{场景：在哪里、什么时候、周围有什么}

ACTION:
{冬草正在做什么 —— 必须是她在做，不是站在旁边看}

PROPS:
{物件1} / {物件2} / {可选物件3}

CHINESE LABELS — default NONE. Only if unavoidable:
{最多 4 处，每处 2-8 字}
If any text appears it must be HAND-WRITTEN WITH A PENCIL, slightly irregular,
in deep indigo or orange-red. Never a printed or digital typeface. Never numbers,
doses, temperatures, durations, step numbers, slogans or headlines.

CONSTRAINTS:
One image, one moment. EXACTLY ONE 冬草 in the frame — never two of her, never a
comic strip of the same character. Her expression is always the same small gentle
closed-mouth smile — never an open surprised mouth, never exaggerated. No manga
emotion symbols: no exclamation strokes, no sweat drops, no sparkle eyes, no hearts.
Subject occupies about 45%-65% of the canvas. Leave at least 30% as clean untouched
paper. Do not use a pure white background. Do not use black outlines. Do not flat-fill
any area. No gradients, no drop shadows, no glossy highlights, no vector look, no 3D,
no anime style, no photorealism. No frame, no title bar, no bottom caption banner, no
watermark, no logo. Keep her face and proportions consistent with the attached
character sheet. Aspect ratio {16:9 / 3:4 / 1:1}.
```

## 常用底

| 用途 | 底 |
| --- | --- |
| 公众号正文配图、小红书、朋友圈 | 米白纸底 |
| 卡片、海报、网页、PPT、印刷品 | 透明底 |

拿不准就问用户这张图要单独发还是要嵌进别的版面。

## 常用比例

| 用途 | 比例 |
| --- | --- |
| 公众号正文配图 | 16:9 |
| 公众号首图 / 小红书 | 3:4 |
| 朋友圈 / 头像 / 单图 | 1:1 |

## 图像编辑提示

### 把米白底改成透明底

```text
Edit the provided image. Keep the character, the composition, the colors and the
colored-pencil rendering exactly as they are. Remove the background completely:
output a PNG with a fully transparent background. Keep only the subject and the
small pencil shadow under the feet. Remove all paper texture and paper grain from
the background — do not replace it with white or any other color.
```

### 修媒介（最常用）

```text
Edit the provided image. Keep the composition, character, and colors exactly as they
are. Only change the rendering: rebuild every colored area out of visible diagonal
colored-pencil hatching strokes on cream textured paper, and redraw all outlines in
deep indigo blue pencil instead of black. Remove any flat fill, gradient, gloss, or
cast shadow. Do not change the layout or add anything new.
```

### 去掉多余文字

```text
Edit the provided image. Remove only the text "{要删除的文字}". Fill that area with
the same cream paper texture, matching the surrounding blank paper. Preserve
everything else exactly: character, props, labels, pencil stroke style, composition,
aspect ratio. Do not add any new text or objects.
```

### 从讲课改回日常（最常用）

```text
Regenerate this illustration. Keep the character, the style and the medium, but change
what it is doing: right now it reads as an instructional diagram. Remove the
comparison / numbered steps / cross marks / captions entirely. Instead show ONE quiet
moment from her ordinary day in which this simply happens by itself, as something she
does for herself. One 冬草 only. No text unless unavoidable, and any text must be
hand-written in pencil. It should read as "this is her life", not "here is how to do it".
```

### 让动作更实

```text
Regenerate this illustration with the same scene and style, but make 冬草 physically
doing the action rather than standing beside it. Her hands should be on the object,
her posture should show effort or attention. Keep the colored-pencil medium, the cream
paper, the indigo outlines, and all three signature objects.
```

### 修脸

```text
Edit the provided image. Redraw only the face to match the attached character sheet:
plain black oval dot eyes with no whites and no highlights, thin short brows, a tiny
curved smile, barely-drawn nose, two round peachy-orange blush circles. Keep the same
colored-pencil texture. Do not change anything else.
```
