# User-supplied WeChat palette cards

Added 2026-10-20. Exact printed HEX labels were read from all nine individual Tuke cards and four PubCNS cards; the cover images repeat those cards and are not additional palettes. PubCNS RGB labels were cross-checked. Source image SHA-256, card locator and attribution are retained per registry record. Full article artwork is not bundled.

Sources: [涂客：9组渐变配色](https://mp.weixin.qq.com/s/pmdMiCk8wdMJy1OUes2iGg) and [PubCNS：跟着顶刊学配色18](https://mp.weixin.qq.com/s/3kdVaFgGGLvQikHTRa8QaA).

| Exact ID | Printed HEX values in source order |
| --- | --- |
| `wechat.tuke.blue` | #D9E6EF · #C5C1D9 · #8BD0DD · #66A6C3 · #415883 |
| `wechat.tuke.green` | #A7E8E2 · #84BEC8 · #659CB2 · #478074 · #185F59 |
| `wechat.tuke.brown` | #F5E0BA · #F5CD8D · #E19863 · #955A4C · #783124 |
| `wechat.tuke.orange` | #FBB858 · #F9B435 · #FAC10C · #FE8817 · #EE6514 |
| `wechat.tuke.red` | #F4D3D7 · #E8ACB3 · #EF9C84 · #DC566F · #851321 |
| `wechat.tuke.purple` | #FEF0F0 · #E8D2DA · #CCA9BE · #CB7EB3 · #A25C8F |
| `wechat.tuke.pink` | #FBF1F5 · #F9E7E6 · #F6CCD4 · #F2AEBC · #EC88A3 |
| `wechat.tuke.yellow` | #FEFAE7 · #F8F2C2 · #F9E99F · #F7DD72 · #F7D35D |
| `wechat.tuke.white` | #FFFFFF · #E2ECF4 · #B5C7D6 · #D2E6ED · #F0F5FD |
| `wechat.pubcns.nature18.fig1` | #1C2588 · #22B14C · #DE4E43 · #85B1E8 · #EA9EAD · #9E9E9E · #E6E6E6 |
| `wechat.pubcns.nature18.fig2` | #98002E · #8CABD6 · #9BA86C · #A5E083 · #F59280 · #BFBFBF · #ECE8F4 · #F9F4E5 |
| `wechat.pubcns.nature18.fig3` | #A6C2E0 · #D8E2EF · #F6E1C2 · #B0C899 · #BDB4D6 · #E0B2BF · #828B9C |
| `wechat.pubcns.nature18.fig4` | #6AA861 · #A7BB89 · #E6826C · #F0CD9B · #F5A087 · #A4D3C8 · #7475BD · #AE002E |

These are discrete swatch collections. Source titles describe gradients, but some collections (especially orange and white) are not monotonic in lightness. Do not imply perceptual uniformity or silently interpolate/reorder them. For continuous measurements prefer an established sequential map, or explicitly label a separately derived scale. Pale/neutral entries may be controls or backgrounds rather than distinguishable category colours.

R and Python: `easyplot_palette("wechat.tuke.blue", n=5)`; `easyplot_palettes(family="wechat")` lists this collection. R loads `scripts/easyplot_palettes.R`; Python imports `easyplot_palettes` from the skill scripts directory. All records are `not_assessed` for CVD. Nature is the paper venue named by the curator, not a publisher endorsement of the swatches. Defaults are unchanged.

## PubCNS issue 122 — added 2026-10-20

[Original article](https://mp.weixin.qq.com/s?__biz=MzU0ODY3Njg5NA==&mid=2247487936&idx=1&sn=76fd4ba3bc0a0c7d8e08e7c6e173cad1). Four unique palettes; the cover repeats the first. All printed RGB and HEX labels agree. The source heading says “Neuron”, but its body cites an HDAC/macrophage paper and its figures show PVN/DVC neurophysiology. Preserve that discrepancy; do not attribute these tables to the cited paper or treat the heading as verified publisher provenance. IDs retain the curator heading for lookup.

| Exact ID | Source-order HEX |
| --- | --- |
| `wechat.pubcns.neuron122.fig1` | #332D2A · #E4202D · #6BC3F5 · #3CB44B · #F543B4 · #FFB6D9 · #FBD136 · #007ACC · #C8C8C8 |
| `wechat.pubcns.neuron122.fig2` | #FF4D4D · #5ACAFF · #FFAA33 · #FF66FF · #90D25D · #E0B6B6 · #52393C · #808080 · #0099FF · #FFEB99 |
| `wechat.pubcns.neuron122.fig3` | #333333 · #E61B1B · #78C4FF · #FF00FF · #00B050 · #9300AF · #FFC878 · #D9D9D9 · #969696 |
| `wechat.pubcns.neuron122.fig4` | #003AFF · #FF00FF · #00FF55 · #FF0000 · #000000 · #A0A0A0 · #FFDCDC · #FFCC00 |

All four are `qualitative`/`prefix` sets, with 9, 10, 9 and 8 swatches respectively. No automatic interpolation, recycling or CVD guarantee. Red/green and saturated magenta combinations need inspection for their actual geometry; grey/black/pale entries may serve controls/backgrounds. `easyplot_palette("wechat.pubcns.neuron122.fig1", n=9)` works in both backends. The user collection now contains 17 palettes.
