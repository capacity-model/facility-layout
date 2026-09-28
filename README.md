# :triangular_ruler: Facility Layout — Qualitative Proximity Relationships

An interactive tool for declaring qualitative proximity relationships between facility centers, placing the layout, and seeing those relationships drawn on it. Developed for **ISyE 6202 & 6335 — Supply Chain Facilities** at the Georgia Institute of Technology (Instructor: Prof. Benoit Montreuil).

- **Live app:** https://capacity-model.github.io/facility-layout/

## What it does

- **Relationship table** — every field a dropdown: the pair of centers, importance, desired proximity, reason, and how the distance is measured. An I/O measurement names its stations explicitly, from the upstream center's output to the downstream center's input.
- **Importance scale** — rename levels, set each one's weight and drawn line width, add levels of your own, or mark one as an unscored feasibility constraint.
- **Satisfaction curves** — one curve per desired proximity, each editable; five ramps plus a bell for relationships that want an ideal separation, where closer is not always better.
- **Layout geometry** — drag centers to move or resize them and drag station markers along their walls. The relationship table decides which stations exist; the drawing follows as you drag.

## Built with

Plain **HTML, CSS, and JavaScript** in a single self-contained file (`index.html`) — no frameworks and no build step.

## Usage

Open **https://capacity-model.github.io/facility-layout/** in any browser — nothing to install.

To run it locally, download `index.html` and open it directly, or serve the folder:

```bash
python -m http.server
```

Then visit http://localhost:8000.

## Contact Us

For any questions about this interactive tool, please contact Yinzhu Quan ([yquan9@gatech.edu](mailto:yquan9@gatech.edu)).
