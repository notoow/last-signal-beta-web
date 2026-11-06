# Asset and dependency provenance

Legacy assets use the sources listed below; the separately documented 2026-10-26 OST uses a hosted generation service and its own licensing conditions. Downloaded source archives and pack license texts are retained in `third-party-source/`. The selected Kenney OGGs, Pretendard font and their licenses ship in `assets/`.

## Runtime audio — Kenney, CC0 1.0

The supplied pack licenses expressly permit personal, educational and commercial use; attribution is optional. We nevertheless credit **Kenney (www.kenney.nl)** here. License texts are included at `assets/licenses/Kenney-Interface-CC0.txt` and `assets/licenses/Kenney-SciFi-CC0.txt`.

Official sources checked 2026-10-05 UTC:

- Interface Sounds 1.0: https://kenney.nl/assets/interface-sounds
- Sci-Fi Sounds 1.0: https://kenney.nl/assets/sci-fi-sounds
- CC0 legal text: https://creativecommons.org/publicdomain/zero/1.0/

| Runtime file | Source pack / original name | Adaptation |
| --- | --- | --- |
| ui.ogg | Interface / click_002.ogg | Renamed; runtime volume and short fade |
| upgrade.ogg | Interface / confirmation_002.ogg | Renamed; runtime volume and short fade |
| anchor.ogg | Sci-Fi / forceField_000.ogg | Renamed; runtime volume and short fade |
| circuit.ogg | Sci-Fi / explosionCrunch_001.ogg | Renamed; runtime volume and short fade |
| dash.ogg | Sci-Fi / thrusterFire_000.ogg | Renamed; playback limited to 0.38 sec with fade |
| hurt.ogg | Sci-Fi / impactMetal_002.ogg | Renamed; runtime volume and short fade |
| shot.ogg | Sci-Fi / laserSmall_000.ogg | Renamed; runtime volume and short fade |

The current harbor mixer caps short samples and synthesized cues at 24 simultaneous voices, throttles repeated cues and applies runtime gain/envelopes. Original source sample bytes are unchanged. Automated decode/envelope checks do not substitute for a human listening pass; that remains a QA task.

## Code and runtime

- Nanum Myeongjo Regular, copyright © 2010 NHN Corporation, bundled unmodified under SIL OFL 1.1 for chapter openings only. Official distribution: https://github.com/google/fonts/tree/main/ofl/nanummyeongjo . Runtime file: assets/fonts/NanumMyeongjo-Regular.ttf. Exact license: assets/licenses/NanumMyeongjo-OFL.txt. Downloaded 2026-10-19; font SHA256: 7ed9e8653a8ed04285d51dc343ffea6eb3d9c73afc27383ea8929ee4ffd03205. No external font request at runtime; UI controls retain Pretendard.

- Electron 44.5.1, MIT: https://github.com/electron/electron . Its `LICENSE` and bundled `LICENSES.chromium.html` remain in the distributed runtime. The complete third-party Chromium notices accompany the binary.
- Playwright 1.63.0, Apache-2.0: https://github.com/microsoft/playwright . Development/test dependency only; not included in the game package.
- The lockfile pins the complete dependency graph. Development `node_modules` are excluded from the distributed app.
- Pretendard Variable 1.3.9 by Kil Hyung-jin is bundled unmodified under SIL OFL 1.1. Official source: https://github.com/orioncactus/pretendard/tree/v1.3.9/packages/pretendard/dist . Font: assets/fonts/PretendardVariable.woff2; exact copyright and license: assets/licenses/Pretendard-OFL.txt. Used in DOM and Canvas; no network or installed font needed. Windows fallback font files are not redistributed.
- Game code, procedural vector geometry, particle effects, synthesized music motifs, UI writing and translations were created in this project with AI assistance. No claim of exclusive rights in purely machine-generated material is made. The project is private and has no public open-source license at this stage.

## Steam content-survey record

AI assisted both code and player-facing content: procedural artwork design, synthesized musical motifs, Korean/English text and translation. Six narrative raster illustrations and portraits were generated using the built-in image_gen tool for v0.13.0. They are bundled unchanged in assets/art; prompts and provenance are in docs/REWARD-ART-PROMPTS.md. They are not gameplay screenshots or third-party licensed stock. No live generative AI runs in the shipped game. The developer must disclose relevant pre-generated player-facing content accurately in the Steam content survey; do not assume code-only tooling exemptions cover these assets. Kenney source assets are third-party CC0 assets, not newly AI-generated content in this project.

## Generated narrative art — v0.13.0

assets/art/jian-v1.png, jeongho-v1.png, homecoming-v1.png, market-v1.png, sluice-v1.png and landing-v1.png were generated with the built-in image_gen tool on 2026-10-19. No external reference photographs or franchise characters were supplied. These AI-created portraits and memory illustrations must be covered by the Steam pre-generated AI disclosure. Do not represent these narrative images as gameplay captures. Prompt provenance: docs/REWARD-ART-PROMPTS.md. No claim of exclusive copyright in purely generated material is made.

All six generation prompts and asset SHA256 hashes are also shipped in assets/art/PROVENANCE.json.

## Generated Dawn story illustration — v0.16.0

assets/art/dawn-rescue-v1.png was generated using the built-in image_gen tool on 2026-10-19 without supplied reference images. It depicts an original fictional coastal-ferry rescue, not the Titanic or a reconstruction of any historical accident. Prompt: docs/DAWN-STORY-ART.md; the prompt and SHA256 are also shipped in assets/art/PROVENANCE.json. Include this seventh illustration in Steam pre-generated AI disclosure. No claim of exclusive copyright in purely generated material is made.

## Generated title layers — v0.16.0

assets/art/menu-harbor-v1.png and menu-tug-v1.png were generated with the built-in image_gen tool on 2026-10-19 using the project’s own dawn-rescue-v1.png as a style reference. The foreground tug has genuine alpha transparency. Nine generated images are now bundled in total. Prompt provenance: docs/TITLE-ART-PROMPTS.md and assets/art/PROVENANCE.json. Include these pre-generated images in Steam AI disclosure; they are not historical images or gameplay captures.


## Generated expedition art — v0.17.0
Seven additional final assets (interior shell, furniture atlas, fleet atlas, harbor materials, crew sprite atlas and two portraits) were generated/edited with the built-in image_gen tool on 2026-10-19. Sixteen PNG illustrations are bundled in total, including preserved earlier portraits. Exact prompts, dimensions, alpha ranges and SHA256 hashes are in assets/art/VOYAGE-PROVENANCE.json. Final character faces use user-provided photographs as authorized likeness references; original photos are not bundled or stored in source. These assets are pre-generated AI content, not photographed gameplay; include them in the Steam AI-content disclosure. No claim of exclusive copyright in purely generated material is made.
## Generated harbor workshop and crew revision — v0.17.1

