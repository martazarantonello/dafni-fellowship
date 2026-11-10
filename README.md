# Probabilistic Risk of Complex Infrastructure Networks

**DAFNI Fellowship 2026–2027 · Dr Ji-Eun Byun, Imperial College London**

Website: **https://martazarantonello.github.io/dafni-fellowship/**

This Fellowship brings a framework that uses probability-based modelling to assess the system-level risk of interconnected transport networks onto the [DAFNI](https://www.dafni.ac.uk/team/ji-eun-byun/) platform, working out how likely the network as a whole is to fail based on the performance of its individual components. It demonstrates the approach on the Eastern Massachusetts highway network under sequences of earthquakes and windstorms, ranks which links matter most to keeping the population connected, and shares the resulting models with infrastructure operators, public bodies and other DAFNI users. A full-day hands-on workshop, "Probabilistic Risk Modelling for Infrastructure Resilience", will bring participants from the basic ideas of probability through to driving the tool themselves; details and outputs are on the website.

Partners: [DAFNI](https://www.dafni.ac.uk/) · [UK Research and Innovation](https://www.ukri.org/) · [Imperial College London](https://www.imperial.ac.uk/)

---

This repository holds the source of the Fellowship website (`index.html` and `assets/`), served by GitHub Pages from `main`. The site itself follows the same layout as the [DAFNI Fellowship page by Yitian Dai](https://yitiandai.github.io/dafni-fellowship/): hero, partner logos, what the Fellowship is about, updates timeline, the models on DAFNI, workshop with proposed agenda, outputs and contact.

```
dafni-workshop-site/
├── index.html            # the whole site (CSS and JS inline)
├── .nojekyll             # tells GitHub Pages to serve the files as they are
└── assets/
    ├── images/
    │   ├── ema-network.png     # hero figure, drawn from dafni_modelling/networks/EMA
    │   ├── bn-model.png        # workshop figure: the tensor-based Bayesian network structure
    │   ├── dafni-logo.jpg      # partner logo
    │   ├── ukri-logo.png       # partner logo
    │   └── imperial-logo.png   # partner logo
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
| Practical guide and report titles and dates | Outputs section |

Also check the drafts written from the code repository: the project title, the workshop aims, and the proposed agenda (its times copy the structure of the reference page). Update the "Last updated" date in the Updates section when you edit.

## Content sources

- Fellow, duration and contacts: `dafni_modelling/model_definition.yaml` and the supervisor's instructions.
- Models on DAFNI: `model_definition.yaml` in `dafni_modelling`, `dafni_inference`, `dafni_inference_cond` and `dafni_importance`.
- Workshop activity: `examples/workshop/workshop.ipynb`.
- Network size and figure: `dafni_modelling/networks/EMA`.
- Bayesian network structure figure (`bn-model.png`) and Dr Byun's bio: Fellowship model definition and her [DAFNI team page](https://www.dafni.ac.uk/team/ji-eun-byun/).
