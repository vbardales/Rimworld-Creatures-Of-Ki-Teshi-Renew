# Creatures of Ki: Teshi Renew: what to check in game

Standalone suite `Tests/Rule-OwnValues.ps1`: 20 checks on compiled game, exact patch shapes, textures, exact values. XML parsing + references covered by shared Check-ModBasics and Check-DefRefs (cut 2026-11-02). Four external validators once cited here absent from repo; their old results not current verification.

`Tests/Rule-OwnValues.ps1` sits between the two. Can't run game, but reads compiled game, runs twenty checks doc once asked of play session — incl. scenario 4b, now settled below. Run first; seconds, free.

Pickle suite played most of these on headless game 2026-09-24; STATUS.md has findings. By hand, run in order: first cheap, catches fatal; fourth only one that can crash save.

Junction into `RimWorld/Mods` first — point at `CreaturesOfKiTeshiRenew/Mod`, not repo root. Dev mode on, keep `Player.log` after session:

```
C:\Users\nelim\AppData\LocalLow\Ludeon Studios\RimWorld by Ludeon Studios\Player.log
```

---

## The passes this suite needs

Declared per `../AUDIT.md`: count, which, coverage. Six passes, small tickets.

| Pass | Map | Language | Plays | Covers |
|---|---|---|---|---|
| Minimal, English | `wsl-deps.sans-facultatifs.map` | English | 11 of 13 discovered, two tickets: all but slow laying, then laying + hatching | Mod alone with Core, DLC, shared tools |
| Minimal, French | same | French | 3 | French translations found, read by game |
| Optional integration | `wsl-deps.avec-ads2.map` | English | 12 of 13 discovered | A Dog Said... Animal Prosthetics 2 mounted, this mod ahead |
| Optional integration | `wsl-deps.avec-nocturnal.map` | English | 1 to 12 of 14 discovered | [XND] Nocturnal Animals (Continued) mounted: teshi crepuscular clock. Exploration plays only `10`, validation plays English set |
| New colony | `wsl-deps.new-colony.map` | English | 1 | Colony starting with mod, not mod added later. **Random: never same colony twice, use sparingly** |
| Gallery captures | `wsl-deps.sanctuary.map` | English | 7 of second series (`12-workshop-captures-v2`, one scenario per image, `docs/GALLERY-V2.md`), + 6 of first series (`11-workshop-captures`) | Three Workshop page images (`11-workshop-captures`), Nelim's tribe (sanctuary, "smiley-north" frame), staged: hay nest + lit torch via StageDecor, hour 18, clear. Presentation, not mod check: open every capture before use |

35 scenarios (`Scenario:` lines) across 12 features, both gallery series (`11`, `12`) incl. `@requires` scenario skipped in passes not mounting its mod; skipped ≠ passed. No incompatibility pass (none declared), no no-DLC pass (no DLC guard). `Tests/Pickle/README.md` has commands + reasons.

---

## 1. It loads

Enable mod alone, Core only. No DLC, no Harmony needed.

**Expect:** `Creatures of Ki: Teshi Renew` in mod list, icon beside, showcase on mod page. No red text at startup.

**Fails if:** any `XML error` or `Could not resolve cross-reference` naming `Teshi`, `EggTeshiFertilized`, `EggTeshiUnfertilized` or `BipedAnimalWithClawsAndTail`. Failed def silently absent after, so clean start underpins next four scenarios.

## 2. The animal draws

Dev mode → *Spawn pawn* → teshi. Spawn several for both sexes + both life stages, or force via *Dev: set age*.

**Expect:** four wide banded ears, dark crest, round low body. Female greyer, kit same drawing smaller. Move animals all four cardinal directions, inspect facing.

**Fails if:** pink/white box for any facing, sex, stage. Nine textures; no north-facing kit or female-north beyond three supplied; missing one shows pink.

## 3. Wildness reads 50 %

First of two 1.6 port changes. `wildness` no longer `<race>` field; now `Wildness` StatDef under `statBases`. Old form not error — just unread, stat defaults `-1`, outside game's `[0,1]`.

Select wild teshi → **Information** tab → *Wildness*. List longer than card: scroll, or type `Wildness` in card search box.

**Expect:** 50 %.

