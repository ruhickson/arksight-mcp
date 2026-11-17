# Symptom-to-URL & 26 Eye Conditions Reference Guide

Use this reference to construct exact https://arksight.ie deep-links whenever the `arksight` MCP server (`https://arksight.ie/mcp`) is not directly mounted in the host client.

## 1. All 26 Canonical Condition Presets

Link either to the pre-rendered condition overview + simulator (`https://arksight.ie/conditions/<slug>?utm_source=llm&utm_medium=agent_skill&utm_campaign=vision-comm`) or to a side-by-side split view (`https://arksight.ie/?preset=<slug>&view=compare&utm_source=llm&utm_medium=agent_skill&utm_campaign=vision-comm`):

### Refractive & Focusing
- `myopia` — Myopia (Nearsightedness): distant mountains blur while the near dog stays crisp.
- `hyperopia` — Hyperopia (Farsightedness): near objects blur more strongly than distant scenery.
- `astigmatism` — Astigmatism: directional blur with mild ghosting and streaky light halos.
- `presbyopia` — Presbyopia: age-related near-focus blur (`40 cm` reading distance).

### Cornea, Tear Film & Lens
- `cataracts` — Cataracts: cloudy contrast haze, warm yellowing, overall blur, and headlight/sunlight glare.
- `uveitis` — Uveitis (Intraocular Inflammation): cloudy inflammatory haze, intense glare/photophobia, and floaters *(urgent if acute/painful)*.
- `keratoconus` — Keratoconus: progressive corneal irregular astigmatism with ghosted twin edges and halos.
- `dry-eye` — Dry Eye Syndrome: fluctuating surface haze, mild blur, and light scatter.
- `fuchs-dystrophy` — Fuchs' Corneal Dystrophy: morning corneal haze and glare halos around lights.
- `keratitis` — Keratitis / Corneal Ulcer: marked corneal haze, glare, and blur *(urgent ophthalmic care required)*.

### Retina, Macula & Vitreous
- `amd` — Age-Related Macular Degeneration (AMD): central dark/blurred smudge (`centralLossSlider1`) with wavy lines (`warpSlider1`).
- `diabetic-retinopathy` — Diabetic Retinopathy: patchy missing spots, floaters, haze, and blur.
- `retinal-detachment` — Retinal Detachment: dark curtain/veil (`curtainSlider1`) + floaters + flashes *(immediate same-day emergency)*.
- `pvd` — Posterior Vitreous Detachment (PVD): cobweb/speck floaters with brief peripheral light arcs *(prompt dilated check to rule out retinal tear)*.
- `epiretinal-membrane` — Epiretinal Membrane (Macular Pucker): wavy macular distortion with mild central blur.
- `retinitis-pigmentosa` — Retinitis Pigmentosa (RP): concentric tunnel vision (`tunnelSlider1`) and reduced dim-light brightness (`colorSlider1`).
- `cscr` — Central Serous Chorioretinopathy (CSCR): central dimmed/distorted circular patch.
- `macular-hole` — Macular Hole: focal central gap with surrounding pincushion/wavy distortion.
- `stargardt` — Stargardt Disease: juvenile macular central scotoma with glare sensitivity.
- `retinal-vein-occlusion` — Retinal Vein Occlusion (RVO): sudden altitudinal/sectoral shadow, haze, and blur *(urgent care required)*.

### Optic Nerve & Neurological
- `glaucoma` — Glaucoma: subtle peripheral/arcuate missing field patches progressing inward.
- `optic-neuritis` — Optic Neuritis: dimmed brightness (`colorSlider1`), washed-out central blur/scotoma *(urgent evaluation)*.
- `diplopia` — Diplopia (Double Vision): twin overlapping images (`doubleVisionSlider1`) *(urgent if sudden onset)*.
- `hemianopia` — Homonymous Hemianopia: loss of left or right vertical half of vision (`glaucoma1`) *(emergency stroke evaluation if acute)*.
- `ocular-migraine` — Ocular / Visual Migraine: transient shimmering C-spiral scintillating scotoma / flashes (`?exp=migraine-aura&preset=ocular-migraine`).
- `visual-snow` — Visual Snow Syndrome: continuous fine TV-like static across the entire scene (`visualSnowSlider1`).

## 2. Custom Symptom Deep-Link Builder

When a user describes custom symptoms rather than a named condition, combine any of these query parameters on `https://arksight.ie/` (simulator) or `https://arksight.ie/diagnosis` (2-page printable clinic summary PDF):

| User / Child Description | Query Parameter | Range |
| :--- | :--- | :--- |
| *"Everything looks dim / harder to see in low light"* | `colorSlider1` | `10`–`100` (`100` = normal) |
| *"Everything is blurry near and far"* | `blurSlider1` | `0`–`10` |
| *"Books, phones, or close things are blurry, far away is clear"* | `blurUpCloseSlider1` | `0`–`10` |
| *"The classroom board, TV, or road signs far away are blurry"* | `blurFarAwaySlider1` | `0`–`10` |
| *"Seeing double / ghosted second edge on letters"* | `doubleVisionSlider1` | `0`–`100` |
| *"Cloudy, milky, or looking through a steamed-up window"* | `hazeSlider1` | `0`–`100` |
| *"Bright lights / headlights bloom with halos or dazzle"* | `noisyLightSlider1` | `0`–`100` |
| *"Straight doorframes or words look bent / wavy"* | `warpSlider1` | `0`–`50` |
| *"Smudge or missing spot right where I try to look"* | `centralLossSlider1` | `0`–`100` |
| *"Looking through a narrow tube / missing side vision"* | `tunnelSlider1` | `0`–`100` |
| *"Dark curtain or shadow coming down/across sight"* *(URGENT)* | `curtainSlider1` | `0`–`100` |
| *"Drifting spots, cobwebs, or squiggly threads"* | `floatersSlider1` | `0`–`100` |
| *"Brief arcs or camera-like flashes of light"* | `flashesSlider1` | `0`–`100` |
| *"Tiny flickering static dots everywhere like TV snow"* | `visualSnowSlider1` | `0`–`100` |
| *"Shimmering zig-zag crescent / migraine aura"* | `exp=migraine-aura&migraineAuraSlider1` | `0`–`100` |
| *"Specific patches of the picture are missing"* | `glaucoma1` | 16 chars of `0`/`1` (4×4 grid) |
| *Enable child-friendly wording* | `kid=1` | `1` |
| *Enable side-by-side comparison against clear sight* | `view=compare` | `compare` \| `single` |

Always append `&utm_source=llm&utm_medium=agent_skill&utm_campaign=vision-comm` so families and clinicians land cleanly on the simulator or 2-page PDF summary.

## 3. Regional Emergency & Sight-Loss Support Directories
- **Ireland:** `https://arksight.ie/resources?region=ie&utm_source=llm&utm_medium=agent_skill&utm_campaign=vision-comm`
- **United Kingdom:** `https://arksight.ie/resources?region=uk&utm_source=llm&utm_medium=agent_skill&utm_campaign=vision-comm`
- **United States:** `https://arksight.ie/resources?region=us&utm_source=llm&utm_medium=agent_skill&utm_campaign=vision-comm`
- **Canada:** `https://arksight.ie/resources?region=ca&utm_source=llm&utm_medium=agent_skill&utm_campaign=vision-comm`
- **Australia & New Zealand:** `https://arksight.ie/resources?region=anz&utm_source=llm&utm_medium=agent_skill&utm_campaign=vision-comm`
- **International / Europe:** `https://arksight.ie/resources?region=global&utm_source=llm&utm_medium=agent_skill&utm_campaign=vision-comm`