assets/art/harbor-workshop-v1.png and crew-sprites-v4.png were generated with the built-in image_gen tool on 2026-10-19. The crew revision uses the existing Woo and Park portraits as identity references; no original user photographs are shipped. Prompts and SHA256 hashes: assets/art/HARBOR-UI-PROVENANCE.json. These are pre-generated AI assets for the Steam content disclosure. Earlier assets are preserved.
## Generated dispatch material — v0.17.2

assets/art/dispatch-folder-v1.png was generated using the built-in image_gen tool on 2026-10-19, without supplied reference images. It is only a background material; live text uses the bundled Pretendard and crew portraits reuse the existing assets. Prompt and hash: assets/art/DISPATCH-PROVENANCE.json. Include this pre-generated material in Steam AI-content disclosure. Character model sheets under docs/design/characters are development references and are not packaged with the game.

## Water feedback — Kenney Particle Pack 1.1, CC0

Official source checked 2026-10-19: https://kenney.nl/assets/particle-pack . Original archive retained at third-party-source/kenney_particle-pack.zip. Exact pack license at assets/licenses/Kenney-Particle-CC0.txt. Runtime assets/vfx/foam.png is unmodified PNG (Transparent)/smoke_01.png; spray.png is unmodified dirt_02.png. These generic particles are animated as foam and spray at runtime; no Unity sample code is used.

## Original harbor music

A Light Beyond the Breakwater is an original AI-assisted eight-bar instrumental composition synthesized by scripts/compose-harbor.py. No external song, recording, sample library or paid generation service was used. The 72 BPM stereo WAV and its hash are recorded in assets/audio/HARBOR-THEME.json. Its melody, pad synthesis and circular delay were authored for this project. Human musical/listening review remains separate from decode and signal tests.

## Generated harbor scale materials — v0.41.0

assets/art/harbor-water-v1.png and harbor-modules-v1.png were generated with the built-in image_gen tool on 2026-10-20. Water used no references. The modular atlas used the project's own harbor-tiles-v1.png and fleet-sprites-v1.png as style references. The atlas has actual alpha transparency; original outputs are preserved unmodified and cropped only by the runtime renderer. Exact prompts, reference filenames, dimensions, alpha ranges and SHA256 hashes are in assets/art/HARBOR-SCALE-PROVENANCE.json. Include these two pre-generated AI assets in Steam AI-content disclosure. No claim of exclusive copyright in purely generated material is made.

## Generated harbor dressing — v0.42.0

assets/art/harbor-details-v1.png was generated with built-in image_gen on 2026-10-20, using only the project harbor-modules-v1.png as a style reference. Four alpha sprites depict fishing net/tray, fender tires, mooring rope and an unlit worklight. The original output is unmodified; runtime uses measured frames. Exact prompt, references, alpha/dimensions and SHA256 are in assets/art/HARBOR-DETAILS-PROVENANCE.json. Include this pre-generated AI asset in Steam AI-content disclosure. No claim of exclusive copyright in purely generated material is made.
# Three-depths and additional crew artwork (2026-10-20)

`assets/art/rogue-bosses-v1.png`, `han-model-sheet-v1.png`,
`jeong-model-sheet-v1.png`, and `crew-han-jeong-v1.png` were generated with
OpenAI's built-in image generation tool for this project. Exact prompts and
references are recorded in `assets/art/THREE-DEPTHS-PROVENANCE.json`.
Han and Jeong use likeness references explicitly supplied by the user; original
personal photographs are not distributed. Woo/Park reference artwork is used
only for stylistic continuity. Generated outputs are preserved unmodified.
These are AI-generated original project assets, not third-party stock licenses.

Follow-up generated assets: `jeong-model-sheet-v2.png` and
`crew-han-jeong-v2.png` apply the user's explicit slimmer-cheek revision while
preserving smiling dimples; `rogue-shore-props-v1.png` provides the dock dog,
salvage chest, fictional closed observation hut and weather buoy. Same generation
tool and provenance file. Han continues to use the v1 sprite.

## Captain departure and fleet — v0.44.0

`assets/art/crew-woo-park-v5.png`, `departure-dock-v1.png` and
`docs/design/characters/{woo,park}-model-sheet-v2.png` were created with built-in
image_gen following the user's new likeness references and menu feedback.
Exact prompts/reference roles/hashes are in `assets/art/DEPARTURE-PROVENANCE.json`.
Original personal photographs are not copied into source or packages.

`assets/art/captain-fleet-top-v1.png`, `captain-fleet-menu-v1.png` and
`departure-dock-v2.png` use existing project illustrations as style/ship references.
Their exact prompts and hashes are in `assets/art/CAPTAIN-FLEET-PROVENANCE.json`.
All PNG source outputs are preserved; the game uses runtime frame composition
and steel-color masks for cosmetic paint. These are pre-generated AI assets
for the project's Steam AI-content disclosure, not third-party stock licenses.
No exclusive copyright claim is made for purely generated material.

## Modular terrain, shore animation and SD crew — v0.45.0

The following project assets were generated using the built-in image_gen tool.
Their recorded references are existing project artwork. The source PNGs are
retained; runtime drawing selects atlas frames and scales them for gameplay.

- `harbor-terrain-v2.png` and `harbor-interactions-v1.png`: modular paving,
  retaining edges, machinery, ropes and dock objects. Prompts, style reference
  and original hashes: `assets/art/TERRAIN-PROVENANCE.json`.
- `shore-fauna-v1.png` and `crew-actions-v1.png`: shore creatures and the earlier
  crew action atlas. Prompts and artwork references:
  `assets/art/SHORE-ANIMATION-PROVENANCE.json`.
- `shore-fauna-v2.png`: generated rat-row revision; other three animal rows
  preserve v1 pixels. Frame rectangles, fixed pivot and source hashes are in
  `assets/art/SHORE-FAUNA-V2-FRAMES.json`. Built-in image generation and packing
  provenance: `art-workshop/2026-10-26/rat-readability-01/HANDOFF.md` and its
  `refinement-prompt.txt`. No third-party artwork was added for this revision.
