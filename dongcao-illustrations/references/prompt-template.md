# 生图提示词模板

每张图单独生成，不要把多张拼在一起。

生图时**把 `assets/reference/` 里的角色三视图一起附上**，模型看图比看字准得多。

## 单张生成

```text
Generate one standalone colored-pencil illustration in a warm children's-book style.

MEDIUM (most important — get this right first):
Drawn with colored pencils on cream ivory textured paper (#F5F2EC), visible paper
grain. Every colored area is built from visible diagonal pencil hatching strokes,
layered, uneven pressure — NEVER flat digital fill, never gradient, never airbrush,
never thick paint. All outlines drawn in DEEP INDIGO BLUE pencil (#152A55), never
black. Outlines show slight repeated searching strokes, gently wobbly, hand-made.
Ground shadow is only a small patch of loose pale-blue pencil scribble under the feet.
Flat even light, no drama, no highlights, no cast shadows. Warm, quiet, tactile.

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

CHINESE HANDWRITTEN LABELS (optional, 0-4 max):
{短标注，2-8 字，深靛蓝或橘红铅笔手写体}

CONSTRAINTS:
One image, one moment. Subject occupies about 45%-65% of the canvas. Leave at least
30% as clean untouched paper. Do not use a pure white background. Do not use black
outlines. Do not flat-fill any area. No gradients, no drop shadows, no glossy
highlights, no vector look, no 3D, no anime style, no photorealism. No frame, no
title bar, no watermark, no logo. Keep her face and proportions consistent with the
attached character sheet. Aspect ratio {16:9 / 3:4 / 1:1}.
```

## 常用比例

| 用途 | 比例 |
| --- | --- |
| 公众号正文配图 | 16:9 |
| 公众号首图 / 小红书 | 3:4 |
| 朋友圈 / 头像 / 单图 | 1:1 |

## 图像编辑提示

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
