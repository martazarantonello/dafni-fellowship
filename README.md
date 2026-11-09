# DAFNI Fellowship workshop site

Static one-page site (no build step) for the DAFNI Fellowship workshop on probabilistic risk modelling of infrastructure networks. It follows the structure of the [DAFNI Fellowship page by Yitian Dai](https://yitiandai.github.io/dafni-fellowship/): hero, partner logos, what the Fellowship is about, updates timeline, the models on DAFNI, workshop with proposed agenda, outputs and contact.

```
dafni-workshop-site/
├── index.html            # the whole site (CSS and JS inline)
├── .nojekyll             # tells GitHub Pages to serve the files as they are
└── assets/
    ├── images/
    │   └── ema-network.png   # hero figure, drawn from dafni_modelling/networks/EMA
    └── resources/            # put PDFs here (poster, guide, report)
```

## Preview locally

```bash
cd dafni-workshop-site
python -m http.server 8000
```

Then open <http://localhost:8000>.

## Publish on GitHub Pages

1. Copy this folder's contents into the root of a new repository (for example `dafni-workshop`), or keep the folder in this repository and publish it from a branch.
2. On GitHub: **Settings → Pages → Build and deployment → Deploy from a branch**, choose `main` and `/ (root)`.
3. The site appears at `https://<your-user>.github.io/<repository>/`.

## Before publishing: items to confirm

Everything highlighted in yellow on the page (class `tbc` in `index.html`) is a placeholder. Search for `class="tbc"`:

| Item | Where |
|---|---|
| Workshop date, venue and registration route | Workshop section, timeline |
| Month of the "models published on DAFNI" milestone | Updates section |
| Partner logos (DAFNI, UKRI, Imperial College London) | Three dashed boxes under the hero. Add the image files to `assets/images/` and replace each box as described in the comment above them |
| Practical guide and report titles and dates | Outputs section |

Also check the drafts written from the code repository: the project title, the workshop aims, and the proposed agenda (its times copy the structure of the reference page). Update the "Last updated" date in the Updates section when you edit.

## Content sources

- Fellow, duration and contacts: `dafni_modelling/model_definition.yaml` and the supervisor's instructions.
- Models on DAFNI: `model_definition.yaml` in `dafni_modelling`, `dafni_inference`, `dafni_inference_cond` and `dafni_importance`.
- Workshop activity: `examples/workshop/workshop.ipynb`.
- Network size and figure: `dafni_modelling/networks/EMA`.
