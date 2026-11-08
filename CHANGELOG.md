# What's new in FoundaTrix Studio

Every release of FoundaTrix Studio in the Microsoft Store, newest first. The same notes are on the website at
https://www.foundatrix.com/whats-new/, which is the authoritative copy; this file mirrors it for readers of this repository.

## Version 1.168 (November 7, 2026)

Footing loads read from a StruTrix Studio structure, a view that turns about your model, and the User's Manual rearranged.

### New

- **File > Import > From StruTrix Studio** (Premium) — a StruTrix Studio structure saved in this model's cloud job gives the model its loads: its supports' reactions, read by load case or as its strength and allowable stress combinations, placing a footing at each support or loading the pedestals there. Its latest saved version is taken before every run. It needs your own StruTrix Studio subscription or trial as well. [How it works](https://www.foundatrix.com/#structure-link)

### Improved

- With nothing selected, the view turns about the centre of the model, and a pan holds the point you pressed on under the cursor.
- The User's Manual is rearranged in seventeen sections, with an engineering notice, getting started, a section on verification, and a tutorial with pictures of the program.

In the Microsoft Store as version 1.1.68.0.

## Version 1.161 (November 1, 2026)

The calculation report free for everyone, a new ribbon, and dimensions in feet and inches.

### New

- **The calculation report, free for everyone** — with no account needed. Your firm's name, logo and the line under it on the report remain a premium feature. A foundation on piles is still reported with both programs' subscriptions.
- **Member Detail** (Premium) — every steel check of a stand or rack member worked equation by equation, in a window and as a PDF, from the Steel pane.

### Improved

- **A new ribbon**: Model, Modify, Drafting, Loads, Analysis, Results, Design, Tables and View, with Move and Copy by an increment, Rotate Copy, the drafting grid and object snaps as buttons, and Select by Criteria. Theme and Units are on the Home tab; the Work Plane and Visibility groups are on the Model tab as well.
- Dimensions lie in the plane of the edge they measure and read in feet and inches to the fraction you choose in Settings; a distance typed on the command line takes feet and inches.
- The opacity and colour of hidden objects are in Settings > Model View; at 0% a hidden object is not drawn.
- Pile models are copied from PileTrix Studio, the new name of PileAxis.

In the Microsoft Store as version 1.1.61.0.

## Version 1.147 (October 20, 2026)

Your AI assistant runs what-if analyses on your computer, and only you apply what it proposes.

### New

- **What-if analyses on your computer** — turn it on in the account menu, and an AI assistant connected to your cloud can read a footing of the open model, run it and up to eight changed versions with this program's own analysis and design on copies of your model, and propose one to you. Only you can apply a proposal, from the new Assistant Requests pane, and one Ctrl+Z takes it back. [See how](https://www.foundatrix.com/#assistant)
- An assistant can also create a footing as you would draw it, with its pedestals, anchor rods, loads, a strap and its partner, or piles.

### Improved

- The Loads menu draws the loads of one load case at a time; Wizard Loads draws a wizard's load sets.

In the Microsoft Store as version 1.1.47.0.

## Version 1.144 (October 18, 2026)

A footing's loads from service loads or from your own combinations, the Combinations pane, and exact picking in every view.

### New

- **Loads from** — a footing takes its loads either from service loads, which the program combines by ASCE 7-22, or from your supplied combinations, which it analyses as they are, never both. The model check tells you when loads are kept but not read.
- **The Combinations pane** beside the Loads pane, and each combination can be included or excluded.
- **Your account menu** — click your avatar for who is signed in, Messages and Sign Out. A red dot means you have unread messages from RamisoftSolutions, such as release notes and service notices.
- An AI assistant connected to your cloud projects can now search every project and model you can open in both programs.

### Improved

- A supplied combination now states only its dead and live factors, the two the program applies to the footing's own weight, the soil over it and the surcharge.
- The Loads pane is now a sheet like the Tables: paste, formulas, sort and filter.
- Picking is exact in every view, small parts and turned views included, and a window selection takes only what is in front of the camera.

In the Microsoft Store as version 1.1.44.0.

## Version 1.130 (October 15, 2026)

Foundations on piles, with PileTrix Studio, and Run All.

### New

- **Pile-supported foundations** (Premium) — a footing can now stand on piles. Copy pile models from the PileTrix Studio (then PileAxis) analyses in the same cloud job, place piles one at a time, as rows and columns or a ring, or in a table, and analyse the rigid cap on its piles under every load combination. Each pile is checked for compression, uplift, lateral soil resistance and section strength, with the results drawn on the model and printed in the report. It needs an active subscription or trial to PileTrix Studio as well as to FoundaTrix Studio. The cap's concrete is not designed in this version. [See it](https://www.foundatrix.com/#piles)
- **Run All** analyses and designs every footing at once.
- **Equipment on no pedestals** (Premium) — a substation unit's or a pipe support's base plates can bear directly on the footing.

### Improved

- Choose one load combination on the Results tab to show the bearing pressure on every footing.
- Help on hover waits for the pointer to rest, and its timing is in Settings.
- Results are marked out of date whenever the model changes, whatever changed it.
- Each program now has its own trial, starting the first time you sign in to it.
- An updated Revit add-in (1.0.1).
- Includes the October 2026.NET security update.

In the Microsoft Store as version 1.1.30.0.

## Version 1.121 (October 11, 2026)

The first release in the Microsoft Store.

### In this release

- **Rigid foundations of any type and shape**: spread, combined, strapped and mat foundations on any outline, carrying any number of pedestals, under columns, vertical and horizontal vessels, heat exchangers, substation equipment and pipe supports.
- **The whole site in 3D**, drawn with drafting precision (coordinates, object snaps, set-out grid lines, and move, copy, rotate, array, mirror and measure, each a single undo step), or typed into spreadsheet-style tables that stay in step with the model.
- **Bearing pressure solved exactly** under a rigid base, a partly lifted base included, with overturning and sliding, on the ASCE 7-22 combinations, strength and allowable stress, seismic included.
- **Concrete design to ACI 318-19**: one-way shear and flexure from a swept envelope, four mats sized and the bars picked, two-way shear, pedestal interaction on a full biaxial strength surface, strap footings, and cast-in anchor rods to Chapter 17.
- **Wizards** for vertical vessels, horizontal vessels and heat exchangers, substation equipment and pipe supports, each decision recorded with the clause behind it (Premium)
- **Steel stands and racks to AISC 360-22**, analysed as 3D frames by the direct analysis method, members by LRFD, base plates to AISC Design Guide 1 (Premium)
- **The typeset calculation report**, every derivation printed symbolically and with your numbers substituted, then a premium feature and free for everyone since version 1.161
- **Export to IFC 4.3 and to Revit** as native elements through the included Ramisoft Revit add-in (Premium)
- **Cloud projects** with version history, a recycle bin and organization sharing, free with sign-in, and a connector for your AI assistant.
- Imperial and metric units, light and dark themes, undo and redo that reach back past a save, and the complete User's Manual inside the program.

In the Microsoft Store as version 1.1.21.0.