**Fails if:** negative, 0 %, or nothing. Visible symptom: taming succeeds almost instantly on animal meant bear-hard.

Cross-check: order taming, watch success chance. First-try success random, proves nothing; check displayed Wildness.

## 4. The unfertilized egg — the only crash risk

Second port change, reason `EggTeshiUnfertilized` written. Justifying claim now read off game, not assumed: see 4b, answered.

Teshi comp:

```
eggFertilizationCountMax   1
eggCountRange              2
eggProgressUnfertilizedMax 0.9
eggLayIntervalDays         15
```

Two eggs per laying, one fertilization. Earlier doc, README, changelog said mated teshi lays one fertilized + one unfertilized. Compiled `CompEggLayer.ProduceEgg` says otherwise; 4a follows reading: `ProduceEgg` makes **one stack** of `eggCountRange` eggs, all fertilized def while fertilization left, else all unfertilized def. Stack = two fertilized. Unfertilized def only when no fertilization left, and unfertilized laying stops at 0.9 (4b), so teshi never lays it. If 4a shows stack of one + stack of one, reading wrong.

### 4a. Mated female

Tame male + female, keep together, let laying cycle finish. Dev mode: egg-layer comp debug gizmo advances cycle a day; push until she lays.

**Expect:** one stack of two `teshi egg (fert.)` on ground, no `teshi egg (unfert.)`. No fertilization left after, so no laying until mated again.

**Fails if:** stack differs, or log exception at laying naming `CompEggLayer` or `ThingMaker.MakeThing`.

### 4b. Lone female

Tame single female, no male on map, advance cycle same way.

**Expect: nothing, ever.** Never lays. Was open question, now answered by reading compiled game, not playing, in `CompEggLayer`:

- `CompTick` accumulates `eggProgress`; while unfertilized writes `eggProgressUnfertilizedMax` straight into field — progress *pinned* to setting, not just compared. Teshi setting 0.9.
- `CanLayNow` needs full `1` of `eggProgress`.

Pinned 0.9, needs 1: stopped for good. Inspect string should say so: comp has `ProgressStoppedBecauseUnfertilized` state for this.

Scenario now confirmation, not experiment. **Fails if** she lays anything — reading wrong, and `Rule-OwnValues.ps1` should've caught first.

Settles about def: crash docs once described impossible for lone teshi; same reading shows mated laying never reaches unfertilized def either. Declared because every Core egg-layer declares one, and dev-mode lay-egg on female without fertilization asks for it. Harmless, not the fix changelog claims.

## 5. The egg hatches

Leave fertilized egg somewhere warm, advance fifteen days, or dev gizmo on egg.

**Expect:** teshi kits, tame, colony-owned: stack of two hatches into two.

**Fails if:** hatches into nothing or wrong pawn kind.

## 6. The desiccated corpse — known defect, confirm it is only cosmetic

Kill teshi, let corpse dry, or spawn desiccated corpse directly.

**Expect:** dromedary desiccated sprite, three draw sizes. **Correct for this mod.** Shooki's choice, inherited on purpose, recorded in `ATTRIBUTION.md`; new art would make rewrite, not port.

**Fails if:** pink box or exception. Borrowing texture intended; not finding it isn't.

## 7. Predator and manhunter, sanity only

Port touched none; regression check, not verification.

- `manhunterOnDamageChance` 0.75: shoot wild teshi once, manhunter ~3 in 4. 4× human health pool, so do away from colony.
- `manhunterOnTameFailChance` 0.05: failed taming rarely provokes.
- `predator` true: wild teshi hunts, not grazes.
- `nuzzleMtbHours` 12: tame one nuzzles colonists within ~a day.

## 8. The optional integration with A Dog Said... Animal Prosthetics 2

Only with that mod (`SamBucher.ADogSaidAnimalProsthetics2`, Workshop 3238353862) enabled, in RimWorld-computed load order: this mod before it, per `About.xml` and its page's request. `Patches/ADS2_Categories.xml` puts teshi in categories that mod uses to pick prosthesis-eligible animals.

Spawn teshi + grizzly bear, select each, Health tab, *Add bill* → operations.

**Expect:** teshi gets same prosthetic + bionic recipes as grizzly (already category 3 there). Whether a prosthesis applies depends on teshi body parts — that mod's arithmetic.