- `crew-sd-woo-v1.png`, `crew-sd-park-v1.png`, `crew-sd-han-v1.png` and
  `crew-sd-jeong-v1.png`: SD gameplay proportions using the established project
  character identities. Prompts and references:
  `assets/art/SD-CREW-PROVENANCE.json`.
- `working-quay-v1.png`: workbench, fish-market, fuel, shelter and quayside
  dressing. Prompt/reference: `assets/art/WORKING-QUAY-PROVENANCE.json`.
  `working-quay-v2.png` is its generated transparency revision.
- `crew-sd-idle-v1.png`: supplementary blink and idle-gesture poses referencing
  the four SD sheets. The idle prompt and quay transparency-edit prompt are
  recorded in `assets/art/IDLE-QUAY-PROVENANCE.json`.

`assets/art/ASSET-CHECKPOINT-v0.45.json` records the current file hashes and
links each PNG to its provenance. Those checkpoint hashes do not independently
certify the quality or frame consistency of generated artwork. Preserved earlier
atlases may be bundled without being the active character renderer.

These are pre-generated AI assets for the project's Steam AI-content
disclosure, not third-party stock assets. No exclusive copyright claim is made
for purely generated material. Original personal photographs are not included
in this asset group.

## Mobile port runtime

The optional mobile/ target adds Capacitor 8.5.3 and Capacitor App 8.1.2 under
MIT licenses. See mobile/LICENSE-NOTICES.md and the exact license files in
mobile/licenses/. Native transitive dependency notices must be audited before
shipping Android or iOS binaries.

## Refit request thumbnails — v0.45.0

`unpowered-pier-v1.png`, `leaking-rescue-vessel-v1.png` and `squall-tow-v1.png`
are pre-generated OpenAI image_gen illustrations using existing project art
references. They are copied byte-for-byte from the approved workshop candidates.
Exact prompts, references and SHA256 hashes are retained in
`assets/art/REFIT-THUMBNAIL-PROVENANCE.json`. These belong in the Steam AI-content
disclosure; they are not third-party stock assets. No exclusive copyright claim
is made for purely generated material. UI text and rewards are rendered by code.

## Dredger counterplay sprites — v0.46.0

The nine `dredger-bucket-*`, `dredger-winch-*` and `dredger-impact-fx-*`
v1 PNGs were generated with OpenAI image_gen using the existing project
`rogue-bosses-v1.png` as reference. Exact prompt, source, frame bounds, pivots
and SHA256 hashes are in `assets/art/dredger-action-v1-contract.json`.
These are pre-generated AI assets for the Steam AI-content disclosure,
not third-party stock. No exclusive copyright claim is made for purely
generated material. Target markers and collision rules are runtime code.

## Sluice modules — v0.48.0

The six `sluice-gate-*`, `sluice-capstan-*` and `sluice-foam-*` runtime PNGs
are pre-generated OpenAI image_gen artwork using existing project art as
references. Exact prompts, source files, rejected alternatives, fixed pivots,
frame dimensions and SHA256 hashes are recorded in
`assets/art/sluice-module-v1-contract.json`. Open gate housings were generated
separately and aligned to a common canvas; their details are not pixel-identical.
No third-party stock was introduced. Include these in Steam's AI-content
disclosure; no exclusive copyright claim is made for purely generated material.

## Lighthouse relay encounter — v0.49.0

`lighthouse-base-v1.png`, `lighthouse-head-v1.png`,
`lighthouse-relay-off-v1.png`, `lighthouse-relay-on-v1.png` and
`lighthouse-breakwater-v1.png` are pre-generated OpenAI image_gen artwork.
Existing project machinery supplied the references. Source image, exact prompt,
processing, pivots, fixed scale and SHA256 hashes are retained in
`assets/art/lighthouse-set-v1-contract.json` and its referenced files.
The searchlight-head filename alias remains as provenance, not a runtime asset.
These belong in the Steam AI-content inventory. No third-party stock or
exclusive copyright claim for purely generated material is introduced.
Searchlight, warning and collision geometry are rendered and checked by code.

## Stranded harbor mechanic — v0.56.0

`shore-worker-v1.png` is pre-generated OpenAI image_gen project artwork,
referencing the existing SD crew style. The fixed frame rectangles, measured
alpha bounds, common foot pivots, source prompts, replacement-frame calibration
and SHA256 hashes are retained in `assets/art/shore-worker-v1-metadata.json`.
Initial walking candidates were rejected and preserved separately; the runtime
sheet uses separately generated opposite-foot poses. Runtime locomotion selects
two contact poses by actual distance traveled. Minor generated detail changes
and a mirrored left-facing side remain. No external stock or exclusive copyright
claim is introduced. Include the runtime sheet in the Steam AI-content inventory.

## Generated social artwork — 2026-10-23

assets/social/last-signal-og-v1.png was generated in the separately requested OG-image task with the built-in image_gen tool, using this project's squall-tow-v1.png as a style reference. It is promotional key art, not a gameplay screenshot. The adjacent last-signal-og-v1-prompt.txt records its prompt and provenance. It is preserved in the development package but is not loaded by the game or applied to the public site by v0.62. No claim of exclusive copyright in purely generated material is made.


## East service quay — v0.63.0

`assets/art/east-quay-repair-v1.png` is pre-generated OpenAI image_gen project artwork: repair bench, welding cart and worklight. Existing `harbor-interactions-v1.png` supplied the style reference. The original sheet is copied unchanged (SHA256 b7dd01fdb18da519f364510e6532662db35a7cdc5047209db1d747e09769686e); adjacent prompt and metadata preserve measured source rectangles and the corrected placement candidate. Runtime placement derives from actual map ground; the earlier x3320 shoreline study was incorrect and is retained only under art-workshop. No third-party stock was introduced. Include the sheet in the Steam AI-content inventory; no exclusive copyright claim is made for purely generated material.

## Crew upgrade icons — 2026-10-23

`assets/art/crew-upgrade-grip-v1.png`, `crew-upgrade-stride-v1.png` and
`crew-upgrade-guard-v1.png` are pre-generated OpenAI image_gen project artwork.
They depict a rope-wrapped glove and hook, a deck boot and a padded life vest.
The transparent generated originals were resized to 256x256 with browser Canvas;
no third-party stock was imported. Exact prompts, original source copies and
source SHA256 hashes are preserved under
`art-workshop/2026-10-23/mobile-land-redesign/` in `CREW-UPGRADE-PROMPTS.txt`
and `CREW-UPGRADE-PROVENANCE.json`. Include these icons in the Steam AI-content
inventory when used. No exclusive copyright claim is made for purely generated
material. Asset delivery alone does not establish runtime integration.

