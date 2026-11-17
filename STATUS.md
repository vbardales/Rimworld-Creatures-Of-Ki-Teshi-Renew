---
localization: complete
translation_en: complete
translation_fr: complete  # 2026-11-12 owner validated the review-translation answers (her word, twice: no recommendation, then three PUBLICATION points applied); review line of TRANSLATION_REVIEW.md filled with her word
settings_audit: not_applicable
workflow_stage: publish[1.2.0]
tested_1_7:   yes  # 2026-10-13, ticket e8c8, feature 01-loads only (1 passed, 0 failed), RimWorld 1.7.4976 rev1043, English, map sans-facultatifs, on 971ac7c; <li>1.7</li> declared on the owner's word 2026-10-13
mod:          Creatures of Ki: Teshi Renew
packageId:    nelim.creaturesofki.teshi  # renamed 2026-11-12 on the owner word (was nelim.creaturesofki, published 1.1.0); players must re-enable the mod
repo:         Rimworld-Creatures-Of-Ki-Teshi-Renew
remote:       https://github.com/vbardales/Rimworld-Creatures-Of-Ki-Teshi-Renew.git
local_path:   C:\Users\nelim\Documents\rimworld\CreaturesOfKiRenew
visibility:   public
detached:     yes
licence:      open
licence_spdx: MIT
licence_github_detection: Other (NOASSERTION)
licence_at:   LICENSE and Mod/LICENSE, copyright 2020 Mlie
upstream_mod_remotes:
  - https://github.com/emipa606/CreaturesOfKi