**Also, since 2026-09-26:** two arm recipes of that mod target `Shoulder`, which teshi lacks; `Patches/ADS2_Arms.xml` adds `Arm` to both. Scenario asks recipe worker if each recipe applies to each arm, applies effect, reads hediff on arm. Doctor bill with medicine + skill check not played: game's job, scenario stops at recipe effect.

**Fails if:** teshi gets none of that mod's recipes, or fewer than bear, or startup error names `ADS_Cat3` or patch. With other mod **absent**, loads exactly as scenario 1: patch finds nothing, logs nothing.

## 9. A new game with the mod

New colony with mod enabled from main menu, play first minutes.

**Expect:** world + first map generate error-free, teshi defined, nothing logged from mod. Fixture colony of other scenarios saved without mod, so only this scenario shows colony starting with it.

**Fails if:** error/warning names mod during start, or teshi undefined after.

**Random, use sparingly.** New colony never same twice: world, tile, colonists differ each start, regardless of scenario seed. Three consequences.

- Green = one clean draw, not all. Red may not recur on rerun, and green rerun doesn't clear it: read run's `new-colony` attachment (names choices, tile, colonists), keep with report.
- Assert only what draw can't change: defs, nothing logged from mod. Anything depending on colony contents excluded.
- Played once in initial or final validation, never in fix or exploration loop (fix judged against different colony each time). Anything needing repeat goes on fixture colony.

## 10. The optional integration with Nocturnal Animals

Only with [XND] Nocturnal Animals (Continued) (`Mlie.XNDNocturnalAnimals`, Workshop 2269731409) enabled. `Patches/NocturnalAnimals.xml` gives teshi crepuscular clock — owner's choice, not source's. Select teshi, open info card.

**Expect:** card names crepuscular rhythm, teshi awake dawn + dusk. Nothing logged from mod. With other mod **absent**, loads exactly as scenario 1: patch is `FindMod`, logs nothing.

**Fails if:** teshi missing from game (what missing extension class does when patch not under `FindMod`), rhythm not crepuscular, or startup error names patch.

---

## What to send back

`Player.log` from session + one line per scenario on outcome — incl. game version, mod list. Scenarios 1–10 here; Pickle suite plays them, hand session plays rest.

## Translation display — English and French

Unverified until done in RimWorld 1.6. Repeat in both languages: inspect adult + baby teshi, both egg types, melee attack labels, all custom body-part labels in health tab. Check baby singular/plural, accents, raw keys, English fallback in French, formatting, clipping. Record results + Player.log evidence in STATUS.md.

---

## What `tested` requires

From `../AUDIT.md`, transition `done -> tested`. Pickle suite played since 2026-09-24; STATUS.md has findings + open items. Not-yet-played = pending, not pass.

- Every scenario above played in game, or listed not applicable with reason.
- Pickle suites green, `@review` captures opened + viewed. Read `exitReason` before counts; compare played scenarios vs discovered features.
- No scenario left `@wip`: fixed + replayed, or deleted with justification.
- Every conditional scenario (`@requires:<packageId>`) had its pass, map mounting that mod. Three: `08-ads2-integration` needs A Dog Said... Animal Prosthetics 2, `09-new-colony` needs NewColony tool, `10-nocturnal-integration` needs [XND] Nocturnal Animals (Continued). Run without mod skips scenario; skipped ≠ passed. Mod needs no DLC; DLC in `loadAfter` ordering only.
- No manual test left. Each of ten scenarios → green Pickle scenario or listed not-applicable. Suite in `Tests/Pickle/`: see README + table below.
- Both languages played, one pass each (`-Language English`, `-Language French`), dev mode: accented gibberish = key missing from active language; clean English inside French = string never translated.

### Scope of the Pickle suite

Only what running game can show. Rest proved offline by `Tests/Rule-OwnValues.ps1`. Features in `Tests/Pickle/Mod/Pickle/Features/`; `Tests/Pickle/README.md` says how to run.

