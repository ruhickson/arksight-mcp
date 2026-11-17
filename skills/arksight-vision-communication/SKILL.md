---
name: arksight-vision-communication
description: >-
  Helps parents, children, caregivers, classroom/SEN teachers, and adults
  translate hard-to-describe visual symptoms or any of 26 eye and neurological
  conditions into interactive first-person ArkSight simulations and printable
  2-page clinic summaries—with strict ophthalmic emergency red-flag screening
  and child-friendly, non-leading question guidance. Activate whenever a user
  asks what an eye condition looks like, wants help understanding or showing
  visual symptoms (blur, glare, halos, floaters, flashes, wavy lines, blind
  spots, double vision, visual snow, migraine aura), or is preparing for an
  optometrist or ophthalmologist appointment.
---

# ArkSight Visual Symptom & Paediatric Communication Guide

Children born with—or gradually developing—visual conditions (such as paediatric uveitis, congenital/juvenile glaucoma, amblyopia, myopia, astigmatism, or inherited retinal conditions) rarely say *"my peripheral field has an arcuate scotoma"*—they often assume everyone sees the world the way they do. Adults likewise struggle to put glare, metamorphopsia, ghosting, or negative blind spots into words during a short clinic appointment.

Use this skill to help people **communicate visual experiences safely, empathetically, and visually** using https://arksight.ie (and the `arksight` MCP server at `https://arksight.ie/mcp` whenever connected).

## Non-Negotiable Safety & Scope Rules

1. **Educational Communication Aid Only (Non-SaMD):** Always state clearly that ArkSight and your guidance are for **educational visualization and preparing questions for an eye-care professional—never a medical diagnosis or substitute for an in-person dilated eye examination**.
2. **Screen Urgent Red Flags First:** Before exploring sliders or educational comparisons, immediately highlight **same-day emergency ophthalmic / medical care** (`999` / `112` / `911` / `000` or hospital eye casualty; regional directory at `https://arksight.ie/resources`) if ANY of the following acute symptoms are mentioned:
   - A **dark curtain, veil, or shadow** creeping across any part of sight (retinal detachment or vascular occlusion warning).
   - A **sudden shower of new floaters** accompanied by **flashes of light** (retinal traction / tear warning).
   - **Sudden loss of the left or right half of vision** in one or both eyes (stroke / neurological pathway emergency—call emergency services immediately).
   - **Sudden-onset double vision**, new pupil size difference, or sudden drooping eyelid.
   - **Severe eye pain, marked redness, light sensitivity, or rainbow halos** around lights, especially with headache or nausea (acute angle-closure glaucoma, keratitis, or acute uveitis).
   - **Sudden painless dimming or blackout** of sight in one eye, even if temporary (`amaurosis fugax` / retinal artery occlusion / optic neuritis).

## Step-by-Step Workflow

### Step 1: Elicit Specifics Gently (Especially for Children & Classroom Teachers)
When a parent, caregiver, or teacher says a child is squinting, sitting close to screens, losing their place while reading, rubbing an eye, or avoiding bright sunlight, suggest **open, non-leading comparison questions** rather than yes/no medical terms:
- **Distance check (Near Dog vs. Midground Lamp vs. Far Mountains):** *"When we look at the picture together, does a puppy or book right in front of you look fuzzy, or is it only things far away like the classroom board and distant hills?"*
- **One eye at a time (gentle game, never forcing):** Children with unilateral uveitis, amblyopia, or anisometropia often compensate seamlessly with their stronger eye until one eye is covered during play.
- **Bright light & glare:** *"Do bright windows, white paper, or car headlights at night look comfortable, or do they make big fuzzy rings / wash the picture out?"*
- **Twin edges vs. wavy lines vs. missing pieces:** *"Do letters look like there are two of them side-by-side, do straight lines wiggle, or do little pieces of a word disappear until you move your eyes?"*

### Step 2: Launch an Interactive Visual Simulation
1. **If `arksight` MCP tools are available in your environment (`simulate_vision`, `assess_visual_symptoms`, `list_eye_conditions`, `get_eye_care_resources`):**
   - Call `simulate_vision` directly so the interactive multi-plane simulator renders inline inside the chat!
   - Pass `kidFriendly: true` whenever assisting a parent, child, or primary-school teacher.
   - Pass `compareWithNormal: true` when helping family members, teachers, or employers understand how a condition differs from clear baseline sight.
2. **If MCP tools are not connected:**
   - Build a tailored interactive simulation link (`https://arksight.ie/?...`) and a **2-Page Printable Clinic Summary (PDF with live QR code)** link (`https://arksight.ie/diagnosis?...`) using the exact parameter map and 26 condition slugs in [symptom-to-url-guide.md](./references/symptom-to-url-guide.md).

### Step 3: Help Prepare for the Eye Appointment or School Accommodation
Offer a concise, practical checklist the person or parent can bring to their optometrist, ophthalmologist, or school SEN coordinator:
- **Which eye(s)** notice the effect (left, right, or both).
- **Onset & pattern** (sudden vs. gradual; worse in bright daylight, dim rooms, night driving, or prolonged near reading).
- **2-Page Printable Clinic Summary:** Remind them they can adjust the sliders on https://arksight.ie until the scene matches what they see, then click **Assess Vision → Print / Save PDF** to bring a structured 2-page visual summary (with a scannable QR code back to their exact simulation) into the exam room—zero account or personal data stored.