## Landing harbor modules — 2026-10-23

The ten runtime PNGs `quay-landing-workshop-v1.png`,
`quay-landing-warehouse-v1.png`, `quay-landing-ground-v2.png`,
`quay-landing-wall-v1.png`, `quay-landing-wet-material-v4.png`,
`quay-landing-ground-gold-v3.png`, `quay-landing-wet-patch-v1.png`,
`quay-landing-props-v1.png`, `quay-landing-supplies-v1.png` and
`quay-landing-water-reflection-v1.png` under `assets/art/` are pre-generated
OpenAI image_gen project artwork. They are byte-identical copies of the
project's approved harbor prototype materials. No third-party stock was
introduced in this delivery. Source artwork, generation records and verified
copy hashes are retained in the development art archive; the public delivery
contains runtime PNGs only, not reference photographs or generation prompts.
Include these assets in the Steam AI-content inventory. No exclusive copyright
claim is made for purely generated material. Asset delivery does not certify
final gameplay integration or visual acceptance.

## Directional supply workboat — 2026-10-23

The eight runtime `assets/art/supply-boat-{e,se,s,sw,w,nw,n,ne}-v1.png`
images are OpenAI image_gen artwork made for this project from its existing
inspection workboat reference. No third-party stock was added. The runtime
files are unchanged crops from the generated candidate; `src/supply-fleet-frames.js`
contains only rendering measurements. Exact prompts, original sheets, hashes,
measurement limits and the production record remain under
`art-workshop/2026-10-23/supply-oblique-eight/PROVENANCE.json` and its contract,
outside public runtime export. Include the selected artwork in the Steam
AI-content inventory; no exclusive copyright claim is made for purely generated
material. Direction/contact consistency still requires actual-game review and
is not established by provenance or an eight-frame count.

`assets/art/supply-boat-world180-v1.png` adds a targeted near180-degree view.
It is byte-identical to the generated `supply-world180-v2-candidate.png` in that
same art archive. Its contract and WORLD180-HANDOFF.md preserve the two prompts,
generated source hash, estimated water-plane contacts and measurement limits.
The same OpenAI image_gen provenance and AI-content disclosure apply. It does
not make the other candidate headings exact or establish motion approval.

## Social sharing artwork — 2026-10-23

assets/social/last-signal-og-v2.png is AI-generated promotional artwork created with OpenAI image_gen from existing project art. It is not a gameplay screenshot. The original prompt and edit prompt are preserved privately in assets/social/. No third-party stock was added; include this artwork in the Steam AI-content inventory.

## Ship equipment reward artwork — 2026-10-24

`assets/art/ship-gear-atlas-v1.png` is OpenAI image_gen project artwork, made
using the existing `quay-landing-props-v1.png` as a style reference. It contains
six distinct equipment illustrations, not gameplay screenshots or third-party
stock. No personal photographs were used for this request. The generated
candidate was technically cropped and repacked to isolate each object; the
accepted production file is byte-identical to the reviewed repacked atlas.
Source prompt, layout, hashes and processing scope: `docs/SHIP-GEAR-ART.md`.
Include this asset in the Steam AI-content inventory. No exclusive copyright
claim is made for purely generated material. Provenance does not establish
pixel-perfect animation or player appeal.


## Woo side gait parts (2026-10-24)

`crew-sd-woo-side-v2-*.png` are generated character parts from OpenAI image generation, derived from the existing original Woo game character. No new photographs or third-party game sprites are included. Root assembles the eight unmodified PNG layers into a distance-driven side gait. Private prompts/source hashes and the limited review are recorded in `assets/art/WOO-SIDE-RIG-v2-PROVENANCE.json` and the referenced art-workshop handoffs; those records are not public runtime assets. This set covers only Woo side idle/walk. Existing front, rear and action images retain their earlier provenance.

## Park side gait parts (2026-10-24)

`crew-sd-park-side-v2-*.png` are generated character parts from OpenAI image generation, derived from the existing original Park game character. Root assembles eight unmodified PNG layers into a distance-driven side gait. Private source hashes and limited visual reviews are recorded in `assets/art/PARK-SIDE-RIG-v2-PROVENANCE.json`; source photographs, prompts and workshop records are excluded from the public export. This set covers Park side idle/walk only. Existing front, rear and action images retain their earlier provenance.


## Service quay material (2026-10-26)

quay-service-diffuse-v1.png and quay-service-wetness-v1.png were generated with OpenAI image generation for this project, with no third-party game assets or photographs supplied. The art owner preserved original prompts, source images and processing provenance in art-workshop/2026-10-26/service-ground-macro-01. The registered 1536x1152 pair covers 160x120 world units once; the grayscale wetness is linear L/255 data, not transparency. Normalized from generated 1024x768 cells, not native1536 artwork. No exclusive copyright or public-domain license is claimed. Include these assets in the Steam AI-content inventory.

## Raised coast development materials (2026-10-26)
assets/art/cliff-top-v1.png and cliff-face-v1.png are project-specific image_gen outputs copied from art-workshop/2026-10-26/cliff-broad-planes-02. Face is byte-identical to broad-planes-01. Original prompts, generation/source records, hashes and notices remain in those folders. No external stock/game downloads or invented OSS license; generated-service terms and reference rights apply. This record does not certify exclusivity or copyright registration. These neutral base materials are development art, not final art approval.

## Disabled dredger body (2026-10-26)

`assets/art/dredger-defeated-v1.png` is the art owner's image_gen-derived variant
of the project's existing dredger illustration. Generation and uniform alignment
records remain in `art-workshop/2026-10-26/dredger-defeat-01/`. No external game
art was copied; no exclusive copyright or open-source license is claimed.
Include this generated variant in the Steam AI-content inventory.

## Generated OST — local integration 2026-10-26

Eleven AI-generated Sonilo Music recordings obtained through Higgsfield MCP are locally integrated as Vorbis derivatives in assets/audio/ost. Original recordings, exact prompts, generation IDs, source hashes and transformation hashes are preserved offline under experiments/last-signal-ost-20261026. No exclusive copyright or wholly human composition is claimed. These tracks are not CC0 assets. Official terms and a rights review are preserved in docs/OST-RIGHTS-20261026.md and the private rights archive. Standalone music distribution/streaming is not cleared; Sonilo's published ordinary license excludes it. Game release eligibility through the Higgsfield/FAL route requires confirmation before public distribution. Do not include private generation receipts or signed media URLs in exports.

## Harbor material and bounded foundations (2026-10-27)

