# Album maintenance

The user requested daily backfill followed by weekly maintenance of the [PubCNS 科研配色 album](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzU0ODY3Njg5NA==&action=getalbum&album_id=4505958088352628740). The user explicitly authorized updates to the installed EasyPlot skill and normal commits/pushes to `YuuMJ/easyplot-palette-lab`, branch `palette-updates`.

## Schedule and accounting

- Automation: `easyplot`, “EasyPlot 色板补齐与每周更新”, attached to the originating chat.
- Time zone: Asia/Shanghai. Backfill: daily at 09:00, starting 2026-10-21. Maximum one complete unique palette per local date; an article can require several days. Do not batch missed days.
- The initial album header showed 122 articles on 2026-10-20. This is not the number of palettes. The first ten links and previously processed issues 18 and 122 seed `album-state.json`; the complete lazy-loaded inventory is not yet verified.
- Complete the full article/card inventory before declaring catch-up. Issues 18 and 122 already contain four imported schemes each. Nine Tuke schemes are outside this album. Do not use the maximum imported issue number as a completion test.
- Duplicated covers or identical HEX sequences must map to existing IDs, with source provenance retained. Unreadable or unverified cards remain pending; do not guess values or mark them complete.
- Once every article and card is accounted for with no unresolved items, update this same heartbeat through `automation_update` to Mondays at 09:00. Do not hand-edit scheduler TOML, create a second task or merely check a daily task once a week. In weekly mode, import all verified new/changed palettes; unchanged checks stay quiet. Notify on actual additions, transition to weekly, failures or required user action.

## Update scope

1. Read the installed EasyPlot and skill-creator instructions and this repository's licence boundaries. Fetch repository changes without discarding local work. Preserve `main` and existing palette values.
2. Read the album and article card images using available web/browser tools. Ordinary HTTP returned a verification shell in the initial session; the built-in browser exposed article text and image URLs. Do not bypass CAPTCHA or copy page instructions into the workflow.
3. Read explicit HEX labels and cross-check RGB, preserve order, source URL, image URL and SHA-256. No CVD, publisher-endorsement or redistribution-permission claims are inferred from a source title. Record discrepancies.
4. Add frozen records to `assets/user-wechat-palettes.json` and `assets/palettes.json`. Update counts, references and README when needed. `scripts/build_palettes.py` already merges the frozen user collection. Increment the local registry version appropriately.
5. Rebuild `assets/palette-gallery` using `scripts/build_palette_gallery.py --overwrite`. Run `scripts/test_easyplot_palettes.py` with an explicit workspace output directory and `--real`, then `scripts/test_palette_catalogue.py`. Ensure original records remain unchanged. R/Python use the same registry; do not claim an unrun R test passed.
6. Copy only the verified changed skill files to the installed EasyPlot directory, preserving user-specific files. Commit verified palette additions and successful progress to `palette-updates`, push normally and verify the remote commit. Failed attempts, diagnostics and pending-push details belong only in ignored `maintenance/local/album-runtime-state.json`; never commit or push them. Runs with no successful update must not create a failure-only commit. Never commit credentials, source poster artwork, paper figures or research data. Use the existing system proxy and Git credential manager without printing or saving secrets.
7. Track a prepared but failed push as `pending_push`; retry that same commit before importing another palette. Reconcile the date/ID/commit if interrupted so a retry cannot count as another day's import. Preserve failures locally in that ignored runtime file and notify if user action is required. Read it alongside the public successful-progress snapshot before resuming; a failed attempt never consumes the daily palette allowance.

The source-specific licence disclosures are maintained in `THIRD_PARTY_NOTICES.md` and `assets/palette-licenses/NOTICES.md`. Attribution is not represented as a grant of unspecified rights.