| Scenario | Fate | Feature | Why |
| --- | --- | --- | --- |
| 1. It loads | Pickle | `01-loads` | Only load shows def that failed + went silently absent, and Wildness game computes for animal. |
| 2. The animal draws | Pickle, `@review` captures | `02-draws` | Pink box = rendering fact. Three captures show nine textures, all four facings. Captures still must be opened. |
| 3. Wildness reads 50 % | Pickle | `01-loads`, `02-draws` | Game-computed value asserted in 01 off race, in 02 off living animal. First run: info card list longer than window, Wildness below fold, so capture shows card opens + reads English, not proof of 50 %. Offline suite shows stat accepts 0.50, not that game reads it. |
| 4a. Mated female lays | Pickle, `@slow` | `03-laying-and-hatching` | One stack of two fertilized eggs, no unfertilized, for colony: behaviour via game's own job. |
| 4b. Lone female | Not applicable | none | Read off compiled game (`CompEggLayer`) by offline suite. Run would test engine. |
| 5. The egg hatches | Pickle, `@slow` | `03-laying-and-hatching` | Two colony kits from her eggs. Needs hatcher's own tick. |
| 6. Desiccated corpse | Pickle, `@review` capture | `04-desiccated-corpse` | Borrowed dromedary sprite not shipped openly; no file reveals it. |
| 7. Predator and manhunter | Not applicable | none | Declarations; mod answers for what it declares: read in XML. Offline suite proves each written field has game reader, not value, so values settled by XML read, change only with it. 0.75 roll random, engine's job; testing it tests game. |
| 8. Optional integration with A Dog Said... Animal Prosthetics 2 | Pickle, `@requires`, third pass | `08-ads2-integration` | Offline suite lacks other mod, checks only patch shape. Only game shows teshi gets grizzly's recipes, and since `ADS2_Arms.xml`, both arm recipes apply per arm + leave hediff (played 2026-09-27). |
| 9. A new game with the mod | Pickle, `@requires`, own pass | `09-new-colony` | No save reaches colony starting with mod: world + first map generated with animal. Random, so once in validation, not fix loops. First run 2026-09-25 failed in tool (started with Ideology on, no ideoligion, no starting pawns); passed 2026-09-26 after tool fix. |
| 10. Optional integration with Nocturnal Animals | Pickle, `@requires`, own pass | `10-nocturnal-integration` | Offline suite lacks other mod, checks only patch shape + extension written only in `FindMod`. Only game shows class found, extension parsed, teshi kept. |
| Save and reload | Pickle | `05-save-reload` | Animal + egg survive round trip; fixture colony saved without mod = mod added to existing colony. |
| FR / EN display | Pickle, one pass per language | `06-labels-en`, `07-labels-fr` | Labels + descriptions read off loaded defs, health tab with each claw + ear on own side; since 2026-09-27 info card of kit + fertilized egg in both languages, adult in French, seen on screen. |

## Evidence to keep

Raw Pickle reports on disk in `Tests/Pickle/Evidence/<run>/`, excluded by `.gitignore`: captures + `Player.log` grow unbounded. Pass `-EvidenceDir` to launcher so report copied before lock released, then check `exitReason` + played/discovered counts in each copy.

Keep, per scenario, latest report for current repo revision. Keep older only if sole proof of check latest run didn't repeat. Delete others once replaced, after listing what goes + stays. Never delete report `STATUS.md` points to: repoint first. History = one text line per run in `docs/runs/`, never folder. Shared Pickle report folder holds all mods' screenshots: keep only this mod's.

Proofs worth keeping, only these:

- animal on each facing: one capture per sex + life stage (adult male, adult female, kit), no pink box;
- stack of two `teshi egg (fert.)` on ground after mated laying, no unfertilized egg;
- hatched kit, tame, colony-owned;
- desiccated corpse;
- adult teshi health tab in English + French, custom body-part labels shown;
- `Player.log` per pass, already searched for `XML error`, `Could not resolve cross-reference` and names `Teshi`, `EggTeshiFertilized`, `EggTeshiUnfertilized`: newest per pass only.

Minify captures before keeping: drop ones verdict doesn't rest on, crop to proving panel, or re-encode JPEG (quality 80, max 1280 px wide). Never retouch; keep original of any capture needing measurement. Text reports (`summary.md`, `junit.xml`) small, stay whole; `report.html` and `messages.ndjson` go.

Nothing to sort today: no Pickle run made, so no report in repo, git or disk.