The project-specific generated images `quay-landing-wall-v2.png`, `quay-service-diffuse-v2.png`, `quay-workshop-floor-v1.png` and `quay-warehouse-foundation-v1.png` are copied byte-for-byte from the art-owner bundle at art-workshop/2026-10-27/harbor-integration-bundle-01/manifest.json. Original prompts, generation outputs and transformations remain in the referenced workshop folders. The two foundations are registered to the existing building pivot and hard-masked to its physical footprint; originals and diagnostic proxy composites are not substituted for these separate layers. Existing building images remain the reflection sources. These are AI-generated project assets, not claimed CC0 or exclusively copyrighted works; include them in the Steam AI-content inventory. The previous v1 wall and paving files are retained.

## JEONG SD revision — 2026-10-27

`assets/art/crew-sd-jeong-v2.png`, `crew-sd-idle-v2.png` and `crew-sd-jeong-strike-v2.png` are project AI-generated/edited character artwork based on user-provided reference and existing project art. This is not a CC0 or exclusive-copyright claim. Original candidates, generation/edit provenance and approximate strike registration are retained privately under `art-workshop/2026-10-26/jeong-slim-01` and `art-workshop/2026-10-27/jeong-strike-isolated-01`. Immutable hashes are in `art-workshop/2026-10-27/jeong-isolated-live-01/candidate-manifest.json`. Shared idle atlas differs only in JEONG's row; other rows were pixel-compared. Original v1 images remain fallback assets. Include these generated assets in the Steam AI-content inventory; private reference photos and prompts are not exported.

## 2026-10-27 shelter and rear-character revisions

AI-generated project artwork, integrated from reviewed internal art workshop:
- assets/art/quay-shelter-v1.png: shelter-only interior,1536x1024; existing workshop remains for service yards. Provenance: art-workshop/2026-10-27/shelter-handoff-01/manifest.json.
- assets/art/crew-sd-han-v2.png and crew-sd-woo-v2.png: isolated rear-row revisions. Original face/action cells outside the rear crop preserved; existing v1 assets retained as load-failure fallback. Provenance: art-workshop/2026-10-27/rear-character-handoff-01/manifest.json.
These assets introduce no third-party asset license. This records provenance, not independent copyright clearance. Collision geometry, pivots and gameplay are unchanged.

## Generated Woo complete side walking poses — 2026-10-27

assets/art/crew-sd-woo-side-walk-v3.png was made with the built-in image_gen tool using the existing project character as reference. The art owner approved the four complete registered poses; source prompts, generation and registration provenance remain in art-workshop/2026-10-27/woo-body-walk-02/HANDOFF.md and contract.json. The runtime uses pre-generated frames, with no live generation. Include this asset in the Steam pre-generated AI content disclosure. No exclusive copyright in purely generated material is claimed.


## Generated Park complete side walking poses — 2026-10-27

assets/art/crew-sd-park-side-walk-v3.png is project-specific built-in image_gen artwork based on the existing Park character. Four complete registered poses were approved for side-walking integration. Source prompts, generation and whole-frame registration records remain privately in art-workshop/2026-10-27/park-body-walk-01/HANDOFF.md and contract.json. No live generation, third-party game asset or exclusive-copyright claim. Include it in the Steam pre-generated AI content inventory.
## Generated scrap-bandolier icon — 2026-10-29

`assets/art/crew-upgrade-shot-v1.png` is a project-specific AI-generated image, copied unchanged from `art-workshop/2026-10-29/scrap-bandolier-icon-01/crew-upgrade-bandolier-candidate.png`. Prompt, raw output and review are preserved in that workshop folder. SHA256: `54a0590e3570fafaadb7657624d57547392ca9067f3e1a231567080fc06a04ac`. This is not a third-party CC0 asset; no exclusively human authorship is claimed. Include it in the Steam AI-content inventory. Root reviewed the actual 568px game reward row before promotion; phone-hardware approval remains unverified.


## Generated spine urchin and cone snail key poses — 2026-11-01

assets/art/spine-urchin-{idle,warning}-v1.png and cone-snail-{idle,warning,special}-v1.png reuse project-specific built-in image_gen artwork from art-workshop/2026-10-20/v5-in-game-threats. Registered512px poses, pivot[256,448], exact source/atlas/crop hashes and source isolation limitations are recorded in art-workshop/2026-11-01/fauna-urchin-cone-01/contract.json. Registration preserved the isolated raster pixels; source-to-atlas historical rounding and omitted source alpha are disclosed there. The runtime uses existing key poses, not live generation or third-party game art. Include these assets in the Steam pre-generated AI content inventory; no exclusive human authorship or exclusive copyright claim. Root reviewed actual568/960 source scenes before selecting this limited role: stationary urchin crown defense and left/right gliding cone-snail broadside. These are not complete walking/hurt/death animation suites. No Shattered Pixel Dungeon source or artwork was copied into this game.

## Registered abandoned net states — 2026-11-02

assets/art/abandoned-net-intact-v1.png and abandoned-net-local-v1.png are byte-identical selections from the project's existing image_gen artwork registered in art-workshop/2026-11-01/abandoned-net-registered-03. Canvas512, pivot256,256, world canvas160. SHA256 respectively221ae0d7caac93206b26a476611d48cbca422fead80eb9b0c7aab2d20673929c and db29d01e7432b757f097bcec8f8c26f0e89d81c8fcd9a3bad22731bb59978611. Exact source isolation and limitations are recorded in that contract. Native-size and maximum-zoom trial frames received bounded static visual acceptance; the original full-art contract remains on hold and residual source red pixels are not claimed removed. Include these pre-generated AI assets in the Steam content inventory; no exclusive human authorship claim. Workshop originals and prompts are not public runtime dependencies.

assets/art/abandoned-net-carried-v1.png is the unchanged registered image_gen carried02 sprite from art-workshop/2026-11-02/carried-net-sprite-02/net-carried.png, SHA256 9c475caa96a8d1e84b8a939c4be6086f7b90953a5a4a6a2f6bfc0b0032241c61. Canvas512, pivot256,256, world canvas256; measured alpha32 body200x114.5 world units. The image owner reviewed twelve actual trial frames and accepted bounded default static use at observed scales1.15/1.37143. Maximum-zoom softness/cropping, mobile dual-target framing and night fog masking remain separate limitations; the original full-art contract flags are unchanged. AI generation used the project's existing03 mesh only as a style reference. No external stock/CC0 license or exclusive human authorship is asserted. Include this pre-generated AI asset in the Steam content inventory; keep raw source, prompt and workshop provenance outside public runtime exports.

