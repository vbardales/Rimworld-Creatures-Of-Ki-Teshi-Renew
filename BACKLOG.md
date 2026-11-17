# Backlog

Undone work. State in [STATUS.md](STATUS.md), tests in [TESTING.md](TESTING.md), publishing in [PUBLICATION.md](PUBLICATION.md).

## Now

- **Nothing in flight.** 1.1.0 published (RimWorld 1.7 declared, load tested only). Unplayed on 1.7: laying, hatching, ADS2, Nocturnal, galleries, French.
- **Teshi people, as Biotech xenotype (owner, 2026-10-15).** Add humanlike race paired with teshi in original Creatures of Ki, via Biotech genes. Not started: read original mod for race (sources: upstream `emipa606/CreaturesOfKi`, `ATTRIBUTION.md`), then scope (xenotype + genes only, or new race), Biotech DLC dependency (optional or required), new tests. New minor version, full chain.
- **DONE 2026-11-13 (review-translation).** **French egg description (owner, 2026-10-15, validated).** `Mod/Languages/French/DefInjected/ThingDef/Teshi.xml`, `EggTeshiUnfertilized.description`: end sentence with "mais il est bien, bien meilleur une fois cuit." (English: "much, much better cooked"). Changes `Mod/`: ship next version (patch min), French labels replayed, `FRENCH_REVIEW.md` regenerated.
- **Gallery filter.** Ticket on this mod excludes `11-workshop-captures` and `12-workshop-captures-v2` (`!11-workshop-captures !12-workshop-captures-v2`) unless using `wsl-deps.sanctuary.map`: gallery scenarios fail on other maps.

## Parked

- **Gallery, next series**: Nelim protagonist, animals facing camera in ≥1 capture (`GALLERY.md`, 2026-10-14). Meat scene (18h30) parked until SanctuaryBacklot fixes sweat on Nelim. Second series (`1-portrait.jpg` to `6-the-infirmary-health-tab.jpg`) accepted; Steam page presence unchecked.

- **Crossbreeding**: parked by owner 2026-09-25, "not for now". Needs partner species absent from source; owner names it, else nothing. Read `CompEggLayer` and `CompHatcher` before promising anything.
- **Upstream PR**: impossible, `emipa606/CreaturesOfKi` archived. Branch stays on fork `vbardales/CreaturesOfKi`.