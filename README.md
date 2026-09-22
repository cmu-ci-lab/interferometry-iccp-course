# Interferometry @ ICCP Summer School

Build a Michelson-style interferometer on a breadboard, align it to see white-light
interference fringes, and use it as a time-domain OCT scanner to recover a depth map of a coin.

## Where to start

**Follow the guide at [cmu-ci-lab.github.io/summer-school](https://cmu-ci-lab.github.io/summer-school/)** (or open [`index.html`](index.html) locally). It walks through the full
lab — construction, alignment, and OCT scanning — with photos and videos of every step.
Open it in a browser after cloning (it loads its media from `instructions_media/`, so keep
the two together):

```bash
git clone https://github.com/cmu-ci-lab/summer-school.git
cd summer-school
open index.html               # macOS; on Windows just double-click it
```

## Quick start (software only)

```bash
./setup.sh                    # builds the iccp-oct environment (conda or .venv)
conda activate iccp-oct       # or: source .venv/bin/activate
python test_hardware.py       # sanity-check the stage + camera
python visualizer.py          # live camera view + coherence scan panel
```

## Page assets

`shared/` holds the Carnegie Mellon computational imaging lab's shared web assets — the Lato
webfont, Font Awesome Free, the lab logo and the favicon — and `index_files/style.css` is the
guide's stylesheet, built on the lab's design tokens. These are a **vendored copy**: the source
of truth is the `shared/` directory of the lab's `website_templates` repository, which is served
at `/shared/` on `imaging.cs.cmu.edu`. This site is published from a different origin at a
project subpath, so a root-absolute `/shared/` URL cannot resolve here and the files are kept
alongside the guide instead. Every reference is relative, so the guide renders correctly both on
GitHub Pages and when `index.html` is opened straight from a clone.

---

Disclaimer: Claude (Anthropic) was used to assist with part of the code base as well as
formatting of the instructions.
