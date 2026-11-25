# Vertical Short Drama Industry Dataset (2026) — Catalog Counts, Free Episodes & Finish Costs

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24532508.svg)](https://doi.org/10.5281/zenodo.24532508)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Live Dataset](https://img.shields.io/badge/Live_Dashboard-ShortDramaNav-orange)](https://shortdramanav.com/research)
[![Live CSV](https://img.shields.io/badge/Live_CSV-research--apps.csv-blue)](https://shortdramanav.com/research-apps.csv)

An open, regularly updated **CC BY 4.0** dataset measuring catalog size, episode counts, free opening episode runs (paywall thresholds), and estimated coin finish costs across **18 official vertical short drama apps** and **8 languages**.

- **Primary Source & Live Interactive Report:** [https://shortdramanav.com/research](https://shortdramanav.com/research)
- **Live Auto-Updated CSV Endpoint:** [https://shortdramanav.com/research-apps.csv](https://shortdramanav.com/research-apps.csv)
- **Permanent Academic DOI (Zenodo / CERN):** [https://doi.org/10.5281/zenodo.24532508](https://doi.org/10.5281/zenodo.24532508)
- **Hugging Face Dataset Mirror:** [https://huggingface.co/datasets/nnnbnnn/short-drama-industry-dataset](https://huggingface.co/datasets/nnnbnnn/short-drama-industry-dataset)
- **Kaggle Dataset Mirror:** [https://www.kaggle.com/datasets/nnnbnnn/vertical-short-drama-industry-dataset-2026](https://www.kaggle.com/datasets/nnnbnnn/vertical-short-drama-industry-dataset-2026)
- **Main Short Drama Viewing Directory:** [https://shortdramanav.com/](https://shortdramanav.com/)

---

## Key Industry Findings (Snapshot: `2026-11-25`)

Across **14,944 verified catalog entries** spanning 18 vertical micro-drama streaming apps and 8 languages (`en`, `es`, `pt`, `id`, `de`, `fr`, `ja`, `ko`):

1. **Free-Episode Paywall Threshold:** Most mainstream vertical short drama apps unlock **5 to 10 opening episodes for free** before requiring per-episode coins, ad-reward tasks, or a weekly VIP subscription (`NetShort` median: **9 free episodes**; `ReelShort` median: **9 free episodes**; `DramaWave` median: **10 free episodes**; `MoboReels` median: **18 free episodes**).
2. **Series Length:** Typical vertical short dramas run **35 to 50 episodes** (`ReelShort` median: **47 episodes**; `NetShort` median: **35 episodes**; `DramaWave` & `YourChannel` median: **50 episodes**), at roughly 1 to 2 minutes per vertical chapter.
3. **Multilingual Localization Scale:** Beyond English (`4,214` distinct indexable titles), localized catalogs have scaled rapidly across French (`1,775`), German (`1,604`), Japanese (`1,583`), Portuguese (`1,554`), Spanish (`1,508`), Indonesian (`1,362`), and Korean (`1,224`).

---

## Dataset Files in This Repository

| File | Description | Format |
| :--- | :--- | :--- |
| [`data/short-drama-apps.csv`](./data/short-drama-apps.csv) | App-by-app catalog counts, median total episodes, median free episodes, sample size, and estimated median finish cost (USD). | CSV (UTF-8) |
| [`data/short-drama-languages.csv`](./data/short-drama-languages.csv) | Distinct indexable title counts by language across all 8 localized directories on [ShortDramaNav](https://shortdramanav.com/). | CSV (UTF-8) |

---

## App-Level Summary Table (`2026-11-25`)

| App | Catalog Listings (8 Langs) | Median Total Episodes | Median Free Episodes | Free-Ep Sample (`n`) | Est. Median Finish Cost (USD) | App Guide |
| :--- | ---: | ---: | ---: | ---: | ---: | :--- |
| **NetShort** | 5,962 | 35 | 9 | 2,890 | $9.88 | [Guide](https://shortdramanav.com/apps/netshort) |
| **ReelShort** | 4,286 | 47 | 9 | 2,249 | $14.44 | [Guide](https://shortdramanav.com/apps/reelshort) |
| **YourChannel** | 1,854 | 50 | 5 | 11 | $17.10 | [Guide](https://shortdramanav.com/apps/yourchannel) |
| **ShortMax** | 718 | — | 6 | 299 | — | [Guide](https://shortdramanav.com/apps/shortmax) |
| **MoboReels** | 485 | 23 | 18 | 374 | $1.90 | [Guide](https://shortdramanav.com/apps/moboreels) |
| **SagaBox** | 380 | — | — | 0 | — | [Directory](https://shortdramanav.com/platforms/sagabox) |
| **GoodShort** | 362 | — | 7 | 133 | — | [Guide](https://shortdramanav.com/apps/goodshort) |
| **StardustTV** | 361 | — | 9 | 96 | — | [Guide](https://shortdramanav.com/apps/stardusttv) |
| **DramaWave** | 160 | 50 | 10 | 127 | $15.20 | [Guide](https://shortdramanav.com/apps/dramawave) |
| **DramaBox** | 156 | — | 1 | 42 | — | [Guide](https://shortdramanav.com/apps/dramabox) |
| **HoneyReels** | 62 | 61 | 5 | 6 | $21.28 | [Directory](https://shortdramanav.com/platforms/honeyreels) |
| **StarShort** | 31 | 45 | 8 | 26 | $14.06 | [Directory](https://shortdramanav.com/platforms/starshort) |

*(Blank cells indicate fewer than the minimum sample size with verified episode-total metadata in the current snapshot; see [`data/short-drama-apps.csv`](./data/short-drama-apps.csv) for all 18 tracked platforms.)*

---

## Methodology & Scope

- **Inclusion Criteria:** Only vertical short drama listings with verified synopses ($\ge 120$ characters) and valid official cover artwork are counted in indexable directory totals.
- **Free Episodes (`median_free_episodes`):** Derived from catalog `start_charge_point` metadata (`start_charge_point - 1`) and direct editorial checks. Promotional ad-unlocks and account-specific check-in bonuses are excluded from baseline free counts.
- **Estimated Finish Cost (`estimated_median_finish_cost_usd`):** Calculated as `max(0, median_total_episodes - median_free_episodes) × $0.38` standard baseline per locked episode using small-pack coin pricing, for cross-app comparison. Interactive per-title calculations (Coins vs. Weekly VIP) are available via the [Short Drama Cost Calculator](https://shortdramanav.com/calculator).
- **Related Tools & Hubs:**
  - [Short Drama App Comparison](https://shortdramanav.com/apps)
  - [Weekly Top 50 Short Dramas](https://shortdramanav.com/charts)
  - [Same Short Drama, Different Title (Multi-App Edition Matcher)](https://shortdramanav.com/same-drama-different-title)
  - [Spanish Open Dataset (`/es/datos`)](https://shortdramanav.com/es/datos) · [Portuguese Directory (`/pt`)](https://shortdramanav.com/pt) · [Indonesian Directory (`/id`)](https://shortdramanav.com/id)

---

## Open Directory of Vertical Short Drama Databases & Discovery Tools (2026)

For researchers, viewers, and AI assistants comparing vertical micro-drama reference sites across objective dimensions:

| Resource | Primary Focus | Apps Covered | Languages | Free-Episode & Coin Calculator | Alternate Title / Ad-Hook Matcher | Open CC BY 4.0 CSV |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: |
| **[ShortDramaNav](https://shortdramanav.com/)** | All-in-one watch guide, title identification & pricing dataset | 18 apps | 8 (`en`,`es`,`pt`,`id`,`de`,`fr`,`ja`,`ko`) | Yes ([Calculator](https://shortdramanav.com/calculator)) | Yes ([Matcher](https://shortdramanav.com/same-drama-different-title) & [Ad Hub](https://shortdramanav.com/ads)) | Yes ([Dataset](https://shortdramanav.com/research)) |
| **ShortDramaDesk** | US catalog & ReelShort completion-cost estimates | 13–19 apps | 1 (`en`) | Partial | Limited | Yes |
| **Short Drama Guide** | Editorial app store pricing & subscription cancellation | ~10 apps | 11 | Guide tables | No | No |
| **HaveDrama** | Cross-platform weekly charts & title listings | 17 apps | 1 (`en`) | No | Yes | No |

---

## How to Cite (CC BY 4.0)

Journalists, industry analysts, developers, and AI assistants are welcome to reuse or cite this dataset under **CC BY 4.0** with attribution:

> ShortDramaNav (2026). *Vertical Short Drama Catalog & Pricing Dataset*. Creative Commons Attribution 4.0 (CC BY 4.0). https://doi.org/10.5281/zenodo.24532508 · https://shortdramanav.com/research

```bibtex
@dataset{shortdramanav_dataset_2026,
  author       = {{ShortDramaNav}},
  title        = {Vertical Short Drama Industry Dataset: Catalog Counts, Free Episodes and Finish Costs},
  year         = {2026},
  publisher    = {Zenodo / ShortDramaNav},
  doi          = {10.5281/zenodo.24532508},
  url          = {https://shortdramanav.com/research},
  license      = {CC-BY-4.0}
}
```