## Approved Jeong appearance — 2026-11-03

`assets/art/crew-sd-jeong-v3.png`, `crew-sd-jeong-idle-v3.png`, `crew-sd-jeong-strike-v3.png` and `crew-jeong-menu-v3.png` are project-specific pre-generated image_gen character artwork based on the user's approved slender body and subtle smile. They are byte-identical selections from `art-workshop/2026-11-03/jeong-approved-runtime-01/`. Original model/sprite references, prompts, rejected candidates, registration contracts and generation records remain in the private workshop. The main atlas and strike retain the approved raster pixels; added idle variants are uniformly registered. No external stock asset, CC0 license, exclusive copyright or wholly human authorship is asserted. Include these four assets in the Steam pre-generated AI content inventory. Original runtime images remain available; private photos, prompts and workshop receipts are not exported.


Near-wall candidate materials (2026-11-04): cliff-top-v2.png, cliff-crown-v2.png, near-wall-body-v1.png and near-wall-cap-v1.png are original project image_gen outputs. Exact sources/hashes and retained crop limitations: assets/art/NEAR-WALL-PROVENANCE.json, art-workshop/2026-11-04/production-cliff-materials-01/generation-record.json and near-wall-dedicated-sheet-01/generation-record.json in the private source workspace. No external stock/sprite or OSS license is asserted; generated-service terms and reference rights apply. Earlier art remains preserved.


## Unpublished parry feedback review — 2026-11-04

`assets/art/crew-sd-park-parry-active-hold-upper-v1.png`, `assets/art/crew-sd-park-parry-success-snap-upper-v1.png`, `assets/art/crew-sd-park-parry-whiff-recover-upper-v1.png`, `assets/art/crew-sd-park-parry-riposte-ready-upper-v1.png`, `assets/art/crew-sd-park-parry-keyposes-v1.png`, `assets/art/crew-sd-woo-parry-active-hold-upper-v2.png`, `assets/art/crew-sd-woo-parry-success-snap-upper-v2.png`, `assets/art/crew-sd-woo-parry-whiff-recover-upper-v2.png`, `assets/art/crew-sd-woo-parry-riposte-ready-upper-v3.png`, `assets/art/crew-sd-woo-parry-keyposes-v3.png`, `assets/art/crew-sd-woo-parry-lower-v2.png`, `assets/art/shore-parry-contact-fx-v1.png` are project-specific pre-generated image_gen resources. They are not third-party game sprites or CC0 stock, and no exclusive copyright or wholly human authorship is asserted. Include adopted resources in the Steam pre-generated AI inventory. Runtime uses prepared images; no live generation. Exact prompts, original outputs, source contracts, masks, authored repairs and limited art acceptances remain in private art-workshop/2026-11-04/shore-parry-park-motion-01, shore-parry-park-upperbody-01, shore-parry-woo-motion-01/revision-02 and revision-03, and shore-contact-fx-01. Provenance receipts in this review identify exact SHA256/source paths. No private photo, prompt or workshop receipt belongs in public runtime exports. These copies are frozen for private integration only; full character/direction/transition acceptance and public release approval are pending. Original audio cues use existing project anchor audio plus synthesized tones; no new external audio asset/license.


## Han side parry review — 2026-11-04

`assets/art/crew-sd-han-parry-active-hold-upper-v1.png`, `assets/art/crew-sd-han-parry-success-snap-upper-v1.png`, `assets/art/crew-sd-han-parry-whiff-recover-upper-v1.png`, `assets/art/crew-sd-han-parry-riposte-ready-upper-v1.png`, `assets/art/crew-sd-han-parry-lower-v1.png` are project-specific pre-generated image_gen resources. Head and original visible lower legs are retained according to the art owner's protected masks; pose torso/arms/bag/strap and newly exposed cloth are authored generated pixels, not recovered historical source. No external game sprite, CC0 license, exclusive copyright or wholly human authorship is asserted. Include adopted images in the Steam pre-generated AI inventory. Prompts, originals, rejected masks, corrected crown clipping and exact pivot/ref375/two-column contracts remain privately in art-workshop/2026-11-04/shore-parry-han-{hold,success,whiff,ready}-01. Provenance records here identify exact hashes. Runtime uses prepared images only. Do not export private photos, prompts or workshop evidence. Actual side/phase captures and one input flow have limited review; front/rear, Jeong and human/device acceptance remain open.


## Jeong side defense art — 2026-11-04

`assets/art/crew-sd-jeong-parry-active-hold-upper-v1.png`, `assets/art/crew-sd-jeong-parry-success-snap-upper-v1.png`, `assets/art/crew-sd-jeong-parry-whiff-recover-upper-v1.png`, `assets/art/crew-sd-jeong-parry-riposte-ready-upper-v1.png`, `assets/art/crew-sd-jeong-parry-lower-v1.png` are project-specific pre-generated image_gen resources. Original approved head, hip calibration and visible lower legs remain protected by the art owner contracts; newly exposed uniform cloth and defensive arms/tool poses contain newly authored generated pixels. No external game sprite, CC0 license, exclusive copyright or wholly human authorship is asserted. Include adopted images in the Steam pre-generated AI inventory. Original/private reference photos, prompts, rejected cells and masks stay private in art-workshop/2026-11-04/shore-parry-jeong-{hold,three-keys}-01. Runtime uses four uppers/shared lower only, not export sheets. Canvas512, pivot256448, reference362, original2column cadence and atomic normalv3 bundle remain. Actual side static captures have limited review; temporal/input/front/rear/human/device approval is separate.


## Jeong ready revision02 — 2026-11-04

`assets/art/crew-sd-jeong-parry-riposte-ready-upper-v2.png` is a project-specific pre-generated image_gen masked revision of the preceding Jeong ready upper. It replaces only the selected ready upper at runtime; original approved head, belt core, lower pixels and pivot/socket contract remain protected. New tool/hand pixels are newly authored generated content. Keep it in the Steam pre-generated AI inventory; no external game sprite or third-party CC0 license, exclusive copyright or wholly human authorship is asserted. Prompts, rejected previous ready overlap and original contracts stay privately in art-workshop/2026-11-04/shore-parry-jeong-ready-02. Runtime loads this resource instead of v1, not both; older files/builds remain preserved. Limited same-scene side/phase review is separate from human/device/front-rear acceptance.


