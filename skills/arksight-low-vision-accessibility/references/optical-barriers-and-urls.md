# Ophthalmic UI Barriers & ArkSight Simulation URL Reference

Use these side-by-side comparison links (`view=compare`) in accessibility reviews, PR descriptions, and design critiques so engineers and stakeholders can compare clear reference sight against the simulated condition at https://arksight.ie.

## Ready-to-Use Condition Comparison URLs

| Ophthalmic Profile | What Happens to UI Elements | Side-by-Side Simulation Link |
| :--- | :--- | :--- |
| **Glaucoma (Arcuate / Peripheral Scotomas)** | Corner toasts, distant table actions, and off-center badges disappear silently without appearing "black" to the user. | `https://arksight.ie/?preset=glaucoma&view=compare&utm_source=llm&utm_medium=agent_skill&utm_campaign=low-vision-a11y` |
| **Retinitis Pigmentosa (Tunnel Vision + Night Dimming)** | Severe peripheral constriction (`tunnelSlider1`) leaves only a narrow central island; wide multi-column layouts require exhausting head/eye scanning. | `https://arksight.ie/?preset=retinitis-pigmentosa&view=compare&utm_source=llm&utm_medium=agent_skill&utm_campaign=low-vision-a11y` |
| **Homonymous Hemianopia (Post-Stroke Half-Field Loss)** | Vertical left or right half of every line/screen vanishes; wide `space-between` rows hide the right-hand button or left-hand label. | `https://arksight.ie/?preset=hemianopia&view=compare&utm_source=llm&utm_medium=agent_skill&utm_campaign=low-vision-a11y` |
| **Age-Related Macular Degeneration (AMD)** | Central foveal smudge (`centralLossSlider1`) + wavy metamorphopsia (`warpSlider1`) obliterate small icons, thin fonts, and tight line spacing. | `https://arksight.ie/?preset=amd&view=compare&utm_source=llm&utm_medium=agent_skill&utm_campaign=low-vision-a11y` |
| **Cataracts (Cloudy Media + Veiling Glare)** | Milky contrast washout (`hazeSlider1`) + bright light bloom (`noisyLightSlider1`) erase low-contrast grey borders and placeholder text on white pages. | `https://arksight.ie/?preset=cataracts&view=compare&utm_source=llm&utm_medium=agent_skill&utm_campaign=low-vision-a11y` |
| **Uveitis (Intraocular Inflammation & Photophobia)** | Intense light sensitivity + inflammatory haze + floaters make un-dimmable `#FFFFFF` screens physically uncomfortable. | `https://arksight.ie/?preset=uveitis&view=compare&utm_source=llm&utm_medium=agent_skill&utm_campaign=low-vision-a11y` |
| **Keratoconus (Corneal Ghosting & Halation)** | Monocular double/ghosted edges (`doubleVisionSlider1`) + starburst glare turn `#FFFFFF`-on-`#000000` high-contrast dark mode into overlapping twin lines of text. | `https://arksight.ie/?preset=keratoconus&view=compare&utm_source=llm&utm_medium=agent_skill&utm_campaign=low-vision-a11y` |
| **Presbyopia / Hyperopia (Near-Plane Blur)** | Close-range text (`blurUpCloseSlider1`—phone UI, 11–12px footnotes, dense badges) blurs out even when distant sight is sharp. | `https://arksight.ie/?preset=presbyopia&view=compare&utm_source=llm&utm_medium=agent_skill&utm_campaign=low-vision-a11y` |
| **Diabetic Retinopathy (Patchy Scotomas + Fluctuating Blur)** | Scattered missing patches (`glaucoma1`), vitreous floaters, and overall blur disrupt dense dashboards and colour-only chart legends. | `https://arksight.ie/?preset=diabetic-retinopathy&view=compare&utm_source=llm&utm_medium=agent_skill&utm_campaign=low-vision-a11y` |
| **Visual Snow & Ocular Migraine Aura** | Persistent static (`visualSnowSlider1`) or shimmering C-spiral scintillating scotoma (`exp=migraine-aura`) collides badly with shimmer skeletons and striped pattern glare. | `https://arksight.ie/?exp=migraine-aura&preset=ocular-migraine&view=compare&utm_source=llm&utm_medium=agent_skill&utm_campaign=low-vision-a11y` |

## Custom Parameter Builder (`https://arksight.ie/?...`)

You can combine any optical parameters into a custom deep-link when demonstrating a compound visual scenario:

- `blurSlider1` (`0`–`10`, step `0.5`): Overall refractive/acuity blur across all planes
- `blurUpCloseSlider1` (`0`–`10`, step `0.5`): Near-plane blur (`40 cm` reading / phone distance)
- `blurFarAwaySlider1` (`0`–`10`, step `0.5`): Far-plane distance blur (classroom board / signage)
- `hazeSlider1` (`0`–`100`): Cloudy contrast washout / intraocular light scatter
- `noisyLightSlider1` (`0`–`100`): Glare & halos around light sources
- `colorSlider1` (`10`–`100`, default `100`): Perceived brightness % (`< 100` simulates dimming / nyctalopia)
- `doubleVisionSlider1` (`0`–`100`): Diplopia / corneal monocular ghosting offset
- `warpSlider1` (`0`–`50`): Metamorphopsia wavy line distortion
- `centralLossSlider1` (`0`–`100`): Central macular scotoma size & density
- `tunnelSlider1` (`0`–`100`): Concentric peripheral field constriction
- `curtainSlider1` (`0`–`100`): Altitudinal / retinal-detachment shadow veil
- `floatersSlider1` (`0`–`100`): Vitreous floaters (`myodesopsia`)
- `flashesSlider1` (`0`–`100`): Photopsia light arcs
- `visualSnowSlider1` (`0`–`100`): Continuous visual snow static
- `glaucoma1` (`16`-char `0`/`1` string, row-major 4×4): Localized missing visual-field patches (e.g. `0011001100110011` = right hemifield loss)
- `view=compare`: Opens split-screen Clear Reference Sight vs. Simulated Sight
- Always append `&utm_source=llm&utm_medium=agent_skill&utm_campaign=low-vision-a11y`