upstream_synced: 2026-11-13 emipa606/CreaturesOfKi@52b8f28  # archived read-only, HEAD = tag 1.4.3, nothing newer; our 1.6 port is by hand (branch teshi-1.6-support)
upstream_pr:  attempted 2026-09-28, refused (repository archived, read-only). Branch kept on vbardales/CreaturesOfKi teshi-1.6-support
dependencies: none
showcase:     complete
tested_on:     2026-11-14 pickle 4c49d1d, English and French labels, ADS2, Nocturnal, new colony, 10 passed of 10 (Docs/runs/2026-11-14.md); the full suite of 2026-09-26 and 2026-10-02 on 1fcc51f/49d9a72 stands; published 2026-10-02 at 49d9a726f64e5d491fb7
workshop:     3806709627
version:      1.1.0 (tag v1.1.0 and GitHub release by CI run 38475087868; 1.0.1 was tag v1.0.1)
target_version: 1.2.0 (packageId rename 2026-11-12; was 1.1.0 minor bump, 2026-10-13: RimWorld 1.7 pass; `<li>1.7</li>` declared, tested on load only: 01-loads, English, 1.7.4976)
maintainer:   Claude Code, the session named in session, which holds this standalone repository
session:      local_3b2dce0c-52e6-49cb-a662-cefbbbd56580
updated:      2026-11-17, stage publish[1.2.0] (12.h): dry-run 44072491299 green on 4feab2a, publish dispatched next, Virginie approves on steam-production
remaining:
  - 2026-11-17 13.a: publish run 44073923357 dispatched on 4feab2a257d7e6723d6ad396f7146eab2fca793c, version 1.2.0, options preview, description, title (same as the dry-run 44072491299). Waits for Virginie on steam-production (https://github.com/vbardales/Rimworld-Creatures-Of-Ki-Teshi-Renew/actions/runs/44073923357). After success: check the tag v1.2.0 and release, the public page (description, note, title, Preview), PublishedFileId.txt unchanged (3806709627), SUBSCRIBE-TEST? to PiI, tell Audit the old packageId is retired, gallery images by hand.
  - 2026-11-17 12.c bis DONE: caveman-compress on TESTING.md, BACKLOG.md, Docs/GALLERY-V2.md (backticks, URLs, shas, versions diffed against the backups: nothing lost). Failed after retries: Docs/PROTOCOLS-READ.md, Tests/Pickle/README.md (left as is). Not compressed on purpose: STATUS.md (status part), Docs/PROMPT_*.md (image prompt), review-names.md and review-refusals.md (sent to ChatGPT).
  - 2026-11-17 11.j DONE: Virginie "je valide la relecture" (her word, chat) on PUBLICATION.md and CHANGELOG.md for the 1.2 line, publication_changelog_review_sha set to 3175873. 11.k DONE: 9a gameplay steps = Tests/Pickle/Source/TeshiSteps.cs (spawn, tame, lay, hatch, lie down), 9b n/a (the mod adds an animal, no prop or apparel for other galleries; GALLERY-PROPS.md only lists Teshi Renew as a user). Open: 12.a to 12.h (12.c bis caveman compress of Docs, 12.e dry-run date and CI are the next gestures, publish stays the owner call).
  - 2026-11-17 replay-audit (ledger .replays/CreaturesOfKiTeshiRenew-20261117.tsv, 103 rows: 91 done, 4 weak, 1 open, 1 ?, 10 n/a): first open 11.j [owner]: Virginie rereads PUBLICATION.md (1.2.0 block, Steam description) and CHANGELOG.md Unreleased, then publication_changelog_review_sha (line x.y moved 1.1 to 1.2). 11.k waits on it. Flags: 9.0 bis plan was scored 4 to 5 under the 2026-10-18 threshold, not 5 on every scene (rule of 2026-11-16 not retro-applied, gallery accepted 2026-11-13); ecosystem report lacks the ecosystem-links block (PiI); Check-ModBasics wants a [url] tail on the About description while sync-about-description.mjs writes plain text (Audit).
  - 2026-11-16 review-translation page 1 DONE (fourth answer): applied 1 (CHANGELOG Unreleased first bullet: dropped "packageId unchanged", contradicted by the next bullet), refused 0. No proper noun. Check-Translations PASS, TRANSLATION_REVIEW.md regenerated. No french_review_pending line, no yellow pastille.
  - 2026-11-15 review-translation page 1 DONE (third answer): applied 1 (PUBLICATION.md line 6: next upload 1.2.0, was 1.1.1), refused 0. No proper noun. Check-Translations PASS, TRANSLATION_REVIEW.md regenerated. No french_review_pending line, no yellow pastille.
  - 2026-11-15 review-translation page 1 DONE (second answer): applied 1 (PUBLICATION.md header: 1.2.0 is in preparation, was 1.1.1), refused 0. No proper noun to decide. Check-Translations PASS, TRANSLATION_REVIEW.md regenerated. No french_review_pending line, no yellow pastille.
  - ticket f5d5 DONE green, image 6 judged 4 (Shotlist table). Was: (image 6, `-EvidenceDir Tests/Pickle/Inbox/gallery-v3-6b`, tree on c4756e1+, lis without pot after run 551e failed "cell already holds PlantPot"). At RUN_DONE: read `summary.json` `total` first (queue showed tests=36 for a 1-scenario filter: if 36, filter did not hold, refile narrower), open the screenshot, judge it against 4, put verdict in the Shotlist table; then write the other six scenarios in 13-workshop-captures-v3.feature one ticket each, results into Inbox/, minify green proofs to Evidence/ with RELEASE.md.
  - evidence: migrated again through Inbox 2026-10-20, Prune-Evidence -Apply; Evidence/ holds 7 minified green folders, 1.4 MB total, each with RELEASE.md; Inbox/ empty; Parked/ none; none of the 9 pickle-reports-archive folders is this mod's (checked junit/Player.log); no report folder in Tests/ or docs/runs/ (lines only).
  - shootGallery[1.1.1]: shotlist reworked 2026-10-25 and scored 4/5 (13-workshop-captures-v3.feature header, tables in "Shotlist" below; Opus director pass done; rate-gallery of the old plan gave 3.3). Scenarios of images 1 to 6 rewritten from the header (2026-10-25, `Check-Steps.ps1`: every step line resolves, uncommitted). Next: file one ticket each on wsl-deps.sanctuary.map (filters `13-workshop-captures-v3::<title start>`: `16h00,`, `16h30,`, `17h00,`, `17h30,`, `18h00,`, `18h30,`), then read each capture against its line.
  - 1.1.0 published (Steam 2026-10-13 22:07 UTC, tag v1.1.0, tags Mod 1.6 1.7). `tested_1_7: yes` = load only, English (ticket e8c8); not played on 1.7: laying, hatching, ADS2, Nocturnal, galleries, French.
  - for dormant: 14.c WSL Workshop mods downloaded by this mod's sessions (list first, owner approves), then `Check-Status.ps1` (crashes on `Get-FileHash`, shared script, for the Audit workflow session).
  - disclosed gaps against AUDIT.md (loop-declared stages, dispatch before lint, 1.7 declared before a green run, no `TEST_SCENARIOS.md`): in docs/runs/status-history.md, "AUDIT.md read in full, 2026-10-15".
  - unverified: gallery images on the Steam page and the thanks comment were posted by the owner (her word); no session read the page.
  - 2026-11-17 12.e DONE: CHANGELOG dated [1.2.0] - 2026-11-17 (4feab2a), dry-run run 44072491299 (https://github.com/vbardales/Rimworld-Creatures-Of-Ki-Teshi-Renew/actions/runs/44072491299) green on 4feab2a257d7e6723d6ad396f7146eab2fca793c, version 1.2.0, options update_preview, update_description, update_title (no tags). 12.f log READ: "Publishing 4feab2a... as version 1.2.0", change note = real BBCode list with changelog url, version above v1.1.0, no build project (Mod/ ships as is), About.xml description = PUBLICATION.md plain text, preview 759045 bytes sha 9e8c7286 (page now 661812 bytes, will be replaced), description 7311 chars with three diffs vs page (fixed "four fifths of a playable race", AI-GENERATED paragraph now DALL-E and in-game captures, Source code link now the Teshi Renew repo), title page "Creatures of Ki - Teshi Renew" becomes "Creatures of Ki: Teshi Renew", tags not sent, DRY RUN: nothing was sent to Steam. Open: 12.g reminder, 12.h (publish[1.2.0] stage), then publish dispatch and Virginie approval on steam-production (13.a).
social_preview_sha256: 9e8c728656fd88ebc0a175f86b04a1c5144e8b3a8e5d9c86dd0662d75f624a52
publication_changelog_review_sha: 317587366da9de84b12b41b51ae97f8d21f0a3ec
echo_review_sha: 0c18456c4538b37b29de392a33e5d4aed2c69f4d
code_review_sha: 4c49d1df5e0b018bc37cdb7d0c9864ed12b4397a
protocols_read_sha: 3e1f8dff18f7e4658931e5ad0ff66f0bc8eed6bb
---
# Creatures of Ki - Teshi Renew — status

## Dated sections (folded)

Full text in `docs/runs/status-history.md`, section "Folded from STATUS.md, 2026-10-15". One line each:

- Audit, 2026-10-10 (HEAD `e6e9b50`, working tree clean before this edit)
- Audit completed, 2026-10-11 (HEAD `4df312a`, read and offline checks only, no game)
- Gallery, second series, 2026-10-11 (HEAD `e358d09`)
- Docs, 2026-10-11 (`writeDocs[1.0.1]`, 11.a to 11.i)
- Published 1.0.1, 2026-10-11
- Dry-run 1.0.1, 2026-10-11
- Owner's reread, 2026-10-11 (11.j)
- Echo and Preview, 2026-10-11 (10.a, 10.d)
- Gallery table, 2026-10-11, accepted by the owner (her word, the six files, `candidate` dropped)
- Pickle runs of `playTests[1.0.1]`, 2026-10-11 (label `04c2119`)
- Code review, 2026-10-11 (8.m), `code_review_sha` bfd5a4567e4f032eed65215c74265f35feaddb69
- Code review, 2026-10-11 (second reading, 12.a)
- Translation audit, 2026-10-10 (revision `34d2dd0`)
- Tests written and rerun, 2026-10-10 (HEAD `aa6070c`, offline, no game)
- Dependencies, 2026-10-10 (HEAD `e6e9b50`, read in the sources, no game)
- Settings audit, 2026-10-10 (HEAD `a227b39`, sources read, no game)
- Warnings closed, 2026-10-13
- Chain 1.1.0, 2026-10-13 (`code` to `playTests`, offline, no game; HEAD before this edit `d2604fe`)
- 1.7 diagnostic filed, 2026-10-13
- 1.7 diagnostic result, 2026-10-13
- Social preview, 2026-10-13 (10.f, owner's go)
- Chain 1.1.0 continued, 2026-10-13
- Owner's reread, 2026-10-13 (11.j, 1.1.0)
- Echo, 2026-10-14 (second reading)
- Dry-run 1.1.0, 2026-10-14
- Publish 1.1.0 launched, 2026-10-14
- Review shas, 2026-10-14
- Published 1.1.0, 2026-10-14
- Tag 1.7, 2026-10-14
- Tag 1.7 applied, 2026-10-14
- Non-regression filed, 2026-10-14 (`followUp`, 14.a)
- Non-regression result, 2026-10-15
- AUDIT.md read in full, 2026-10-15
- Non-regression 1.1.0 complete, 2026-10-15
- Use This Instead posted, 2026-10-15

## Shotlist, 2026-10-25 (gallery reopened, `shootGallery[1.1.1]`, AUDIT 9.0, reworked against GALLERY.md of 2026-10-23 and 2026-10-25)

Full lines in the header of `Tests/Pickle/Mod/Pickle/Features/13-workshop-captures-v3.feature`. Scenarios of that file rewritten from it the same day (steps checked, not played). Nothing of this rework is played. Opus director pass done (kept and refused points in the feature header). Published gallery unchanged; new images stay candidates until the owner agrees.

**Story.** One evening on the 4th of September 5500 (the fixture day, permanent summer), Clear all evening, start 16h then +30 game minutes per image (cumulative waits 60, 1310, 2560, 3810, 5060, 6310 ticks; image 7 at 19h30, 8810). Nelim, the protagonist, comes down to the pond to watch a sleeping teshi and stays through the dusk: the waking, the courting, the straw she carries to the nest, the egg, the hatching, the first meal. She always moves or faces East (pond x about 156, nest x about 213). One outfit all evening: sage CollarShirt (126, 150, 118), dark brown Pants (70, 56, 44), Bob (62, 44, 32), brown eyes, MouthSmile and LidCheerful. In image 7 (published) she wears a clean white shirt: she changed to tend the injured teshi. Lit lantern from image 3 (dusk marker).

| # | Place, hour, frame | Subject, instant, how obtained |
|---|---|---|
| 1 | water-garden west bank, 16h00, MEDIUM-WIDE root 2.8 centre (157, 173) | mother asleep on the bed (156, 172); Nelim starts (154, 174), forced walk to (157, 174), 30 ticks pass (about 2.5 cells), pause; no smile required (written: wide opener, face under 40 px) |
| 2 | same bank, 16h30, TIGHT root 2.4 centre (157, 172) | the mother awake on her bed, head up, face to the camera; Nelim whole at the left (154, 171), waits in place (120 dress-up ticks), then the mother is placed, smile held, no walk | **v26 (2026-11-08)**: decor dense, lit DR_StickLantern (160, 171), Plant_Daylily (159, 171), (159, 173), (160, 173), Stool (153, 172), PlantPot_Bonsai (153, 170), YellowTallGrass band (153 to 158, 174).
| 3 | same bank, 17h00, MEDIUM root 3.3 centre (158, 173) | the pair nose to nose, hearts (mate step); Nelim stopped on the bank at (153, 174) facing East, waits in place 120 ticks, watches, smile held; no hay (the straw goes to image 4) |
| 4 | calm-zone, 17h30, MEDIUM-CLOSE root 3.2 centre (213, 185) | mother on the bed (215, 185), egg in its box; Nelim has carried the straw from the bank and reaches the nest, next she lays it by the bed; she carries 1 Hay, stands at (208, 185) facing East, forced to walk to (212, 185), pause after about 35 ticks (mid-stride) | **v26**: grass row (213 to 218, 187), Plant_Daylily (209, 188), (210, 188), (219, 183), (219, 187), TorchLamp lit (209, 183).
| 5 | calm-zone, 18h00, TIGHT root 2.4 centre (215, 185) | hatch by the game, Nelim waits in place at (212, 185) 10 ticks, THEN mother (215, 185) and kit (217, 184) facing West placed, nothing ticks after, BrowRaised, smile held |
| 6 | calm-zone west of the nest, 18h30, MEDIUM root 2.8 centre (210, 185) | Nelim holds out the meal and the kit steps up, the mother watches (closing story image); as run f5d5 (stand, carry Meat_Chicken, kit one cell away), only the shirt and the root change | **v26**: centre (211, 185), grass band (210 to 214, 186 to 187), empty nest bed (215, 185) and EggBox (217, 185), Brazier lit (206, 186), Stool (207, 187).
| 7 | hut, 19h30, Health tab | published image, interface, set aside |

**Criteria, cell by cell** (a time, b decor, c living, d pawns, e action, f composition, g subject, j mod in thumbnail; k on the series below).

| # | a | b | c | d | e | f | g | j | Est. | Main risk and plan |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | 16h00, Clear, 60 ticks | GSAnimalBedBigPrestige (156, 172), Plant_Daylily (153, 175) | asleep mother, daylily, lily pads | sage shirt, Highpony, no smile written (wide, face under 40 px) | mid-stride walk, 30 ticks | medium-wide root 2.8, Nelim whole at the left | the sleeper is watched | mother about 55 px at 268 px, accepted for the opener | 4.5 | mother reads as a pale shape (j weak); geyser at the edge, frame x 152.0 to 162.0 |
| 2 | 16h30, 1310 ticks | bed (156, 172) behind, Plant_Daylily (159, 171) | mother awake face to the camera, daylily | Nelim whole at the left, sage shirt, smile held | she lifts her head toward Nelim | tight root 2.4, mother off-centre | she has just woken | fills the frame | 4.5 | mother sits upright and reads as posed (e weak) |
| 3 | 17h00, 2560 ticks | empty bed (156, 172), DR_StickLantern lit (161, 171), Plant_Daylily (153, 171), (153, 170) | pair, daylilies | sage shirt, Highpony, smile held, profile | watches the pair, waits in place (the pair mating is the action) | medium root 3.3, pair centre | the courting | hearts and pair read | 5 | Nelim small and in profile at 268 px |
| 4 | 17h30, 3810 ticks | EggBox (217, 185), GSAnimalBedBigPrestige (215, 185), Plant_YellowTallGrass 3 x 5 minus (216, 185), lantern lit (213, 186) | mother front view, egg | sage shirt, Bob, smile | mid-stride with Hay (above) | medium-close, Nelim west of the grass at row 185 | she builds the nest, Nelim helps | mother and egg fill the right half | 4 | hay covered her face last run: pause mid-stride (35 ticks), not at pick-up; plan B Meat_Chicken |
| 5 | 18h00, 5060 ticks | same nest minus grass (216, 184), (217, 184), daylilies (213, 184), (213, 185), lantern lit | kit (facing West) and mother front view | sage shirt, Highpony, BrowRaised, smile held, waits at (212, 185) | watches the kit | tight root 2.4, kit below the box on bare soil | it is born at dusk | kit about 25 px at 268 px (j weak) | 4.5 | kit small and pale on soil; facing West step not played on a kit |
| 6 | 18h30, 6310 ticks | lantern lit (213, 186), Plant_Daylily (209, 183), (211, 183), bare corner | kit, mother, daylilies | sage shirt, Bob, smile | holds out the meal (above) | medium, Nelim left, kit centre, mother right | the first meal, the teshi lives with people | subjects fill the frame | 4.5 | none new: accepted at 4 in run f5d5 |

**k, series.** One story written once at the top of the feature header (who, where, day, rhythm); scenes move from the pond to the nest, East to the nest; variety wide (1), tight (2, 5), medium (3, 4, 6); opening image sets the place (1), closing image is 6 with 7 as the night epilogue; teshi seen from the front in 2, 4, 5, 6.

**Series score 4 of 5.** Weak points: image 1 thumbnail (wide opener), image 2 relies on a named spawn whose sex cannot be fixed (plan B written), steps never combined (forced walk plus carry plus follow). Previous run, verdicts on the 2026-10-18 plan: image 3 at 3.5 (Nelim seen from behind), 4 at 3 (hay over her face), 5 at 2 (no kit in frame), 6 at 4 (run f5d5, proof `Evidence/gallery-v3-6b`); the gap with the estimate of 4 taught: write the instant, the method and the order of the steps. Images 1 and 2 never produced a report (Inbox, launcher exit -1073741205, twice on image 1).

Verdict after run: image 3 (ticket 2bff, green, total 1, Inbox/gallery-v4-3-the-parents) judged 3.5 of 5 (2026-10-27): pair nose to nose with hearts, lit lantern, bed, daylilies, strong; Nelim cut by the left edge, face under the hay, so she does not read as the protagonist. Fix idea: forced walk target one cell further East (156 or 157, 174) or camera centre shifted 1 cell West. Image 4 (ticket 2006, green, total 1, 191 s, Inbox/gallery-v4-4-nesting-box) judged 3.5 of 5 (2026-10-28): mother front view on the bed in the grass, egg in its box, lit lantern, daylilies, all strong; Nelim small at the left edge, seen from behind, face hidden by the hay, so she is not the protagonist. Same fix idea as image 3 (forced walk target further East or Nelim started closer). Image 3 replayed with Highpony (ticket f8c8, green, total 1, 163 s, 2026-10-29, Evidence/gallery-v6-3-the-parents) judged 3.5 of 5: pair nose to nose, hearts, lit lantern, bed, daylilies strong; Nelim still cut by the left edge, face under the hay, hair not readable as Highpony. Same fix idea (forced walk target further East). Images 1, 2, 5, 6 pending (9bb8 lost exit 98 and refiled 7271; 8734 red on (156, 160) not standable, fixed in 8f6b631 and refiled bd81).
Verdict v24 (2026-11-06, shotlist rows 1 and 4 as in the v24 scenarios on bd7e280; rows 2, 3, 5 as v23, row 6 as v22): image 1 4.5 (ticket 0efb), image 2 4, image 3 4, image 4 3.5 (ticket dc0f: sweat drop, red forbidden X on the hay, Nelim about 7 cells from the nest), image 5 4.5, image 6 4; mean about 4.1. Plan estimates were 4.5, 4.5, 5, 4, 4.5, 4.5 (mean 4.5): the gap comes from image 4 (sweat, forbidden icon) and the mother posed upright in 2. Row 4 of the table above is stale: in v24 Nelim lays the hay down at about (211, 186) after 45 ticks instead of carrying it mid-stride.
## NSB

Sync of 2026-11-06, run twice the same day (no NSB `Docs` commit between the two runs; the first run had no earlier section). Rules of the owner (2026-11-05): all of NSB (places, colonists, domestic animals) is free; a colonist or domestic animal outside NSB needs her express validation; a colonist's properties change only with her express validation; every outfit is free. Changes in NSB that touch this mod: (1) 2026-11-05 `water-garden` decor: all lotus removed, nothing in the water, two willows (171, 162) and (165, 162) and reeds (168, 163) on the south bank; the pink water flowers at the bottom right of the v18 image 1 capture are those lotus and will be gone on the next run; no frame of this mod reaches z 162, no scenario change. (2) `NELIM-PROFIL.md` 2026-11-05: 14-outfit wardrobe (daily is `LTS_Tunika`), canon skin `GES_Skin_Almond` (#CFAB79) and hair gene `Hair_DarkSaturatedReddish` (#382412, (56, 36, 18)) replace the figures in the feature header (skin (228, 158, 90), hair (51, 33, 16)); the scenarios override neither, so nothing played changes, only two stale header lines of `13-workshop-captures-v3.feature` (left alone: Tests/ stays on ceb0e26 until NPT answers). Left alone and why: sage `Apparel_CollarShirt` and brown `Apparel_Pants` stay (outfits are free, rule 4; sage reads against the brown soil and yellow grass, GALLERY.md criterion d); no NSB animal is used (the teshi are this mod's own creatures, not pets or livestock, so rule 2 does not apply; names "Mother", "Kit", "Teshi" are no NSB names); mouth `MouthSmile` and image 5 `BrowRaised` replace the canon `MouthLipsSmirk` and `BrowNormal`: these are expressions (APPARENCES-CANON: mouth, brows, eyes are suggestions, owner 2026-10-28; GALLERY.md "Colons qui sourient" asks for a smile), not a roster property, so no validation is asked; `LidCheerful` is the canon lid. No mod added to the DepMap (`wsl-deps.sanctuary.map`).

Third run, 2026-11-06 (15:30): NSB commits 43f0786, aa7586a, 7779c4a (docs/VALIDE.md, AVANCEMENT.md: Shogun, Soren, pediatrics validations) read as diffs only: nothing on Nelim, `water-garden`, `calm-zone` or animals this mod uses, so nothing changed here and no "last read" date moved. Fourth run, 2026-11-06 (16:37): NSB commits 42b5f66 and a92275c read as diffs (`NELIM-PROFIL.md`, `VALIDE.md`, `AVANCEMENT.md`): only wardrobe rows of Nelim changed (coder: fitted shirt `LisaWork_ApparelShirtButtoned` and skirt, horn-rimmed glasses on trial; swim: one-piece `Swimwear_Sukumizu`, waits for 1.7), hair `Roo_HD_Hair_Highpony` and body unchanged; the mod's sage `Apparel_CollarShirt` and brown pants are not in those rows (outfits are free), so nothing changed here and no "last read" date moved. Rule 5 (included animals), built from the defs (`Races_Animal_Teshi.xml`: one ThingDef and one PawnKindDef `Teshi`, life stages adult and kit): no row MISSING.

Fifth run, 2026-11-07: NSB `Docs` commits of 2026-11-06 17:00 to 2026-11-07 (f4268bc, 922a990, 31fde17, 4db5ab9, 05d6640, a92547d, c40e82f, ac34b0a and others) read as diffs only. Touching this mod: (1) `NELIM-PROFIL.md` 2026-11-07: 1.7 body hair validated (ticket 69b4); the gallery plays Nelim clothed (sage shirt, brown pants) and the pilosity is a body-hair layer under clothes, nothing changes here. (2) `EMBELLISSEMENT-LIEUX.md` third order: `calm-zone` (our images 4 to 6, nest east of the cream square) is order 20, "decor around, not inside: the inside stays free for captures"; our decor is placed by the scenario and removed after, no conflict. `water-garden` unchanged ("nothing in the water", already known). (3) `play-area` frame (100, 117) zoom 11, animal validations, Swim outfit validated: not used here. No animal or colonist outside NSB added; teshi validation of 2026-11-06 stands. No "last read" date moved. Rule 5 unchanged: no row MISSING.

| Included animal | Shots | Missing |
|---|---|---|
| teshi (adult, defName `Teshi`) | 1, 2, 3, 4, 5, 6 | no |
| teshi kit (newborn stage of the same kind) | 5, 6 | no |

Sixth run, 2026-11-08: NSB `Docs` commits 2026-11-07 to 2026-11-08 (f4268bc, 4db5ab9, b664c23, 564f12b, fdf06d7, 8aec4a1, ffd294b, 046c6a2, 0037883, c2706c5, 6d73581) read as diffs. None touches `water-garden`, `calm-zone`, the Nelim outfit rows used here, or any animal used: they validate other places (play-area, plant-garden, sofa-corner, dining-nook, sleeping-nook, workshops, rice-paddies) and Nelim body hair 1.7 (clothed in the gallery, no change). NPT `docs/steps.md` 2026-11-07 to 2026-11-08 read: `puts down what it carries` no longer says the item is forbidden only while the game runs (image 4 v25 carries nothing, unaffected); new steps (lies asleep in the bed, light lifted to at least, decor made of, growing-zone clean-ups) serve no shot of this mod today; no step of ours was renamed or removed. Nothing changed in the shotlist or scenarios. Rule 5 unchanged: no row MISSING. Idea, not applied: newly validated NSB decor places could densify image 4 decor (criterion b), a session call at the rework.

Seventh run, 2026-11-09: NSB `Docs` commits cc61d17, d8895a2, 1677380 (and run journals) read as diffs. (1) `SANCTUAIRE-LIEUX.md` and `VALIDE.md`: redecoration finished, all places validated; final decorated save `Nelims-tribe-decor-mods-z3.rws` (sha256 6bfb4a48...) copied into NSB `Mod/Pickle/Fixtures`; `Nelims-tribe.rws` stays the old Sanctuary until scenarios are repointed. `calm-zone` (images 4 to 6) validated 2026-11-07, `water-garden` unchanged. Our scenarios still use the existing sanctuary DepMap and fixture; not repointed. (2) `NSB-ROSTER.md` and `QUILL-PROFIL.md`: Quill eye globes `EyeNormal`, not used here. No Nelim, outfit or animal change. NPT `docs/steps.md` 2026-11-08 to 2026-11-09 read: new steps (Beauty2 mouth offset, carries X made of Y, point framing `I frame the area centred on the point`, drawing of a class skipped, sleeping-Z flecks not thrown, colonist does not flee) serve no shot of ours today; the point-framing step could help image 4 if a half-cell centre is wanted, a session call at the v28 rework. Idea, not applied: z3 decor fixture may give `calm-zone` denser ground around the nest (criterion b); to test with a probe ticket only if v28 stays bare. Nothing changed in shotlist or scenarios. Rule 5 unchanged: no row MISSING. No outside-NSB colonist or domestic animal, no property change, so no owner question.

Eighth run, 2026-11-12: NSB has one `Docs` commit since 2026-11-09 (18abf53, folder renamed docs to Docs, no content change): places, colonists, animals, outfits unchanged for this mod. NPT: steps and catalogues changed (StageDecor decor burns, flooring terrain, pot with a grown plant, ColonistRace filth removal and culture steps, DefFieldSteps thought text, ScreenshotStudio step hiding the main tab bar, the speed controls and the mouse-over readout while the windows stay, docs/steps.md moved to Docs). Nothing here replaces a hand-made setup of a played scenario. One option, not applied (image 7 is under Virginie's review): the ScreenshotStudio hiding step would clear the bottom tab bar, the speed controls and the readout from image 7 (health tab). Rules 1 to 5 of the owner restated; no colonist or domestic animal outside NSB, no colonist property changed, all outfits free. Included animals (Teshi, kit): both shown, none MISSING.Places then read 2026-11-12 (nothing changed, calm-zone and water-garden as on 2026-11-09). Tribe then read 2026-11-12 (nothing changed for this mod). steps then read 2026-11-13 (PickleTools docs/steps.md log since 2026-11-09).

Ninth run, 2026-11-13 (gallery accepted, stage mountPreview, no shot rewritten): NSB not reread (no nsb-sync warning). NPT `Docs/steps.md` since 2026-11-12: 13 insertions, 0 steps removed or renamed (ScreenshotStudio animals kept out with 4 to 6 exceptions, ColonistRace render nodes hidden, fast-forward step on the main thread, assertion colonist at a building, StageDecor growing-zone guard and building blueprint, garment dye on animals). Nothing a played scenario of this mod calls changed; nothing replaces a hand-made setup. Included animals (teshi, teshi kit) both shown, no MISSING. Rules 1 to 5 of the owner (2026-11-05): everything in NSB free; colonist or domestic animal outside NSB needs her express validation (none used: only Nelim and the mod's own teshi); colonist properties changed only with her validation (none changed); every outfit free; every included animal in the gallery. Tenth run, 2026-11-14: NPT since 2026-11-13, two commits (c38417c render node hide uses the debugEnabled flag; a9965f8 SloppyMods Entertaining Ideas catalogue, 5 building shots): no step removed or renamed, nothing a scenario of this mod calls, nothing replaces a hand-made setup; NSB: 0 Docs commits since 2026-11-12, nothing changed for this mod (re-checked on owner request, no reread needed). Included animals (teshi, teshi kit) both shown, no MISSING; rules 1 to 5 stand, no colonist or domestic animal outside NSB, no property changed. Steps then read 2026-11-14.

Eleventh run, 2026-11-17 (stage writeReleaseDocs, nothing rewritten): NSB `Docs` commits since 2026-11-12 (503b567, c5416c1, 957fe55, a9a0ef8, a9ab64b, 9a74c75, c82e8b2, a0172bb, 7ad4957, 0847888) read as diffs: Miel lipstick, neutral colonists head investigation, Soren/Ada/Lyra validations, VTW body types, Quill head probe. Nothing on Nelim, `water-garden`, `calm-zone`, the outfit rows used here or any animal used; the gallery is accepted and the Preview validated. NPT `Docs/steps.md` since 2026-11-14 (b6dec3ef Beauty2 mouth DY step, c6deb771 blueprint and gizmo hover, e647e9f6 filth spread, 5c5693f8 aim step): no step removed or renamed, nothing a scenario of this mod calls, nothing replaces a hand-made setup. Included animals (teshi, teshi kit) both shown, no MISSING. Rules 1 to 5 stand: no colonist or domestic animal outside NSB, no colonist property changed, all outfits free. Places read: 2026-11-17 (no place doc changed). Tribe read: 2026-11-17 (VALIDE.md diffs, nothing for this mod). Steps read: 2026-11-17.

Checked in SANCTUAIRE-CASES (calm-zone block): the free-standable list for z 185 skips x 208 and 209 (the cells of Nelim in images 4 to 6 and of the kit in image 6), but green v18 and v6 runs stood Nelim on both, so the list marks something on the cell (grass), not a block; no change. Earlier tribe read: 2026-11-08 (diffs only, nothing for this mod; full read 2026-11-06: NELIM-PROFIL, APPARENCES-CANON, CATALOGUE-ANIMAUX, GALERIE-COLONS, LOOKS-VALIDATION, HUMAINS-PROFILS; NSB-ROSTER by search for Nelim only).

| Place | Shots | Changes made to it for the gallery | Last read |
|---|---|---|---|
| `water-garden` west bank (x 143-158, z 168-176; hole (149, 173), geyser (150, 173) out of frame) | 1, 2, 3 | bed GSAnimalBedBigPrestige (156, 172), Plant_Daylily (153, 175), (153, 171), (153, 170), lantern lit (161, 171) in 3; all removed after the scenario; reworked 2026-11-06: image 1 root 3.2 centre (157, 172), image 2 mother on the bed face to the camera (no walk) | 2026-11-06 |
| `calm-zone` corner (nest x about 213, z 185) | 4, 5, 6 | bed (215, 185), EggBox (217, 185), Plant_YellowTallGrass, lantern lit (213, 186), daylilies; all removed after the scenario | 2026-11-06 (NSB marks the cream square x 194.5-205.5, the nest is east of it, read on the capture) |

| Colonist | Shots | Outfit per shot | Last read of its profile | Exceptions |
|---|---|---|---|---|
| Nelim (in the save) | 1, 3, 4, 5, 6 (2: out of frame) | sage `Apparel_CollarShirt` rgb (126, 150, 118) and dark brown `Apparel_Pants` (70, 56, 44) in all: one outfit for the whole evening, readable against brown soil and yellow grass, not the canon daily `LTS_Tunika` (that mod is not in the map) | 2026-11-06 | none (hair `Roo_HD_Hair_Highpony`, skin, eyes as the save gives them; mouth and brow are expressions, see above) |

| Animal | Shots | Outfit | Last read of its sheet | Exceptions |
|---|---|---|---|---|
| teshi "Mother", "Teshi", "Kit" (this mod's creature, tamed or spawned for the scene; outside NSB) | 1 to 6 | none (no apparel mod fits the teshi body) | n/a, not an NSB animal | VALIDATED by the owner, 2026-11-06: "je valide le teshi" (not a pet or livestock, rule 2 did not strictly apply; validation covers the teshi for this mod) |

## Ecosystem

2026-11-17 refresh, PiI (same report, protocols commit 8b8a75c): nine Steam queries (Creatures of Ki, Kija, Teshi, Shooki, patch, translation, retexture, Royalty, Biotech xenotype), result unchanged. Only the original 2726461020 (Creatures of Ki (Continued), 1.0 to 1.4) and the Renews carry the name. No duplicate, fork, replacement, translation, patch or retexture, so nothing to integrate at localize and no worklist row. Zoology: Realistic Animal Overhaul 3679396881 stays a load-order check (no shared defName). Report now ends with the ecosystem-links block. Nothing subscribed.

2026-11-13, PiI Workshop search by Chrome (docs/inventory/ecosystem-steam/CreaturesOfKiTeshiRenew.md, protocols commit f7f2362): no duplicate, fork or replacement. Only the original 2726461020 (Mlie.CreaturesOfKi, tags 1.0 to 1.4, dead for 1.6) shares our defNames (3, expected). No other mod links, patches, retextures or translates it. Zoology: Realistic Animal Overhaul is a weak lead only (no shared defName, rebalances animal stats): test load order if wanted. Nothing subscribed. Package id of the original: Mlie.CreaturesOfKi.

## Earlier state

State of 2026-10-02 (non-regression, publication 1.0.0, gates, integrations, icon, Preview) moved to `docs/runs/status-history.md` on 2026-10-13 (size, `Check-Status.ps1`).

## Identity and title

Mod name `Creatures of Ki - Teshi Renew`; packageId `nelim.creaturesofki.teshi` (renamed 2026-11-12 from `nelim.creaturesofki` on the owner word, which 1.1.0 had published; before that renamed from
`nelim.creaturesofkirenew` 2026-09-28, before anything public carried it). Suffix `Teshi Renew` already distinguishes
this animal-only continuation from original Creatures of Ki. RimWorld 1.6 declared in About.xml. About URL
and description both contain GitHub repository link.

## License and justification

**MIT**, classified `open`. Repo LICENSE records copyright 2020 Mlie and upstream source
https://github.com/emipa606/CreaturesOfKi. Continuation inherits teshi assets and definitions from Shooki and Mlie;
not wholly original work. Local license offers Nelim's extraction and 1.6 port under same MIT terms.
ATTRIBUTION.md records provenance and changes. LICENSE and Mod/LICENSE byte-identical (SHA-256 checked 2026-09-12).

GitHub labels our LICENSE `Other` / `NOASSERTION`, not MIT, probably due to provenance appendix (not verified
diagnosis); declared license stays MIT, `licence_spdx` records declared terms. Upstream
`emipa606/CreaturesOfKi` LICENSE.md contains MIT text, copyright 2020 Mlie (checked 2026-09-12). Upstream Steam page
(2726461020) announces no further support, shows no explicit MIT grant or prohibition; reason for stopping
unspecified, original asset permissions only partly traced (linked original item 1726422863 returned error).
`visibility: public` describes repo access; `licence: open` rests on published upstream MIT grant and local
port's explicit MIT statement, not public access alone.


**WSL cleanup, 2026-10-15 (14.c).** Nothing removed: two optional Workshop mods this mod's passes fetched, 3238353862 (ADS2) and 2269731409 (Nocturnal Animals), still named by `wsl-deps` of other mods (at least 10 and 9; ACertainSeries, AlphaMythology, ASlothMod, DustBunnies, Ebbbs, Dalmatians and others), so stay. Ticket Manager asked for slot, no answer; machine lock free and queue empty at check, nothing deleted. Protocols re-read: AUDIT.md 14.c (cleanup message gives owner Workshop links to unsubscribe), USE_THIS_INSTEAD.md (this mod's row `posted`). Check-Status.ps1 run under pwsh: 0 error, 0 warning.

**Gallery subtitles, 2026-10-15 (owner's request).** English movie-style subtitles (white text, black outline, centred at bottom) drawn into `Art/Gallery/1-portrait.jpg` to `5-asleep.jpg`; `0-preview.png` and `6-the-infirmary-health-tab.jpg` (interface) untouched. Originals in git history before this commit. Owner uploads six images to Steam by hand; not read on page.

**Echo reading, 2026-10-15.** `Art/Gallery/` changed since `df1a839` only by subtitles; six captioned images each opened and read (text legible, no animal or interface element hidden except small `Nelim` label on image 6). `echo_review_sha` moved to `5dc5a7dd3b39251cc90cb6cad6cc281fef94c2df`.

**Review by ChatGPT (Codex) and owner's validation, 2026-10-15.** Taken: `PUBLICATION.md` "Dependencies and DLC" said `supportedVersions` 1.6 only, now 1.6 and 1.7 (`1212abc` + next commit). Not changed: `FRENCH_REVIEW.md` says no source language recorded and Original column repeats English: true, generated file, renew whose source is English; its `?` column stays empty, owner's reading of French is hers (2026-10-10 in chat, no French text changed in 1.1.0). Optional style point on `EggTeshiUnfertilized.description` ("bien meilleur" vs English "much, much better"): not applied, changes `Mod/`. Owner validated variant "bien, bien meilleur" (put in BACKLOG.md for next version, not applied now) and word `kit` in gallery subtitle ("The kit hatches beside its mother.", her word, 2026-10-15).