Story1 industrial prop replacement (2026-11-04): story1-cutter-base-v1.png, story1-cutter-rotor-v1.png, story1-floating-steel-v2.png, story1-gate-closed-v2.png and story1-gate-open-v2.png are project-specific pre-generated image_gen resources, not third-party game sprites or CC0 stock. No exclusive copyright or wholly human authorship is asserted. Include these adopted images in the Steam pre-generated AI inventory. Runtime loads prepared images only. Exact generated originals, prompts, rejected versions and authored separation/normalization contracts remain privately in art-workshop/2026-11-04/story1-missing-props-01 (contract-v2.json). Existing fleet, harbor and crew atlases retain their preceding provenance. Do not export private photos, prompts or workshop receipts. Visual envelopes/pivots preserve original aspect ratios; collision bodies are separate and unchanged. Actual scene reviews and their limits are recorded separately.


Skippable voyage presentation (2026-11-04): dredger-outro-{ignition,burst,smoke}-512.png and region-{1,2,3}-clear-background.png are original project pre-generated image_gen assets, not external game sprites/CC0 stock. No exclusive rights or wholly human authorship are asserted. Include adopted images in the Steam pre-generated AI inventory. Runtime uses prepared images, not live generation. Exact originals, prompts, rejected concept and normalization/pivot contracts remain private in art-workshop/2026-11-04/boss-outro-region-clear-01. The concept-only fullscene is excluded. Existing defeated dredger is reused under its preceding provenance. Narrative text is separately supplied in experiments/story-region-cards-20261104/region-cards.json and rendered as HTML, not baked into images. No private photo/prompt/workshop receipt is included in public runtime exports. Limited actual-scene acceptance is separate from full gameplay/device verification.


## Guardian pressure contact art — 2026-11-04

assets/art/dev9-guardian-pressure-contact-{early,peak,disperse}.png are project-specific pre-generated image_gen resources. Existing dev9-pump-jet-jet-a/b.png water material is reused without new third-party assets. No external game sprites, exclusive copyright or wholly human authorship is asserted. Include adopted images in the Steam pre-generated AI inventory. Private prompt, original sheet, extraction and pivot contracts remain in art-workshop/2026-11-04/guardian-pressure-art-01 and must not be exported as runtime assets. Runtime uses prepared images only; actual scene acceptance is separate from generation.


## Player guardian pressure stream — 2026-11-04

assets/art/dev9-guardian-pressure-player-jet-{a,b}-v2.png are project-specific pre-generated image_gen edits for the player support stream. Existing pump warden stream assets remain unchanged. Private original edit output, prompt, uniform-scale normalization and socket contracts remain in art-workshop/2026-11-04/guardian-pressure-player-jet-02. No external game sprites, exclusive copyright or wholly human authorship is asserted; include adopted images in the Steam pre-generated AI inventory. Prepared-image runtime only, no live generation. Private workshop materials are excluded from runtime exports.


## Additional original pre-generated AI artwork — 2026-11-05

The project-specific files `assets/art/dev9-machine-heart-idle-v1.png`, `assets/art/dev9-machine-heart-warn-v1.png`, `assets/art/dev9-machine-heart-idle-loop-v1.png`, and `assets/art/voyage-harbor-ui-v1.png` are built-in OpenAI image_gen outputs prepared from original project artwork/reference material. Exact adopted runtime bytes are matched to the retained private source and registration contracts. These files do not introduce an external stock/game-sprite license. No CC0 status, exclusive copyright or wholly human authorship is asserted; generated-service terms and reference rights apply.

Include these four adopted files in the Steam pre-generated AI content inventory when preparing the content survey. Generation sources, private prompts, original photographs, workshop concepts and review receipts are not runtime assets and must not be exported. A scoped beta art adoption does not assert complete attack/death animation, human readability, device performance or Steam readiness.

## Project lighthouse tab icons — 2026-11-05

`assets/social/last-signal-favicon-32-v1.png` and `last-signal-favicon-48-v1.png` are original project pre-generated image_gen artwork. They reuse unchanged PNG bytes from the retained2026-11-02 icon candidate, adopted after a separate32/48px readability review on2026-11-05. They are not external game icons or CC0 stock; no exclusive rights or wholly human authorship is asserted. Include these two files in the Steam pre-generated AI inventory. Private original, prompt and prior unintegrated contract stay in art-workshop/2026-11-02/last-signal-favicon-01 and are not runtime exports. Only the reviewed32/48PNG files are adopted; larger sizes, ICO and source sheets are not included by this adoption.

## Distribution build tooling (2026-11-05)

esbuild 0.28.2, Copyright (c) 2020 Evan Wallace, MIT License. Build-only dependency; the development tool and its dependency tree are not shipped with the game. Exact license: scripts/distribution-protection/licenses/esbuild-MIT.txt. Official source: https://github.com/evanw/esbuild . Existing runtime asset and third-party notices remain unchanged.

Exact build-tool MIT license:

MIT License

Copyright (c) 2020 Evan Wallace

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.


## Rig force response sprites — 2026-11-05

assets/art/rig-standard-sheet.png, rig-bilge-sheet.png and rig-winch-sheet.png derive from three project-specific OpenAI image_gen generation events (nine aligned keys), using only this project’s gameplay art as the style reference. Original sources/prompts and exact equal-cell registration records remain in the private art workshop. Runtime canvas, common pivots, world scale and source digests are recorded in assets/art/RIG-FORCE-PROVENANCE.json. These are pre-generated player-facing AI assets, not CC0 stock or live generation. Include them in the Steam pre-generated AI content inventory; no exclusive copyright or wholly human authorship claim. Actual standard/bilge placement and the winch single-rope response received bounded scene acceptance, not whole-motion, human-enjoyment or physical-phone approval.


## Pump closed-valve plate edit — 2026-11-05

assets/art/dev9-pump-warden-valve-closed.png (SHA256 a60a3e14b7ca32ecb5ea6921dbc5e27ee03e77b644c644ffb0d502ceaf1933b3) is a pre-generated OpenAI image_gen edit, one generation event, of this project’s existing closed-valve artwork. The authored masked composite retains the original512×512 canvas, pivot[256,448], .024 world units per pixel, protected pipe/base pixels and physical footprint; the existing open-valve image is unchanged. Original prompt, generated source, mask, processing script and source/output digests remain in the private art-workshop/2026-11-05/pump-valve-lock-readability-02 contract. No new external stock, CC0 status, exclusive generated copyright or wholly human authorship is claimed. Fixed artwork only; no live generation. Include this incremental edit in Steam pre-generated AI disclosures. Preparation pending final bounded art/UI acceptance; existing PC three-scene review does not establish motion, phone performance or human approval.

