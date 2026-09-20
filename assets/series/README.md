# Series-level approved assets

Assets supplied from the OpenArt "animated series" folder. These are the canonical designs. Every new generation of a character must use the files here as image references, not a fresh text prompt.

## KANGA (approved)

| File | What it is | Use |
|---|---|---|
| `kanga/kanga-hero-beach.png` | Full-body hero still, front view, beach-town background (2:3 portrait) | Primary image reference for image-to-image, element-to-video and storyboard panels |
| `kanga/kanga-turnaround-a.png` | Four-view turnaround: front, three-quarter, side, back, neutral grey | Attach alongside the hero still for any shot that is not front-on |
| `kanga/kanga-turnaround-b.png` | Second four-view turnaround, same design, slightly different proportions | Backup reference; prefer turnaround A |
| `kanga/video/kanga-clip-1.mp4` | 12s talking-to-camera test, beach-town background, 1280x720, 24fps | Style and motion reference for dialogue shots |
| `kanga/video/kanga-clip-2.mp4` | 5s idle / talking test, same set | Motion reference |
| `kanga/video/kanga-clip-3.mp4` | 5s wave-then-talk test, same set | Motion reference (matches the "waves, then rests paw on pouch" endpoint pattern) |

Locked design details visible in these files (use these words in every prompt):
`soft grey-brown fur, cream belly, large dark eyes with small lashes, light green short-sleeved t-shirt under an olive-green sleeveless work vest with two front flap pockets and a small chest pocket, faint warm gold glow at the pouch, no other clothing`

## MAGGIE, HOPPER, WOMBAT (approved)

| File | Character | Source |
|---|---|---|
| `maggie/maggie-ref-sheet.png` | MAGGIE, three-view sheet | OpenArt `wgi65ab3d1ZAwh8z4Keh` |
| `hopper/hopper-ref-sheet.png` | HOPPER, three-view sheet | OpenArt `asshHLjaqWbZmwUyv73G` |
| `wombat/wombat-ref-sheet.png` | WOMBAT MECHANIC, three-view sheet | OpenArt `sO13cYPPxnW9ff4lsniz` |

OpenArt reference ids for image-to-image (pass as `visualReferences`, lead character first):
KANGA hero `vWfYJE8bj28ATNZDlrnE`, KANGA turnaround `TGYOo8MFUIhR8BrhQeN8`, MAGGIE `92cypkRioU7Aa9kbCTQ1`, HOPPER `tLIwpkdCKcRWPh9zdMwz`, WOMBAT `zZ2j4AqBsIn5C1ZXmCub`, ENV1 `gNSjWB1cXQ4bPjzhJEql`, ENV2 `wEZrqV4cF8P4o39Y7I8X`, ENV3 `4nqFkN4seEXBSNulKRd9`, ENV4 `YFGTxdvJcyXtQ7MTeD9a`.
