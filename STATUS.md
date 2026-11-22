---
localization: complete
translation_en: complete
translation_fr: complete  # 2026-11-12 owner validated the review-translation answers (her word, twice: no recommendation, then three PUBLICATION points applied); review line of TRANSLATION_REVIEW.md filled with her word
settings_audit: not_applicable
workflow_stage: dormant[1.2.0]
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
tested_on:     2026-11-14 pickle 4c49d1d, English and French labels, ADS2, Nocturnal, new colony, 10 passed of 10 (Docs/runs/pickle.md); the full suite of 2026-09-26 and 2026-10-02 on 1fcc51f/49d9a72 stands; published 2026-10-02 at 49d9a726f64e5d491fb7
workshop:     3806709627
version:      1.2.0 (tag v1.2.0 and GitHub release by CI run 44073923357, 2026-11-17 11:35 UTC; 1.1.0 was tag v1.1.0)
target_version: 1.2.0 (packageId rename 2026-11-12; was 1.1.0 minor bump, 2026-10-13: RimWorld 1.7 pass; `<li>1.7</li>` declared, tested on load only: 01-loads, English, 1.7.4976)
maintainer:   Claude Code, the session named in session, which holds this standalone repository
session:      local_3b2dce0c-52e6-49cb-a662-cefbbbd56580
updated:      2026-11-17, cleanUp done, stage dormant[1.2.0]
remaining:
  - 14.f DONE 2026-11-17: Virginie enabled the Steam comment notifications on the Workshop page (her word "fait"); item already in the collection "RimWorld through Nelim.s eyes".
  - Unverified: the eight gallery images were uploaded by Virginie by hand (her word "fait") and the public change note was not read; no session read the Steam page images.
  - 14.c DONE 2026-11-17: STATUS.md folded into git history of STATUS.md; PUBLICATION.md (change notes 1.2.0 and 1.1.0 moved to git history, declined heads-up draft deleted, header and Next update in the present), BACKLOG.md (done items dropped); TESTING.md already compressed and current, PROTOCOLS-READ.md left as is; no Art/archive. WSL: nothing removed, ADS2 3238353862 and Nocturnal 2269731409 still named by `wsl-deps` of other mods, no Workshop link for Virginie from this mod. 14.d: only main, nothing to delete; branch teshi-1.6-support on vbardales/CreaturesOfKi stays.
  - For Audit, not this mod: Check-ModBasics wants a [url] tail on the About description while sync-about-description.mjs writes plain text.
  - History of 2026-10 to 2026-11-17 (14.a green 9 of 9 on 2026-11-17, publish run 44073923357, replay-audit, review-translation, gallery v26, 1.1.0): git history of STATUS.md, section "Folded from STATUS.md, 2026-11-17".
social_preview_sha256: 9e8c728656fd88ebc0a175f86b04a1c5144e8b3a8e5d9c86dd0662d75f624a52
publication_changelog_review_sha: 317587366da9de84b12b41b51ae97f8d21f0a3ec
echo_review_sha: 0c18456c4538b37b29de392a33e5d4aed2c69f4d
code_review_sha: 4c49d1df5e0b018bc37cdb7d0c9864ed12b4397a
protocols_read_sha: 45fe675796d2688b18b086e6d64b337ad98a648e
---
# Creatures of Ki - Teshi Renew — status

State: 1.2.0 published (tag v1.2.0, CI run 44073923357, 2026-11-17), stage `cleanUp[1.2.0]`. Non-regression 14.a green: 9 of 9 on the published Mod tree (Evidence/nonreg-fast, RELEASE.md, 2026-11-17); the 2026-11-14 run (10 of 10, 4c49d1d) stands for 06 to 10.

## Identity, licence

Name `Creatures of Ki - Teshi Renew` (page title "Creatures of Ki: Teshi Renew"); packageId `nelim.creaturesofki.teshi` (renamed 2026-11-12 from `nelim.creaturesofki`, which 1.1.0 published). Animal-only continuation of Creatures of Ki, MIT, copyright 2020 Mlie; LICENSE and Mod/LICENSE byte-identical; ATTRIBUTION.md records provenance. GitHub labels the licence `Other` (NOASSERTION), declared SPDX stays MIT. Full reasoning: history file.

## Ecosystem

2026-11-17 refresh (PiI, protocols 8b8a75c): only the original 2726461020 (Creatures of Ki (Continued), 1.0 to 1.4) and the Renews carry the name. No duplicate, fork, replacement, translation, patch or retexture; Realistic Animal Overhaul 3679396881 stays a load-order check. Nothing subscribed.

## Gallery, NSB

Gallery accepted 2026-11-13 (v26, eight images in Art/Gallery). Colonist: Nelim (NSB, sage shirt, brown pants); animals: teshi, teshi kit (this mod's creature, validated by the owner 2026-11-06). Places: `water-garden` west bank (images 1 to 3), `calm-zone` nest east of the cream square (4 to 6). Last NSB, places and tribe read: 2026-11-17, nothing changed for this mod. Shotlist tables and run verdicts: history file.