Source40 integration update: designated art/UI owners and root accepted only the existing1280×800 static PC scenes; see private ACTUAL-PC-REVIEW-03.md, UI02 visual-review.json and renderer03/root-review.json. The earlier preparation-pending status and original contract flags are historical; mobile, continuous motion and human/performance acceptance remain unestablished.


## Mechanical heart stopped-state edit — 2026-11-05

assets/art/dev9-machine-heart-stopped-v1.png (SHA256 ae155273d8f76476cecf492638416e9efec61010a84220b525ecabe391963d47) is one pre-generated OpenAI image_gen edit of this project’s existing mechanical-heart idle artwork. The authored masked composite preserves the original512×512 canvas, pivot[256,448], reference body400px/world height28 (.07 world units per pixel), protected lower base pixels and existing physical footprint. It is a fixed stopped-state image; no live generation or stopped animation loop. Private source, prompt, mask, processing and original/output hashes remain in art-workshop/2026-11-05/machine-heart-stopped-01/contract.json. No new external stock, CC0 status, exclusive generated copyright or wholly human authorship is claimed. Include this incremental edit in Steam pre-generated AI disclosures. Root has bounded static PC dead/won scene evidence; final designated art/UI confirmation and integration gates remain pending. No mobile, continuous motion, physical-phone or human acceptance claim. Existing assets, licenses and reserved father-face work remain untouched.

Source41 integration update: designated art/UI owners and root accepted only the existing1280×800 static dead-body and KO-result PC scenes; see private machine-heart-stopped01/ACTUAL-PC-REVIEW-02.md, result-summary01/visual-review.json and homecoming renderer02/root-review.json. The earlier preparation-pending status and original contract flags are historical; mobile, continuous motion and human/performance acceptance remain unestablished.


## W land-wall body material — 2026-11-05

assets/art/near-wall-W-body-v1.png (SHA256 ec9e1aaa1428ad7de1ecf53afd9be1c80af395211de555684c715a7df9b757ed) is the selected fixed pre-generated OpenAI image_gen material from two generation calls. It uses this project’s existing wall body/cap/role sheet as references; no external stock was introduced. Original sources, two prompts, mask, processing script and output/reference hashes remain in private art-workshop/2026-11-05/W-role-material-candidate-01/contract.json. The512×256 body uses the existing19.2 world-unit tangent period,9.6 body/2.4 cap height and original role/owner/UV/fog contracts; shared cap and original N/coastal/E/S materials remain. Material foot detail stays inside the original body. W land-wall body selection and retained original crown coverage are presentation only; no simulation/camera/survey change is intended. One actual PC W-scene art review is bounded acceptance; mobile follow-up and integrated43 checks are pending. Not CC0, exclusive generated copyright or wholly human authorship; no live AI. Include the selected asset and two generation calls in incremental pre-generated AI disclosures.

Integration43 bounded update: explicit root approval accepts existing mobile02 won/nav44px and W connection captures only, plus artist actualPC W-scene acceptance. Earlier contract/preparation pending flags remain historical. Heart natural radio expiry/base restoration was prevented by an actual natural defeat and remains unverified; pure cache guards are distinct. No mobile/human/FPS/whole-wall or sound04 approval follows.


## Connected-mass top raster and sampled mechanical latch — 2026-11-05

assets/art/cliff-top-connected-mass-v1.png (SHA256 717cff67ab517c14126f9ab1a3cdf45013681870c746d00cec97f269b791e032) is one pre-generated OpenAI image_gen call, uniformly resized to512×512. Prompt, generated original and exact reference/output hashes remain in private art-workshop/2026-11-05/connected-mass-top-raster-01/contract.json. This is painted-volume material in the existing z12/worldXY÷19.2 top domain; no new geometry, cutaway, ownership, collider or numeric shoulder. No new external stock, CC0 designation, exclusive generated copyright or wholly human authorship is claimed for this image. Include one new image-generation call in pre-generated AI disclosures; no live AI. PC art review is bounded; mobile/integration acceptance remains pending.

assets/audio/latch.ogg (SHA256 ef29c3943ee701616f65e3d596c13eb3ff6b11ca5b3ac01e7bc923366a5c6f76) is the byte-exact Kenney Sci-Fi Sounds1.0 Audio/impactMetal_003.ogg from third-party-source/kenney_sci-fi-sounds.zip, CC0 1.0. Exact original License.txt bytes are already retained in assets/licenses/Kenney-SciFi-CC0.txt. No audio generation or sample editing; existing player uses at most160ms with50ms tail fade, cue gain0.4 and existing effects/master/focus buses. Root selected this sample to address prior electronic-explosion feedback; no user listening/semantic acceptance or live BGM-masking claim. Synthesized04 preview remains excluded.

Integration45 bounded update: root accepts PC art view plus mobile art-only44 capture with most interior top obscured; no full material aesthetics/height recognition claim. Mobile review retained44 audio and did not test this CC0 sample. Combined45 sample decode and prior OfflineAudioContext evidence are separate. Root accepts sample integration as feedback correction; user listening acceptance remains false.


## Reused AI low-ground and low-edge material (evaluation52)

assets/art/unserviced-ground-v1.png reuses the project bedrock-v3 image byte-for-byte (SHA256 4961d1b47b89ea93af42ae014ffccc8c189877d0b6209c28475055dd2390b910). The existing cliff-face-v1.png supplies low side material. Both are existing project-specific OpenAI image_gen assets based on project references; no new generation, processing or external stock was added. Existing generated-service terms and rights in the project references apply. No CC0 or exclusive copyright claim is made. Original prompts, source imagery and separate ground/low-edge role contracts remain preserved in the private AI-content review inventory.
Ground/coping use world XY period19.2; low side retains existing7.68-world drop and2.544-world coping width. The side V reference12 defines texture density, not new geometry height. Original raised-cliff HOLD remains. Owner acceptance is limited to one static material-separation scene; not natural-coast/fog/GPU/phone-performance or gameplay acceptance.


## Evaluation53 retained GPU material route
The existing evaluation52 low-ground/coping raster and original side image are unchanged. The retained GPU route now explicitly opts in only for experimental shared frames at depth>0 without a cliff mask, with gate/material revision in its cache key. Owner GPU art acceptance remains one static scene of material-role separation; not coast geometry, actor/filtering equality, WebGL1/context-loss, all fog/fleet or phone FPS acceptance. Original source/role contracts, AI provenance and non-CC0/non-exclusive-rights notices remain preserved.
